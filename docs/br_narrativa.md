# Narrativa atual — Cap1 e Cap2

## Cap1 — Introdução

Se eu fosse explicar de forma simples, eu diria assim: eu sou engenheiro de Controle e Automação, então comecei procurando um problema de engenharia de controle e automação para resolver. Com isso, cheguei no artigo 'art1_A-Plantwide-Industrial-Process-Control-Problem_Downs_Vogel'. Ele foi o benchmark perfeito; além de ter um problema perfeito ele tem um largo histórico de trabalhos de colegas que podem ser usados para comparação e revisão. Esse artigo propõe uma planta inteira, com modos de operação, objetivos econômicos, restrições, perturbações, variáveis manipuladas e medições.

    Então, para mim, o ponto forte do TEP é que ele força uma pergunta maior: quem decide como a planta deve operar? Não é só manter uma variável em um setpoint. A planta pode operar em diferentes modos, com diferentes proporções de produto, diferentes metas de produção e diferentes restrições. Isso já coloca o problema em um nível supervisório. O controle automático continua existindo, mas ele atua dentro de uma política operacional maior.

    Por exemplo: uma coisa é controlar pressão, nível ou temperatura. Outra coisa é decidir que a planta deve operar no modo 1, ou migrar para máxima produção, ou proteger uma restrição, ou alterar uma referência porque houve uma perturbação — aliás, identificar que está havendo uma perturbação e que ela merece mudança de política. Essa segunda camada não é simplesmente PID. Ela é uma camada de supervisão: observa o estado da planta, compara com uma política declarada e decide que ajustes operacionais devem ser aplicados.

É nesse ponto que a analogia com Kubernetes se torna tecnicamente relevante. Eu parti para encontrar um artigo que me ajudasse  construir isso, encontrei 'art12_Cloud-Native-Computing-A-Survey-from-the-Perspective-of-Services_Shuiguang_et_al', que traz a definição de Cloud-Native e também outras definições. Kubernetes pode ser entendido como uma plataforma de supervisão declarativa para sistemas computacionais distribuídos. Nele, não se programa apenas uma sequência fixa de comandos; declara-se um estado operacional desejado, e a plataforma passa a observar continuamente o estado real do sistema para reduzi-lo à coerência com essa declaração.

    Daí, em 'art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes', eu entendi porque o Kubernetes é bem-sucedido; Ele organiza a operação de aplicações distribuídas em torno de uma ideia simples e poderosa: declarar o estado desejado do sistema e deixar a plataforma trabalhar continuamente para aproximar o estado real dessa declaração. Essa força vem de cinco escolhas principais: ele desloca o foco da máquina para a aplicação, padroniza os recursos por uma API comum, separa estado desejado de estado observado, usa loops de reconciliação para corrigir desvios e divide a supervisão em componentes especializados, em vez de concentrar tudo em um único bloco rígido. Assim, ele transforma a complexidade de sistemas distribuídos em objetos observáveis, configuráveis e automaticamente reconciliáveis.

    Essa supervisão, embora descrita por abstrações como aplicações, serviços, réplicas e configurações, tem efeitos físicos sobre a infraestrutura computacional. Quando uma política é declarada, o Kubernetes pode decidir em quais servidores os processos vão rodar, criar ou remover instâncias, reiniciar processos falhos, substituir cargas em máquinas indisponíveis, aplicar configurações ao ambiente de execução, limitar consumo de CPU e memória, organizar rotas de comunicação e preservar a disponibilidade do serviço. Portanto, sua atuação não é apenas lógica ou administrativa: ela altera concretamente a ocupação de máquinas, o uso de recursos, o tráfego de rede e a continuidade operacional das aplicações cloud-native.

Achei que seria estratégico buscar o que a comunidade de engenharia de controle está propondo de uso, se é que estava né. Para minha surpresa, encontrei dois artigos que, parando para pensar, são bem ousados:
- 'art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al' → Esse artigo simplesmente confiou ao k8s a orquestração de VDCN, literalmente um controlador industrial virtualizado, literalmente o componente que mantém a malha estável. Então, deixar o k8s ligar ou desligar um componente como esse é até mais agressivo do que o que eu estou proponto.
- 'art11_Design-of-an-IoT-PLC-A-Containerized-Programmeble-Logical-Controller-for-the-Industry-4_Mellado_Nunez' → Esse artigo, por sua vez, propõe e implementa um PLC especial que ele chama de IoT-PLC, filosoficamente pensado para ser 'cloud-native'. A ideia é justamente facilitar esse tipo de abordagem onde uma função é implantada remotamente, o que é, novamente, ainda mais agressivo do que o que eu estou propondo.

