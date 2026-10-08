# Mudanças propostas na monografia — 08/10/26

## Título — feito

> *Supervisão Declarativa do Processo Tennessee Eastman com Kubernetes: Função de Custo e Qualidade de Malhas sobre uma Planta Simulada em OPC UA*

## Resumo / Abstract

- **Remover:** "gêmeo digital", gRPC, `PLCMachine`, "17 experimentos" e "futura integração via OPC UA".
- **Incluir:**
  - a planta sobre o `monjolo`, exposta via OPC UA;
  - o supervisor com 3 CRDs genéricos, que julga J (Downs & Vogel) e o PI das malhas (Bradu) e só observa;
  - J nominal 166,83 contra 170,6 $/h;
  - o resultado do #82.
- Reescrever por último.

## Cap 1 — Introdução

- **Manter** os 4 primeiros parágrafos.
- **Incluir uma questão de pesquisa explícita:**
  > É viável usar o modelo declarativo do Kubernetes (recursos customizados com `spec`/`status` e controlador de reconciliação) como camada supervisória que avalia continuamente uma planta de processo contra uma política operacional declarada, sem conhecimento embutido da planta e sem atuar sobre ela?
- **Trocar o parágrafo dos "três artefatos"** pelos componentes atuais:
  - planta (`tep-plant` + `monjolo`, OPC UA);
  - `tep-historian`;
  - `plant-supervisor`;
  - `tep-ihm` (cliente OPC UA + painel do veredito);
  - `tep-lab`.
- **Trocar a lista da Proposta** por:
  1. reimplementar o TEP em Rust sobre um runtime genérico, exposto via OPC UA;
  2. verificar a fidelidade dinâmica;
  3. expressar a política do Modo 1 (função de custo da Tabela 9, metas, restrições) como recursos do Kubernetes, sem código específico da planta;
  4. avaliar a planta em dois níveis, econômico (J) e de qualidade de malhas (PI);
  5. mostrar o veredito acompanhando a degradação da planta sob distúrbio, com a política fixa.
- **Reescrever os objetivos específicos** sobre esses cinco itens.
  - Sai o objetivo da IHM/IEC 63303 (vira detalhe do Cap 3).
  - Sai o "CRD observa a planta".
- **Incluir um parágrafo de escopo:**
  - é uma tese de viabilidade, não de comparação;
  - o supervisor só observa;
  - não é gêmeo digital.
- **Corrigir a Organização:** hoje cita seções sobre IEC 61499 e gRPC que não existem no Cap 2.

## Cap 2 — Referencial teórico

- **Eq. de J:** trocar a forma "conceitual, não literal" pela forma real da Tabela 9 (os 12 termos detalhados ficam no Cap 3).
- **Incluir um parágrafo sobre os modos de Downs & Vogel:**
  - o modo é especificação de negócio e não deriva de J;
  - modo + restrições + J = política.
- **CLPM:** detalhar o PI de Bradu como foi implementado:
  - modelo AR e horizonte b;
  - portão de variabilidade;
  - persistência.
- **Linha 202:** remover a menção ao `ControllerBank`.
- **Final:** "futuramente, por OPC UA" → "por OPC UA".

## Cap 3 — Desenvolvimento — reescrever inteiro

- **Sai:**
  - `te-core`, gRPC, `ControllerBank`, `PLCMachine`;
  - `STEP_DELAY_MS`, `RECORD_CSV`;
  - `host.docker.internal:50051` e a tabela de conectividade;
  - "PLCMachine traduz o IEC 61499".
- **Níveis IEC 62264:**
  - 0/1 = planta com os 3 controladores P;
  - 2 = IHM;
  - 3 = supervisor + historian (hoje o texto diz supervisor no 2 e Kubernetes no 4);
  - 4 = futuro (Apêndice A).
- **Novas seções:**
  1. Visão geral: a cadeia planta → historian → supervisor → `Plant.status` → kubectl/IHM, com os níveis acima.
  2. `monjolo`: runtime genérico, RK4, `StateRegistry`, sensores com ruído, atuadores, distúrbios por interceptação, adaptador OPC UA.
  3. `tep-plant`:
     - subsistemas e os 3 controladores P;
     - IDV 1, 2, 3, 6 e 7;
     - velocidade (`control.set_speed`);
     - espaço de endereçamento OPC UA.
  4. `tep-historian`: coleta OPC UA, buffer, `/aggregate`, `/loop-performance`.
  5. `plant-supervisor`:
     - `CostFunction`, `OperatingPolicy` e `Plant`;
     - laço de avaliação, condições, persistência, `Pending`;
     - `ControlLoopsHealthy`, RBAC, testes (Tabela 9 = 170,6 $/h).
  6. Manifestos do TEP: a Tabela 9 em YAML, a política do Modo 1 e o `Plant tep`.
  7. `tep-ihm`: cliente OPC UA e painel lendo o `Plant` da API do Kubernetes.
  8. `tep-lab`: Kind, `setup.sh`, scripts de gravação.

## Cap 4 — Resultados — reorganizar

- **Fase I (Exp 1–10):** mantém.
- **Fase II (Exp 11–13 + 18–24):**
  - os 11–13 ficam como histórico curto;
  - **incluir os 18–24** (investigação do `twr`, fidelidade depois da migração).
- **Fase III (Exp 14–17):** são da planta antiga. **Decidir:** ressalva ou refazer IDV1/IDV2.
- **Fase IV — nova:**
  - teste ponta a ponta da #77 (veredito virando ao mudar o `maxCost`);
  - J nominal contra o artigo (−2,5 %);
  - calibração (bloco 6);
  - **#82 com IDV6**.
- **Discussão:**
  - sai "Viabilidade do Operator" (gRPC, 30.000 h);
  - entram os dois níveis juntos, a latência do veredito e os limites (janela em tempo de relógio, malha de pressão não julgada, PI dominado por ruído).
- **Atualizar a tabela-resumo.**

## Cap 5 — Conclusão — reescrever

- **Sai:**
  - "ações corretivas via gRPC";
  - "PLCMachine ≈ IEC 61499";
  - "30.000 h";
  - a resposta a uma questão sobre IEC 61499;
  - os trabalhos futuros já feitos (OPC UA, índice do CERN — a citação `CERN_WEAPL02` também está quebrada).
- **Conclusões:** responder a questão de pesquisa do Cap 1 item por item, discutindo o overhead do Kubernetes.
- **Trabalhos futuros:**
  1. agir sobre a planta (Apêndice A);
  2. janela em tempo simulado (#88);
  3. outros modos de operação;
  4. IDVs restantes (#71);
  5. Harris e detecção de oscilação (Tilaro);
  6. malha de pressão (#86);
  7. borda (k3s/KubeEdge);
  8. EPICS/TANGO.

## Apêndice A

- Ajustar a referência ao Nível 4 para ficar coerente com o Cap 3. O resto fica.
