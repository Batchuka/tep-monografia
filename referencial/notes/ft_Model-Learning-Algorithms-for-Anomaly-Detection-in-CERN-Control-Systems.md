---
annotation-target: articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf
titulo: Model Learning Algorithms for Anomaly Detection in CERN Control Systems
autor: Tilaro, F.; Bradu, B.; Berges, A.; Varela, C.; Roshchin, M.
ano:
fonte:
papel: tecnica_diagnostico
---

>%%
>```annotation-json
>{"created":"2026-06-18T00:57:48.485Z","text":"Segundo esse artigo, os dados informam o estado atual, o desempenho, a estabilidade e o comportamento geral do processo. Ele defende uma abstração portanto.\n\n```yaml\napiVersion: tep.lab/v1\nkind: ProcessUnit\nmetadata:\n  name: reactor\nstatus:\n  stability: Degraded\n  performance: BelowExpected\n  observedSignals:\n    - XMEAS_9   # reactor temperature\n    - XMV_10    # reactor cooling water valve\n```\nOu seja, o k8s não sabe que a temperatura é sei lá, 122.4c, ele sabe que está degradada.","updated":"2026-06-18T00:57:48.485Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":2760,"end":2883},{"type":"TextQuoteSelector","exact":"source of useful information about the current state of the processes, their performance, stability and over-all behaviour.","prefix":"proper analysis, con-stitutes a ","suffix":" Obviously, an extensive analysi"}]}]}
>```
>%%
>*%%PREFIX%%proper analysis, con-stitutes a%%HIGHLIGHT%% ==source of useful information about the current state of the processes, their performance, stability and over-all behaviour.== %%POSTFIX%%Obviously, an extensive analysi*
>%%LINK%%[[#^u2k431tfjlm|show annotation]]
>%%COMMENT%%
>Segundo esse artigo, os dados informam o estado atual, o desempenho, a estabilidade e o comportamento geral do processo. Ele defende uma abstração portanto.
>
>```yaml
>apiVersion: tep.lab/v1
>kind: ProcessUnit
>metadata:
>  name: reactor
>status:
>  stability: Degraded
>  performance: BelowExpected
>  observedSignals:
>    - XMEAS_9   # reactor temperature
>    - XMV_10    # reactor cooling water valve
>```
>Ou seja, o k8s não sabe que a temperatura é sei lá, 122.4c, ele sabe que está degradada.
>%%TAGS%%
>
^u2k431tfjlm


>%%
>```annotation-json
>{"created":"2026-06-18T18:54:07.710Z","text":"Nesse modelo, o Kubernetes não consulta diretamente sensores ou PLCs como se eles fossem runtimes computacionais. A planta continua sendo controlada pela camada industrial própria, enquanto os sinais coletados são persistidos em uma base histórica e analisados por um serviço especializado de diagnóstico. Esse serviço transforma séries temporais de sensores, atuadores e malhas em um meta-estado supervisionável, como perda de padrão, oscilação, movimento excessivo de válvula, incoerência entre sinais ou degradação de desempenho. O supervisor inspirado em Kubernetes passa então a consultar esse serviço para comparar o estado observado com uma política declarada e, quando autorizado, acionar uma reconciliação: recomendar ressintonia, trocar perfil de controle, bloquear uma mudança de setpoint, abrir alerta operacional ou solicitar validação humana.\n\n```yaml\nkind: ControlLoopHealth\nmetadata:\n  name: reactor-temperature-loop\nspec:\n  loop:\n    pv: XMEAS_9\n    mv: XMV_10\n    controlled_unit: reactor\nstatus:\n  health: Degraded\n  observedPattern: Oscillatory\n  evidence:\n    - excessive_mv_movement\n    - persistent_pattern_deviation\n    - weak_response_coherence\n  probableCauses:\n    - pid_tuning_degradation\n    - cooling_valve_issue\n    - unmeasured_disturbance\n  recommendedActions:\n    - ReviewPIDTuning\n    - CheckCoolingValve\n    - RequireOperatorConfirmation\n```\n\nO supervisor não observa a planta apenas como um vetor instantâneo de medições, mas como um conjunto de estados derivados temporalmente. Esses estados são produzidos por serviços de diagnóstico que analisam histórico, coerência entre sinais e comportamento dinâmico das malhas, permitindo que uma política declarativa atue sobre condições como degradação, oscilação ou perda de padrão, sem substituir o controle local executado pelo PLC.","updated":"2026-06-18T18:54:07.710Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":1311,"end":1597},{"type":"TextQuoteSelector","exact":"ndeed, consistent deviations from the historical evolutions can be seen as warning signs of a possible future anomaly; these warning signs have been used to trigger a generic anomaly alarm for the specific in-coherent sensors, requiring further checks by system ex-perts and operators. ","prefix":"r time in the historical data. I","suffix":"The paper also presents some res"}]}]}
>```
>%%
>*%%PREFIX%%r time in the historical data. I%%HIGHLIGHT%% ==ndeed, consistent deviations from the historical evolutions can be seen as warning signs of a possible future anomaly; these warning signs have been used to trigger a generic anomaly alarm for the specific in-coherent sensors, requiring further checks by system ex-perts and operators.== %%POSTFIX%%The paper also presents some res*
>%%LINK%%[[#^4mle14mqi6m|show annotation]]
>%%COMMENT%%
>Nesse modelo, o Kubernetes não consulta diretamente sensores ou PLCs como se eles fossem runtimes computacionais. A planta continua sendo controlada pela camada industrial própria, enquanto os sinais coletados são persistidos em uma base histórica e analisados por um serviço especializado de diagnóstico. Esse serviço transforma séries temporais de sensores, atuadores e malhas em um meta-estado supervisionável, como perda de padrão, oscilação, movimento excessivo de válvula, incoerência entre sinais ou degradação de desempenho. O supervisor inspirado em Kubernetes passa então a consultar esse serviço para comparar o estado observado com uma política declarada e, quando autorizado, acionar uma reconciliação: recomendar ressintonia, trocar perfil de controle, bloquear uma mudança de setpoint, abrir alerta operacional ou solicitar validação humana.
>
>```yaml
>kind: ControlLoopHealth
>metadata:
>  name: reactor-temperature-loop
>spec:
>  loop:
>    pv: XMEAS_9
>    mv: XMV_10
>    controlled_unit: reactor
>status:
>  health: Degraded
>  observedPattern: Oscillatory
>  evidence:
>    - excessive_mv_movement
>    - persistent_pattern_deviation
>    - weak_response_coherence
>  probableCauses:
>    - pid_tuning_degradation
>    - cooling_valve_issue
>    - unmeasured_disturbance
>  recommendedActions:
>    - ReviewPIDTuning
>    - CheckCoolingValve
>    - RequireOperatorConfirmation
>```
>
>O supervisor não observa a planta apenas como um vetor instantâneo de medições, mas como um conjunto de estados derivados temporalmente. Esses estados são produzidos por serviços de diagnóstico que analisam histórico, coerência entre sinais e comportamento dinâmico das malhas, permitindo que uma política declarativa atue sobre condições como degradação, oscilação ou perda de padrão, sem substituir o controle local executado pelo PLC.
>%%TAGS%%
>
^4mle14mqi6m


>%%
>```annotation-json
>{"created":"2026-06-19T10:04:02.138Z","text":"Essa é uma outra abordagem, uma outra estratégia. Identificar clusters de sensores a partir de suas atribuições também indica anomalias da operação. \n\nA camada diagnóstica pode criar objetos de alto nível baseados em relações: grupos de sensores, malhas, unidades de processo, atuadores correlacionados. O supervisor observa essas entidades, não cada tag crua separadamente.\n\n## Exemplo\n\n```yaml\nkind: SignalRelationship\nmetadata:\n  name: reactor-temperature-control-relation\nspec:\n  inputs:\n    - XMV_10   # reactor cooling water flow\n  outputs:\n    - XMEAS_9  # reactor temperature\n  relationType: LogicalControlRelation\nstatus:\n  coherent: false\n  reason: OutputNotRespondingAsExpected\n```","updated":"2026-06-19T10:04:02.138Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":7524,"end":8026},{"type":"TextQuoteSelector","exact":"The analysis exploits the well-defined control system structure to discover possible sys-tematic relationships among different signals; these rela-tionships can be classified in 2 main categories: •  Physical  relationships:  two  or  more  sensors  de-ployed in the same sector or even in the same cell should not differ much in value (like to temperature sensors in contiguous cells). •  Logical  relationship:  the  control  loops  regulate some output signals as a function of some input sig-nals. ","prefix":" the complexity of the problem. ","suffix":" Both classes of these relations"}]}]}
>```
>%%
>*%%PREFIX%%the complexity of the problem.%%HIGHLIGHT%% ==The analysis exploits the well-defined control system structure to discover possible sys-tematic relationships among different signals; these rela-tionships can be classified in 2 main categories: •  Physical  relationships:  two  or  more  sensors  de-ployed in the same sector or even in the same cell should not differ much in value (like to temperature sensors in contiguous cells). •  Logical  relationship:  the  control  loops  regulate some output signals as a function of some input sig-nals.== %%POSTFIX%%Both classes of these relations*
>%%LINK%%[[#^y22ya4l7xwl|show annotation]]
>%%COMMENT%%
>Essa é uma outra abordagem, uma outra estratégia. Identificar clusters de sensores a partir de suas atribuições também indica anomalias da operação. 
>
>A camada diagnóstica pode criar objetos de alto nível baseados em relações: grupos de sensores, malhas, unidades de processo, atuadores correlacionados. O supervisor observa essas entidades, não cada tag crua separadamente.
>
>## Exemplo
>
>```yaml
>kind: SignalRelationship
>metadata:
>  name: reactor-temperature-control-relation
>spec:
>  inputs:
>    - XMV_10   # reactor cooling water flow
>  outputs:
>    - XMEAS_9  # reactor temperature
>  relationType: LogicalControlRelation
>status:
>  coherent: false
>  reason: OutputNotRespondingAsExpected
>```
>%%TAGS%%
>
^y22ya4l7xwl


>%%
>```annotation-json
>{"created":"2026-06-19T10:31:02.200Z","text":"Na mesma lógica de usar cluster, pode-se montar um modelo 'nominal' de operação, uma operação normal e detectar anomalias a partir disso. \n\nEsse modelo aprendido pode alimentar o status dos objetos: a política declarada diz o que deveria ser verdadeiro; o diagnóstico diz se o observado ainda está coerente.\n\n```yaml\nkind: PlantPolicy\nmetadata:\n  name: tep-mode-1-policy\nspec:\n  mode: Mode1\n  require:\n    reactorTemperatureLoop: Stable\n    productQuality: WithinSpec\n    pressureConstraint: Safe\nstatus:\n  observed:\n    reactorTemperatureLoop: Oscillatory\n    productQuality: WithinSpec\n    pressureConstraint: Safe\n  reconciliationNeeded: true\n```","updated":"2026-06-19T10:31:02.200Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":8121,"end":8245},{"type":"TextQuoteSelector","exact":" make a model of the system. The latter can be then used to detect change points that are distance from the reference state.","prefix":"in the controls data in order to","suffix":" It is worth noting that the cry"}]}]}
>```
>%%
>*%%PREFIX%%in the controls data in order to%%HIGHLIGHT%% ==make a model of the system. The latter can be then used to detect change points that are distance from the reference state.== %%POSTFIX%%It is worth noting that the cry*
>%%LINK%%[[#^3tokhqnpst2|show annotation]]
>%%COMMENT%%
>Na mesma lógica de usar cluster, pode-se montar um modelo 'nominal' de operação, uma operação normal e detectar anomalias a partir disso. 
>
>Esse modelo aprendido pode alimentar o status dos objetos: a política declarada diz o que deveria ser verdadeiro; o diagnóstico diz se o observado ainda está coerente.
>
>```yaml
>kind: PlantPolicy
>metadata:
>  name: tep-mode-1-policy
>spec:
>  mode: Mode1
>  require:
>    reactorTemperatureLoop: Stable
>    productQuality: WithinSpec
>    pressureConstraint: Safe
>status:
>  observed:
>    reactorTemperatureLoop: Oscillatory
>    productQuality: WithinSpec
>    pressureConstraint: Safe
>  reconciliationNeeded: true
>```
>%%TAGS%%
>
^3tokhqnpst2


>%%
>```annotation-json
>{"created":"2026-06-19T10:32:49.859Z","text":"Esse trecho sustenta a existência de uma interface entre análise e supervisão industrial. A sua contribuição pode ser propor que, em vez de apenas mostrar no SCADA, esses resultados virem estado observado formal, consumido por um supervisor declarativo que só executa ações autorizadas.","updated":"2026-06-19T10:32:49.859Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":28045,"end":28253},{"type":"TextQuoteSelector","exact":"Furthermore a specialized reporting tool has been designed and implemented in order to show the analytical results directly into the SCADA (Supervisory Control and Data Acquisition) applications at CERN [17].","prefix":"ers and oper-ators can consult. ","suffix":" The detection of these anomalie"}]}]}
>```
>%%
>*%%PREFIX%%ers and oper-ators can consult.%%HIGHLIGHT%% ==Furthermore a specialized reporting tool has been designed and implemented in order to show the analytical results directly into the SCADA (Supervisory Control and Data Acquisition) applications at CERN [17].== %%POSTFIX%%The detection of these anomalie*
>%%LINK%%[[#^52awfrids38|show annotation]]
>%%COMMENT%%
>Esse trecho sustenta a existência de uma interface entre análise e supervisão industrial. A sua contribuição pode ser propor que, em vez de apenas mostrar no SCADA, esses resultados virem estado observado formal, consumido por um supervisor declarativo que só executa ações autorizadas.
>%%TAGS%%
>
^52awfrids38
