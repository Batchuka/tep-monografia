---
annotation-target: books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf
titulo: From Mechatronics to Cyber-Physical Systems — cap. in Mechatronic Futures
autor: Hehenberger, P. et al.
ano: 2016
fonte: Springer (eds. Hehenberger, P.; Bradley, D.)
papel: conceito_cps
---

>%%
>```annotation-json
>{"created":"2026-06-20T19:02:20.159Z","text":"Bom, o que temos não é uma digital twin, é isso! Meu trabalho se enquadra como um 'ambiente cyber-físico experimental', porque eu tenho exatamente esses elementos:\n- computação;\n- PLC's físicos;\n- rede;\n- planta simulada;\n- sinais de medição;\n- variaveis manipuladas;\n- realimentação\n\nSe CPS depende de computadores embarcados e redes monitorando/controlando processos fi´sicos, então surge a necessidade de uma camada de comunicação industrial capaz de export variáveis, estados, comandos e eventos de forma interoperável: OPC UA.\n","updated":"2026-06-20T19:02:20.159Z","document":{"title":"book1_Mechatronic-Futures.pdf","link":[{"href":"urn:x-pdf:ec43aca1016d19a556804a649f4fa914"},{"href":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf"}],"documentFingerprint":"ec43aca1016d19a556804a649f4fa914"},"uri":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","target":[{"source":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","selector":[{"type":"TextPositionSelector","start":2901,"end":3143},{"type":"TextQuoteSelector","exact":"....  integration  of  computation  and  physical  processes.  Embedded  computers  and  net-works  monitor  and  control  the  physical  processes,  usually  with  feedback  loops  where physical processes affect computations and vice versa.","prefix":"r-Physical Systems (CPS) as the:","suffix":"Such  systems  can  be  found  i"}]}]}
>```
>%%
>*%%PREFIX%%r-Physical Systems (CPS) as the:%%HIGHLIGHT%% ==....  integration  of  computation  and  physical  processes.  Embedded  computers  and  net-works  monitor  and  control  the  physical  processes,  usually  with  feedback  loops  where physical processes affect computations and vice versa.== %%POSTFIX%%Such  systems  can  be  found  i*
>%%LINK%%[[#^i2s9l2u889|show annotation]]
>%%COMMENT%%
>Bom, o que temos não é uma digital twin, é isso! Meu trabalho se enquadra como um 'ambiente cyber-físico experimental', porque eu tenho exatamente esses elementos:
>- computação;
>- PLC's físicos;
>- rede;
>- planta simulada;
>- sinais de medição;
>- variaveis manipuladas;
>- realimentação
>
>Se CPS depende de computadores embarcados e redes monitorando/controlando processos fi´sicos, então surge a necessidade de uma camada de comunicação industrial capaz de export variáveis, estados, comandos e eventos de forma interoperável: OPC UA.
>
>%%TAGS%%
>
^i2s9l2u889


>%%
>```annotation-json
>{"created":"2026-06-21T14:34:22.936Z","text":"A planta simulada, os PLCs, os serviços gRPC/OPC UA, o supervisor e os módulos de diagnóstico não são blocos isolados. Eles precisam ser integrados horizontalmente entre si e verticalmente com uma camada supervisória.\n\nAqui entra a demanda por um protocolo/modelo de integração que não seja apenas troca de bytes. OPC UA pode ser introduzido como candidato porque permite organizar a comunicação entre níveis: dispositivo, controle, supervisão e sistemas externos. O capítulo cria a necessidade; OPC UA entra como tecnologia de integração industrial.","updated":"2026-06-21T14:34:22.936Z","document":{"title":"book1_Mechatronic-Futures.pdf","link":[{"href":"urn:x-pdf:ec43aca1016d19a556804a649f4fa914"},{"href":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf"}],"documentFingerprint":"ec43aca1016d19a556804a649f4fa914"},"uri":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","target":[{"source":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","selector":[{"type":"TextPositionSelector","start":2615,"end":2848},{"type":"TextQuoteSelector","exact":"As many sub-systems are sourced from external suppliers, there is a need for both horizontal integration within  organizations  and  for  vertical  integration  between the sub-system suppli-ers and the suppliers of the full systems.","prefix":"delling of complex systems [6]. ","suffix":" Lee [7] defines Cyber-Physical "}]}]}
>```
>%%
>*%%PREFIX%%delling of complex systems [6].%%HIGHLIGHT%% ==As many sub-systems are sourced from external suppliers, there is a need for both horizontal integration within  organizations  and  for  vertical  integration  between the sub-system suppli-ers and the suppliers of the full systems.== %%POSTFIX%%Lee [7] defines Cyber-Physical*
>%%LINK%%[[#^ar2pir71tsw|show annotation]]
>%%COMMENT%%
>A planta simulada, os PLCs, os serviços gRPC/OPC UA, o supervisor e os módulos de diagnóstico não são blocos isolados. Eles precisam ser integrados horizontalmente entre si e verticalmente com uma camada supervisória.
>
>Aqui entra a demanda por um protocolo/modelo de integração que não seja apenas troca de bytes. OPC UA pode ser introduzido como candidato porque permite organizar a comunicação entre níveis: dispositivo, controle, supervisão e sistemas externos. O capítulo cria a necessidade; OPC UA entra como tecnologia de integração industrial.
>%%TAGS%%
>
^ar2pir71tsw


>%%
>```annotation-json
>{"created":"2026-06-21T14:38:37.706Z","text":"Se a “cyber part” é a rede de integração, podemos argumentar que a arquitetura precisa de uma camada de comunicação industrial que represente os elementos físicos e seus estados de forma padronizada. \n\nOPC UA entra como candidato natural para essa rede de integração entre PLCs, simulação e supervisão.","updated":"2026-06-21T14:38:37.706Z","document":{"title":"book1_Mechatronic-Futures.pdf","link":[{"href":"urn:x-pdf:ec43aca1016d19a556804a649f4fa914"},{"href":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf"}],"documentFingerprint":"ec43aca1016d19a556804a649f4fa914"},"uri":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","target":[{"source":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","selector":[{"type":"TextPositionSelector","start":4902,"end":5399},{"type":"TextQuoteSelector","exact":"These core elements are all com-prised  of  a hardware  element  and a  software  element.  The  interactions  between these  can occur in  the physical domain (e.g.  clash between two robots  detected, thanks  to their sensors), or in the cyber part (e.g.  dialogue  between these robots supported  by  network  protocols). The  cyber part is  then  considered as  the  inte-gration network. All these core elements are themselves made up of several mod-ules represented by the small white boxes.","prefix":"stems and CPS (shades of grey). ","suffix":" The mechatronic systems and the"}]}]}
>```
>%%
>*%%PREFIX%%stems and CPS (shades of grey).%%HIGHLIGHT%% ==These core elements are all com-prised  of  a hardware  element  and a  software  element.  The  interactions  between these  can occur in  the physical domain (e.g.  clash between two robots  detected, thanks  to their sensors), or in the cyber part (e.g.  dialogue  between these robots supported  by  network  protocols). The  cyber part is  then  considered as  the  inte-gration network. All these core elements are themselves made up of several mod-ules represented by the small white boxes.== %%POSTFIX%%The mechatronic systems and the*
>%%LINK%%[[#^5mybx3yqdvm|show annotation]]
>%%COMMENT%%
>Se a “cyber part” é a rede de integração, podemos argumentar que a arquitetura precisa de uma camada de comunicação industrial que represente os elementos físicos e seus estados de forma padronizada. 
>
>OPC UA entra como candidato natural para essa rede de integração entre PLCs, simulação e supervisão.
>%%TAGS%%
>
^5mybx3yqdvm


>%%
>```annotation-json
>{"created":"2026-06-21T14:40:16.707Z","text":"Isso está fundamentando a minha decisão de decomposição arquitetural, a minha decisão em não fazer do Rust um bloco monolítico.\n\nEu defendo que a planta tem que ser separada em planta, barramento de sinais, controladores, PLC's, adaptadores de comunicação, diagnóstico... É preciso haver domínios e eles precisam estar em uma hierarquia de relação.\n\nO OPC-UA é uma tecnologia que transforma essas interfaces de domínio em objetos comunicáveis, isto é, é uma proposta de interface que já tem aderência industrial. Não tem porque eu fugir disso.","updated":"2026-06-21T14:40:16.707Z","document":{"title":"book1_Mechatronic-Futures.pdf","link":[{"href":"urn:x-pdf:ec43aca1016d19a556804a649f4fa914"},{"href":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf"}],"documentFingerprint":"ec43aca1016d19a556804a649f4fa914"},"uri":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","target":[{"source":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","selector":[{"type":"TextPositionSelector","start":6952,"end":7190},{"type":"TextQuoteSelector","exact":"The chosen approach is based on a modular structure of models (modular model architecture, model base, hierarchical structure of models) that allows for the configuration of system models from a library of sub-models and interface models.","prefix":"del and master complex systems. ","suffix":" A sub-model can be a model of a"}]}]}
>```
>%%
>*%%PREFIX%%del and master complex systems.%%HIGHLIGHT%% ==The chosen approach is based on a modular structure of models (modular model architecture, model base, hierarchical structure of models) that allows for the configuration of system models from a library of sub-models and interface models.== %%POSTFIX%%A sub-model can be a model of a*
>%%LINK%%[[#^aj25d04in1|show annotation]]
>%%COMMENT%%
>Isso está fundamentando a minha decisão de decomposição arquitetural, a minha decisão em não fazer do Rust um bloco monolítico.
>
>Eu defendo que a planta tem que ser separada em planta, barramento de sinais, controladores, PLC's, adaptadores de comunicação, diagnóstico... É preciso haver domínios e eles precisam estar em uma hierarquia de relação.
>
>O OPC-UA é uma tecnologia que transforma essas interfaces de domínio em objetos comunicáveis, isto é, é uma proposta de interface que já tem aderência industrial. Não tem porque eu fugir disso.
>%%TAGS%%
>
^aj25d04in1


>%%
>```annotation-json
>{"created":"2026-06-21T14:48:29.954Z","text":"Isso é perfeito:\n\n* A base de uma metodologia integrada para CPS é modelagem e simulação.\n* Os modelos de projeto precisam ser intercambiáveis entre ferramentas, isto é, não devem ficar presos a uma única implementação ou ambiente.\n* A simulação não serve apenas para “ver gráficos”; ela produz informação sobre o problema de projeto.\n* Essa informação melhora: (1) o conhecimento sobre o sistema; (2) a qualidade das análises; (3) a qualidade das decisões de engenharia.\n* A abordagem defendida depende de uma arquitetura modular de modelos.\n* O foco central é simulação como modelagem e experimentação virtual do comportamento de um sistema.\n* Isso exige explicitar a descrição matemática dos modelos usados.\n* Há uma carência de métodos e ferramentas de software para apoiar modelagem e simulação de CPS.\n* Nas fases iniciais, modelos detalhados muitas vezes não são possíveis por falta de informação completa... Por isso, o sistema precisa ser modelado em um nível mais alto de abstração.\n* Um desafio relevante é derivar requisitos para essas ferramentas e desenvolver software apropriado para esse propósito.\n\nIsso é perfeito para expor o que fiz. Explicando no meu trabalho:\n\n* O TEP em Rust é o modelo executável em nível de sistema.\n* A separação entre planta, integrador numérico, XMEAS, XMV, estados internos, perturbações e controladores é a sua arquitetura modular de modelo.\n* O uso do TEP para testar controle, supervisão, falhas e integração com PLCs é system testing.\n* O gRPC atual e o OPC UA futuro entram como resposta ao problema de intercambialidade, interface e integração entre ferramentas/subsistemas.\n\n\n","updated":"2026-06-21T14:48:29.954Z","document":{"title":"book1_Mechatronic-Futures.pdf","link":[{"href":"urn:x-pdf:ec43aca1016d19a556804a649f4fa914"},{"href":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf"}],"documentFingerprint":"ec43aca1016d19a556804a649f4fa914"},"uri":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","target":[{"source":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","selector":[{"type":"TextPositionSelector","start":36052,"end":36747},{"type":"TextQuoteSelector","exact":"The key to an integrated design  methodology for  CPS is  modelling and  simula-tion  (see  Fig. 10.8).  In  this  context  design  models  and  their  interchangeability between different design tools are very important during the design process. From the mechatronic design process viewpoint, models are containers of the knowledge of the product during its total life cycle. Simulations are producing information of the design problem. This may improve product knowledge and potentially also the quality of many analyses and decisions. The presented approach relies on modular model architecture and enables innovative design, flexibility, speed and assistance in nonroutine design questions.","prefix":"roaches and industrial practice.","suffix":"The main point of view of the wo"}]}]}
>```
>%%
>*%%PREFIX%%roaches and industrial practice.%%HIGHLIGHT%% ==The key to an integrated design  methodology for  CPS is  modelling and  simula-tion  (see  Fig. 10.8).  In  this  context  design  models  and  their  interchangeability between different design tools are very important during the design process. From the mechatronic design process viewpoint, models are containers of the knowledge of the product during its total life cycle. Simulations are producing information of the design problem. This may improve product knowledge and potentially also the quality of many analyses and decisions. The presented approach relies on modular model architecture and enables innovative design, flexibility, speed and assistance in nonroutine design questions.== %%POSTFIX%%The main point of view of the wo*
>%%LINK%%[[#^a1yt9ckqdxe|show annotation]]
>%%COMMENT%%
>Isso é perfeito:
>
>* A base de uma metodologia integrada para CPS é modelagem e simulação.
>* Os modelos de projeto precisam ser intercambiáveis entre ferramentas, isto é, não devem ficar presos a uma única implementação ou ambiente.
>* A simulação não serve apenas para “ver gráficos”; ela produz informação sobre o problema de projeto.
>* Essa informação melhora: (1) o conhecimento sobre o sistema; (2) a qualidade das análises; (3) a qualidade das decisões de engenharia.
>* A abordagem defendida depende de uma arquitetura modular de modelos.
>* O foco central é simulação como modelagem e experimentação virtual do comportamento de um sistema.
>* Isso exige explicitar a descrição matemática dos modelos usados.
>* Há uma carência de métodos e ferramentas de software para apoiar modelagem e simulação de CPS.
>* Nas fases iniciais, modelos detalhados muitas vezes não são possíveis por falta de informação completa... Por isso, o sistema precisa ser modelado em um nível mais alto de abstração.
>* Um desafio relevante é derivar requisitos para essas ferramentas e desenvolver software apropriado para esse propósito.
>
>Isso é perfeito para expor o que fiz. Explicando no meu trabalho:
>
>* O TEP em Rust é o modelo executável em nível de sistema.
>* A separação entre planta, integrador numérico, XMEAS, XMV, estados internos, perturbações e controladores é a sua arquitetura modular de modelo.
>* O uso do TEP para testar controle, supervisão, falhas e integração com PLCs é system testing.
>* O gRPC atual e o OPC UA futuro entram como resposta ao problema de intercambialidade, interface e integração entre ferramentas/subsistemas.
>
>
>
>%%TAGS%%
>
^a1yt9ckqdxe


>%%
>```annotation-json
>{"created":"2026-06-21T14:54:23.216Z","text":"Essa seção é um convite explícito. Ele está dizendo que CPS ainda exige pesquisa em modelagem, integração, interfaces, desempenho, robustez, fluxo de informação e aproximação com a prática industrial. O  meu trabalho entra como uma proposta experimental dentro desse espaço.\n\nA lista de desafios funciona como uma ponte entre problema teórico e contribuição prática. Ela permite dizer que seu trabalho não é apenas “implementar TEP em Rust”, mas construir um artefato experimental para atacar alguns desafios de CPS: \n- integração de modelos, \n- interfaces entre subsistemas, \n- avaliação de desempenho multivariável, \n- integração cyber-física e fluxo de informação entre controle, simulação e supervisão. \n\nO capítulo afirma que a tendência atual envolve sistemas mecatrônicos em rede, ou CPS, e que PLM e troca de dados têm papel importante; em seguida, diz que é necessário ampliar pesquisa em modelagem de sistemas para melhorar a visão sistêmica.","updated":"2026-06-21T14:54:23.216Z","document":{"title":"book1_Mechatronic-Futures.pdf","link":[{"href":"urn:x-pdf:ec43aca1016d19a556804a649f4fa914"},{"href":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf"}],"documentFingerprint":"ec43aca1016d19a556804a649f4fa914"},"uri":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","target":[{"source":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","selector":[{"type":"TextPositionSelector","start":34333,"end":35012},{"type":"TextQuoteSelector","exact":"Design  of  CPSs  involves  close  examination  and  further  development  of  design methods,  design  processes,  models  and  tools.  The  current  trend  in  mechatron-ics  involves  networked  mechatronic  systems,  or  cyber-physical  systems  (CPS). Therefore  product  lifecycle  management  and  product  data  exchange  play  an important role in CPS design.  In order to push the  performance of CPS and the related design process, it is necessary to increase the research on system model-ling,  thus  significantly  improving  the  system  view.  There  are  many  challenges for future research towards improving the efficiency and quality of CPS product development","prefix":"rated Design Methodology for CPS","suffix":". In terms of model-based method"}]}]}
>```
>%%
>*%%PREFIX%%rated Design Methodology for CPS%%HIGHLIGHT%% ==Design  of  CPSs  involves  close  examination  and  further  development  of  design methods,  design  processes,  models  and  tools.  The  current  trend  in  mechatron-ics  involves  networked  mechatronic  systems,  or  cyber-physical  systems  (CPS). Therefore  product  lifecycle  management  and  product  data  exchange  play  an important role in CPS design.  In order to push the  performance of CPS and the related design process, it is necessary to increase the research on system model-ling,  thus  significantly  improving  the  system  view.  There  are  many  challenges for future research towards improving the efficiency and quality of CPS product development== %%POSTFIX%%. In terms of model-based method*
>%%LINK%%[[#^z7smsw37jcn|show annotation]]
>%%COMMENT%%
>Essa seção é um convite explícito. Ele está dizendo que CPS ainda exige pesquisa em modelagem, integração, interfaces, desempenho, robustez, fluxo de informação e aproximação com a prática industrial. O  meu trabalho entra como uma proposta experimental dentro desse espaço.
>
>A lista de desafios funciona como uma ponte entre problema teórico e contribuição prática. Ela permite dizer que seu trabalho não é apenas “implementar TEP em Rust”, mas construir um artefato experimental para atacar alguns desafios de CPS: 
>- integração de modelos, 
>- interfaces entre subsistemas, 
>- avaliação de desempenho multivariável, 
>- integração cyber-física e fluxo de informação entre controle, simulação e supervisão. 
>
>O capítulo afirma que a tendência atual envolve sistemas mecatrônicos em rede, ou CPS, e que PLM e troca de dados têm papel importante; em seguida, diz que é necessário ampliar pesquisa em modelagem de sistemas para melhorar a visão sistêmica.
>%%TAGS%%
>
^z7smsw37jcn


>%%
>```annotation-json
>{"created":"2026-06-22T22:32:20.417Z","text":"Esse trecho reduz a abordagem a dois pré-requisitos técnicos:\n- Modelar os subsistemas → cada parte relevante do CPS precisa ter uma representação explícita. No meu caso está havendo o 'modelo dinâmico TEP', o 'Integrador Numérico', o 'Barramento'... tudo separadinho.\n\n- Integrar esses modelos em um modelo global de CPS → Não basta cada parte existir isolada. O valor está em integrar tudo em uma arquitetura coerente: planta virtual + controle + PLC físico + rede + supervisão + observabilidade.\n\nOu seja, o que eu fiz é uma exigência metodológica de CPS. Eu não estou apenas fazendo uma refatoração, eu estou cumprindo os dois passos centrais de uma abordagem CPS baseada em simulação: \n1. explicitar os modelos dos subsistemas;\n2. integrá-los em um sistema cyber-físico observável e testável;\n\nIntegrar exige interface. A fronteira entre os sistemas precisa ser formalizada. Eu estou indo para o OPC-UA que parece o ideal.","updated":"2026-06-22T22:32:20.417Z","document":{"title":"book1_Mechatronic-Futures.pdf","link":[{"href":"urn:x-pdf:ec43aca1016d19a556804a649f4fa914"},{"href":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf"}],"documentFingerprint":"ec43aca1016d19a556804a649f4fa914"},"uri":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","target":[{"source":"vault:/books/book1_Mechatronic-to-CyberPhysical-Mechatronic-Futures_Hehenberger-et-al.pdf","selector":[{"type":"TextPositionSelector","start":37912,"end":38399},{"type":"TextQuoteSelector","exact":"For  a  simulation-based  engineering  approach,  a  model-based  description  of the system, with respect to its sub-systems, under consideration is a prerequisite. Especially for mechatronic systems this addresses:• The models of the sub-systems.• The integration of these models to an overall CPS—system model.This  engineering  approach  facilitates  a  holistic  view  on  the  overall  system  and should be continuously applied even from the very beginning of product develop-ment","prefix":"urpose.162 P. Hehenberger et al.","suffix":". Thus it becomes possible to mo"}]}]}
>```
>%%
>*%%PREFIX%%urpose.162 P. Hehenberger et al.%%HIGHLIGHT%% ==For  a  simulation-based  engineering  approach,  a  model-based  description  of the system, with respect to its sub-systems, under consideration is a prerequisite. Especially for mechatronic systems this addresses:• The models of the sub-systems.• The integration of these models to an overall CPS—system model.This  engineering  approach  facilitates  a  holistic  view  on  the  overall  system  and should be continuously applied even from the very beginning of product develop-ment== %%POSTFIX%%. Thus it becomes possible to mo*
>%%LINK%%[[#^hfo3ts8zc4a|show annotation]]
>%%COMMENT%%
>Esse trecho reduz a abordagem a dois pré-requisitos técnicos:
>- Modelar os subsistemas → cada parte relevante do CPS precisa ter uma representação explícita. No meu caso está havendo o 'modelo dinâmico TEP', o 'Integrador Numérico', o 'Barramento'... tudo separadinho.
>
>- Integrar esses modelos em um modelo global de CPS → Não basta cada parte existir isolada. O valor está em integrar tudo em uma arquitetura coerente: planta virtual + controle + PLC físico + rede + supervisão + observabilidade.
>
>Ou seja, o que eu fiz é uma exigência metodológica de CPS. Eu não estou apenas fazendo uma refatoração, eu estou cumprindo os dois passos centrais de uma abordagem CPS baseada em simulação: 
>1. explicitar os modelos dos subsistemas;
>2. integrá-los em um sistema cyber-físico observável e testável;
>
>Integrar exige interface. A fronteira entre os sistemas precisa ser formalizada. Eu estou indo para o OPC-UA que parece o ideal.
>%%TAGS%%
>
^hfo3ts8zc4a
