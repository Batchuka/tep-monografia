# Rascunho de estrutura — Capítulo 3: Desenvolvimento

---

## BLOCO 1 — Árvore atual

```
DESENVOLVIMENTO
│
├── Visão Geral da Arquitetura Proposta
│     Apresenta a hierarquia IEC 62264 (Níveis 0–4) com o mapeamento dos componentes,
│     delimita o escopo implementado (Níveis 0–2) e posiciona o K8s no Nível 4
│     como destino arquitetural da proposta.
│
├── Simulador da Planta — tep-plant
│     Contextualiza a escolha do Rust e apresenta o repositório como implementação
│     do modelo matemático do TEP + servidor gRPC.
│
│   ├── Estrutura Interna
│   │     Descreve os dois crates: te-core (biblioteca do modelo) e
│   │     tennessee-eastman-service (binário + gRPC).
│   │
│   ├── Loop de Simulação
│   │     Explica o ciclo step(): integração RK4 → ControllerBank → broadcast gRPC,
│   │     e o fator de aceleração 100× (STEP_DELAY_MS=36).
│   │
│   ├── Controladores — ControllerBank
│   │     Apresenta a trait Controller, o PController proporcional e as três malhas
│   │     P do ponto de operação nominal (pressão, nível separador, nível stripper).
│   │
│   ├── Servidor gRPC
│   │     Documenta os quatro métodos do tep.proto: StreamMetrics, GetPlantStatus,
│   │     ListControllers, UpdateController.
│   │
│   └── Sistema de Distúrbios
│         Explica a ativação dos IDV1–IDV20 via variável de ambiente ou IHM,
│         com fidelidade ao FORTRAN original de Downs e Vogel.
│
├── Operator Kubernetes — tep-operator
│     Apresenta o Operator Go (Kubebuilder) como observador supervisório da planta,
│     operando em modo de observação pura nos experimentos realizados.
│
│   ├── O CRD PLCMachine
│   │     Descreve spec (plantAddress, variables, controllers) e status
│   │     (phase, plantTime, lastReconcile), com exemplo de manifest YAML.
│   │
│   ├── Loop de Reconciliação
│   │     Documenta as cinco etapas do Reconcile(): leitura → conexão gRPC →
│   │     observação → avaliação de política → atualização de status.
│   │
│   └── Conectividade com a Planta
│         Explica o problema de rede Kind↔Docker e a solução via
│         host.docker.internal:50051.
│
├── Interface Homem-Máquina — tep-ihm
│     Apresenta a IHM Python (FastAPI + WebSocket) como interface de operação
│     em tempo real.
│
│   ├── Arquitetura
│   │     Descreve o pipeline assíncrono: grpc_reader → asyncio.Queue →
│   │     ws_broadcaster → clientes WebSocket.
│   │
│   ├── Dashboard
│   │     Documenta os seis painéis (SVG da planta, gráficos ECharts, controladores,
│   │     distúrbios, analítico, status PLCMachine) e a conformidade com ISA-101.
│   │
│   └── Registro de Dados (CSV)
│         Explica a gravação contínua de XMEAS/XMV ativada por RECORD_CSV=true;
│         os CSVs são a fonte de dados dos experimentos do Cap. 4.
│
├── Infraestrutura Local — tep-supervisor
│     Reúne os arquivos de configuração para execução em Windows local.
│
│   ├── Modo de Desenvolvimento — Docker Compose
│   │     Descreve os serviços te-plant e tep-ihm no docker-compose.yml e a
│   │     rede interna que permite resolução por nome de serviço.
│   │
│   └── Modo de Produção — Cluster Kind
│         Documenta o roteiro de seis passos para subir o cluster Kind com o
│         Operator ativo, e a tabela de endereços por modo de execução.
│
└── Considerações Finais
      Sintetiza a separação de responsabilidades (planta / controle / IHM),
      o papel da PLCMachine como política declarativa, e encaminha o Cap. 4.
```

---

## BLOCO 2 — Proposta de nova estrutura (rascunho tosco)

> Ideia central: antes de descrever os componentes, contextualizar **por que** o código foi escrito em Rust (em contraste com o FORTRAN original) e **por que** a arquitetura adota OPC UA. Isso dá ao leitor o quadro conceitual antes dos detalhes técnicos.

