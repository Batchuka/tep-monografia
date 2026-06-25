---
annotation-target: articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf
titulo: UNICOS — A Framework to Build Industry-Like Control Systems
autor:
ano:
fonte: CERN
papel: plataforma_abstracao
---

>%%
>```annotation-json
>{"created":"2026-06-19T21:43:48.839Z","text":"O artigo separa a planta em três níveis: \n- objetos de I/O → encapsula o canal físico; \n- objetos de campo → representa válvulas, motores, heaters ou até uma malha PID; \n- objetos de controle de processo → agrupa objetos menores e representa partes mais abstratas da planta.\n\nÉ um framework que sustenta a ideia de que o supervisor não deve observar apenas XMEAS e XMV. Ele deve observar objetos com significado: Reactor, CoolingLoop, Stripper, Separator, PIDLoop, Valve, Compressor.\n\n```yaml\nkind: ControlObject\nmetadata:\n  name: reactor-cooling-loop\nobserved:\n  pv: XMEAS(9)\n  mv: XMV(10)\n  mode: auto\n  status: running\n  interlocked: false\n```\n\nUma separação importante: isso vem do artigo como ideia de objetos hierárquicos; o YAML e a analogia com Kubernetes é minha analogia.","updated":"2026-06-19T21:43:48.839Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","target":[{"source":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":7221,"end":7995},{"type":"TextQuoteSelector","exact":"‚ The  I/O  objects  provide  the  interface  to  the  plant.  They  link  the  sensors  and  actuators  to  the  control system. Here the digitalisation process is performed and some basic treatments are carried out. Input/Output (I/O) channels shall be accessed through such objects exclusively. ‚ The  field  objects,  they  are  the  images  of  the  hardware  elements  such  as  valves,  heaters,  motors,  and others or they perform control task like such as PID loop. Process values are acquired through Input objects and process outputs are set via Output objects.  ‚ The process control objects (PCO), responsible for the control of equipment units grouping several Field objects and/or other process control objects coping with subparts of the specific equipment.","prefix":"Industry Like Control ... 3 of 9","suffix":"  The I/O and field objects are "}]}]}
>```
>%%
>*%%PREFIX%%Industry Like Control ... 3 of 9%%HIGHLIGHT%% ==‚ The  I/O  objects  provide  the  interface  to  the  plant.  They  link  the  sensors  and  actuators  to  the  control system. Here the digitalisation process is performed and some basic treatments are carried out. Input/Output (I/O) channels shall be accessed through such objects exclusively. ‚ The  field  objects,  they  are  the  images  of  the  hardware  elements  such  as  valves,  heaters,  motors,  and others or they perform control task like such as PID loop. Process values are acquired through Input objects and process outputs are set via Output objects.  ‚ The process control objects (PCO), responsible for the control of equipment units grouping several Field objects and/or other process control objects coping with subparts of the specific equipment.== %%POSTFIX%%The I/O and field objects are*
>%%LINK%%[[#^vrlwz1me4wl|show annotation]]
>%%COMMENT%%
>O artigo separa a planta em três níveis: 
>- objetos de I/O → encapsula o canal físico; 
>- objetos de campo → representa válvulas, motores, heaters ou até uma malha PID; 
>- objetos de controle de processo → agrupa objetos menores e representa partes mais abstratas da planta.
>
>É um framework que sustenta a ideia de que o supervisor não deve observar apenas XMEAS e XMV. Ele deve observar objetos com significado: Reactor, CoolingLoop, Stripper, Separator, PIDLoop, Valve, Compressor.
>
>```yaml
>kind: ControlObject
>metadata:
>  name: reactor-cooling-loop
>observed:
>  pv: XMEAS(9)
>  mv: XMV(10)
>  mode: auto
>  status: running
>  interlocked: false
>```
>
>Uma separação importante: isso vem do artigo como ideia de objetos hierárquicos; o YAML e a analogia com Kubernetes é minha analogia.
>%%TAGS%%
>
^vrlwz1me4wl


>%%
>```annotation-json
>{"created":"2026-06-19T21:57:54.997Z","text":"O objeto de controle real está no PLC. O SCADA possui uma representação sincronizada dele, chamada 'proxy'. Esse proxy permite o operador visualizar, comandar, parametrizar e confirmar se o PLC tratou a solicitação.\n\nEssa é uma passagem forte para pensar a interface entre PLC/planta e supervisor. O supervisor tipo Kubernetes não precisa escrever diretamente em sensores ou válvulas; ele pode falar com uma camada de objetos/proxies/adapters que expõe estado e aceita ações autorizadas.\n\n```yaml\nspec:\n  desiredMode: auto\nstatus:\n  plcMode: manual\n  commandAccepted: false\n  reason: \"operator_mode_required\"\n```\n\nA reconciliação não seria “abrir válvula X”; seria solicitar ao adapter industrial: “coloque o objeto em auto, se permitido pelo PLC”.","updated":"2026-06-19T21:57:54.997Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","target":[{"source":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":8448,"end":8820},{"type":"TextQuoteSelector","exact":"The UNICOS objects are implemented in the PLCs and each of them is provided with a proxy in the supervision layer. The UNICOS middleware guarantees the synchronisation between the PLC objects and  their  respective  proxies.  In  particular,  the  result  of  each  command  or  process changes  is  transmitted from a PLC object to its proxy to be displayed and archived.","prefix":"st in those selected at CERN).  ","suffix":" Operators can then check that t"}]}]}
>```
>%%
>*%%PREFIX%%st in those selected at CERN).%%HIGHLIGHT%% ==The UNICOS objects are implemented in the PLCs and each of them is provided with a proxy in the supervision layer. The UNICOS middleware guarantees the synchronisation between the PLC objects and  their  respective  proxies.  In  particular,  the  result  of  each  command  or  process changes  is  transmitted from a PLC object to its proxy to be displayed and archived.== %%POSTFIX%%Operators can then check that t*
>%%LINK%%[[#^bewryoht879|show annotation]]
>%%COMMENT%%
>O objeto de controle real está no PLC. O SCADA possui uma representação sincronizada dele, chamada 'proxy'. Esse proxy permite o operador visualizar, comandar, parametrizar e confirmar se o PLC tratou a solicitação.
>
>Essa é uma passagem forte para pensar a interface entre PLC/planta e supervisor. O supervisor tipo Kubernetes não precisa escrever diretamente em sensores ou válvulas; ele pode falar com uma camada de objetos/proxies/adapters que expõe estado e aceita ações autorizadas.
>
>```yaml
>spec:
>  desiredMode: auto
>status:
>  plcMode: manual
>  commandAccepted: false
>  reason: "operator_mode_required"
>```
>
>A reconciliação não seria “abrir válvula X”; seria solicitar ao adapter industrial: “coloque o objeto em auto, se permitido pelo PLC”.
>%%TAGS%%
>
^bewryoht879


>%%
>```annotation-json
>{"created":"2026-06-19T22:00:10.623Z","text":"O artigo mostra que um objeto PLC tem estado operacional, não apenas valor numérico. Ele recebe entradas do processo, comandos manuais, comandos automáticos, parâmetros e publica status. A lógica interna decide as ordens conforme modo, interlocks e estado.\n\nIsso vira exatamente o tipo de observed state que um supervisor pode consumir. Em vez de decidir a partir de um valor cru, ele observa estado interpretado: modo, intertravamento, partida, parada, falha, comando aceito, comando rejeitado.\n\n```yaml\nkind: PIDLoop\nmetadata:\n  name: reactor-temperature-loop\nspec:\n  desiredMode: auto\nstatus:\n  mode: auto\n  started: true\n  interlocked: false\n  saturated: true\n  health: degraded\n```\n\nAqui, `mode`, `started` e `interlocked` são sustentados pelo artigo. `health: degraded` seria uma extensão minha, calculada por diagnóstico externo, como PI, Harris, oscilação ou erro persistente.\n","updated":"2026-06-19T22:00:10.623Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","target":[{"source":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":8978,"end":9395},{"type":"TextQuoteSelector","exact":"The PLC objects implement the process behaviour. The object internal logic receives: ‚ Information from the process (process inputs: analogue or binary values from sensors and statuses of other objects);   ‚ Commands from operators;  ‚ Commands from the control logic (Auto Requests from parent PCO); ‚ Configuration parameters set during the programming phase and accessible for modification by a program specialist.","prefix":" the same principles (fig. 3).  ","suffix":" Programmer Information to Other"}]}]}
>```
>%%
>*%%PREFIX%%the same principles (fig. 3).%%HIGHLIGHT%% ==The PLC objects implement the process behaviour. The object internal logic receives: ‚ Information from the process (process inputs: analogue or binary values from sensors and statuses of other objects);   ‚ Commands from operators;  ‚ Commands from the control logic (Auto Requests from parent PCO); ‚ Configuration parameters set during the programming phase and accessible for modification by a program specialist.== %%POSTFIX%%Programmer Information to Other*
>%%LINK%%[[#^kex3gbyh9v|show annotation]]
>%%COMMENT%%
>O artigo mostra que um objeto PLC tem estado operacional, não apenas valor numérico. Ele recebe entradas do processo, comandos manuais, comandos automáticos, parâmetros e publica status. A lógica interna decide as ordens conforme modo, interlocks e estado.
>
>Isso vira exatamente o tipo de observed state que um supervisor pode consumir. Em vez de decidir a partir de um valor cru, ele observa estado interpretado: modo, intertravamento, partida, parada, falha, comando aceito, comando rejeitado.
>
>```yaml
>kind: PIDLoop
>metadata:
>  name: reactor-temperature-loop
>spec:
>  desiredMode: auto
>status:
>  mode: auto
>  started: true
>  interlocked: false
>  saturated: true
>  health: degraded
>```
>
>Aqui, `mode`, `started` e `interlocked` são sustentados pelo artigo. `health: degraded` seria uma extensão minha, calculada por diagnóstico externo, como PI, Harris, oscilação ou erro persistente.
>
>%%TAGS%%
>
^kex3gbyh9v


>%%
>```annotation-json
>{"created":"2026-06-19T22:15:45.519Z","text":"O ponto central é que o PCO não é apenas um agrupamento visual de objetos. Ele é tratado como um nó da hierarquia operacional da planta. Isso significa que ele ocupa uma posição intermediária: acima dos objetos de campo, como válvulas, motores e malhas PID, mas abaixo da operação global da planta. Como nó, ele recebe informações dos filhos, combina estados, avalia entradas de processo, aplica interlocks, executa lógica global ou máquina de estados e envia auto requests para os objetos subordinados.\n\n\nPara uma arquitetura inspirada em Kubernetes, o PCO é uma boa analogia de recurso supervisionável, mas com uma diferença essencial: ele continua pertencendo à lógica industrial/PLC. O supervisor tipo Kubernetes não substitui o PCO nem executa controle PID; ele observa o estado agregado desse nó e solicita ações autorizadas. Assim, a reconciliação não ocorre sobre sensores crus, mas sobre objetos operacionais: reator, separador, compressor, stripper, malha de resfriamento, sistema de purga etc.\n\n```yaml\nkind: PlantControlObject\nmetadata:\n  name: tep-reactor-pco\nstatus:\n  mode: normal-production\n  started: true\n  interlocked: false\n  pressureCondition: near-upper-limit\n  temperatureLoop: healthy\n  coolingValve: available\n  allowedActions:\n    - requestControlledStop\n    - reduceProductionRate\n    - switchToSafeMode\n```\n\ntransformar esse nó em um objeto observável por uma camada Kubernetes-like. O artigo sustenta a parte de que o PCO é um nó hierárquico com estado, interlocks, lógica global e comandos para filhos; a leitura Kubernetes é uma extensão arquitetural sua.","updated":"2026-06-19T22:15:45.519Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","target":[{"source":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":10881,"end":12109},{"type":"TextQuoteSelector","exact":"Whereas  the  I/O  and  field  objects  are  fully  generic  and  can  be  re-used  as  such  by  any  application,  the PCOs which are the nodes of the object hierarchy must be versatile enough to cope with complex and  application  specific  process  logic.  They  provide  indeed  developers  with  placeholders  for  the  application specific logic: ‚ Conditions for the Controlled Stop completion (used to stop the object in a controlled way). ‚ Configurable  interlock  conditions  to  stop  PCOs  in  case  of  severe  process  anomalies:  Start  interlock (avoid start-up but inducing no stop), Temporary-stop (to stop in case of anomalies but allow restart when it disappears) and Full-stop (to stop in case of anomalies but allow restart only after an operator  acknowledgement). ‚ Configurable feedbacks: The On/Off status of a PCO is the result of the combination of status of its child objects and process inputs. ‚ Global Logic: to implement global parameters computation or a finite state machine. ‚ Dependant object logic: Piece of code which drive each child object of a given PCO. It define the “auto” requests to be sent according to process inputs, the status of the PCO and if any, the finite state machine.","prefix":"or the Unit & Equipment Module  ","suffix":"   In addition to the internal o"}]}]}
>```
>%%
>*%%PREFIX%%or the Unit & Equipment Module%%HIGHLIGHT%% ==Whereas  the  I/O  and  field  objects  are  fully  generic  and  can  be  re-used  as  such  by  any  application,  the PCOs which are the nodes of the object hierarchy must be versatile enough to cope with complex and  application  specific  process  logic.  They  provide  indeed  developers  with  placeholders  for  the  application specific logic: ‚ Conditions for the Controlled Stop completion (used to stop the object in a controlled way). ‚ Configurable  interlock  conditions  to  stop  PCOs  in  case  of  severe  process  anomalies:  Start  interlock (avoid start-up but inducing no stop), Temporary-stop (to stop in case of anomalies but allow restart when it disappears) and Full-stop (to stop in case of anomalies but allow restart only after an operator  acknowledgement). ‚ Configurable feedbacks: The On/Off status of a PCO is the result of the combination of status of its child objects and process inputs. ‚ Global Logic: to implement global parameters computation or a finite state machine. ‚ Dependant object logic: Piece of code which drive each child object of a given PCO. It define the “auto” requests to be sent according to process inputs, the status of the PCO and if any, the finite state machine.== %%POSTFIX%%In addition to the internal o*
>%%LINK%%[[#^ihzbc27lcir|show annotation]]
>%%COMMENT%%
>O ponto central é que o PCO não é apenas um agrupamento visual de objetos. Ele é tratado como um nó da hierarquia operacional da planta. Isso significa que ele ocupa uma posição intermediária: acima dos objetos de campo, como válvulas, motores e malhas PID, mas abaixo da operação global da planta. Como nó, ele recebe informações dos filhos, combina estados, avalia entradas de processo, aplica interlocks, executa lógica global ou máquina de estados e envia auto requests para os objetos subordinados.
>
>
>Para uma arquitetura inspirada em Kubernetes, o PCO é uma boa analogia de recurso supervisionável, mas com uma diferença essencial: ele continua pertencendo à lógica industrial/PLC. O supervisor tipo Kubernetes não substitui o PCO nem executa controle PID; ele observa o estado agregado desse nó e solicita ações autorizadas. Assim, a reconciliação não ocorre sobre sensores crus, mas sobre objetos operacionais: reator, separador, compressor, stripper, malha de resfriamento, sistema de purga etc.
>
>```yaml
>kind: PlantControlObject
>metadata:
>  name: tep-reactor-pco
>status:
>  mode: normal-production
>  started: true
>  interlocked: false
>  pressureCondition: near-upper-limit
>  temperatureLoop: healthy
>  coolingValve: available
>  allowedActions:
>    - requestControlledStop
>    - reduceProductionRate
>    - switchToSafeMode
>```
>
>transformar esse nó em um objeto observável por uma camada Kubernetes-like. O artigo sustenta a parte de que o PCO é um nó hierárquico com estado, interlocks, lógica global e comandos para filhos; a leitura Kubernetes é uma extensão arquitetural sua.
>%%TAGS%%
>
^ihzbc27lcir


>%%
>```annotation-json
>{"created":"2026-06-19T22:17:51.515Z","text":"Essa passagem aproxima o artigo de práticas modernas como model-driven engineering, schema-driven development e recursos declarativos. Não é Kubernetes, mas há uma lógica parecida: uma descrição estruturada do sistema gera artefatos operacionais coerentes.\n\n ```yaml\nkind: PlantObject\nmetadata:\n  name: reactor-pressure-control\nspec:\n  type: loop\n  measurement: XMEAS(7)\n  actuator: XMV(6)\n  allowedActions:\n    - updateSetpoint\n    - switchMode\n    - acknowledgeAlarm\nstatus:\n  mode: auto\n  pressure: 2705\n  alarm: false\n```\n\nEssa especificação poderia gerar bindings para o simulador TEP, estrutura de telemetria, endpoints de diagnóstico e objetos observáveis para o supervisor.","updated":"2026-06-19T22:17:51.515Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","target":[{"source":"vault:/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":14854,"end":16211},{"type":"TextQuoteSelector","exact":"Objects specification  In addition to the Functional analysis, the process team has to define the complete list of parameters of each I/O and field objects. This is achieved by filling the provided EXCEL object type spreadsheets.  These  parameters  include  process  information  for  the  PLC  and  configuration  data  for  the supervision proxies.  Instantiation generation  The  first  phase  of  the  coding  can  then  start:  the  PLC  objects  and  their  PVSS  proxies  have  to  be  instantiated in the two layers. The Instance Generator, a data-driven tool, produces configuration files from the object list spreadsheets. These configuration files are imported into the PLC and SCADA, the middleware is automatically configured. From this stage, it is already possible to start the commissioning of the installation from the supervision down to the sensors and actuators.  Logic and specific HMI production/generation.  The  second  coding  phase  consists  in  producing  the  application  specific  PLC  code.  The  logic  generator tool is used to provide developers with PLC program skeletons which are compliant with the PCO hierarchy. From the functional analysis the programmer can directly start the coding of the logic into the PLC routines following precise guidelines and using the PLC skeletons as placeholders of his specific code. ","prefix":"  interact  with  the process.  ","suffix":" No  code  development  is  requ"}]}]}
>```
>%%
>*%%PREFIX%%interact  with  the process.%%HIGHLIGHT%% ==Objects specification  In addition to the Functional analysis, the process team has to define the complete list of parameters of each I/O and field objects. This is achieved by filling the provided EXCEL object type spreadsheets.  These  parameters  include  process  information  for  the  PLC  and  configuration  data  for  the supervision proxies.  Instantiation generation  The  first  phase  of  the  coding  can  then  start:  the  PLC  objects  and  their  PVSS  proxies  have  to  be  instantiated in the two layers. The Instance Generator, a data-driven tool, produces configuration files from the object list spreadsheets. These configuration files are imported into the PLC and SCADA, the middleware is automatically configured. From this stage, it is already possible to start the commissioning of the installation from the supervision down to the sensors and actuators.  Logic and specific HMI production/generation.  The  second  coding  phase  consists  in  producing  the  application  specific  PLC  code.  The  logic  generator tool is used to provide developers with PLC program skeletons which are compliant with the PCO hierarchy. From the functional analysis the programmer can directly start the coding of the logic into the PLC routines following precise guidelines and using the PLC skeletons as placeholders of his specific code.== %%POSTFIX%%No  code  development  is  requ*
>%%LINK%%[[#^n194wnhvm7|show annotation]]
>%%COMMENT%%
>Essa passagem aproxima o artigo de práticas modernas como model-driven engineering, schema-driven development e recursos declarativos. Não é Kubernetes, mas há uma lógica parecida: uma descrição estruturada do sistema gera artefatos operacionais coerentes.
>
> ```yaml
>kind: PlantObject
>metadata:
>  name: reactor-pressure-control
>spec:
>  type: loop
>  measurement: XMEAS(7)
>  actuator: XMV(6)
>  allowedActions:
>    - updateSetpoint
>    - switchMode
>    - acknowledgeAlarm
>status:
>  mode: auto
>  pressure: 2705
>  alarm: false
>```
>
>Essa especificação poderia gerar bindings para o simulador TEP, estrutura de telemetria, endpoints de diagnóstico e objetos observáveis para o supervisor.
>%%TAGS%%
>
^n194wnhvm7
