---
annotation-target: articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf
titulo: Borg, Omega, and Kubernetes
autor: Verma, A. et al. (Google)
ano: 2015
fonte: ACM Queue, v.13, n.5
tema: runtime_supervisao/espirito
---

## O que diz


## O que me interessa


## Conexões

- [[]]

## Citação ABNT

```bibtex
@article{VERMA2015,
  author  = {Verma, Abhishek and others},
  title   = {Large-scale cluster management at {Google} with {Borg}},
  journal = {ACM Queue},
  volume  = {13},
  number  = {5},
  year    = {2015},
}
```


>%%
>```annotation-json
>{"created":"2026-06-09T12:55:17.078Z","text":"Este trecho fornece o lastro arquitetural para tratar a simulação como um sistema observável, no qual diferentes componentes podem reagir a alterações de estado. No TCC, isso justifica separar a planta simulada dos controladores e da camada supervisória, usando um estado compartilhado ou barramento de sinais como ponto de integração entre medições, atuadores e decisões de controle.","updated":"2026-06-09T12:55:17.078Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":3667,"end":4081},{"type":"TextQuoteSelector","exact":"Like Omega, Kubernetes has at its core a shared persistent store, with components watching for changes to relevant objects. In contrast to Omega, which exposes the store directly to trusted control-plane components, state in Kubernetes is accessed exclusively through a domain-specific REST API that applies higher-level versioning, validation, semantics, and policy, in support of a more diverse array of clients.","prefix":"purely Google-internal systems. ","suffix":" More importantly, Kubernetes wa"}]}]}
>```
>%%
>*%%PREFIX%%purely Google-internal systems.%%HIGHLIGHT%% ==Like Omega, Kubernetes has at its core a shared persistent store, with components watching for changes to relevant objects. In contrast to Omega, which exposes the store directly to trusted control-plane components, state in Kubernetes is accessed exclusively through a domain-specific REST API that applies higher-level versioning, validation, semantics, and policy, in support of a more diverse array of clients.== %%POSTFIX%%More importantly, Kubernetes wa*
>%%LINK%%[[#^2micfpbttzy|show annotation]]
>%%COMMENT%%
>Este trecho fornece o lastro arquitetural para tratar a simulação como um sistema observável, no qual diferentes componentes podem reagir a alterações de estado. No TCC, isso justifica separar a planta simulada dos controladores e da camada supervisória, usando um estado compartilhado ou barramento de sinais como ponto de integração entre medições, atuadores e decisões de controle.
>%%TAGS%%
>#semantica/MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^2micfpbttzy


>%%
>```annotation-json
>{"created":"2026-06-09T14:34:30.402Z","text":"Este trecho é útil porque desloca a discussão de infraestrutura bruta para unidade operacional. No TCC, a digital twin deve ser tratada como uma aplicação de processo industrial, não apenas como uma rotina numérica. Isso sustenta a decisão de modelar explicitamente a planta, seus sinais, seus controladores e sua supervisão como entidades de domínio.","updated":"2026-06-09T14:34:30.402Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":6746,"end":6849},{"type":"TextQuoteSelector","exact":"Containerization transforms the data center from being machine-oriented to being application-oriented. ","prefix":"g higher levels of utilization. ","suffix":"This section discusses two examp"}]}]}
>```
>%%
>*%%PREFIX%%g higher levels of utilization.%%HIGHLIGHT%% ==Containerization transforms the data center from being machine-oriented to being application-oriented.== %%POSTFIX%%This section discusses two examp*
>%%LINK%%[[#^6tyayrsutdb|show annotation]]
>%%COMMENT%%
>Este trecho é útil porque desloca a discussão de infraestrutura bruta para unidade operacional. No TCC, a digital twin deve ser tratada como uma aplicação de processo industrial, não apenas como uma rotina numérica. Isso sustenta a decisão de modelar explicitamente a planta, seus sinais, seus controladores e sua supervisão como entidades de domínio.
>%%TAGS%%
>#semantica/MECANISMO-MODELAGEM-POSITIVO
^6tyayrsutdb


>%%
>```annotation-json
>{"created":"2026-06-09T14:36:08.404Z","text":"Este trecho sustenta a necessidade de interfaces padronizadas entre a planta simulada e os componentes externos. No contexto do TCC, o equivalente não são endpoints HTTP necessariamente, mas canais bem definidos de troca de informação: medições observadas, variáveis manipuladas, estados operacionais, comandos e diagnósticos.\n\nA contribuição deste trecho é o conceito de saúde operacional explícita. Em uma digital twin, health checks podem representar tanto saúde de software quanto saúde da simulação: estabilidade numérica, coerência temporal, validade dos sinais e respeito aos limites físicos do processo. Isso permite supervisão automática sem misturar essa lógica com as equações da planta.","updated":"2026-06-09T14:36:08.404Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":11324,"end":11790},{"type":"TextQuoteSelector","exact":"n Borg, this API is a series of HTTP endpoints attached to each container. For example, the /healthz endpoint reports application health to the orchestrator. When an unhealthy application is detected, it is automatically terminated and restarted. This self-healing is a key building block for reliable distributed systems. (Kubernetes offers similar functionality; the health check uses a user-specified HTTP endpoint or exec command that runs inside the container.)","prefix":"of the other’s implementation. I","suffix":"Additional information can be pr"}]}]}
>```
>%%
>*%%PREFIX%%of the other’s implementation. I%%HIGHLIGHT%% ==n Borg, this API is a series of HTTP endpoints attached to each container. For example, the /healthz endpoint reports application health to the orchestrator. When an unhealthy application is detected, it is automatically terminated and restarted. This self-healing is a key building block for reliable distributed systems. (Kubernetes offers similar functionality; the health check uses a user-specified HTTP endpoint or exec command that runs inside the container.)== %%POSTFIX%%Additional information can be pr*
>%%LINK%%[[#^alzrq80v74|show annotation]]
>%%COMMENT%%
>Este trecho sustenta a necessidade de interfaces padronizadas entre a planta simulada e os componentes externos. No contexto do TCC, o equivalente não são endpoints HTTP necessariamente, mas canais bem definidos de troca de informação: medições observadas, variáveis manipuladas, estados operacionais, comandos e diagnósticos.
>
>A contribuição deste trecho é o conceito de saúde operacional explícita. Em uma digital twin, health checks podem representar tanto saúde de software quanto saúde da simulação: estabilidade numérica, coerência temporal, validade dos sinais e respeito aos limites físicos do processo. Isso permite supervisão automática sem misturar essa lógica com as equações da planta.
>%%TAGS%%
>#semantica/REQUISITO-SUPERVISAO-POSITIVO
^alzrq80v74


>%%
>```annotation-json
>{"created":"2026-06-09T14:43:23.878Z","text":"Aqui o ponto central é que Kubernetes não resolve complexidade adicionando mais ferramentas soltas, mas impondo uma gramática comum para representar objetos operacionais. Para o TCC, isso sustenta a ideia de que a digital twin não deve expor sensores, atuadores, experimentos e controladores como estruturas desconexas; todos devem seguir um modelo comum de representação para permitir automação, inspeção e extensão.","updated":"2026-06-09T14:43:23.878Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":17396,"end":17498},{"type":"TextQuoteSelector","exact":"Kubernetes attempts to avert this increased complexity by adopting a consistent approach to its APIs. ","prefix":"ications in the Borg ecosystem. ","suffix":"For example, 11 of 24acmqueue | "}]}]}
>```
>%%
>*%%PREFIX%%ications in the Borg ecosystem.%%HIGHLIGHT%% ==Kubernetes attempts to avert this increased complexity by adopting a consistent approach to its APIs.== %%POSTFIX%%For example, 11 of 24acmqueue |*
>%%LINK%%[[#^myjb8yiplhh|show annotation]]
>%%COMMENT%%
>Aqui o ponto central é que Kubernetes não resolve complexidade adicionando mais ferramentas soltas, mas impondo uma gramática comum para representar objetos operacionais. Para o TCC, isso sustenta a ideia de que a digital twin não deve expor sensores, atuadores, experimentos e controladores como estruturas desconexas; todos devem seguir um modelo comum de representação para permitir automação, inspeção e extensão.
>%%TAGS%%
>#semantica/MECANISMO-SOFTWARE-POSITIVO
^myjb8yiplhh



>%%
>```annotation-json
>{"created":"2026-06-09T14:45:04.191Z","text":"Esse é um dos trechos mais fortes para aplicar no TCC. A divisão entre metadados, especificação e status permite separar três coisas que frequentemente ficam misturadas em simuladores: a identidade do objeto, aquilo que se deseja que aconteça e aquilo que está acontecendo de fato. Na Tennessee Eastman, isso pode virar uma estrutura para representar experimento, planta, controlador, perturbação ou malha de controle.","updated":"2026-06-09T14:45:04.191Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":17692,"end":17934},{"type":"TextQuoteSelector","exact":"The Object Metadata is the same for all objects in the system; it contains information such as the object’s name, UID (unique identifier), an object version number (for optimistic concurrency control), and labels (key-value pairs, see below).","prefix":"fication (or Spec), and Status. ","suffix":" The contents of Spec and Status"}]}]}
>```
>%%
>*%%PREFIX%%fication (or Spec), and Status.%%HIGHLIGHT%% ==The Object Metadata is the same for all objects in the system; it contains information such as the object’s name, UID (unique identifier), an object version number (for optimistic concurrency control), and labels (key-value pairs, see below).== %%POSTFIX%%The contents of Spec and Status*
>%%LINK%%[[#^279orsxwwui|show annotation]]
>%%COMMENT%%
>Esse é um dos trechos mais fortes para aplicar no TCC. A divisão entre metadados, especificação e status permite separar três coisas que frequentemente ficam misturadas em simuladores: a identidade do objeto, aquilo que se deseja que aconteça e aquilo que está acontecendo de fato. Na Tennessee Eastman, isso pode virar uma estrutura para representar experimento, planta, controlador, perturbação ou malha de controle.
>%%TAGS%%
>#semantica/MECANISMO-MODELAGEM-POSITIVO
^279orsxwwui


>%%
>```annotation-json
>{"created":"2026-06-09T14:45:28.303Z","text":"Este trecho conecta diretamente Kubernetes com controle supervisório. Em controle de processos, existe sempre uma diferença entre referência e variável medida; aqui, a mesma ideia aparece em nível arquitetural. Para o TCC, Spec pode representar setpoints, modos de operação, distúrbios ativos e limites desejados, enquanto Status pode representar XMEAS, XMV efetivamente aplicado, alarmes, saturações e condição numérica da simulação.","updated":"2026-06-09T14:45:28.303Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":17935,"end":18159},{"type":"TextQuoteSelector","exact":"The contents of Spec and Status vary by object type, but their concept does not: Spec is used to describe the desired state of the object, whereas Status provides read-only information about the current state of the object. ","prefix":"s (key-value pairs, see below). ","suffix":"This uniform API provides many b"}]}]}
>```
>%%
>*%%PREFIX%%s (key-value pairs, see below).%%HIGHLIGHT%% ==The contents of Spec and Status vary by object type, but their concept does not: Spec is used to describe the desired state of the object, whereas Status provides read-only information about the current state of the object.== %%POSTFIX%%This uniform API provides many b*
>%%LINK%%[[#^8pouim8tgy|show annotation]]
>%%COMMENT%%
>Este trecho conecta diretamente Kubernetes com controle supervisório. Em controle de processos, existe sempre uma diferença entre referência e variável medida; aqui, a mesma ideia aparece em nível arquitetural. Para o TCC, Spec pode representar setpoints, modos de operação, distúrbios ativos e limites desejados, enquanto Status pode representar XMEAS, XMV efetivamente aplicado, alarmes, saturações e condição numérica da simulação.
>%%TAGS%%
>#semantica/MECANISMO-SUPERVISAO-POSITIVO
^8pouim8tgy


>%%
>```annotation-json
>{"created":"2026-06-09T14:46:09.448Z","text":"O valor aqui não é apenas organização estética. Uma API uniforme permite que ferramentas diferentes operem sobre os mesmos objetos sem conhecer todos os detalhes internos. No TCC, isso justifica a criação de uma camada de sinais e objetos operacionais que possa ser usada tanto pelo simulador quanto por controladores PID, scripts de experimento, dashboards, logs e futura supervisão.","updated":"2026-06-09T14:46:09.448Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":18231,"end":18414},{"type":"TextQuoteSelector","exact":" similar information applies to all objects, and writing generic tools that work across all objects is simpler, which in turn enables the development of a consistent user experience. ","prefix":" Learning the system is simpler:","suffix":"Learning from Borg and Omega, Ku"}]}]}
>```
>%%
>*%%PREFIX%%Learning the system is simpler:%%HIGHLIGHT%% ==similar information applies to all objects, and writing generic tools that work across all objects is simpler, which in turn enables the development of a consistent user experience.== %%POSTFIX%%Learning from Borg and Omega, Ku*
>%%LINK%%[[#^qt6q97hbd0p|show annotation]]
>%%COMMENT%%
>O valor aqui não é apenas organização estética. Uma API uniforme permite que ferramentas diferentes operem sobre os mesmos objetos sem conhecer todos os detalhes internos. No TCC, isso justifica a criação de uma camada de sinais e objetos operacionais que possa ser usada tanto pelo simulador quanto por controladores PID, scripts de experimento, dashboards, logs e futura supervisão.
>%%TAGS%%
>#semantica/MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^qt6q97hbd0p


>%%
>```annotation-json
>{"created":"2026-06-09T14:47:16.024Z","text":"Esse trecho é crucial para não misturar camadas. O autoscaler não cria pods diretamente; ele ajusta o estado desejado e deixa outro componente executar a convergência. Para a digital twin, a analogia correta é: a supervisão não deve manipular diretamente as equações diferenciais nem o vetor interno de estados; ela deve alterar referências, modos ou objetivos, enquanto planta, integrador e controladores executam a dinâmica e a atuação.","updated":"2026-06-09T14:47:16.024Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":19261,"end":19667},{"type":"TextQuoteSelector","exact":"A replication controller ensures the existence of the desired number of pods for a given role (e.g., “front end”). The autoscaler, in turn, relies on this capability and simply adjusts the desired number of pods, without worrying about how those pods are created or deleted. The autoscaler implementation can focus on demand—and usage—predictions, and ignore the details of how to implement its decisions. ","prefix":"horizontal auto-scaling system. ","suffix":"Decoupling ensures that multiple"}]}]}
>```
>%%
>*%%PREFIX%%horizontal auto-scaling system.%%HIGHLIGHT%% ==A replication controller ensures the existence of the desired number of pods for a given role (e.g., “front end”). The autoscaler, in turn, relies on this capability and simply adjusts the desired number of pods, without worrying about how those pods are created or deleted. The autoscaler implementation can focus on demand—and usage—predictions, and ignore the details of how to implement its decisions.== %%POSTFIX%%Decoupling ensures that multiple*
>%%LINK%%[[#^63hkje87gh7|show annotation]]
>%%COMMENT%%
>Esse trecho é crucial para não misturar camadas. O autoscaler não cria pods diretamente; ele ajusta o estado desejado e deixa outro componente executar a convergência. Para a digital twin, a analogia correta é: a supervisão não deve manipular diretamente as equações diferenciais nem o vetor interno de estados; ela deve alterar referências, modos ou objetivos, enquanto planta, integrador e controladores executam a dinâmica e a atuação.
>%%TAGS%%
>#semantica/MECANISMO-SUPERVISAO-POSITIVO
^63hkje87gh7


>%%
>```annotation-json
>{"created":"2026-06-09T14:48:00.024Z","text":"Este é provavelmente o trecho mais importante da seção. O padrão de reconciliação compara estado desejado e estado observado, depois toma ações para reduzir a diferença. Para o TCC, isso fornece o fundamento da camada supervisória: observar a planta simulada, comparar com uma condição operacional desejada e agir por meio de comandos discretos, ajustes de setpoint, ativação de controladores ou tratamento de falhas. A ideia de “choreography” reforça que o comportamento global pode surgir da cooperação entre pequenos loops especializados, sem exigir um controlador monolítico central.","updated":"2026-06-09T14:48:00.024Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":20268,"end":20717},{"type":"TextQuoteSelector","exact":"Consistency is also achieved through common design patterns for different Kubernetes components. The idea of a reconciliation controller loop is shared throughout Borg, Omega, and Kubernetes to improve the resiliency of a system: it compares a desired state (e.g., how many pods should match a label-selector query) against the observed state (the number of such pods that it can find), and takes actions to converge the observed and desired states.","prefix":"he containers they wish to run. ","suffix":" 13 of 24acmqueue | january-febr"}]}]}
>```
>%%
>*%%PREFIX%%he containers they wish to run.%%HIGHLIGHT%% ==Consistency is also achieved through common design patterns for different Kubernetes components. The idea of a reconciliation controller loop is shared throughout Borg, Omega, and Kubernetes to improve the resiliency of a system: it compares a desired state (e.g., how many pods should match a label-selector query) against the observed state (the number of such pods that it can find), and takes actions to converge the observed and desired states.== %%POSTFIX%%13 of 24acmqueue | january-febr*
>%%LINK%%[[#^tfcyzhuf4l|show annotation]]
>%%COMMENT%%
>Este é provavelmente o trecho mais importante da seção. O padrão de reconciliação compara estado desejado e estado observado, depois toma ações para reduzir a diferença. Para o TCC, isso fornece o fundamento da camada supervisória: observar a planta simulada, comparar com uma condição operacional desejada e agir por meio de comandos discretos, ajustes de setpoint, ativação de controladores ou tratamento de falhas. A ideia de “choreography” reforça que o comportamento global pode surgir da cooperação entre pequenos loops especializados, sem exigir um controlador monolítico central.
>%%TAGS%%
>#semantica/MECANISMO-SUPERVISAO-POSITIVO
^tfcyzhuf4l


>%%
>```annotation-json
>{"created":"2026-06-09T14:49:47.096Z","text":"Este trecho sustenta a decomposição do sistema em componentes especializados. No TCC, isso permite separar responsabilidades sem perder coerência: a planta calcula a dinâmica, o integrador avança o tempo, os controladores atuam sobre sinais e o supervisor reconcilia objetivos. A decomposição, porém, deve respeitar determinismo e ordem temporal da simulação.","updated":"2026-06-09T14:49:47.096Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":20988,"end":21475},{"type":"TextQuoteSelector","exact":"The design of Kubernetes as a combination of microservices and small control loops is an example of control through choreography—achieving a desired emergent behavior by combining the effects of separate, autonomous entities that collaborate. This is a conscious design choice in contrast to a centralized orchestration system, which may be easier to construct at first but tends to become brittle and rigid over time, especially in the presence of unanticipated errors or state changes.","prefix":"ply picks up where it left off. ","suffix":" THINGS TO AVOID While developin"}]}]}
>```
>%%
>*%%PREFIX%%ply picks up where it left off.%%HIGHLIGHT%% ==The design of Kubernetes as a combination of microservices and small control loops is an example of control through choreography—achieving a desired emergent behavior by combining the effects of separate, autonomous entities that collaborate. This is a conscious design choice in contrast to a centralized orchestration system, which may be easier to construct at first but tends to become brittle and rigid over time, especially in the presence of unanticipated errors or state changes.== %%POSTFIX%%THINGS TO AVOID While developin*
>%%LINK%%[[#^i17mwiv7gxg|show annotation]]
>%%COMMENT%%
>Este trecho sustenta a decomposição do sistema em componentes especializados. No TCC, isso permite separar responsabilidades sem perder coerência: a planta calcula a dinâmica, o integrador avança o tempo, os controladores atuam sobre sinais e o supervisor reconcilia objetivos. A decomposição, porém, deve respeitar determinismo e ordem temporal da simulação.
>%%TAGS%%
>#semantica/MECANISMO-SOFTWARE-POSITIVO
^i17mwiv7gxg


>%%
>```annotation-json
>{"created":"2026-06-09T14:53:14.461Z","text":"A ideia aplicável ao TCC é que comandos sobre a planta devem passar por validação semântica. Um supervisor não deveria escrever qualquer valor em qualquer variável. Uma camada de API ou barramento validado permite impor limites, valores padrão, versionamento de configuração e consistência entre estado desejado e operação simulada.","updated":"2026-06-09T14:53:14.461Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":29088,"end":29289},{"type":"TextQuoteSelector","exact":" It does this by forcing all store accesses through a centralized API server that hides the details of the store implementation and provides services for object validation, defaulting, and versioning. ","prefix":"icies, and data transformations.","suffix":"As in Omega, the client componen"}]}]}
>```
>%%
>*%%PREFIX%%icies, and data transformations.%%HIGHLIGHT%% ==It does this by forcing all store accesses through a centralized API server that hides the details of the store implementation and provides services for object validation, defaulting, and versioning.== %%POSTFIX%%As in Omega, the client componen*
>%%LINK%%[[#^ct83gfik2z7|show annotation]]
>%%COMMENT%%
>A ideia aplicável ao TCC é que comandos sobre a planta devem passar por validação semântica. Um supervisor não deveria escrever qualquer valor em qualquer variável. Uma camada de API ou barramento validado permite impor limites, valores padrão, versionamento de configuração e consistência entre estado desejado e operação simulada.
>%%TAGS%%
>#semantica/REQUISITO-INTEGRACAO_INDUSTRIAL-POSITIVO
^ct83gfik2z7


>%%
>```annotation-json
>{"created":"2026-06-09T14:57:07.406Z","text":"Este trecho é importante porque alerta contra transformar configuração em uma linguagem informal e difícil de testar. Para o TCC, isso sustenta a decisão de representar cenários, setpoints, modos de operação e perturbações da digital twin como dados simples e versionáveis, enquanto a lógica de validação, cálculo, controle e supervisão deve permanecer em código real, testável e depurável. A configuração deve descrever o experimento; não deve esconder a lógica do sistema.","updated":"2026-06-09T14:57:07.406Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/notes/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":31677,"end":31859},{"type":"TextQuoteSelector","exact":"We believe the most effective approach is to accept this need, embrace the inevitability of programmatic configuration, and maintain a clean separation between computation and data. ","prefix":"ggers and unit test frameworks. ","suffix":"The language to represent the da"}]}]}
>```
>%%
>*%%PREFIX%%ggers and unit test frameworks.%%HIGHLIGHT%% ==We believe the most effective approach is to accept this need, embrace the inevitability of programmatic configuration, and maintain a clean separation between computation and data.== %%POSTFIX%%The language to represent the da*
>%%LINK%%[[#^usla9zax1yc|show annotation]]
>%%COMMENT%%
>Este trecho é importante porque alerta contra transformar configuração em uma linguagem informal e difícil de testar. Para o TCC, isso sustenta a decisão de representar cenários, setpoints, modos de operação e perturbações da digital twin como dados simples e versionáveis, enquanto a lógica de validação, cálculo, controle e supervisão deve permanecer em código real, testável e depurável. A configuração deve descrever o experimento; não deve esconder a lógica do sistema.
>%%TAGS%%
>#semantica/MECANISMO-SOFTWARE-POSITIVO
^usla9zax1yc
