---
annotation-target: books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf
titulo: OPC Unified Architecture — System Architecture
autor: Mahnke, W.; Leitner, S.-H.; Damm, M.
ano: 2009
fonte: Springer
papel: integracao_formal
---

>%%
>```annotation-json
>{"created":"2026-06-24T13:53:08.585Z","text":"Esse capítulo está colocando a discussão assim: quando existem vários controladores, servidores, clientes, sistemas MES, sistemas Batch, ERP, redes industriais e redes corporativas, como as aplicações OPC UA se organizam e conversam entre si?\n\nNão é “sistema” no sentido de sistema dinâmico tipo TEP.\nÉ “sistema” no sentido de ecossistema de aplicações industriais conectadas.\n\nPelo visto, o OPC-UA encontra alojamento em todas as camadas:\n\n```\n[Controladores / PLCs]\n        |\n[SCADA / Batch / MES]\n        |\n[ERP / Planejamento / Sistemas corporativos]\n```\n\nEntão o foco é: como estruturar comunicação industrial entre várias camadas de software e automação.","updated":"2026-06-24T13:53:08.585Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":1,"end":23},{"type":"TextQuoteSelector","exact":"9 System Architecture ","prefix":"a50%75%100%125%150%200%300%400% ","suffix":"9.1   System Environment We ment"}]}]}
>```
>%%
>*%%PREFIX%%a50%75%100%125%150%200%300%400%%%HIGHLIGHT%% ==9 System Architecture== %%POSTFIX%%9.1   System Environment We ment*
>%%LINK%%[[#^txietgr3qdg|show annotation]]
>%%COMMENT%%
>Esse capítulo está colocando a discussão assim: quando existem vários controladores, servidores, clientes, sistemas MES, sistemas Batch, ERP, redes industriais e redes corporativas, como as aplicações OPC UA se organizam e conversam entre si?
>
>Não é “sistema” no sentido de sistema dinâmico tipo TEP.
>É “sistema” no sentido de ecossistema de aplicações industriais conectadas.
>
>Pelo visto, o OPC-UA encontra alojamento em todas as camadas:
>
>```
>[Controladores / PLCs]
>        |
>[SCADA / Batch / MES]
>        |
>[ERP / Planejamento / Sistemas corporativos]
>```
>
>Então o foco é: como estruturar comunicação industrial entre várias camadas de software e automação.
>%%TAGS%%
>
^txietgr3qdg



>%%
>```annotation-json
>{"created":"2026-06-24T14:25:31.940Z","text":"No meu caso, será o k8s como uma espécie de supervisor de políticas. Um CPS.","updated":"2026-06-24T14:25:31.940Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":928,"end":1284},{"type":"TextQuoteSelector","exact":"Besides the possibility to run OPC UA on different platforms, it can also be used for applying different architectural concepts at system level. In our example, several architectural concepts can be identified such as redundancy (Batch serv-ers), server-chaining (MES and Batch), or server aggregation (Batch and OPC UA servers running on the controllers).","prefix":"be deployed on UNIX plat-forms. ","suffix":" other concepts at system level."}]}]}
>```
>%%
>*%%PREFIX%%be deployed on UNIX plat-forms.%%HIGHLIGHT%% ==Besides the possibility to run OPC UA on different platforms, it can also be used for applying different architectural concepts at system level. In our example, several architectural concepts can be identified such as redundancy (Batch serv-ers), server-chaining (MES and Batch), or server aggregation (Batch and OPC UA servers running on the controllers).== %%POSTFIX%%other concepts at system level.*
>%%LINK%%[[#^xmtgv6tq0ch|show annotation]]
>%%COMMENT%%
>No meu caso, será o k8s como uma espécie de supervisor de políticas. Um CPS.
>%%TAGS%%
>
^xmtgv6tq0ch


>%%
>```annotation-json
>{"created":"2026-06-24T14:26:50.988Z","text":"É uma proposta genérica pensada para integrar todos os níveis da hierarquia industrial. É uma proposta de arquitetura para diferentes aplicações.","updated":"2026-06-24T14:26:50.988Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":93,"end":663},{"type":"TextQuoteSelector","exact":"OPC UA is designed in a generic manner and can therefore be applied in a diverse range of applications running at various locations within an organization’s network. Figure 9.1 shows an example of an environment in which OPC UA is used in various ways. In this scenario, OPC UA servers are running on controllers of the Control Network, on Batch sys-tems in the Operations Network, and are applied for MES application as a part of the production planning. Furthermore, an ERP system uses an OPC UA client as an interface for consuming services in the Corporate Network. ","prefix":"several times in this book that ","suffix":"In addition, there are not only "}]}]}
>```
>%%
>*%%PREFIX%%several times in this book that%%HIGHLIGHT%% ==OPC UA is designed in a generic manner and can therefore be applied in a diverse range of applications running at various locations within an organization’s network. Figure 9.1 shows an example of an environment in which OPC UA is used in various ways. In this scenario, OPC UA servers are running on controllers of the Control Network, on Batch sys-tems in the Operations Network, and are applied for MES application as a part of the production planning. Furthermore, an ERP system uses an OPC UA client as an interface for consuming services in the Corporate Network.== %%POSTFIX%%In addition, there are not only*
>%%LINK%%[[#^wcl5lrom4j|show annotation]]
>%%COMMENT%%
>É uma proposta genérica pensada para integrar todos os níveis da hierarquia industrial. É uma proposta de arquitetura para diferentes aplicações.
>%%TAGS%%
>
^wcl5lrom4j


>%%
>```annotation-json
>{"created":"2026-06-24T14:29:28.476Z","text":"Já a **Figura 9.2** reduz essa arquitetura ao seu padrão elementar, descrito na seção 9.2.1: um OPC UA Client envia uma requisição a um OPC UA Server, que oferece um serviço e retorna uma resposta. Assim, a arquitetura geral da Figura 9.1 é construída a partir dessa relação básica cliente-servidor, repetida em diferentes níveis da planta e da organização.","updated":"2026-06-24T14:29:28.476Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":2940,"end":2970},{"type":"TextQuoteSelector","exact":"Fig. 9.2 Client–Server pattern","prefix":"r an OPC UA system environment  ","suffix":" 9.2.2  Chained Server In the Ch"}]}]}
>```
>%%
>*%%PREFIX%%r an OPC UA system environment%%HIGHLIGHT%% ==Fig. 9.2 Client–Server pattern== %%POSTFIX%%9.2.2  Chained Server In the Ch*
>%%LINK%%[[#^i7k02sje8y|show annotation]]
>%%COMMENT%%
>Já a **Figura 9.2** reduz essa arquitetura ao seu padrão elementar, descrito na seção 9.2.1: um OPC UA Client envia uma requisição a um OPC UA Server, que oferece um serviço e retorna uma resposta. Assim, a arquitetura geral da Figura 9.1 é construída a partir dessa relação básica cliente-servidor, repetida em diferentes níveis da planta e da organização.
>%%TAGS%%
>
^i7k02sje8y


>%%
>```annotation-json
>{"created":"2026-06-24T14:30:51.406Z","text":"A **Figura 9.1** apresenta um ambiente típico de sistema OPC UA organizado em três níveis de rede: \n- a rede de controle → onde controladores expõem dados como OPC UA Servers; \n- a rede de operações → onde sistemas como Batch e MES podem atuar simultaneamente como clientes e servidores;\n- a rede corporativa → onde sistemas como ERP consomem serviços vindos das camadas inferiores. \n\nA imagem mostra, portanto, que o OPC UA não é pensado apenas como comunicação ponto a ponto entre uma aplicação e um controlador, mas como uma arquitetura de integração vertical entre diferentes aplicações industriais. \n\nA ideia é que a verticalidade se estabeleça através de uma simples relação cliente/serviço.","updated":"2026-06-24T14:30:51.406Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":2889,"end":2939},{"type":"TextQuoteSelector","exact":"Fig. 9.1 Example for an OPC UA system environment ","prefix":"ERP<<OPC UA Client>>Engineering ","suffix":" Fig. 9.2 Client–Server pattern "}]}]}
>```
>%%
>*%%PREFIX%%ERP<<OPC UA Client>>Engineering%%HIGHLIGHT%% ==Fig. 9.1 Example for an OPC UA system environment== %%POSTFIX%%Fig. 9.2 Client–Server pattern*
>%%LINK%%[[#^vckmi708w8d|show annotation]]
>%%COMMENT%%
>A **Figura 9.1** apresenta um ambiente típico de sistema OPC UA organizado em três níveis de rede: 
>- a rede de controle → onde controladores expõem dados como OPC UA Servers; 
>- a rede de operações → onde sistemas como Batch e MES podem atuar simultaneamente como clientes e servidores;
>- a rede corporativa → onde sistemas como ERP consomem serviços vindos das camadas inferiores. 
>
>A imagem mostra, portanto, que o OPC UA não é pensado apenas como comunicação ponto a ponto entre uma aplicação e um controlador, mas como uma arquitetura de integração vertical entre diferentes aplicações industriais. 
>
>A ideia é que a verticalidade se estabeleça através de uma simples relação cliente/serviço.
>%%TAGS%%
>
^vckmi708w8d


>%%
>```annotation-json
>{"created":"2026-06-24T14:37:13.568Z","text":"A **Figura 9.3** mostra o padrão Chained Server, no qual um servidor OPC UA intermediário também incorpora um cliente OPC UA interno. Com isso, uma aplicação cliente pode acessar indiretamente outro servidor através de uma camada intermediária. O ponto estratégico dessa arquitetura não é agregar ou interpretar dados, mas permitir intermediação, encadeamento e eventual função de gateway entre diferentes segmentos ou condições de comunicação.","updated":"2026-06-24T14:37:13.568Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":4025,"end":4057},{"type":"TextQuoteSelector","exact":"Fig. 9.3 Chained Server pattern ","prefix":"s a server to OPC UA Client 1.  ","suffix":"9.2.3 Server-to-Server Communica"}]}]}
>```
>%%
>*%%PREFIX%%s a server to OPC UA Client 1.%%HIGHLIGHT%% ==Fig. 9.3 Chained Server pattern== %%POSTFIX%%9.2.3 Server-to-Server Communica*
>%%LINK%%[[#^g7ug0at7xcd|show annotation]]
>%%COMMENT%%
>A **Figura 9.3** mostra o padrão Chained Server, no qual um servidor OPC UA intermediário também incorpora um cliente OPC UA interno. Com isso, uma aplicação cliente pode acessar indiretamente outro servidor através de uma camada intermediária. O ponto estratégico dessa arquitetura não é agregar ou interpretar dados, mas permitir intermediação, encadeamento e eventual função de gateway entre diferentes segmentos ou condições de comunicação.
>%%TAGS%%
>
^g7ug0at7xcd


>%%
>```annotation-json
>{"created":"2026-06-24T14:40:11.680Z","text":"Na **Figura 9.5**, o OPC UA Client externo fala apenas com o OPC UA Server 1. Mas esse Server 1 contém internamente um OPC UA Client, que consulta vários outros servidores — Server 2, Server 3 e Server 4. \n\nA diferença para o Chained Server é decisiva: \n- no chaining, o servidor intermediário funciona mais como passagem/gateway; \n- no Aggregating Server, ele coleta dados de múltiplas fontes, prepara ou processa esses dados e devolve ao cliente uma resposta composta. \n\nO próprio capítulo diz que os dados recuperados dos servidores podem ser “prepared or processed” antes da resposta, e depois reforça que o servidor agregador “concentrates the information” dos servidores subjacentes.\n\no Kubernetes não deveria conversar diretamente com todos os sinais crus da planta, nem consultar isoladamente cada serviço técnico. Ele se beneficia de uma camada intermediária que transforma múltiplas fontes — histórico, avaliação de malhas, alarmes, restrições, custo, modo operacional, diagnósticos — em um estado observado consolidado. Esse estado consolidado é o que pode alimentar o status de um recurso Kubernetes ou orientar um loop de reconciliação.\n\nExemplo da sua arquitetura:\n```\nTEP Plant Server\n  ├── XMEAS / XMV\n  ├── estados internos\n  └── distúrbios ativos\n\nHistory Service\n  └── séries temporais, tendências, eventos passados\n\nLoop Assessment Service\n  └── PI, Harris Index, oscilação, degradação\n\nConstraint / Cost Service\n  └── margem de restrição, custo operacional, modo TEP\n\nAggregating Service\n  └── compila tudo em estado supervisionável\n\nKubernetes Operator\n  └── reconcilia estado desejado vs estado observado\n```","updated":"2026-06-24T14:40:11.680Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":6144,"end":6179},{"type":"TextQuoteSelector","exact":"Fig. 9.5 Aggregating Server pattern","prefix":"4RESPONSEREQUESTRESPONSEREQUEST ","suffix":"  \u0015\u0019\u001b 9 System ArchitectureSuch "}]}]}
>```
>%%
>*%%PREFIX%%4RESPONSEREQUESTRESPONSEREQUEST%%HIGHLIGHT%% ==Fig. 9.5 Aggregating Server pattern== %%POSTFIX%% 9 System ArchitectureSuch*
>%%LINK%%[[#^4hf1svinbem|show annotation]]
>%%COMMENT%%
>Na **Figura 9.5**, o OPC UA Client externo fala apenas com o OPC UA Server 1. Mas esse Server 1 contém internamente um OPC UA Client, que consulta vários outros servidores — Server 2, Server 3 e Server 4. 
>
>A diferença para o Chained Server é decisiva: 
>- no chaining, o servidor intermediário funciona mais como passagem/gateway; 
>- no Aggregating Server, ele coleta dados de múltiplas fontes, prepara ou processa esses dados e devolve ao cliente uma resposta composta. 
>
>O próprio capítulo diz que os dados recuperados dos servidores podem ser “prepared or processed” antes da resposta, e depois reforça que o servidor agregador “concentrates the information” dos servidores subjacentes.
>
>o Kubernetes não deveria conversar diretamente com todos os sinais crus da planta, nem consultar isoladamente cada serviço técnico. Ele se beneficia de uma camada intermediária que transforma múltiplas fontes — histórico, avaliação de malhas, alarmes, restrições, custo, modo operacional, diagnósticos — em um estado observado consolidado. Esse estado consolidado é o que pode alimentar o status de um recurso Kubernetes ou orientar um loop de reconciliação.
>
>Exemplo da sua arquitetura:
>```
>TEP Plant Server
>  ├── XMEAS / XMV
>  ├── estados internos
>  └── distúrbios ativos
>
>History Service
>  └── séries temporais, tendências, eventos passados
>
>Loop Assessment Service
>  └── PI, Harris Index, oscilação, degradação
>
>Constraint / Cost Service
>  └── margem de restrição, custo operacional, modo TEP
>
>Aggregating Service
>  └── compila tudo em estado supervisionável
>
>Kubernetes Operator
>  └── reconcilia estado desejado vs estado observado
>```
>%%TAGS%%
>
^4hf1svinbem


>%%
>```annotation-json
>{"created":"2026-06-24T14:43:31.830Z","text":"A **Figura 9.10** descreve o caso de **Simple Discovery** em OPC UA. Nesse cenário, o cliente já conhece previamente o endereço do servidor, mas ainda precisa obter as descrições dos endpoints disponíveis. Para isso, ele envia uma requisição `GetEndpoints` ao `DiscoveryEndpoint` do servidor, recebe uma lista de `EndpointDescriptions` e, a partir dessas informações, seleciona um `SessionEndpoint` apropriado para iniciar a comunicação. Em seguida, o cliente envia um `OpenSecureChannel request`, indicando que a descoberta não é ainda o uso operacional dos dados, mas a etapa preliminar que permite escolher como a conexão segura será estabelecida.\n","updated":"2026-06-24T14:43:31.830Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":19081,"end":19107},{"type":"TextQuoteSelector","exact":"Fig. 9.10 Simple discovery","prefix":"s is illustrated in Fig. 9.10.  ","suffix":" \u0015\u001a\u00189.4 Discovery9.4.3.2  Normal"}]}]}
>```
>%%
>*%%PREFIX%%s is illustrated in Fig. 9.10.%%HIGHLIGHT%% ==Fig. 9.10 Simple discovery== %%POSTFIX%%9.4 Discovery9.4.3.2  Normal*
>%%LINK%%[[#^u3fnopahxhk|show annotation]]
>%%COMMENT%%
>A **Figura 9.10** descreve o caso de **Simple Discovery** em OPC UA. Nesse cenário, o cliente já conhece previamente o endereço do servidor, mas ainda precisa obter as descrições dos endpoints disponíveis. Para isso, ele envia uma requisição `GetEndpoints` ao `DiscoveryEndpoint` do servidor, recebe uma lista de `EndpointDescriptions` e, a partir dessas informações, seleciona um `SessionEndpoint` apropriado para iniciar a comunicação. Em seguida, o cliente envia um `OpenSecureChannel request`, indicando que a descoberta não é ainda o uso operacional dos dados, mas a etapa preliminar que permite escolher como a conexão segura será estabelecida.
>
>%%TAGS%%
>
^u3fnopahxhk


>%%
>```annotation-json
>{"created":"2026-06-24T14:44:35.640Z","text":"A **Figura 9.11** descreve o caso de **Normal Discovery** em OPC UA. Nesse cenário, o cliente consulta primeiro um `Local Discovery Server` por meio de uma requisição `FindServers`, recebendo como resposta uma lista de `ServerDescriptions`. A partir dessa lista, ele identifica o servidor desejado, obtém seu `DiscoveryURL` e passa então ao mesmo procedimento do caso simples: consultar o `DiscoveryEndpoint` com `GetEndpoints`, receber os `EndpointDescriptions` e abrir um canal seguro com o `SessionEndpoint`. Assim, o cliente deixa de depender do conhecimento direto de cada servidor OPC UA disponível e passa a depender de um serviço local de descoberta, que organiza e expõe os servidores existentes naquele escopo.\n","updated":"2026-06-24T14:44:35.640Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":19815,"end":19841},{"type":"TextQuoteSelector","exact":"Fig. 9.11 Normal discovery","prefix":"Normal Discovery is performed.  ","suffix":" 9.4.3.3  Hierarchical Discovery"}]}]}
>```
>%%
>*%%PREFIX%%Normal Discovery is performed.%%HIGHLIGHT%% ==Fig. 9.11 Normal discovery== %%POSTFIX%%9.4.3.3  Hierarchical Discovery*
>%%LINK%%[[#^1sg8r7fu4x4|show annotation]]
>%%COMMENT%%
>A **Figura 9.11** descreve o caso de **Normal Discovery** em OPC UA. Nesse cenário, o cliente consulta primeiro um `Local Discovery Server` por meio de uma requisição `FindServers`, recebendo como resposta uma lista de `ServerDescriptions`. A partir dessa lista, ele identifica o servidor desejado, obtém seu `DiscoveryURL` e passa então ao mesmo procedimento do caso simples: consultar o `DiscoveryEndpoint` com `GetEndpoints`, receber os `EndpointDescriptions` e abrir um canal seguro com o `SessionEndpoint`. Assim, o cliente deixa de depender do conhecimento direto de cada servidor OPC UA disponível e passa a depender de um serviço local de descoberta, que organiza e expõe os servidores existentes naquele escopo.
>
>%%TAGS%%
>
^1sg8r7fu4x4


>%%
>```annotation-json
>{"created":"2026-06-24T14:46:11.611Z","text":"A **Figura 9.12** descreve o caso de **Hierarchical Discovery** em OPC UA. Nesse cenário, o cliente consulta inicialmente um `Global Discovery Server`, que fornece descrições de servidores ou de máquinas que oferecem `Local Discovery Servers`. Caso o servidor desejado não seja encontrado diretamente, o cliente seleciona um `Local Discovery Server` apropriado e repete o processo de busca por meio de `FindServers`. Depois de identificar o servidor final, o fluxo retorna ao padrão já visto nos casos anteriores: o cliente consulta o `DiscoveryEndpoint` com `GetEndpoints`, recebe os `EndpointDescriptions` e abre um canal seguro com o `SessionEndpoint`. Esse modelo é relevante porque permite que servidores OPC UA distribuídos em diferentes locais da rede sejam descobertos por uma estrutura hierárquica, sem exigir que cada cliente conheça previamente todos os serviços disponíveis.\n","updated":"2026-06-24T14:46:11.611Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:02fea73487f87e24c3a51f760fb90761"},{"href":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"02fea73487f87e24c3a51f760fb90761"},"uri":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_System-Architecture-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":20946,"end":20979},{"type":"TextQuoteSelector","exact":"Fig. 9.12 Hierarchical discovery ","prefix":"overy is depicted in Fig. 9.12. ","suffix":"9.5   Auditing 9.5.1  Overview A"}]}]}
>```
>%%
>*%%PREFIX%%overy is depicted in Fig. 9.12.%%HIGHLIGHT%% ==Fig. 9.12 Hierarchical discovery== %%POSTFIX%%9.5   Auditing 9.5.1  Overview A*
>%%LINK%%[[#^pkycleqgozs|show annotation]]
>%%COMMENT%%
>A **Figura 9.12** descreve o caso de **Hierarchical Discovery** em OPC UA. Nesse cenário, o cliente consulta inicialmente um `Global Discovery Server`, que fornece descrições de servidores ou de máquinas que oferecem `Local Discovery Servers`. Caso o servidor desejado não seja encontrado diretamente, o cliente seleciona um `Local Discovery Server` apropriado e repete o processo de busca por meio de `FindServers`. Depois de identificar o servidor final, o fluxo retorna ao padrão já visto nos casos anteriores: o cliente consulta o `DiscoveryEndpoint` com `GetEndpoints`, recebe os `EndpointDescriptions` e abre um canal seguro com o `SessionEndpoint`. Esse modelo é relevante porque permite que servidores OPC UA distribuídos em diferentes locais da rede sejam descobertos por uma estrutura hierárquica, sem exigir que cada cliente conheça previamente todos os serviços disponíveis.
>
>%%TAGS%%
>
^pkycleqgozs
