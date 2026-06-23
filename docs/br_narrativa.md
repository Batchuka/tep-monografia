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


Em `art2` eu sei se uma malha está "controlada". Em `art9` eu sei se o controle dela pode ser aprimorado ou não. Em `art7` comportamento anômalo observável, como oscilação. Em `art8` começamos a agrupar sensores em clusters a partir de atribuições compartilhas e também temos a idea de um serviço de avaliação de telemetria. Isso me lembrou da minha iniciação científica em que estudei métodos de avaliar avarias em mancais de rolamento usando análise de sinais e transformada wavelet. Me lembrou porque é uma espécie de telemetria online. Eu trouxe o artigo também, seria o 'art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al'

Outro artigo interessante que li foi o 'art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere'. De tanto falarem de UNICOS nos artigos do CERN, eu resolvi dar uma lida sobre isso. É interessante porque é um framework que projeta exatamente a coisa de 'abstrair a complexidade dos PLC's e outros objetos em um objeto virtual que tem um estado'. Isso comunga com as normas. A questão com esse artigo é que ele tem uma técnica para predizer, ou captar, falha em atuadores. Isso é absurdo se unido com o k8s. Isso daria uma supervisão absurda.

Bom, traçando um panorama do que eu li até agora. Li muitas coisas que demonstram viabilidade da ideia. É uma visão interessante e eu diria que uma abordagem inovadora e moderna, que aproxima mais a tecnologia da industria. Tende a fazer bem para os dois universos. Seria realmente uma consolidação de uma metodologia de industria 4.0, seria o fundamento de como fazer uma industria realmente integrada. Daí, eu caio na real: "tá, o que eu realmente farei nesse projeto?"

Bom, voltando um pouco para o início, eu sou engenheiro de controle e automação. Minha ênfase é em integração industrial, então dentre os diferentes problemas que essa seara toda tangencia, eu estou interessado em focar especificamente em **elaborar um sistema de integração industrial de uma dada planta** , esse é o meu objeto de interesse. Trata-se de um `Cyber-Physical System`, ou CPS, como irá relatar 'book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al', um sistema onde um supervisor inspirado em Kubernetes observa abstrações de alto nível de uma planta industrial (modo operacional, saúde de malhas, restrições) e reconcilia esse estado observado com uma política declarada. Isso é a integração computação-processo-físico-em-loop que define CPS.

Entranto, eu não posso fazer nem 10% do que eu almejo e do que eu entendi ser possível. Eu sequer consigo molhar os pés. A única coisa que dá para fazer é a refatoração do TEP de Fortran para Rust como serviço. Isso, por si só, não é o CPS — é a construção do substrato físico/simulado que o CPS vai precisar para existir. É a planta digitalizada e exposta como serviço, pré-requisito para que um supervisor algum dia observe e atue sobre ela. Eu proponho um CPS, e construí, como primeiro degrau verificável dessa proposta, uma modernização do benchmark Tennessee Eastman Process — originalmente em Fortran — para um serviço em Rust. Esse serviço é o substrato sobre o qual um supervisor real precisaria operar para validar a proposta de CPS.

> uma coisa que descobri lendo 'book1_DigitalTwin-Mechatronic-Futures_Hehenberger_Bradley' é que de maneira alguma essa implementação Rust se confunde com `digital twin`. Faltaria espelhar um processo real e manter sincronização com o que acontece no processo real. Então o que eu fiz não é um gêmeo digital, pois a TEP sequer existe.

Bom, acabou que 'book1_Mechatronic-to-CyberPhysical' foi uma das principais citações para conceituar o que eu estou fazendo. No final dele ele formaliza 2 pré-requisitos que devo cumprir para tal: 
1. explicitar os modelos dos subsistemas; 
2. integrá-los em um sistema cyber-físico observável e testável.

Integrar exige interface. Se os subsistemas precisam compor um modelo geral de CPS, então as fronteiras entre eles precisam ser formalizadas. Daí eu parti para entender o OPC-UA que parece ser uma promessa nesses termos. A planta já usa gRPC que eu acabei derivando do ecosistema k8s, mas é fato que posso rodar OPC-UA em cima de gRPC, diria até que seria uma das inovações. Então eu parti para entender o OPC-UA. Identificar subsistemas também requer uma definição formal que tangencia aquele modelo Purdue, eu sei que a norma IEC 62264 é uma formalização disso. Daí parti para isso.

No livro 'book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm' eu avaliei os capítulos de `System Architecture`, `Services` e a introdução. Além disso avaliei as normas `IEC 62541: 1, 3 e 8` que achei relavante para OPC-UA e `IEC 62264: 1` que versa sobre o modelo Purdue.

