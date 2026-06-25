---
annotation-target: articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf
titulo: Condition Monitoring of Bearing Damage in Electromechanical Drive Systems by Using Motor Current Signals of Electric Motors — A Benchmark Data Set for Data-Driven Classification
autor: Lessmeier, C.; Kimotho, J.K.; Zimmer, D.; Sextro, W.
ano: 2016
fonte: PHM Europe — European Conference of the Prognostics and Health Management Society
papel: tecnica_diagnostico
---

>%%
>```annotation-json
>{"created":"2026-06-19T22:22:32.478Z","text":"O artigo defende que o sinal de corrente do motor pode carregar informação sobre falhas mecânicas no sistema de acionamento. O ponto forte é econômico e arquitetural: em vez de instalar sensores adicionais, usa-se um sinal que já existe no inversor de frequência. O sinal é uma coisa abundante, dá até para captar no ar.\n\nIsso ajuda a pensar uma camada de supervisão porque transforma infraestrutura existente — inversor, acionamento, motor — em fonte de telemetria para diagnóstico. Mas atenção: o artigo não diz que o inversor “controla” a falha; ele apenas fornece sinal para um método externo inferir o estado do equipamento.\n\n```yaml\ncoolingPump:\n  bearingHealth: degraded\n  source: motor-current\n  confidence: 0.82\n```\nEle observa essa condição e pode abrir alerta, bloquear um modo de operação agressivo ou solicitar troca para bomba redundante, se essa ação existir.","updated":"2026-06-19T22:22:32.478Z","document":{"title":"art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","link":[{"href":"urn:x-pdf:4d2c236104636847af315274e7c30a53"},{"href":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf"}],"documentFingerprint":"4d2c236104636847af315274e7c30a53"},"uri":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","target":[{"source":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","selector":[{"type":"TextPositionSelector","start":1102,"end":1271},{"type":"TextQuoteSelector","exact":"The advantage  of  this  approach  in  general  is  that  no  additional sensors are required, as current measurements can be performed in existing  frequency inverters.","prefix":"tem  for  bearing  diagnostic.  ","suffix":" This  will help to reduce  the "}]}]}
>```
>%%
>*%%PREFIX%%tem  for  bearing  diagnostic.%%HIGHLIGHT%% ==The advantage  of  this  approach  in  general  is  that  no  additional sensors are required, as current measurements can be performed in existing  frequency inverters.== %%POSTFIX%%This  will help to reduce  the*
>%%LINK%%[[#^1ius47az3t9|show annotation]]
>%%COMMENT%%
>O artigo defende que o sinal de corrente do motor pode carregar informação sobre falhas mecânicas no sistema de acionamento. O ponto forte é econômico e arquitetural: em vez de instalar sensores adicionais, usa-se um sinal que já existe no inversor de frequência. O sinal é uma coisa abundante, dá até para captar no ar.
>
>Isso ajuda a pensar uma camada de supervisão porque transforma infraestrutura existente — inversor, acionamento, motor — em fonte de telemetria para diagnóstico. Mas atenção: o artigo não diz que o inversor “controla” a falha; ele apenas fornece sinal para um método externo inferir o estado do equipamento.
>
>```yaml
>coolingPump:
>  bearingHealth: degraded
>  source: motor-current
>  confidence: 0.82
>```
>Ele observa essa condição e pode abrir alerta, bloquear um modo de operação agressivo ou solicitar troca para bomba redundante, se essa ação existir.
>%%TAGS%%
>
^1ius47az3t9


>%%
>```annotation-json
>{"created":"2026-06-19T22:27:59.533Z","text":"O estado relevante — dano no mancal — não é uma variável medida diretamente. Ele é um estado latente inferido a partir de sinais imperfeitos. Isso reforça minha tese de que o Kubernetes não deveria consumir sinal cru; ele deveria consumir um diagnóstico já interpretado.\n\nA malha de temperatura do reator observa XMEAS(9) e atua em XMV(10). Isso é controle. Mas um serviço separado observa a corrente do motor associado ao sistema de resfriamento e detecta um padrão compatível com dano externo no rolamento.\n\n```yaml\nobservedState:\n  reactorCoolingTrain:\n    mechanicalCondition: suspected-bearing-damage\n    signalQuality: noisy\n    diagnosticConfidence: medium\n```","updated":"2026-06-19T22:27:59.533Z","document":{"title":"art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","link":[{"href":"urn:x-pdf:4d2c236104636847af315274e7c30a53"},{"href":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf"}],"documentFingerprint":"4d2c236104636847af315274e7c30a53"},"uri":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","target":[{"source":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","selector":[{"type":"TextPositionSelector","start":4934,"end":5118},{"type":"TextQuoteSelector","exact":"Detection  of  damage  in  external  bearings  is  more complex  as  the  damage  signature  has  to  be  transmitted indirectly  through  torque  variations  along  the  drive  train.","prefix":"ncies  in  the  motor current.  ","suffix":" Therefore, it is damped and sup"}]}]}
>```
>%%
>*%%PREFIX%%ncies  in  the  motor current.%%HIGHLIGHT%% ==Detection  of  damage  in  external  bearings  is  more complex  as  the  damage  signature  has  to  be  transmitted indirectly  through  torque  variations  along  the  drive  train.== %%POSTFIX%%Therefore, it is damped and sup*
>%%LINK%%[[#^c27samrwa3j|show annotation]]
>%%COMMENT%%
>O estado relevante — dano no mancal — não é uma variável medida diretamente. Ele é um estado latente inferido a partir de sinais imperfeitos. Isso reforça minha tese de que o Kubernetes não deveria consumir sinal cru; ele deveria consumir um diagnóstico já interpretado.
>
>A malha de temperatura do reator observa XMEAS(9) e atua em XMV(10). Isso é controle. Mas um serviço separado observa a corrente do motor associado ao sistema de resfriamento e detecta um padrão compatível com dano externo no rolamento.
>
>```yaml
>observedState:
>  reactorCoolingTrain:
>    mechanicalCondition: suspected-bearing-damage
>    signalQuality: noisy
>    diagnosticConfidence: medium
>```
>%%TAGS%%
>
^c27samrwa3j


>%%
>```annotation-json
>{"created":"2026-06-19T22:29:58.428Z","text":"Aqui está a conexão mais clara com a ideia de um status supervisionável. O artigo fornece uma ontologia de saúde do equipamento. Em arquitetura inspirada em Kubernetes, isso poderia virar algo próximo de uma condição declarada em um recurso: Healthy, Degraded, Faulted, DamageExtent, DamageLocation, DamageType.\n\n```yaml\nstatus:\n  conditions:\n    - type: BearingHealth\n      status: Degraded\n      reason: DistributedDamage\n      component: outer-ring\n      extentLevel: 3\n      source: diagnostic-service\n```\n\na politica poderia ser:\n\n```yaml\npolicy:\n  maxAllowedBearingExtent: 1\n  allowHighProductionMode: false\n```","updated":"2026-06-19T22:29:58.428Z","document":{"title":"art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","link":[{"href":"urn:x-pdf:4d2c236104636847af315274e7c30a53"},{"href":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf"}],"documentFingerprint":"4d2c236104636847af315274e7c30a53"},"uri":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","target":[{"source":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","selector":[{"type":"TextPositionSelector","start":12937,"end":13230},{"type":"TextQuoteSelector","exact":"The criteria were grouped into four main categories, the first three  giving  information  about  the  bearing  and  the  fourth providing detailed information about the damage. According to  these  criteria,  a  detailed  profile  (or  fact  sheet)  can  be created for any damaged bearing.  ","prefix":"criteria are shown in Table 1.  ","suffix":"The  criteria  of  the  first  g"}]}]}
>```
>%%
>*%%PREFIX%%criteria are shown in Table 1.%%HIGHLIGHT%% ==The criteria were grouped into four main categories, the first three  giving  information  about  the  bearing  and  the  fourth providing detailed information about the damage. According to  these  criteria,  a  detailed  profile  (or  fact  sheet)  can  be created for any damaged bearing.== %%POSTFIX%%The  criteria  of  the  first  g*
>%%LINK%%[[#^3oti59cma18|show annotation]]
>%%COMMENT%%
>Aqui está a conexão mais clara com a ideia de um status supervisionável. O artigo fornece uma ontologia de saúde do equipamento. Em arquitetura inspirada em Kubernetes, isso poderia virar algo próximo de uma condição declarada em um recurso: Healthy, Degraded, Faulted, DamageExtent, DamageLocation, DamageType.
>
>```yaml
>status:
>  conditions:
>    - type: BearingHealth
>      status: Degraded
>      reason: DistributedDamage
>      component: outer-ring
>      extentLevel: 3
>      source: diagnostic-service
>```
>
>a politica poderia ser:
>
>```yaml
>policy:
>  maxAllowedBearingExtent: 1
>  allowHighProductionMode: false
>```
>%%TAGS%%
>
^3oti59cma18


>%%
>```annotation-json
>{"created":"2026-06-19T22:32:25.419Z","text":"Ele precisa carregar em que condição de operação aquilo foi observado. Uma oscilação, uma assinatura de falha ou uma degradação podem ter significado diferente conforme carga, modo produtivo, regime e perturbação.\n\nUm diagnóstico de bomba poderia ser válido apenas em uma faixa operacional:\n\n```yaml\ndiagnosis:\n  component: cooling-water-pump\n  condition: degraded\n  validWhen:\n    flowRange: \"40-60%\"\n    reactorMode: \"Mode 1\"\n    loadCondition: nominal\n```\n\nSe a TEP mudar para um modo de maior produção, o supervisor não deveria reutilizar cegamente o diagnóstico antigo. Ele deveria marcar a condição como “válida parcialmente” ou exigir nova janela de observação.","updated":"2026-06-19T22:32:25.419Z","document":{"title":"art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","link":[{"href":"urn:x-pdf:4d2c236104636847af315274e7c30a53"},{"href":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf"}],"documentFingerprint":"4d2c236104636847af315274e7c30a53"},"uri":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","target":[{"source":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","selector":[{"type":"TextPositionSelector","start":41470,"end":41818},{"type":"TextQuoteSelector","exact":" Supportive  measurement  of  speed,  torque,  radial  load, and temperature.  Four different operating conditions (Table 6).  20  measurements  of  4  seconds  each  for  each  setting, saved  as  a  matlab  file  with  a  name  consisting  of  the code of the operating condition and the four-digit bearing code (e.g. N15_M07_F10_KA01_1.mat). ","prefix":"healthy) states for reference.  ","suffix":"  Systematic description of the"}]}]}
>```
>%%
>*%%PREFIX%%healthy) states for reference.%%HIGHLIGHT%% == Supportive  measurement  of  speed,  torque,  radial  load, and temperature.  Four different operating conditions (Table 6).  20  measurements  of  4  seconds  each  for  each  setting, saved  as  a  matlab  file  with  a  name  consisting  of  the code of the operating condition and the four-digit bearing code (e.g. N15_M07_F10_KA01_1.mat).== %%POSTFIX%% Systematic description of the*
>%%LINK%%[[#^089337zrxs5|show annotation]]
>%%COMMENT%%
>Ele precisa carregar em que condição de operação aquilo foi observado. Uma oscilação, uma assinatura de falha ou uma degradação podem ter significado diferente conforme carga, modo produtivo, regime e perturbação.
>
>Um diagnóstico de bomba poderia ser válido apenas em uma faixa operacional:
>
>```yaml
>diagnosis:
>  component: cooling-water-pump
>  condition: degraded
>  validWhen:
>    flowRange: "40-60%"
>    reactorMode: "Mode 1"
>    loadCondition: nominal
>```
>
>Se a TEP mudar para um modo de maior produção, o supervisor não deveria reutilizar cegamente o diagnóstico antigo. Ele deveria marcar a condição como “válida parcialmente” ou exigir nova janela de observação.
>%%TAGS%%
>
^089337zrxs5


>%%
>```annotation-json
>{"created":"2026-06-19T22:35:01.136Z","text":"O artigo propõe um mecanismo: adquirir dados, extrair características, treinar classificador e produzir uma classe prevista. Mas ele também mostra limites: sinais de vibração classificam melhor que corrente; treinar com dano artificial e testar em dano real tem desempenho baixo; danos múltiplos reduzem a acurácia.\n\nA minha IC reforçou essa parte ao explorar transformada wavelet, descritores estatísticos e modelos como SVM, KNN e Decision Tree. Eu tive um desempenho melhor com wavelet.","updated":"2026-06-19T22:35:01.136Z","document":{"title":"art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","link":[{"href":"urn:x-pdf:4d2c236104636847af315274e7c30a53"},{"href":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf"}],"documentFingerprint":"4d2c236104636847af315274e7c30a53"},"uri":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","target":[{"source":"vault:/articles/art13_Condition-Monitoring-of-Bearing-Damage-in-Electromechanical-Drive_Lessmeier_et_al.pdf","selector":[{"type":"TextPositionSelector","start":46916,"end":46984},{"type":"TextQuoteSelector","exact":"Figure 10. Application of machine learning (ML) for fault diagnosis.","prefix":"Selected FeaturesPredictedClass ","suffix":"   Figure 8. Frequency spectrum "}]}]}
>```
>%%
>*%%PREFIX%%Selected FeaturesPredictedClass%%HIGHLIGHT%% ==Figure 10. Application of machine learning (ML) for fault diagnosis.== %%POSTFIX%%Figure 8. Frequency spectrum*
>%%LINK%%[[#^djns2t116ef|show annotation]]
>%%COMMENT%%
>O artigo propõe um mecanismo: adquirir dados, extrair características, treinar classificador e produzir uma classe prevista. Mas ele também mostra limites: sinais de vibração classificam melhor que corrente; treinar com dano artificial e testar em dano real tem desempenho baixo; danos múltiplos reduzem a acurácia.
>
>A minha IC reforçou essa parte ao explorar transformada wavelet, descritores estatísticos e modelos como SVM, KNN e Decision Tree. Eu tive um desempenho melhor com wavelet.
>%%TAGS%%
>
^djns2t116ef
