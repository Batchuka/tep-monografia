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
>{"created":"2026-06-15T19:09:33.871Z","text":"É por isso que k8s é poderoso: ele não foi criado só para “subir containers”, mas para tornar viável a operação de sistemas distribuídos complexos. \n\nEssa passagem explica por que ele virou central no cloud-native: ele pega a complexidade de rodar aplicações distribuídas e oferece uma camada operacional comum para deploy, gerenciamento e automação.","updated":"2026-06-15T19:09:33.871Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":3555,"end":4389},{"type":"TextQuoteSelector","exact":"Kubernetes is open source—a contrast to Borg and Omega, which were developed as purely Google-internal systems. Like Omega, Kubernetes has at its core a shared persistent store, with components watching for changes to relevant objects. In contrast to Omega, which exposes the store directly to trusted control-plane components, state in Kubernetes is accessed exclusively through a domain-specific REST API that applies higher-level versioning, validation, semantics, and policy, in support of a more diverse array of clients. More importantly, Kubernetes was developed with a stronger focus on the experience of developers writing applications that run in a cluster: its main design goal is to make it easy to deploy and manage complex distributed systems, while still benefiting from the improved utilization that containers enable.","prefix":"ng public-cloud infrastructure. ","suffix":" This article describes some of "}]}]}
>```
>%%
>*%%PREFIX%%ng public-cloud infrastructure.%%HIGHLIGHT%% ==Kubernetes is open source—a contrast to Borg and Omega, which were developed as purely Google-internal systems. Like Omega, Kubernetes has at its core a shared persistent store, with components watching for changes to relevant objects. In contrast to Omega, which exposes the store directly to trusted control-plane components, state in Kubernetes is accessed exclusively through a domain-specific REST API that applies higher-level versioning, validation, semantics, and policy, in support of a more diverse array of clients. More importantly, Kubernetes was developed with a stronger focus on the experience of developers writing applications that run in a cluster: its main design goal is to make it easy to deploy and manage complex distributed systems, while still benefiting from the improved utilization that containers enable.== %%POSTFIX%%This article describes some of*
>%%LINK%%[[#^dfmnntdf9a|show annotation]]
>%%COMMENT%%
>É por isso que k8s é poderoso: ele não foi criado só para “subir containers”, mas para tornar viável a operação de sistemas distribuídos complexos. 
>
>Essa passagem explica por que ele virou central no cloud-native: ele pega a complexidade de rodar aplicações distribuídas e oferece uma camada operacional comum para deploy, gerenciamento e automação.
>%%TAGS%%
>
^dfmnntdf9a


>%%
>```annotation-json
>{"created":"2026-06-15T19:12:03.469Z","text":"Esse é o motivo conceitual do poder do Kubernetes. Ele muda o objeto gerenciado: em vez de pensar “qual servidor está rodando isso?”, a operação passa a pensar “qual aplicação, com quais instâncias, métricas, versões e configurações?”. \n\nIsso é exatamente a cultura cloud-native: abstrair a infraestrutura física sem ignorá-la, e transformar aplicação em unidade operacional gerenciável.\n\nJá puxando a sardinha para uma possível aplicação do k8s em uma lógica 'plantwide', imagina poder pensar em 'política da planta' em termos de 'negócio' e não em termos de 'sinais e setpoints'? ","updated":"2026-06-15T19:12:03.469Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":6746,"end":7372},{"type":"TextQuoteSelector","exact":"Containerization transforms the data center from being machine-oriented to being application-oriented. This section discusses two examples: 3 Containers encapsulate the application environment, abstracting away many details of machines and operating systems from the application developer and the deployment infrastructure. 3 Because well-designed containers and container images are scoped to a single application, managing containers means managing applications rather than machines. This shift of management APIs from machine-oriented to application oriented dramatically improves application deployment and introspection. ","prefix":"g higher levels of utilization. ","suffix":"Application environmentThe origi"}]}]}
>```
>%%
>*%%PREFIX%%g higher levels of utilization.%%HIGHLIGHT%% ==Containerization transforms the data center from being machine-oriented to being application-oriented. This section discusses two examples: 3 Containers encapsulate the application environment, abstracting away many details of machines and operating systems from the application developer and the deployment infrastructure. 3 Because well-designed containers and container images are scoped to a single application, managing containers means managing applications rather than machines. This shift of management APIs from machine-oriented to application oriented dramatically improves application deployment and introspection.== %%POSTFIX%%Application environmentThe origi*
>%%LINK%%[[#^4o8s3mzbsm|show annotation]]
>%%COMMENT%%
>Esse é o motivo conceitual do poder do Kubernetes. Ele muda o objeto gerenciado: em vez de pensar “qual servidor está rodando isso?”, a operação passa a pensar “qual aplicação, com quais instâncias, métricas, versões e configurações?”. 
>
>Isso é exatamente a cultura cloud-native: abstrair a infraestrutura física sem ignorá-la, e transformar aplicação em unidade operacional gerenciável.
>
>Já puxando a sardinha para uma possível aplicação do k8s em uma lógica 'plantwide', imagina poder pensar em 'política da planta' em termos de 'negócio' e não em termos de 'sinais e setpoints'? 
>%%TAGS%%
>
^4o8s3mzbsm


>%%
>```annotation-json
>{"created":"2026-06-15T19:15:21.741Z","text":"Esse é o salto arquitetural. Kubernetes fica poderoso porque transforma recursos diferentes em objetos com uma gramática comum. Isso permite que aplicações, controladores, ferramentas externas e automações falem a mesma língua. Para defender popularidade, esse trecho é forte porque mostra que Kubernetes não é só runtime; ele é uma plataforma extensível baseada em objetos declarativos.\n\nNovamente, isso converge bastante a ideia do OPC-UA e da IEC 61512.","updated":"2026-06-15T19:15:21.741Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":17396,"end":17498},{"type":"TextQuoteSelector","exact":"Kubernetes attempts to avert this increased complexity by adopting a consistent approach to its APIs. ","prefix":"ications in the Borg ecosystem. ","suffix":"For example, 11 of 24acmqueue | "}]}]}
>```
>%%
>*%%PREFIX%%ications in the Borg ecosystem.%%HIGHLIGHT%% ==Kubernetes attempts to avert this increased complexity by adopting a consistent approach to its APIs.== %%POSTFIX%%For example, 11 of 24acmqueue |*
>%%LINK%%[[#^nyx82iz2we|show annotation]]
>%%COMMENT%%
>Esse é o salto arquitetural. Kubernetes fica poderoso porque transforma recursos diferentes em objetos com uma gramática comum. Isso permite que aplicações, controladores, ferramentas externas e automações falem a mesma língua. Para defender popularidade, esse trecho é forte porque mostra que Kubernetes não é só runtime; ele é uma plataforma extensível baseada em objetos declarativos.
>
>Novamente, isso converge bastante a ideia do OPC-UA e da IEC 61512.
>%%TAGS%%
>
^nyx82iz2we


>%%
>```annotation-json
>{"created":"2026-06-15T19:40:34.829Z","text":"Esse é o coração da operação declarativa. O usuário não precisa programar cada passo operacional; ele declara o que quer, e o sistema passa a observar a realidade para tentar convergir. Essa é uma das razões de Kubernetes ser tão forte em ambientes cloud-native: ele torna a infraestrutura e a aplicação manipuláveis por intenção declarada, não por sequência manual de comandos.","updated":"2026-06-15T19:40:34.829Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":17935,"end":18159},{"type":"TextQuoteSelector","exact":"The contents of Spec and Status vary by object type, but their concept does not: Spec is used to describe the desired state of the object, whereas Status provides read-only information about the current state of the object. ","prefix":"s (key-value pairs, see below). ","suffix":"This uniform API provides many b"}]}]}
>```
>%%
>*%%PREFIX%%s (key-value pairs, see below).%%HIGHLIGHT%% ==The contents of Spec and Status vary by object type, but their concept does not: Spec is used to describe the desired state of the object, whereas Status provides read-only information about the current state of the object.== %%POSTFIX%%This uniform API provides many b*
>%%LINK%%[[#^jd34omztpom|show annotation]]
>%%COMMENT%%
>Esse é o coração da operação declarativa. O usuário não precisa programar cada passo operacional; ele declara o que quer, e o sistema passa a observar a realidade para tentar convergir. Essa é uma das razões de Kubernetes ser tão forte em ambientes cloud-native: ele torna a infraestrutura e a aplicação manipuláveis por intenção declarada, não por sequência manual de comandos.
>%%TAGS%%
>
^jd34omztpom


>%%
>```annotation-json
>{"created":"2026-06-15T19:42:08.205Z","text":"Essa é a melhor explicação de por que Kubernetes funciona tão bem como supervisor. Ele não depende de um plano linear perfeito. Se algo falha, reinicia ou sai do esperado, o controller observa o estado atual e volta a tentar convergir. Isso é poderoso porque combina automação, tolerância a falhas e operação contínua.","updated":"2026-06-15T19:42:08.205Z","document":{"title":"art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","link":[{"href":"urn:x-pdf:0d92414597dc41d498fbbb79956be1af"},{"href":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf"}],"documentFingerprint":"0d92414597dc41d498fbbb79956be1af"},"uri":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","target":[{"source":"vault:/articles/art5_Borg-Omega-and-Kubernetes_Burns_Grant_Oppenheimer_Brewer_Wilkes.pdf","selector":[{"type":"TextPositionSelector","start":20268,"end":20717},{"type":"TextQuoteSelector","exact":"Consistency is also achieved through common design patterns for different Kubernetes components. The idea of a reconciliation controller loop is shared throughout Borg, Omega, and Kubernetes to improve the resiliency of a system: it compares a desired state (e.g., how many pods should match a label-selector query) against the observed state (the number of such pods that it can find), and takes actions to converge the observed and desired states.","prefix":"he containers they wish to run. ","suffix":" 13 of 24acmqueue | january-febr"}]}]}
>```
>%%
>*%%PREFIX%%he containers they wish to run.%%HIGHLIGHT%% ==Consistency is also achieved through common design patterns for different Kubernetes components. The idea of a reconciliation controller loop is shared throughout Borg, Omega, and Kubernetes to improve the resiliency of a system: it compares a desired state (e.g., how many pods should match a label-selector query) against the observed state (the number of such pods that it can find), and takes actions to converge the observed and desired states.== %%POSTFIX%%13 of 24acmqueue | january-febr*
>%%LINK%%[[#^s8wmjzyslg8|show annotation]]
>%%COMMENT%%
>Essa é a melhor explicação de por que Kubernetes funciona tão bem como supervisor. Ele não depende de um plano linear perfeito. Se algo falha, reinicia ou sai do esperado, o controller observa o estado atual e volta a tentar convergir. Isso é poderoso porque combina automação, tolerância a falhas e operação contínua.
>%%TAGS%%
>
^s8wmjzyslg8
