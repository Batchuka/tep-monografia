---
type: ft
annotation-target: articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf
titulo: Kubernetes Orchestration of High Availability Distributed Control Systems
autor: Bjarne Johansson, Mats Rågebrergi, Thomas Nolte, Alessandro V. Papadopoulos
ano:
fonte: ABB, Västerås, Sweden; Mälardalen University
tema: Kubernetes, Orquestração, Sistemas de Controle Distribuído, Alta Disponibilidade
conecta-com: []
lido-em: 2026-06-12
tags: [RUNTIME_PROPOSTA]
status: lido
---

# Nota: Kubernetes Orchestration of High Availability Distributed Control Systems

## O que diz
> *Descrição objetiva do conteúdo — sem opinião. O que o autor argumenta, prova ou propõe.*



## O que me interessa
> *Filtre o que é relevante para o TCC. Citações diretas com número de página.*



## Conexões
> *Links para outras notas, capítulos da monografia ou conceitos relacionados.*

- [[]]

## Citação ABNT
> *Cole aqui a referência formatada para usar no references.bib*

```
@article{Johansson_et_al,
  author  = {Johansson, Bjarne and Rågebrergi, Mats and Nolte, Thomas and Papadopoulos, Alessandro V.},
  title   = {Kubernetes Orchestration of High Availability Distributed Control Systems},
  institution = {ABB, Västerås, Sweden; Mälardalen University},
}
```