```
DESENVOLVIMENTO
│
├── Visão Geral da Arquitetura Proposta
│     [mantém o que já está — hierarquia IEC 62264, mapeamento dos componentes,
│      as duas figuras (hierarquia e fluxo de dados), escopo implementado vs. proposta]
│
├── Do FORTRAN ao Rust: mudança de paradigma
│     Seção narrativa que justifica a reimplementação do TEP em Rust.
│     Não descreve código ainda — prepara o leitor para entender as escolhas
│     das subseções seguintes.
│
│     § Parágrafo inicial: contexto histórico do FORTRAN 77.
│       Downs e Vogel (1993) escreveram o código no paradigma imperativo sequencial
│       típico da época — subrotinas globais, estado compartilhado por COMMON blocks,
│       sem tipagem forte. O objetivo deles era portabilidade e reprodutibilidade,
│       não extensibilidade. Isso foi correto para 1993.
│
│     § Rust: origem (Mozilla Research, 2010), foco em segurança de memória sem GC,
│       sistema de tipos algébrico, traits como abstração sem custo de desempenho.
│       Por que é ideal aqui: simulação numérica de longa duração sem vazamento de
│       memória; modelo de ownership que elimina race conditions no loop de threads;
│       compilação para binário estático adequada a contêineres.
│
│   ├── Big picture do código FORTRAN original
│   │     Descreve a estrutura do código de Downs e Vogel em alto nível:
│   │     TEFUNC (dinâmica da planta, ~600 linhas), TESUB1–TESUB8 (subrotinas
│   │     auxiliares de termodinâmica), COMMON blocks como estado global,
│   │     arrays XMEAS[41] e XMV[12] como interface de I/O, IDV[20] como
│   │     vetor de distúrbios. A planta é "caixa-preta" com entradas XMV e
│   │     saídas XMEAS — interface que te-core preserva.
│   │
│   ├── Limitações e problemas de implementação
│   │     — Estado global via COMMON blocks: não reentrante, impede múltiplas
│   │       instâncias simultâneas da planta.
│   │     — Ausência de tipos: XMV e XMEAS são arrays de double sem semântica;
│   │       erros de índice são silenciosos.
│   │     — Ausência de separação entre modelo e controle: os controladores
│   │       originais (subrotinas XMEAS → XMV) estão embutidos no loop principal.
│   │     — Sem interface de rede: o código foi projetado para rodar local,
│   │       sem nenhuma abstração de comunicação.
│   │     — Integrador fixo: RK4 com dt fixo, sem possibilidade de troca sem
│   │       refatoração global.
│   │
│   └── O que o Rust endereça — design interno do te-core
│         Em linhas gerais (sem código ainda), descrever como te-core resolve
│         cada limitação acima:
│         — TepPlant como struct encapsulando estado → múltiplas instâncias possíveis.
│         — tep_derivatives() pura (sem efeitos colaterais) → testável unitariamente.
│         — Trait Controller + ControllerBank → separação modelo/controle.
│         — Integrador RK4 como função separada → trocável.
│         — Interface XMEAS/XMV preservada como contrato público → compatibilidade
│           com o FORTRAN original para validação.
│
├── Simulador da Planta — tep-plant
│     [mantém estrutura atual, mas pode ser mais enxuta agora que a seção acima
│      fez o trabalho narrativo de justificativa]
│
│   ├── Estrutura Interna (te-core + tennessee-eastman-service)
│   ├── Loop de Simulação
│   ├── Controladores — ControllerBank
│   ├── Servidor gRPC
│   └── Sistema de Distúrbios
│
├── Implementação OPC UA                          ← NOVA SEÇÃO (a desenvolver)
│     [a desenvolver — posicionar a escolha de OPC UA dentro da arquitetura,
│      relação com a norma IEC 62541, como o servidor OPC UA se relaciona com
│      o gRPC já existente ou o substitui, e o que foi implementado vs. proposto]
│
├── Operator Kubernetes — tep-operator            [mantém estrutura atual]
│   ├── O CRD PLCMachine
│   ├── Loop de Reconciliação
│   └── Conectividade com a Planta
│
├── Interface Homem-Máquina — tep-ihm             [mantém estrutura atual]
│   ├── Arquitetura
│   ├── Dashboard
│   └── Registro de Dados (CSV)
│
├── Infraestrutura Local — tep-supervisor         [mantém estrutura atual]
│   ├── Modo de Desenvolvimento — Docker Compose
│   └── Modo de Produção — Cluster Kind
│
└── Considerações Finais
      [atualizar para incorporar a narrativa Fortran→Rust e OPC UA]
```

---

## Notas para formalizar

- A seção "Do FORTRAN ao Rust" deve vir **antes** de tep-plant porque ela fornece o
  quadro conceitual que justifica as escolhas de design — o leitor entende o *porquê*
  antes de ver o *como*.
- A seção OPC UA precisa definir claramente se é **implementação paralela** ao gRPC
  ou **substituição** — isso impacta onde ela se encaixa na hierarquia IEC 62264.
- As subseções 1.1/1.2/1.3 da seção Fortran→Rust podem se transformar em parágrafos
  dentro de uma única seção sem subsections, dependendo da profundidade que o autor
  quiser dar ao tema.
