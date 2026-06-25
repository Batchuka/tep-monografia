---
annotation-target: articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf
titulo: Kubernetes Orchestration of High Availability Distributed Control Systems
autor: Bjarne Johansson, Mats Rågebrergi, Thomas Nolte, Alessandro V. Papadopoulos
ano:
fonte: ABB, Västerås, Sweden; Mälardalen University
tags: precedente_ousado
---

>%%
>```annotation-json
>{"text":"O foco prático do artigo é alta disponibilidade de controladores virtualizados, usando Kubernetes para recuperar/reimplantar VDCNs após falhas.\n\nEle não tenta usar Kubernetes para controlar o processo em tempo real; usa Kubernetes como camada de orquestração/supervisão para reduzir dependência de substituição manual e restaurar redundância mais rápido.\n\n## Provocação\n\nPodemos dizer que não há diferença em derrubar um controlador defeituso por um controlador que não está performando conforme a política da planta","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":0,"end":72},{"type":"TextQuoteSelector","exact":"Kubernetes Orchestration of High AvailabilityDistributed Control Systems","prefix":"na50%75%100%125%150%200%300%400%","suffix":"Bjarne Johansson1,2, Mats R ̊agb"}]}],"created":"2026-06-12T11:56:16.221Z","updated":"2026-06-12T11:56:16.221Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}
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
>Podemos dizer que não há diferença em derrubar um controlador defeituso por um controlador que não está performando conforme a política da planta
>%%TAGS%%
>
^168kxptvjoc









>%%
>```annotation-json
>{"created":"2026-06-15T19:56:20.747Z","text":"Aqui o artigo atribui ao orquestrador uma decisão operacional: escolher onde implantar containers conforme a situação dos recursos. Para mim, isso é supervisão de execução, não apenas infraestrutura passiva.","updated":"2026-06-15T19:56:20.747Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":3884,"end":4025},{"type":"TextQuoteSelector","exact":". The central functionalityprovided by the orchestrator is situation-aware scheduling anddeployment of containers on the available resources.","prefix":"arathon on Mesos, and Kubernetes","suffix":"We study the failure recovery pr"}]}]}
>```
>%%
>*%%PREFIX%%arathon on Mesos, and Kubernetes%%HIGHLIGHT%% ==. The central functionalityprovided by the orchestrator is situation-aware scheduling anddeployment of containers on the available resources.== %%POSTFIX%%We study the failure recovery pr*
>%%LINK%%[[#^22pvotovnw|show annotation]]
>%%COMMENT%%
>Aqui o artigo atribui ao orquestrador uma decisão operacional: escolher onde implantar containers conforme a situação dos recursos. Para mim, isso é supervisão de execução, não apenas infraestrutura passiva.
>%%TAGS%%
>
^22pvotovnw


>%%
>```annotation-json
>{"created":"2026-06-15T19:57:10.836Z","text":"O autor observa que Kubernetes opera por laço de reconciliação, empurrando o estado atual para o estado desejado. Isso é diretamente análogo a controle supervisório discreto.","updated":"2026-06-15T19:57:10.836Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":11183,"end":11272},{"type":"TextQuoteSelector","exact":"kube-controller-manager: control loops drivingthe actual state towards the desired state.","prefix":"and node resource availability.•","suffix":"Compute node components:•kubelet"}]}]}
>```
>%%
>*%%PREFIX%%and node resource availability.•%%HIGHLIGHT%% ==kube-controller-manager: control loops drivingthe actual state towards the desired state.== %%POSTFIX%%Compute node components:•kubelet*
>%%LINK%%[[#^hizflflrj1r|show annotation]]
>%%COMMENT%%
>O autor observa que Kubernetes opera por laço de reconciliação, empurrando o estado atual para o estado desejado. Isso é diretamente análogo a controle supervisório discreto.
>%%TAGS%%
>
^hizflflrj1r


>%%
>```annotation-json
>{"created":"2026-06-15T19:59:03.243Z","text":"O artigo literalmente descreve uma funcionalidade obtida usando Kubernetes para controlar instâncias de controladores virtualizados. Aqui o objeto supervisionado não é uma aplicação web: é um VDCN, isto é, um nó controlador industrial virtualizado.","updated":"2026-06-15T19:59:03.243Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":21222,"end":21384},{"type":"TextQuoteSelector","exact":"VDCN Pod controller: The VDCN Pod controller is thename we have given to denote the functionality we achieveby utilizing Kubernetes for controlling the VDCN Pods.","prefix":"the node(host) network directly.","suffix":" Anapplication running on a Kube"}]}]}
>```
>%%
>*%%PREFIX%%the node(host) network directly.%%HIGHLIGHT%% ==VDCN Pod controller: The VDCN Pod controller is thename we have given to denote the functionality we achieveby utilizing Kubernetes for controlling the VDCN Pods.== %%POSTFIX%%Anapplication running on a Kube*
>%%LINK%%[[#^ld85cpnlz7i|show annotation]]
>%%COMMENT%%
>O artigo literalmente descreve uma funcionalidade obtida usando Kubernetes para controlar instâncias de controladores virtualizados. Aqui o objeto supervisionado não é uma aplicação web: é um VDCN, isto é, um nó controlador industrial virtualizado.
>%%TAGS%%
>
^ld85cpnlz7i


>%%
>```annotation-json
>{"created":"2026-06-15T20:00:23.299Z","text":"Essa é a mais forte para impacto direto na planta: Kubernetes decide o roteamento para o VDCN primário com base no estado da aplicação. Isso afeta qual controlador recebe comunicação OPC UA e, portanto, qual instância participa da operação.","updated":"2026-06-15T20:00:23.299Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":25040,"end":25182},{"type":"TextQuoteSelector","exact":"To allow Kubernetes to redirect the trafficto VDCN in primary mode, we need Kubernetes to updatethe routes depending on the application state.","prefix":"nt VDCN isapplication-specific. ","suffix":" A Kubernetesmechanism for that "}]}]}
>```
>%%
>*%%PREFIX%%nt VDCN isapplication-specific.%%HIGHLIGHT%% ==To allow Kubernetes to redirect the trafficto VDCN in primary mode, we need Kubernetes to updatethe routes depending on the application state.== %%POSTFIX%%A Kubernetesmechanism for that*
>%%LINK%%[[#^wxsxxu4um99|show annotation]]
>%%COMMENT%%
>Essa é a mais forte para impacto direto na planta: Kubernetes decide o roteamento para o VDCN primário com base no estado da aplicação. Isso afeta qual controlador recebe comunicação OPC UA e, portanto, qual instância participa da operação.
>%%TAGS%%
>
^wxsxxu4um99


>%%
>```annotation-json
>{"created":"2026-06-15T20:01:23.275Z","text":"Aqui o artigo confia ao Kubernetes detectar falha e reimplantar o VDCN afetado; no caso redundante, o backup vira primário e o Kubernetes recria o backup. Isso é decisão supervisória com efeito direto na continuidade do controle.","updated":"2026-06-15T20:01:23.275Z","document":{"title":"art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","link":[{"href":"urn:x-pdf:b8db418eb169ff0f2f93de0a9cc24250"},{"href":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf"}],"documentFingerprint":"b8db418eb169ff0f2f93de0a9cc24250"},"uri":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","target":[{"source":"vault:/articles/art10_Kubernetes-Orchestration-of-High-Availability_Johansson_et_al.pdf","selector":[{"type":"TextPositionSelector","start":30276,"end":30495},{"type":"TextQuoteSelector","exact":"Then, Kubernetes failure detection and rescheduling re-deploy the VDCN affected by the node failure. In the redun-dant VDCN case, the backup VDCN resumes operation asprimary, while Kubernetes re-deploy a new backup VDCN","prefix":"single VDCN after a randomtime. ","suffix":". AVerification DCN sample the s"}]}]}
>```
>%%
>*%%PREFIX%%single VDCN after a randomtime.%%HIGHLIGHT%% ==Then, Kubernetes failure detection and rescheduling re-deploy the VDCN affected by the node failure. In the redun-dant VDCN case, the backup VDCN resumes operation asprimary, while Kubernetes re-deploy a new backup VDCN== %%POSTFIX%%. AVerification DCN sample the s*
>%%LINK%%[[#^ia0qrovuiei|show annotation]]
>%%COMMENT%%
>Aqui o artigo confia ao Kubernetes detectar falha e reimplantar o VDCN afetado; no caso redundante, o backup vira primário e o Kubernetes recria o backup. Isso é decisão supervisória com efeito direto na continuidade do controle.
>%%TAGS%%
>
^ia0qrovuiei
