# Narrativa atual — Cap1 e Cap2

## Cap1 — Introdução

Se eu fosse explicar de forma simples, eu diria assim: eu sou engenheiro de Controle e Automação, então comecei procurando um problema de engenharia de controle e automação para resolver. Com isso, cheguei no artigo do Downs e Vogel sobre o Tennessee Eastman Process, 'art1_A-Plantwide-Industrial-Process-Control-Problem_Downs_Vogel'. Ele foi o benchmark perfeito, além de ter um problema perfeito ele tem um largo histórico de trabalhos de colegas que podem ser usados para comparação e revisão. Esse artigo propõe uma planta inteira, com modos de operação, objetivos econômicos, restrições, perturbações, variáveis manipuladas e medições.

    Então, para mim, o ponto forte do TEP é que ele força uma pergunta maior: quem decide como a planta deve operar? Não é só manter uma variável em um setpoint. A planta pode operar em diferentes modos, com diferentes proporções de produto, diferentes metas de produção e diferentes restrições. Isso já coloca o problema em um nível supervisório. O controle automático continua existindo, mas ele atua dentro de uma política operacional maior.

    Por exemplo: uma coisa é controlar pressão, nível ou temperatura. Outra coisa é decidir que a planta deve operar no modo 1, ou migrar para máxima produção, ou proteger uma restrição, ou alterar uma referência porque houve uma perturbação — aliás, identificar que está havendo uma perturbação e que ela merece mudança de política. Essa segunda camada não é simplesmente PID. Ela é uma camada de supervisão: observa o estado da planta, compara com uma política declarada e decide que ajustes operacionais devem ser aplicados.

É nesse ponto que a analogia com Kubernetes se torna tecnicamente relevante. Eu parti para encontrar um artigo que me ajudasse  construir isso, encontrei 'art12_Cloud-Native-Computing-A-Survey-from-the-Perspective-of-Services_Shuiguang_et_al', que traz a definição de Cloud-Native e também outras definições. Kubernetes pode ser entendido como uma plataforma de supervisão declarativa para sistemas computacionais distribuídos. Nele, não se programa apenas uma sequência fixa de comandos; declara-se um estado operacional desejado, e a plataforma passa a observar continuamente o estado real do sistema para reduzi-lo à coerência com essa declaração.

    Daí, em 'art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes', eu entendi porque o Kubernetes é bem-sucedido; Ele organiza a operação de aplicações distribuídas em torno de uma ideia simples e poderosa: declarar o estado desejado do sistema e deixar a plataforma trabalhar continuamente para aproximar o estado real dessa declaração. Essa força vem de cinco escolhas principais: ele desloca o foco da máquina para a aplicação, padroniza os recursos por uma API comum, separa estado desejado de estado observado, usa loops de reconciliação para corrigir desvios e divide a supervisão em componentes especializados, em vez de concentrar tudo em um único bloco rígido. Assim, ele transforma a complexidade de sistemas distribuídos em objetos observáveis, configuráveis e automaticamente reconciliáveis.

    Essa supervisão, embora descrita por abstrações como aplicações, serviços, réplicas e configurações, tem efeitos físicos sobre a infraestrutura computacional. Quando uma política é declarada, o Kubernetes pode decidir em quais servidores os processos vão rodar, criar ou remover instâncias, reiniciar processos falhos, substituir cargas em máquinas indisponíveis, aplicar configurações ao ambiente de execução, limitar consumo de CPU e memória, organizar rotas de comunicação e preservar a disponibilidade do serviço. Portanto, sua atuação não é apenas lógica ou administrativa: ela altera concretamente a ocupação de máquinas, o uso de recursos, o tráfego de rede e a continuidade operacional das aplicações cloud-native.

Achei que seria estratégico buscar na comunidade de engenharia propostas de uso, eu fui buscar por aplicações do k8s na industria. Eu encontrei dois artigos: 'art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al' e 'art11_Design-of-an-IoT-PLC-A-Containerized-Programmeble-Logical-Controller-for-the-Industry-4_Mellado_Nunez'

A minha ideia é trazer essa lógica para a planta simulada. Em vez de usar Kubernetes apenas para manter aplicações rodando, eu quero usá-lo como uma camada supervisória sobre a digital twin do Tennessee Eastman. Ou seja: eu declaro uma política de operação da planta — modo de operação, setpoints, restrições, perturbações permitidas, estratégia de controle ativa — e um supervisor inspirado em Kubernetes observa o estado da planta e aplica ações para manter a operação coerente com essa política.

---

**Abertura:** supervisão de múltiplas malhas é inviável manualmente em escala industrial (CERN LHC como exemplo extremo: 5000 malhas PID).

**Gêmeo digital** como solução: permite introduzir distúrbios e degradar controladores deliberadamente, sem risco à planta real.

**TEP** como benchmark: planta química realista, não-linear, 20 distúrbios programados, amplamente adotada — resultados comparáveis à literatura.

**Plantwide control** (Skogestad): hierarquia de três camadas — regulatório → supervisório → otimização em tempo real. É exatamente o que o lab pretende implementar.

**Ênfase do trabalho:** Integração de Sistemas de Controle — interoperabilidade, protocolos abertos, arquitetura de sistemas heterogêneos (não automação pura).

**Kubernetes + Operators** como plataforma supervisória: reconciliação declarativa, separação entre política (CRD) e execução (controller loop).

**Proposta concreta:**
- núcleo validado: simulador Rust (gRPC) + IHM (FastAPI/WebSocket) + 17 experimentos
- extensões não validadas: Operator K8s, plantwide control, OPC UA, Índice de Preditividade

---

**Seções do capítulo:**
1. Problema — ambiente de experimentação seguro e reprodutível
2. A Proposta — o que foi entregue e o que ficou em aberto
3. Objetivos — geral + 5 específicos
4. Organização do trabalho

---

## Cap2 — Referencial Teórico

**Fio condutor declarado:** TEP + IEC 61499 + Kubernetes/Operators + gRPC + RK4 + Gêmeo Digital

**Seções, em ordem:**

1. **TEP** — o processo (5 unidades, reações, 50 EDOs), XMEAS/XMV, distúrbios IDV, condições de shutdown (ISD)
2. **Controle P + Índice de Preditividade** — controlador P (3 malhas na planta), PI como métrica de qualidade de malha (CERN), motivação de longo prazo do lab
3. **Kubernetes e Operators** — reconciliação declarativa, CRDs (spec/status), loop Observar–Avaliar–Agir, Kubebuilder
4. **gRPC** — protobuf, HTTP/2, 4 modalidades (unário, server streaming, client streaming, bidirecional), escolha motivada por streaming + tipagem + poliglota (Rust/Go/Python)
5. **OPC UA / IEC 62541** — contexto histórico (antes: protocolos proprietários), arquitetura (espaço de endereçamento, nós, referências), partes relevantes da norma (3, 4, 6, 8, 9, 11, 14), papel futuro no lab (expor XMEAS como AnalogItemType, IDV como métodos)
6. **RK4** — integração das 50 EDOs, erro O(h⁴), dt=0,001h, deriv_norm como indicador de saúde
7. **Gêmeo Digital** — origem (NASA Apollo / Iron Bird), 3 níveis (modelo digital → shadow → completo), ciclo de vida, uso para geração de dados de qualidade de malha, enquadramento do lab (shadow em transição para completo)
8. **Considerações finais** — amarra as escolhas tecnológicas