>%%
>```annotation-json
>{"created":"2026-06-12T11:51:34.869Z","text":"Defende que a arquitetura tradicional centrada no controlador está sendo substituída por uma topologia de rede.\n\nBase para dizer que Kubernetes não entra como modismo, mas como resposta a uma mudança arquitetural em DCS.\n\nDCS é Distributed Control System: um sistema de controle industrial distribuído, usado para controlar processos contínuos com vários controladores, sensores, atuadores e estações de operação interconectados.","updated":"2026-06-12T11:51:34.869Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":408,"end":630},{"type":"TextQuoteSelector","exact":"A mesh-like, network-centric topologyreplaces the traditional controller-centered architecture, enforc-ing the interest of cloud-, fog-, and edge-computing, wherelightweight container-based virtualization is a cornerstone.","prefix":"e In-dustry 4.0 paradigm shift. ","suffix":" Ku-bernetes is a well-known con"}]}]}
>```
>%%
>*%%PREFIX%%e In-dustry 4.0 paradigm shift.%%HIGHLIGHT%% ==A mesh-like, network-centric topologyreplaces the traditional controller-centered architecture, enforc-ing the interest of cloud-, fog-, and edge-computing, wherelightweight container-based virtualization is a cornerstone.== %%POSTFIX%%Ku-bernetes is a well-known con*
>%%LINK%%[[#^fdpinn8pyl7|show annotation]]
>%%COMMENT%%
>Defende que a arquitetura tradicional centrada no controlador está sendo substituída por uma topologia de rede.
>
>Base para dizer que Kubernetes não entra como modismo, mas como resposta a uma mudança arquitetural em DCS.
>
>DCS é Distributed Control System: um sistema de controle industrial distribuído, usado para controlar processos contínuos com vários controladores, sensores, atuadores e estações de operação interconectados.
>%%TAGS%%
>
^fdpinn8pyl7


>%%
>```annotation-json
>{"created":"2026-06-12T11:54:35.276Z","text":"Mostra a limitação operacional do modelo tradicional: falha de controlador ainda exige intervenção manual para restaurar redundância.\n\nEsse é o problema que a orquestração tenta atacar: recuperação automática após falha. isso nesse artigo né. ","updated":"2026-06-12T11:54:35.276Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":2157,"end":2362},{"type":"TextQuoteSelector","exact":"The controlledprocess dictates the critical upper bound takeover time, whichtranslates to around 500 ms for DCS in process automation [1].Manual replacement of a failed DCN is required to restoreredundancy","prefix":"e-out-of-two (1oo2) redundancy. ","suffix":".The Industry 4.0 [2] data thirs"}]}]}
>```
>%%
>*%%PREFIX%%e-out-of-two (1oo2) redundancy.%%HIGHLIGHT%% ==The controlledprocess dictates the critical upper bound takeover time, whichtranslates to around 500 ms for DCS in process automation [1].Manual replacement of a failed DCN is required to restoreredundancy== %%POSTFIX%%.The Industry 4.0 [2] data thirs*
>%%LINK%%[[#^rig58ewa39|show annotation]]
>%%COMMENT%%
>Mostra a limitação operacional do modelo tradicional: falha de controlador ainda exige intervenção manual para restaurar redundância.
>
>Esse é o problema que a orquestração tenta atacar: recuperação automática após falha. isso nesse artigo né. 
>%%TAGS%%
>
^rig58ewa39


>%%
>```annotation-json
>{"created":"2026-06-12T11:56:16.221Z","text":"O foco prático do artigo é alta disponibilidade de controladores virtualizados, usando Kubernetes para recuperar/reimplantar VDCNs após falhas.\n\nEle não tenta usar Kubernetes para controlar o processo em tempo real; usa Kubernetes como camada de orquestração/supervisão para reduzir dependência de substituição manual e restaurar redundância mais rápido.\n\n## Provocação\n\nPodemos dizer que não há diferença em derrubar um controlador defeituso por um controlador que naõ está performando conforme a política da planta","updated":"2026-06-12T11:56:16.221Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":0,"end":72},{"type":"TextQuoteSelector","exact":"Kubernetes Orchestration of High AvailabilityDistributed Control Systems","prefix":"na50%75%100%125%150%200%300%400%","suffix":"Bjarne Johansson1,2, Mats R ̊agb"}]}]}
>```
>%%
>*%%PREFIX%%na50%75%100%125%150%200%300%400%%%HIGHLIGHT%% ==Kubernetes Orchestration of High AvailabilityDistributed Control Systems== %%POSTFIX%%Bjarne Johansson1,2, Mats R ̊agb*
>%%LINK%%[[#^168kxptvjoc|show annotation]]
>%%COMMENT%%
>O foco prático do artigo é alta disponibilidade de controladores virtualizados, usando Kubernetes para recuperar/reimplantar VDCNs após falhas.
>
>Ele não tenta usar Kubernetes para controlar o processo em tempo real; usa Kubernetes como camada de orquestração/supervisão para reduzir dependência de substituição manual e restaurar redundância mais rápido.
>
>## Provocação
>
>Podemos dizer que não há diferença em derrubar um controlador defeituso por um controlador que naõ está performando conforme a política da planta
>%%TAGS%%
>
^168kxptvjoc


>%%
>```annotation-json
>{"created":"2026-06-12T11:57:02.075Z","text":"Liga Industry 4.0 à demanda por mais coleta, circulação e acesso a dados no sistema de controle.\n\nÚtil para justificar barramento de sinais, gRPC e supervisão externa ao núcleo da planta.\n\n## k8s-supervisor\nMostra que o DCS está migrando de arquitetura centrada no controlador para arquitetura centrada em rede e dados. Isso abre espaço para uma camada supervisória observando sinais distribuídos.","updated":"2026-06-12T11:57:02.075Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":2363,"end":2509},{"type":"TextQuoteSelector","exact":"The Industry 4.0 [2] data thirst drives DCS towards anetwork-centric architecture with an increased possibility ofinformation and data retrieval. ","prefix":"s required to restoreredundancy.","suffix":"Figure 1 shows a simplifiedview "}]}]}
>```
>%%
>*%%PREFIX%%s required to restoreredundancy.%%HIGHLIGHT%% ==The Industry 4.0 [2] data thirst drives DCS towards anetwork-centric architecture with an increased possibility ofinformation and data retrieval.== %%POSTFIX%%Figure 1 shows a simplifiedview*
>%%LINK%%[[#^j0xd0y27nni|show annotation]]
>%%COMMENT%%
>Liga Industry 4.0 à demanda por mais coleta, circulação e acesso a dados no sistema de controle.
>
>Útil para justificar barramento de sinais, gRPC e supervisão externa ao núcleo da planta.
>
>## k8s-supervisor
>Mostra que o DCS está migrando de arquitetura centrada no controlador para arquitetura centrada em rede e dados. Isso abre espaço para uma camada supervisória observando sinais distribuídos.
>%%TAGS%%
>
^j0xd0y27nni


>%%
>```annotation-json
>{"created":"2026-06-12T11:57:58.998Z","text":"Define a função central do orquestrador: alocar e implantar containers conforme recursos e situação do cluster.\n\n# k8s-supervisor\nAqui o Kubernetes aparece como mecanismo que reage à “situação” do sistema. Você pode reinterpretar isso como supervisão: observar condição atual e aplicar ação de orquestração.","updated":"2026-06-12T11:57:58.998Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":3885,"end":4024},{"type":"TextQuoteSelector","exact":" The central functionalityprovided by the orchestrator is situation-aware scheduling anddeployment of containers on the available resources","prefix":"rathon on Mesos, and Kubernetes.","suffix":".We study the failure recovery p"}]}]}
>```
>%%
>*%%PREFIX%%rathon on Mesos, and Kubernetes.%%HIGHLIGHT%% ==The central functionalityprovided by the orchestrator is situation-aware scheduling anddeployment of containers on the available resources== %%POSTFIX%%.We study the failure recovery p*
>%%LINK%%[[#^mphaaroj33e|show annotation]]
>%%COMMENT%%
>Define a função central do orquestrador: alocar e implantar containers conforme recursos e situação do cluster.
>
># k8s-supervisor
>Aqui o Kubernetes aparece como mecanismo que reage à “situação” do sistema. Você pode reinterpretar isso como supervisão: observar condição atual e aplicar ação de orquestração.
>%%TAGS%%
>
^mphaaroj33e


>%%
>```annotation-json
>{"created":"2026-06-12T12:02:57.172Z","text":"Os dados de processo podem circular fora do controlador principal. Isso ajuda a defender o Kubernetes/Operator como observador externo do estado da planta.","updated":"2026-06-12T12:02:57.172Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":2743,"end":2855},{"type":"TextQuoteSelector","exact":"Access to data produced near theprocess, i.e., the I/O, sensors, and actuators, does not need toinvolve the DCN.","prefix":"evicesconnected to the network. ","suffix":"This work is funded by the Knowl"}]}]}
>```
>%%
>*%%PREFIX%%evicesconnected to the network.%%HIGHLIGHT%% ==Access to data produced near theprocess, i.e., the I/O, sensors, and actuators, does not need toinvolve the DCN.== %%POSTFIX%%This work is funded by the Knowl*
>%%LINK%%[[#^cl2e5k3eln|show annotation]]
>%%COMMENT%%
>Os dados de processo podem circular fora do controlador principal. Isso ajuda a defender o Kubernetes/Operator como observador externo do estado da planta.
>%%TAGS%%
>
^cl2e5k3eln


>%%
>```annotation-json
>{"created":"2026-06-12T12:04:43.345Z","text":"O paradigma do Kubernetes é literalmente um loop de reconciliação: estado observado → comparação com estado desejado → ação corretiva.","updated":"2026-06-12T12:04:43.345Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":11183,"end":11271},{"type":"TextQuoteSelector","exact":"kube-controller-manager: control loops drivingthe actual state towards the desired state","prefix":"and node resource availability.•","suffix":".Compute node components:•kubele"}]}]}
>```
>%%
>*%%PREFIX%%and node resource availability.•%%HIGHLIGHT%% ==kube-controller-manager: control loops drivingthe actual state towards the desired state== %%POSTFIX%%.Compute node components:•kubele*
>%%LINK%%[[#^628xo0amf6|show annotation]]
>%%COMMENT%%
>O paradigma do Kubernetes é literalmente um loop de reconciliação: estado observado → comparação com estado desejado → ação corretiva.
>%%TAGS%%
>
^628xo0amf6


>%%
>```annotation-json
>{"created":"2026-06-12T12:06:09.170Z","text":"Essa passagem mostra Kubernetes reagindo ao estado da aplicação, não só ao estado da infraestrutura. É o gancho direto para supervisão: decisões externas baseadas no estado observado do sistema.","updated":"2026-06-12T12:06:09.170Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":25040,"end":25340},{"type":"TextQuoteSelector","exact":"To allow Kubernetes to redirect the trafficto VDCN in primary mode, we need Kubernetes to updatethe routes depending on the application state. A Kubernetesmechanism for that is the probes, probes that probe theapplication’s state. The application tailors the application endof the probe for its need.","prefix":"nt VDCN isapplication-specific. ","suffix":"Kubernetes provides three types "}]}]}
>```
>%%
>*%%PREFIX%%nt VDCN isapplication-specific.%%HIGHLIGHT%% ==To allow Kubernetes to redirect the trafficto VDCN in primary mode, we need Kubernetes to updatethe routes depending on the application state. A Kubernetesmechanism for that is the probes, probes that probe theapplication’s state. The application tailors the application endof the probe for its need.== %%POSTFIX%%Kubernetes provides three types*
>%%LINK%%[[#^s6gw1ufhszl|show annotation]]
>%%COMMENT%%
>Essa passagem mostra Kubernetes reagindo ao estado da aplicação, não só ao estado da infraestrutura. É o gancho direto para supervisão: decisões externas baseadas no estado observado do sistema.
>%%TAGS%%
>
^s6gw1ufhszl


>%%
>```annotation-json
>{"created":"2026-06-12T12:08:23.210Z","text":"Aqui aparece a ponte conceitual entre controlador industrial virtualizado e controlador Kubernetes.","updated":"2026-06-12T12:08:23.210Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":12146,"end":12205},{"type":"TextQuoteSelector","exact":" (iii) VDCN Pod Controller, for managingVDCN Pod instances,","prefix":"instantiated fromthe VDCN Image,","suffix":" and (iv) VDCN OPC UA Service, f"}]}]}
>```
>%%
>*%%PREFIX%%instantiated fromthe VDCN Image,%%HIGHLIGHT%% ==(iii) VDCN Pod Controller, for managingVDCN Pod instances,== %%POSTFIX%%and (iv) VDCN OPC UA Service, f*
>%%LINK%%[[#^62amnv446k8|show annotation]]
>%%COMMENT%%
>Aqui aparece a ponte conceitual entre controlador industrial virtualizado e controlador Kubernetes.
>%%TAGS%%
>
^62amnv446k8


>%%
>```annotation-json
>{"created":"2026-06-12T12:10:44.105Z","text":"Essa passagem mostra o ponto de encontro entre OPC UA e Kubernetes: o controlador industrial não desaparece; ele é empacotado como uma aplicação virtualizada dentro de um Pod. O OPC UA continua sendo a interface industrial para publicar variáveis, expor serviços e trocar dados de processo; o Kubernetes entra por fora, como camada que executa, monitora, reimplanta e roteia essa aplicação conforme seu estado.\n\nEm termos simples: OPC UA é o protocolo de comunicação industrial; Kubernetes é o runtime que hospeda e supervisiona o controlador que fala OPC UA.\nIsso é útil para o TCC porque mostra que a supervisão via Kubernetes não precisa substituir padrões industriais: ela pode operar sobre eles.","updated":"2026-06-12T12:10:44.105Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":25993,"end":26743},{"type":"TextQuoteSelector","exact":"VDCN Application: In a traditional DCN, the VDCN Ap-plication is the FW capable of executing the control loop logic.The VDCN Application used in our testbed is an ABB pro-prietary software, i.e., a modern DCN FW. It consists of threemain parts, an OPC UA stack for industrial use, a middleware,and the control loop logic. The OPC UA stack provides theOPC UA communication means, and the middleware offersfunctionality to the control logic. The middleware functionalityrelevant for this testbed is redundancy-related. Finally, thecontrol logic in the VDCN Application consists of a cyclictask with a configurable interval time. The cyclic task updatesconfigured variables each iteration and exposes the updatedvariables externally using OPC UA PubSub.","prefix":"rnetes Readiness-probe requests.","suffix":"In addition to the cyclic OPC UA"}]}]}
>```
>%%
>*%%PREFIX%%rnetes Readiness-probe requests.%%HIGHLIGHT%% ==VDCN Application: In a traditional DCN, the VDCN Ap-plication is the FW capable of executing the control loop logic.The VDCN Application used in our testbed is an ABB pro-prietary software, i.e., a modern DCN FW. It consists of threemain parts, an OPC UA stack for industrial use, a middleware,and the control loop logic. The OPC UA stack provides theOPC UA communication means, and the middleware offersfunctionality to the control logic. The middleware functionalityrelevant for this testbed is redundancy-related. Finally, thecontrol logic in the VDCN Application consists of a cyclictask with a configurable interval time. The cyclic task updatesconfigured variables each iteration and exposes the updatedvariables externally using OPC UA PubSub.== %%POSTFIX%%In addition to the cyclic OPC UA*
>%%LINK%%[[#^172gq1hzxwr|show annotation]]
>%%COMMENT%%
>Essa passagem mostra o ponto de encontro entre OPC UA e Kubernetes: o controlador industrial não desaparece; ele é empacotado como uma aplicação virtualizada dentro de um Pod. O OPC UA continua sendo a interface industrial para publicar variáveis, expor serviços e trocar dados de processo; o Kubernetes entra por fora, como camada que executa, monitora, reimplanta e roteia essa aplicação conforme seu estado.
>
>Em termos simples: OPC UA é o protocolo de comunicação industrial; Kubernetes é o runtime que hospeda e supervisiona o controlador que fala OPC UA.
>Isso é útil para o TCC porque mostra que a supervisão via Kubernetes não precisa substituir padrões industriais: ela pode operar sobre eles.
>%%TAGS%%
>
^172gq1hzxwr
