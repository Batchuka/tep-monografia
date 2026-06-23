---
annotation-target: books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf
titulo: OPC Unified Architecture — Services
autor: Mahnke, W.; Leitner, S.-H.; Damm, M.
ano: 2009
fonte: Springer
tema:
---

## O que diz


## O que me interessa


## Conexões

- [[]]

## Citação ABNT

```bibtex
@book{Mahnke2009,
  author    = {Mahnke, Wolfgang and Leitner, Stefan-Helmut and Damm, Matthias},
  title     = {{OPC} Unified Architecture},
  publisher = {Springer},
  year      = {2009},
}
```


>%%
>```annotation-json
>{"created":"2026-06-22T23:56:15.559Z","text":"Camadas do OPC-UA e suas respectivas abstrações.","updated":"2026-06-22T23:56:15.559Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":3108,"end":3146},{"type":"TextQuoteSelector","exact":"Fig. 5.1 OPC UA communication layering","prefix":"tions.  For  example,  a  Read  ","suffix":" Table 5.1 Services grouped by u"}]}]}
>```
>%%
>*%%PREFIX%%tions.  For  example,  a  Read%%HIGHLIGHT%% ==Fig. 5.1 OPC UA communication layering== %%POSTFIX%%Table 5.1 Services grouped by u*
>%%LINK%%[[#^x1mu7q6ul09|show annotation]]
>%%COMMENT%%
>Camadas do OPC-UA e suas respectivas abstrações.
>%%TAGS%%
>
^x1mu7q6ul09


>%%
>```annotation-json
>{"created":"2026-06-22T23:57:10.157Z","text":"OPC UA Services definem a comunicação em nível de aplicação entre cliente e servidor OPC UA, permitindo acessar dados do Information Model exposto pelo servidor.","updated":"2026-06-22T23:57:10.157Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":18,"end":91},{"type":"TextQuoteSelector","exact":"OPC UA Services are defining the data communication on application level.","prefix":"0%200%300%400%5.1  Overview The ","suffix":" Services are methods used by an"}]}]}
>```
>%%
>*%%PREFIX%%0%200%300%400%5.1  Overview The%%HIGHLIGHT%% ==OPC UA Services are defining the data communication on application level.== %%POSTFIX%%Services are methods used by an*
>%%LINK%%[[#^fpubwm6tp18|show annotation]]
>%%COMMENT%%
>OPC UA Services definem a comunicação em nível de aplicação entre cliente e servidor OPC UA, permitindo acessar dados do Information Model exposto pelo servidor.
>%%TAGS%%
>
^fpubwm6tp18


>%%
>```annotation-json
>{"created":"2026-06-22T23:57:54.403Z","text":"A definição desses serviços é abstrata e independente do protocolo de transporte e da linguagem de programação, diferentemente do Classic OPC ligado ao COM da Microsoft.","updated":"2026-06-22T23:57:54.403Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":416,"end":736},{"type":"TextQuoteSelector","exact":"The definition of the Services is independent of the transport protocol and the pro-gramming environment that is used to develop an OPC UA application. This is the fundamental difference to Classic OPC where the definition of the APIs was bound to a specific transport mechanism – Microsoft Component Object Model (COM).","prefix":"erface between UA applications. ","suffix":" The independence of the transpo"}]}]}
>```
>%%
>*%%PREFIX%%erface between UA applications.%%HIGHLIGHT%% ==The definition of the Services is independent of the transport protocol and the pro-gramming environment that is used to develop an OPC UA application. This is the fundamental difference to Classic OPC where the definition of the APIs was bound to a specific transport mechanism – Microsoft Component Object Model (COM).== %%POSTFIX%%The independence of the transpo*
>%%LINK%%[[#^z5n4j05xaos|show annotation]]
>%%COMMENT%%
>A definição desses serviços é abstrata e independente do protocolo de transporte e da linguagem de programação, diferentemente do Classic OPC ligado ao COM da Microsoft.
>%%TAGS%%
>
^z5n4j05xaos


>%%
>```annotation-json
>{"created":"2026-06-23T00:00:36.227Z","text":"Essa tabela está aí para fazer uma coisa simples: traduzir necessidades típicas de comunicação OPC UA em conjuntos formais de Services.\n\nA coluna da esquerda é o caso de uso: “o que um cliente OPC UA quer fazer?”.\nA coluna da direita é o Service Set ou serviço que a especificação fornece para isso.\n\nPor exemplo:\n\n* Para encontrar servidores, usa-se Discovery Services Set.\n* Para abrir e manter conexão segura, usa-se Secure Channel Service Set e Session Service Set.\n* Para navegar no modelo de informação do servidor, usa-se View Service Set.\n* Para ler e escrever variáveis e metadados, usa-se Read e Write.\n* Para receber mudanças de dados e eventos, usa-se Subscription Service Set e Monitored Item Service Set.\n* Para chamar métodos expostos pelo servidor, usa-se Call Service.\n* Para ler histórico, usa-se HistoryRead e HistoryUpdate.\n* Para consultas mais complexas no Address Space, usa-se Query Service Set.\n* Para alterar a estrutura do Address Space, usa-se Node Management Service Set.\n\npara cada tipo de interação formal entre aplicações OPC UA, existe um conjunto de serviços padronizado","updated":"2026-06-23T00:00:36.227Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":3147,"end":3186},{"type":"TextQuoteSelector","exact":"Table 5.1 Services grouped by use cases","prefix":"1 OPC UA communication layering ","suffix":" Use case  Service sets or servi"}]}]}
>```
>%%
>*%%PREFIX%%1 OPC UA communication layering%%HIGHLIGHT%% ==Table 5.1 Services grouped by use cases== %%POSTFIX%%Use case  Service sets or servi*
>%%LINK%%[[#^c3cv7j7o0lq|show annotation]]
>%%COMMENT%%
>Essa tabela está aí para fazer uma coisa simples: traduzir necessidades típicas de comunicação OPC UA em conjuntos formais de Services.
>
>A coluna da esquerda é o caso de uso: “o que um cliente OPC UA quer fazer?”.
>A coluna da direita é o Service Set ou serviço que a especificação fornece para isso.
>
>Por exemplo:
>
>* Para encontrar servidores, usa-se Discovery Services Set.
>* Para abrir e manter conexão segura, usa-se Secure Channel Service Set e Session Service Set.
>* Para navegar no modelo de informação do servidor, usa-se View Service Set.
>* Para ler e escrever variáveis e metadados, usa-se Read e Write.
>* Para receber mudanças de dados e eventos, usa-se Subscription Service Set e Monitored Item Service Set.
>* Para chamar métodos expostos pelo servidor, usa-se Call Service.
>* Para ler histórico, usa-se HistoryRead e HistoryUpdate.
>* Para consultas mais complexas no Address Space, usa-se Query Service Set.
>* Para alterar a estrutura do Address Space, usa-se Node Management Service Set.
>
>para cada tipo de interação formal entre aplicações OPC UA, existe um conjunto de serviços padronizado
>%%TAGS%%
>
^c3cv7j7o0lq


>%%
>```annotation-json
>{"created":"2026-06-23T00:05:16.334Z","text":"Antes de trocar dados, cliente e servidor precisam estabelecer contextos de comunicação em camadas. É preciso settar o servidor e o cliente para se prepararem, eles precisam estar em um estado. \n\nPonto importante: a maior parte dos Services existe para criar, manter e gerenciar contexto, não simplesmente para transportar dados.\n\nUm contexto é o conjunto de informações que cliente e servidor mantêm sobre aquela relação: quem é o cliente, qual sessão está ativa, quais permissões existem, quais subscriptions foram criadas, quais itens estão sendo monitorados, quais timeouts valem, quais handles identificam chamadas anteriores.\n\n* **Secure Channel:** é o contexto de segurança da comunicação.\n* **Session:** é o contexto lógico entre cliente e servidor.\n* **Subscription: **é o contexto de notificações criado dentro de uma Session.\n* **Monitored Item:** é o contexto de “este Node/Attribute deve ser observado”.","updated":"2026-06-23T00:05:16.334Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":11168,"end":11443},{"type":"TextQuoteSelector","exact":"OPC UA  Services are  not stateless and  cannot be  called without establishing  a communication context on different levels. For this reason a lot of Services are not used for data transfer but to create, maintain, and modify these different levels of communication context ","prefix":"ts. 5.2.5 Communication Context ","suffix":"illustrated in Fig. 5.2.  Fig. 5"}]}]}
>```
>%%
>*%%PREFIX%%ts. 5.2.5 Communication Context%%HIGHLIGHT%% ==OPC UA  Services are  not stateless and  cannot be  called without establishing  a communication context on different levels. For this reason a lot of Services are not used for data transfer but to create, maintain, and modify these different levels of communication context== %%POSTFIX%%illustrated in Fig. 5.2.  Fig. 5*
>%%LINK%%[[#^a7wjv52qo7r|show annotation]]
>%%COMMENT%%
>Antes de trocar dados, cliente e servidor precisam estabelecer contextos de comunicação em camadas. É preciso settar o servidor e o cliente para se prepararem, eles precisam estar em um estado. 
>
>Ponto importante: a maior parte dos Services existe para criar, manter e gerenciar contexto, não simplesmente para transportar dados.
>
>Um contexto é o conjunto de informações que cliente e servidor mantêm sobre aquela relação: quem é o cliente, qual sessão está ativa, quais permissões existem, quais subscriptions foram criadas, quais itens estão sendo monitorados, quais timeouts valem, quais handles identificam chamadas anteriores.
>
>* **Secure Channel:** é o contexto de segurança da comunicação.
>* **Session:** é o contexto lógico entre cliente e servidor.
>* **Subscription: **é o contexto de notificações criado dentro de uma Session.
>* **Monitored Item:** é o contexto de “este Node/Attribute deve ser observado”.
>%%TAGS%%
>
^a7wjv52qo7r


>%%
>```annotation-json
>{"created":"2026-06-23T00:12:07.619Z","text":"| Parâmetro                       | Significado simples                                                                                                                 |\n| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |\n| `View`                          | Limita a navegação a uma visão específica do `Address Space`. Se quiser navegar tudo, deixa vazio.                                  |\n| `RequestedMaxReferencesPerNode` | Limita quantos nós o servidor pode devolver por nó inicial. Evita resposta gigante. Se faltar resultado, usa `BrowseNext`.          |\n| `NodesToBrowse[]`               | Lista de nós de partida que o cliente quer explorar. Cada item tem filtros próprios.                                                |\n| `NodeId`                        | O identificador do nó inicial. É o “comece a navegar a partir daqui”.                                                               |\n| `BrowseDirection`               | Diz se o servidor deve seguir referências para frente, para trás ou nos dois sentidos.                                              |\n| `ReferenceTypeId`               | Diz qual tipo de relação seguir. Exemplo: seguir só referências hierárquicas, como `HasComponent`, `Organizes`, etc.                |\n| `IncludeSubtypes`               | Diz se subtipos daquele tipo de referência também devem ser considerados. Normalmente fica `true`.                                  |\n| `NodeClassMask`                 | Filtra o tipo de nó retornado: `Object`, `Variable`, `Method`, `View`, etc.                                                         |\n| `ResultMask`                    | Controla quais informações vêm na resposta. O `NodeId` sempre vem; o resto, como nome, classe e tipo, pode ser incluído ou omitido. |\n","updated":"2026-06-23T00:12:07.619Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":33994,"end":34030},{"type":"TextQuoteSelector","exact":"Table 5.13 Browse Service parameters","prefix":"rameters of the Browse Service. ","suffix":" Request parameters  Description"}]}]}
>```
>%%
>*%%PREFIX%%rameters of the Browse Service.%%HIGHLIGHT%% ==Table 5.13 Browse Service parameters== %%POSTFIX%%Request parameters  Description*
>%%LINK%%[[#^nqbitwz4o7l|show annotation]]
>%%COMMENT%%
>| Parâmetro                       | Significado simples                                                                                                                 |
>| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
>| `View`                          | Limita a navegação a uma visão específica do `Address Space`. Se quiser navegar tudo, deixa vazio.                                  |
>| `RequestedMaxReferencesPerNode` | Limita quantos nós o servidor pode devolver por nó inicial. Evita resposta gigante. Se faltar resultado, usa `BrowseNext`.          |
>| `NodesToBrowse[]`               | Lista de nós de partida que o cliente quer explorar. Cada item tem filtros próprios.                                                |
>| `NodeId`                        | O identificador do nó inicial. É o “comece a navegar a partir daqui”.                                                               |
>| `BrowseDirection`               | Diz se o servidor deve seguir referências para frente, para trás ou nos dois sentidos.                                              |
>| `ReferenceTypeId`               | Diz qual tipo de relação seguir. Exemplo: seguir só referências hierárquicas, como `HasComponent`, `Organizes`, etc.                |
>| `IncludeSubtypes`               | Diz se subtipos daquele tipo de referência também devem ser considerados. Normalmente fica `true`.                                  |
>| `NodeClassMask`                 | Filtra o tipo de nó retornado: `Object`, `Variable`, `Method`, `View`, etc.                                                         |
>| `ResultMask`                    | Controla quais informações vêm na resposta. O `NodeId` sempre vem; o resto, como nome, classe e tipo, pode ser incluído ou omitido. |
>
>%%TAGS%%
>
^nqbitwz4o7l


>%%
>```annotation-json
>{"created":"2026-06-23T19:20:02.471Z","text":"Imagine um **PLC/DCS do TEP** servindo dados industriais via **UA Server**: temperaturas, pressões, níveis, válvulas, alarmes e estados de malha. Esse servidor usa o serviço **RegisterServer **para se anunciar no **Discovery Server**, dizendo basicamente: \n>“eu existo, estou online e estes são meus dados de identificação”.\n\nDepois, uma aplicação cliente — por exemplo, um **historiador**, uma **IHM **ou um **serviço de diagnóstico** — consulta o **Discovery Server **com **FindServers **para descobrir quais servidores OPC UA estão disponíveis na rede.\n\nAo encontrar o servidor do PLC, o cliente chama **GetEndpoints **diretamente no UA Server para obter os detalhes concretos de conexão: endereço, protocolo, política de segurança, certificados e modos de autenticação.\n\nEntão a imagem mostra o fluxo básico: o servidor se registra, o cliente descobre quem existe, e depois pergunta ao servidor como se conectar de forma correta e segura.","updated":"2026-06-23T19:20:02.471Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":16619,"end":16682},{"type":"TextQuoteSelector","exact":"Fig. 5.3 Use of Discovery server and the Discovery Service Set ","prefix":" OPC UA. \u0014\u0016\u00145.3 Finding Servers ","suffix":"5.3.1 Service FindServers The Fi"}]}]}
>```
>%%
>*%%PREFIX%%OPC UA. 5.3 Finding Servers%%HIGHLIGHT%% ==Fig. 5.3 Use of Discovery server and the Discovery Service Set== %%POSTFIX%%5.3.1 Service FindServers The Fi*
>%%LINK%%[[#^ayg87kmdg7q|show annotation]]
>%%COMMENT%%
>Imagine um **PLC/DCS do TEP** servindo dados industriais via **UA Server**: temperaturas, pressões, níveis, válvulas, alarmes e estados de malha. Esse servidor usa o serviço **RegisterServer **para se anunciar no **Discovery Server**, dizendo basicamente: 
>>“eu existo, estou online e estes são meus dados de identificação”.
>
>Depois, uma aplicação cliente — por exemplo, um **historiador**, uma **IHM **ou um **serviço de diagnóstico** — consulta o **Discovery Server **com **FindServers **para descobrir quais servidores OPC UA estão disponíveis na rede.
>
>Ao encontrar o servidor do PLC, o cliente chama **GetEndpoints **diretamente no UA Server para obter os detalhes concretos de conexão: endereço, protocolo, política de segurança, certificados e modos de autenticação.
>
>Então a imagem mostra o fluxo básico: o servidor se registra, o cliente descobre quem existe, e depois pergunta ao servidor como se conectar de forma correta e segura.
>%%TAGS%%
>
^ayg87kmdg7q


>%%
>```annotation-json
>{"created":"2026-06-23T19:55:59.058Z","text":"Nessa imagem, um cliente OPC UA está consultando um servidor OPC UA para descobrir o modelo de uma máquina de estados exposta no `Address Space`. O servidor implementa uma instância concreta chamada `ReadingUaBook`, que possui um estado atual (`CurrentState`), mas a descrição completa da máquina — seus estados possíveis, transições e métodos associados — está na definição de tipo `ReadingStateType`.\n\nPara reconstruir essa máquina, o cliente não precisa conhecer tudo previamente. Ele usa Services como `Browse` para navegar pelas referências do `Address Space`, encontra os estados `Idle` e `Reading`, identifica as transições `IdleToReading` e `ReadingToIdle`, e verifica quais métodos causam essas transições, como `StartReading` e `StopReading`. Assim, o cliente consegue exibir a máquina de estados, acompanhar o estado atual e monitorar eventos de transição sem depender de uma estrutura proprietária fora do modelo OPC UA.\n","updated":"2026-06-23T19:55:59.058Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":63578,"end":63638},{"type":"TextQuoteSelector","exact":"Fig. 5.7 ReadingUaBook State Machine and its Type Definition","prefix":"nformation in the Address Space ","suffix":" If a client finds a StateMachin"}]}]}
>```
>%%
>*%%PREFIX%%nformation in the Address Space%%HIGHLIGHT%% ==Fig. 5.7 ReadingUaBook State Machine and its Type Definition== %%POSTFIX%%If a client finds a StateMachin*
>%%LINK%%[[#^1lqfn4ewzfg|show annotation]]
>%%COMMENT%%
>Nessa imagem, um cliente OPC UA está consultando um servidor OPC UA para descobrir o modelo de uma máquina de estados exposta no `Address Space`. O servidor implementa uma instância concreta chamada `ReadingUaBook`, que possui um estado atual (`CurrentState`), mas a descrição completa da máquina — seus estados possíveis, transições e métodos associados — está na definição de tipo `ReadingStateType`.
>
>Para reconstruir essa máquina, o cliente não precisa conhecer tudo previamente. Ele usa Services como `Browse` para navegar pelas referências do `Address Space`, encontra os estados `Idle` e `Reading`, identifica as transições `IdleToReading` e `ReadingToIdle`, e verifica quais métodos causam essas transições, como `StartReading` e `StopReading`. Assim, o cliente consegue exibir a máquina de estados, acompanhar o estado atual e monitorar eventos de transição sem depender de uma estrutura proprietária fora do modelo OPC UA.
>
>%%TAGS%%
>
^1lqfn4ewzfg


>%%
>```annotation-json
>{"created":"2026-06-23T20:43:15.223Z","text":"A **Fig. 5.8** mostra a estrutura lógica: uma `Session` pode ter várias `Subscriptions`, e cada `Subscription`pode ter vários `Monitored Items`. Traduzindo: primeiro o cliente cria uma sessão com o servidor; dentro dela cria uma assinatura; dentro da assinatura escolhe exatamente quais variáveis, eventos ou agregados quer acompanhar.","updated":"2026-06-23T20:43:15.223Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":72680,"end":72747},{"type":"TextQuoteSelector","exact":"Fig. 5.8 Context necessary to subscribe for data changes and Events","prefix":"ing to data changes or Events.  ","suffix":" All Monitored Items have common"}]}]}
>```
>%%
>*%%PREFIX%%ing to data changes or Events.%%HIGHLIGHT%% ==Fig. 5.8 Context necessary to subscribe for data changes and Events== %%POSTFIX%%All Monitored Items have common*
>%%LINK%%[[#^i1y6bzjliu|show annotation]]
>%%COMMENT%%
>A **Fig. 5.8** mostra a estrutura lógica: uma `Session` pode ter várias `Subscriptions`, e cada `Subscription`pode ter vários `Monitored Items`. Traduzindo: primeiro o cliente cria uma sessão com o servidor; dentro dela cria uma assinatura; dentro da assinatura escolhe exatamente quais variáveis, eventos ou agregados quer acompanhar.
>%%TAGS%%
>
^i1y6bzjliu


>%%
>```annotation-json
>{"created":"2026-06-23T20:44:02.829Z","text":"A **Fig. 5.9** mostra os parâmetros dessa assinatura. Um `Monitored Item` pode observar valor de variável, evento ou dado agregado. Ele tem `sampling interval`, `filter`, `queue`, `monitoring mode`. A `Subscription` tem `publish interval` e `publish enabled`. Ou seja: aqui o OPC UA define como amostrar, filtrar, acumular e publicar mudanças.","updated":"2026-06-23T20:44:02.829Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":73556,"end":73610},{"type":"TextQuoteSelector","exact":"Fig. 5.9 Settings for Subscription and Monitored Items","prefix":" Figure. 5.8 shows the relation ","suffix":" The sampling interval defines t"}]}]}
>```
>%%
>*%%PREFIX%%Figure. 5.8 shows the relation%%HIGHLIGHT%% ==Fig. 5.9 Settings for Subscription and Monitored Items== %%POSTFIX%%The sampling interval defines t*
>%%LINK%%[[#^0mkw1svcivop|show annotation]]
>%%COMMENT%%
>A **Fig. 5.9** mostra os parâmetros dessa assinatura. Um `Monitored Item` pode observar valor de variável, evento ou dado agregado. Ele tem `sampling interval`, `filter`, `queue`, `monitoring mode`. A `Subscription` tem `publish interval` e `publish enabled`. Ou seja: aqui o OPC UA define como amostrar, filtrar, acumular e publicar mudanças.
>%%TAGS%%
>
^0mkw1svcivop


>%%
>```annotation-json
>{"created":"2026-06-23T20:48:09.636Z","text":"A **Fig. 5.10 **mostra como as notificações são entregues. O cliente manda *Publish Requests* e o servidor segura essas requisições até ter uma notificação pronta, ou envia *Keep Alive* se nada mudou. Se alguma mensagem se perder, o cliente usa *Republish *com número de sequência.","updated":"2026-06-23T20:48:09.636Z","document":{"title":"book2_OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","link":[{"href":"urn:x-pdf:3aa16455783c204fa440443ec99dbb75"},{"href":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf"}],"documentFingerprint":"3aa16455783c204fa440443ec99dbb75"},"uri":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","target":[{"source":"vault:/books/book2_Services-OPC-Unified-Architecture_Mahnke,_Leitner_Damm.pdf","selector":[{"type":"TextPositionSelector","start":79555,"end":79598},{"type":"TextQuoteSelector","exact":"Fig. 5.10 Delivery of notification messages","prefix":"ivery of notification messages. ","suffix":" 5.7.1.2  Keep Alive Messages An"}]}]}
>```
>%%
>*%%PREFIX%%ivery of notification messages.%%HIGHLIGHT%% ==Fig. 5.10 Delivery of notification messages== %%POSTFIX%%5.7.1.2  Keep Alive Messages An*
>%%LINK%%[[#^xbbnzodrvx9|show annotation]]
>%%COMMENT%%
>A **Fig. 5.10 **mostra como as notificações são entregues. O cliente manda *Publish Requests* e o servidor segura essas requisições até ter uma notificação pronta, ou envia *Keep Alive* se nada mudou. Se alguma mensagem se perder, o cliente usa *Republish *com número de sequência.
>%%TAGS%%
>
^xbbnzodrvx9