Então, para mim já ficou claro que não só é viável, será uma demanda! Eu comecei a pensar então em como o k8s poderia ser um supervisor. Que tipo de coisas ele estaria observando da planta? como ele saberia que algo precisa ser alterado? O que exatamente ele iria manipular ness planta? Então eu me voltei para o problema original da TEP mais uma vez e tornei a refletir sobre ele. 
    
Foi ai que eu percebi que precisava entender melhor o que era a ideia de 'Plantwide'. Lendo 'art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad', eu entendi que para implementar uma camada de supervisão com k8s eu precisaria representar a planta como um sistema operacionalmente observável: 
  - quais variáveis são estados críticos, 
  - quais medições indicam qualidade, produção, segurança e estabilidade, 
  - quais atuadores ainda possuem autoridade de controle, 
  - quais restrições estão ativas, 
  - quais malhas estão saturadas, 
  - quais distúrbios estão deslocando a planta e ;
  - quais objetivos globais continuam válidos naquele modo de operação. 

Em outras palavras, o Kubernetes não poderia apenas “mandar um novo valor” para um PID; ele teria que reconciliar uma política operacional desejada com o estado real observado da planta. Isso envolve decidir quando uma malha local já não é suficiente, quando um setpoint deixou de ser economicamente ou dinamicamente adequado, quando uma restrição passou a dominar a operação, quando um atuador perdeu grau de liberdade e quando a estratégia de controle precisa mudar de configuração. Foi aí que ficou claro para mim que o buraco era TOTALMENTE mais em baixo e eu tive pela primeira vez a dimensão do tamanho desse problema kkk... Eu comecei a ler 'art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad' que parece uma versão mais ampla do artigo 3. Tentei entender melhor as considerações do Skogestad.

A essa altura, eu estava entendendo que ia precisar de duas coisas:
1. Um método para definir as minhas políticas de supervisão → que na minha opinião está bastante abstrato;
2. Um método para saber quando a planta estava fora das minhas políticas de supervisão → que é relativamente fácil, encontrei 4 excelentes artigos nesse sentido;

Ao ler:
- 'art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro'
- 'art9_Assessment-of-Control-Loop-Performance_Harris'
- 'art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin'
- 'art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin'

Eu tive muitos insights sobre como o k8s poderia ser implementado. Eu percebi que ele seria um ente que iria consultar várias coisas para entender se uma política estaria sendo aplicada na planta, uma política de alto nível. E ele encontraria muitos subsídios para tal. O método da definição da política é perfeito porque ele parte do exato objetivo de alto nível do controle, a função de custo. E os diversos métodos de qualidade do controle são perfeitos porque eles dão ao k8s o poder de concluir se a planta está na política e o que pode ser feito para levar ela até a política.


Em `art2` eu sei se uma malha está "controlada". Em `art9` eu sei se o controle dela pode ser aprimorado ou não. Em `art7` comportamento anômalo observável, como oscilação. 


---

Uma das coisas mais top é que, quando você para pra pensar, você entende que a supervisão é feita sob medida e fica "queimada" no supervisório e na cabeça do operador. Ter o k8s seria uma mudança bem grande nesse paradigma, porque controle sairia da cabeça e dos limites de uma implantação. A abstração permitiria difundir o controle para mais pessoas. Digamos que a curva de adaptação seria bem menor.

A minha ideia é trazer essa lógica para a planta simulada. Em vez de usar Kubernetes apenas para manter aplicações rodando, eu quero usá-lo como uma camada supervisória sobre a digital twin do Tennessee Eastman. Ou seja: eu declaro uma política de operação da planta — modo de operação, setpoints, restrições, perturbações permitidas, estratégia de controle ativa — e um supervisor inspirado em Kubernetes observa o estado da planta e aplica ações para manter a operação coerente com essa política.
