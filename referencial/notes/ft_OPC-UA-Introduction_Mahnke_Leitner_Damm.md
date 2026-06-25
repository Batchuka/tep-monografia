---
annotation-target: books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf
titulo: OPC Unified Architecture — Introduction
autor: Mahnke, W.; Leitner, S.-H.; Damm, M.
ano: 2009
fonte: Springer
papel: integracao_formal
---

>%%
>```annotation-json
>{"created":"2026-06-22T23:06:48.443Z","text":"Explica de onde o OPC UA vem. Nasce para substituir as especificações Classic OPC baseadas em COM/DCOM. **COM/DCOM** são tecnologias antigas da Microsoft usadas pelo Classic OPC para permitir que programas trocassem dados no Windows.\n\n### COM significa Component Object Model.\nÉ um modelo em que um software expõe “objetos” com métodos e interfaces, e outro software chama esses métodos. Exemplo simples: um SCADA chama uma interface exposta por um driver OPC para ler uma variável de um PLC.\n\n### DCOM significa Distributed COM.\nÉ a extensão do COM para comunicação entre computadores diferentes na rede. Ou seja: o cliente OPC poderia chamar métodos de um servidor OPC rodando em outra máquina.\n\nClassic OPC dependia de COM/DCOM, então ficava muito preso ao ecossistema Windows.","updated":"2026-06-22T23:06:48.443Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:5617f3639030ebbbfd83c2060278af92"},{"href":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"5617f3639030ebbbfd83c2060278af92"},"uri":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":17317,"end":17490},{"type":"TextQuoteSelector","exact":"The OPC Unified Architecture was born out of the desire to create a true replace-ment for all existing COM-based specifications without losing any features or per-formance. ","prefix":"the limitations of Classic OPC. ","suffix":"Additionally it must cover all r"}]}]}
>```
>%%
>*%%PREFIX%%the limitations of Classic OPC.%%HIGHLIGHT%% ==The OPC Unified Architecture was born out of the desire to create a true replace-ment for all existing COM-based specifications without losing any features or per-formance.== %%POSTFIX%%Additionally it must cover all r*
>%%LINK%%[[#^o8xlkk8u45l|show annotation]]
>%%COMMENT%%
>Explica de onde o OPC UA vem. Nasce para substituir as especificações Classic OPC baseadas em COM/DCOM. **COM/DCOM** são tecnologias antigas da Microsoft usadas pelo Classic OPC para permitir que programas trocassem dados no Windows.
>
>### COM significa Component Object Model.
>É um modelo em que um software expõe “objetos” com métodos e interfaces, e outro software chama esses métodos. Exemplo simples: um SCADA chama uma interface exposta por um driver OPC para ler uma variável de um PLC.
>
>### DCOM significa Distributed COM.
>É a extensão do COM para comunicação entre computadores diferentes na rede. Ou seja: o cliente OPC poderia chamar métodos de um servidor OPC rodando em outra máquina.
>
>Classic OPC dependia de COM/DCOM, então ficava muito preso ao ecossistema Windows.
>%%TAGS%%
>
^o8xlkk8u45l


>%%
>```annotation-json
>{"created":"2026-06-22T23:14:17.443Z","text":"Tabela é citável como referência porque enumera propriedades esperadas de OPC UA. Para o referencial teórico, esses termos devem ser preservados quase literalmente. Eles ajudam a sustentar que OPC UA foi pensado para sistemas industriais distribuídos, interoperáveis, seguros, escaláveis e semanticamente modeláveis.","updated":"2026-06-22T23:14:17.443Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:5617f3639030ebbbfd83c2060278af92"},{"href":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"5617f3639030ebbbfd83c2060278af92"},"uri":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":19024,"end":19485},{"type":"TextQuoteSelector","exact":"Table 1.1 Requirements for OPC UA • Reliability by • Robustness and fault tolerance • Redundancy •  Platform-independence •  Scalability  •  High performance •  Internet and firewalls •  Security and access control •  Interoperability • Common model for all OPC data • Object-oriented • Extensible type system  • Meta information • Complex data and methods • Scalability from simple to complex models  • Abstract base model • Base for other standard data models","prefix":"the most important requirement. ","suffix":" Modeling of data was very limit"}]}]}
>```
>%%
>*%%PREFIX%%the most important requirement.%%HIGHLIGHT%% ==Table 1.1 Requirements for OPC UA • Reliability by • Robustness and fault tolerance • Redundancy •  Platform-independence •  Scalability  •  High performance •  Internet and firewalls •  Security and access control •  Interoperability • Common model for all OPC data • Object-oriented • Extensible type system  • Meta information • Complex data and methods • Scalability from simple to complex models  • Abstract base model • Base for other standard data models== %%POSTFIX%%Modeling of data was very limit*
>%%LINK%%[[#^46p6p2fky3n|show annotation]]
>%%COMMENT%%
>Tabela é citável como referência porque enumera propriedades esperadas de OPC UA. Para o referencial teórico, esses termos devem ser preservados quase literalmente. Eles ajudam a sustentar que OPC UA foi pensado para sistemas industriais distribuídos, interoperáveis, seguros, escaláveis e semanticamente modeláveis.
>%%TAGS%%
>
^46p6p2fky3n


>%%
>```annotation-json
>{"created":"2026-06-22T23:18:06.559Z","text":"**Transport **é o mecanismo concreto que leva mensagens de um cliente para um servidor.\n\nOs autores dizem que o transporte define mecanismos otimizados para diferentes usos. No meu caso que fiz uma comunicação em cima de gRPC:\n* gRPC não substitui a ideia de OPC UA.\n* gRPC poderia ser uma escolha de transporte/RPC.\n* OPC UA fornece a semântica industrial e o modelo de informação.\n\n**Data modeling** é a forma como OPC UA descreve aquilo que existe no sistema industrial.\n\nNão é só dizer: `XMEAS(9) = 120.4`; com modelagem, você consegue dizer algo mais estruturado:\n\n```\nReactor\n ├── Temperature\n │    ├── value = 120.4\n │    ├── engineering unit = °C\n │    ├── quality = good\n │    ├── timestamp = ...\n │    └── alarm limits = ...\n ├── Pressure\n ├── Level\n └── CoolingWaterFlow\n```\nUm **information model** é o modelo concreto de uma planta, equipamento ou domínio.\n**meta model** é o conjunto de regras que permite construir esse modelo. Ou seja:\n- Information Model = o modelo da planta\n- Meta Model = as regras para construir modelos de planta\n\nAnalogica simes:\n\n```\nFrase concreta:\n\"O reator tem temperatura de 120 °C.\"\n\nGramática:\nsujeito + verbo + objeto + unidade\n```\n\nNo OPC-UA:\n\n```\nInformation Model:\nReactor.Temperature\n\nMeta Model:\nObject, Variable, Method, Reference, DataType, ObjectType, VariableType...\n```","updated":"2026-06-22T23:18:06.559Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:5617f3639030ebbbfd83c2060278af92"},{"href":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"5617f3639030ebbbfd83c2060278af92"},"uri":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":21417,"end":21881},{"type":"TextQuoteSelector","exact":"The transport defines different mechanisms optimized for different use cases. The first version of OPC UA is defining an optimized binary TCP protocol for high performance intranet communication as well as a mapping to accepted inter-net standards like Web Services, XML, and HTTP for firewall-friendly internet communication. Both transports are using the same message-based security model known from Web Services. The abstract communication model does not depend","prefix":" mecha-nisms and data modeling. ","suffix":" transport mechanisms are descri"}]}]}
>```
>%%
>*%%PREFIX%%mecha-nisms and data modeling.%%HIGHLIGHT%% ==The transport defines different mechanisms optimized for different use cases. The first version of OPC UA is defining an optimized binary TCP protocol for high performance intranet communication as well as a mapping to accepted inter-net standards like Web Services, XML, and HTTP for firewall-friendly internet communication. Both transports are using the same message-based security model known from Web Services. The abstract communication model does not depend== %%POSTFIX%%transport mechanisms are descri*
>%%LINK%%[[#^w684vg9yjc|show annotation]]
>%%COMMENT%%
>**Transport **é o mecanismo concreto que leva mensagens de um cliente para um servidor.
>
>Os autores dizem que o transporte define mecanismos otimizados para diferentes usos. No meu caso que fiz uma comunicação em cima de gRPC:
>* gRPC não substitui a ideia de OPC UA.
>* gRPC poderia ser uma escolha de transporte/RPC.
>* OPC UA fornece a semântica industrial e o modelo de informação.
>
>**Data modeling** é a forma como OPC UA descreve aquilo que existe no sistema industrial.
>
>Não é só dizer: `XMEAS(9) = 120.4`; com modelagem, você consegue dizer algo mais estruturado:
>
>```
>Reactor
> ├── Temperature
> │    ├── value = 120.4
> │    ├── engineering unit = °C
> │    ├── quality = good
> │    ├── timestamp = ...
> │    └── alarm limits = ...
> ├── Pressure
> ├── Level
> └── CoolingWaterFlow
>```
>Um **information model** é o modelo concreto de uma planta, equipamento ou domínio.
>**meta model** é o conjunto de regras que permite construir esse modelo. Ou seja:
>- Information Model = o modelo da planta
>- Meta Model = as regras para construir modelos de planta
>
>Analogica simes:
>
>```
>Frase concreta:
>"O reator tem temperatura de 120 °C."
>
>Gramática:
>sujeito + verbo + objeto + unidade
>```
>
>No OPC-UA:
>
>```
>Information Model:
>Reactor.Temperature
>
>Meta Model:
>Object, Variable, Method, Reference, DataType, ObjectType, VariableType...
>```
>%%TAGS%%
>
^w684vg9yjc


>%%
>```annotation-json
>{"created":"2026-06-22T23:32:29.620Z","text":"Por isso vou ler um pouco essa norma.","updated":"2026-06-22T23:32:29.620Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:5617f3639030ebbbfd83c2060278af92"},{"href":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"5617f3639030ebbbfd83c2060278af92"},"uri":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":24893,"end":24937},{"type":"TextQuoteSelector","exact":"OPC UA will be known as IEC 62541 standards.","prefix":"quired for IEC standardization. ","suffix":" Figure 1.8 shows an overview of"}]}]}
>```
>%%
>*%%PREFIX%%quired for IEC standardization.%%HIGHLIGHT%% ==OPC UA will be known as IEC 62541 standards.== %%POSTFIX%%Figure 1.8 shows an overview of*
>%%LINK%%[[#^9l7v9h0aol|show annotation]]
>%%COMMENT%%
>Por isso vou ler um pouco essa norma.
>%%TAGS%%
>
^9l7v9h0aol


>%%
>```annotation-json
>{"created":"2026-06-22T23:35:16.807Z","text":"É uma das partes que irei lei. No meu projeto seria algo assim:\n- Servidor = planta TEP expondo informações;\n- Cliente = supervisor, dashboard, controller, logger, diagnóstico\n- Services = operações possíveis entre eles;\n\nOs serviços OPC-UA definem qual informação é trocada, mas não fixam diretamente:\n- a representação concreta na rede;\n- a representação concreta na API usada pela aplicação;\n\nExiste uma separação arquitetural entre serviço abstrato e representação concreta na rede.\n\n","updated":"2026-06-22T23:35:16.807Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:5617f3639030ebbbfd83c2060278af92"},{"href":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"5617f3639030ebbbfd83c2060278af92"},"uri":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":25693,"end":26046},{"type":"TextQuoteSelector","exact":"The abstract UA Services defined in [UA Part 4] represent the possible inter-actions between UA client and UA server applications. The client uses the Services but not the concrete representation on the wire and also not the concrete represen-tation in an API used by the applications. Figure 1.9 shows the layered communi-cation architecture of OPC UA.","prefix":"an OPC UA server address space. ","suffix":"  Fig. 1.9 Layered OPC UA commun"}]}]}
>```
>%%
>*%%PREFIX%%an OPC UA server address space.%%HIGHLIGHT%% ==The abstract UA Services defined in [UA Part 4] represent the possible inter-actions between UA client and UA server applications. The client uses the Services but not the concrete representation on the wire and also not the concrete represen-tation in an API used by the applications. Figure 1.9 shows the layered communi-cation architecture of OPC UA.== %%POSTFIX%%Fig. 1.9 Layered OPC UA commun*
>%%LINK%%[[#^ei2o64qh0oj|show annotation]]
>%%COMMENT%%
>É uma das partes que irei lei. No meu projeto seria algo assim:
>- Servidor = planta TEP expondo informações;
>- Cliente = supervisor, dashboard, controller, logger, diagnóstico
>- Services = operações possíveis entre eles;
>
>Os serviços OPC-UA definem qual informação é trocada, mas não fixam diretamente:
>- a representação concreta na rede;
>- a representação concreta na API usada pela aplicação;
>
>Existe uma separação arquitetural entre serviço abstrato e representação concreta na rede.
>
>
>%%TAGS%%
>
^ei2o64qh0oj


>%%
>```annotation-json
>{"created":"2026-06-22T23:38:41.958Z","text":"A Part 4 define quais interações existem entre cliente e servidor, como ler, escrever, navegar e assinar dados.\nA Part 6 define como esses serviços são mapeados para uma tecnologia concreta, como Web Service ou UA TCP Binding.\nA API no topo é apenas a forma como a aplicação/programador acessa essa pilha; ela não é a definição formal do OPC UA.\n\nOu seja, é uma proposta de camadas.","updated":"2026-06-22T23:38:41.958Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:5617f3639030ebbbfd83c2060278af92"},{"href":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"5617f3639030ebbbfd83c2060278af92"},"uri":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":26048,"end":26098},{"type":"TextQuoteSelector","exact":"Fig. 1.9 Layered OPC UA communication architecture","prefix":"cation architecture of OPC UA.  ","suffix":" \u0014\u0015 \u0014\u0003,QWURGXFWLRQto find and ac"}]}]}
>```
>%%
>*%%PREFIX%%cation architecture of OPC UA.%%HIGHLIGHT%% ==Fig. 1.9 Layered OPC UA communication architecture== %%POSTFIX%% ,QWURGXFWLRQto find and ac*
>%%LINK%%[[#^anecfhr9xu9|show annotation]]
>%%COMMENT%%
>A Part 4 define quais interações existem entre cliente e servidor, como ler, escrever, navegar e assinar dados.
>A Part 6 define como esses serviços são mapeados para uma tecnologia concreta, como Web Service ou UA TCP Binding.
>A API no topo é apenas a forma como a aplicação/programador acessa essa pilha; ela não é a definição formal do OPC UA.
>
>Ou seja, é uma proposta de camadas.
>%%TAGS%%
>
^anecfhr9xu9


>%%
>```annotation-json
>{"created":"2026-06-22T23:48:07.751Z","text":"Essa imagem só está dizendo que existem duas aplicações OPC UA conversando:\n```\nUA Client  → consome informação\nUA Server  → fornece informação\n```\n\nEntre elas existe uma fronteira:\n\n```\nProcess Boundary or Network\n```\nOu seja: elas podem estar no mesmo computador, em processos diferentes, ou em máquinas diferentes pela rede.\n\nCada lado tem três camadas:\n\nApplication  = lógica do seu sistema\nSDK          = biblioteca que facilita usar OPC UA\nStack        = camada que cuida da comunicação OPC UA\n\na imagem também indica que essas aplicações podem ser implementadas em tecnologias diferentes, como C/C++, .NET ou Java. Então um servidor OPC UA poderia estar em C++, enquanto um cliente OPC UA poderia estar em Java, desde que ambos respeitem a pilha OPC UA.","updated":"2026-06-22T23:48:07.751Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:5617f3639030ebbbfd83c2060278af92"},{"href":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"5617f3639030ebbbfd83c2060278af92"},"uri":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Introduction-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":30102,"end":30134},{"type":"TextQuoteSelector","exact":"Fig. 1.10 OPC UA software layers","prefix":"ndation UA Stack deliverables.  ","suffix":" An OPC UA Application is a syst"}]}]}
>```
>%%
>*%%PREFIX%%ndation UA Stack deliverables.%%HIGHLIGHT%% ==Fig. 1.10 OPC UA software layers== %%POSTFIX%%An OPC UA Application is a syst*
>%%LINK%%[[#^3o5bkotnx1f|show annotation]]
>%%COMMENT%%
>Essa imagem só está dizendo que existem duas aplicações OPC UA conversando:
>```
>UA Client  → consome informação
>UA Server  → fornece informação
>```
>
>Entre elas existe uma fronteira:
>
>```
>Process Boundary or Network
>```
>Ou seja: elas podem estar no mesmo computador, em processos diferentes, ou em máquinas diferentes pela rede.
>
>Cada lado tem três camadas:
>
>Application  = lógica do seu sistema
>SDK          = biblioteca que facilita usar OPC UA
>Stack        = camada que cuida da comunicação OPC UA
>
>a imagem também indica que essas aplicações podem ser implementadas em tecnologias diferentes, como C/C++, .NET ou Java. Então um servidor OPC UA poderia estar em C++, enquanto um cliente OPC UA poderia estar em Java, desde que ambos respeitem a pilha OPC UA.
>%%TAGS%%
>
^3o5bkotnx1f
