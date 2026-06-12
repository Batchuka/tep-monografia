---
type: ft
annotation-target: articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf
titulo: Model Learning Algorithms for Anomaly Detection in CERN Control Systems
autor: Tilaro, F.; Bradu, B.; Berges, A.; Varela, C.; Roshchin, M.
ano:
fonte:
tema:
conecta-com: []
tags:
  - REQUISITO-SUPERVISAO-POSITIVO
  - MECANISMO-MODELAGEM-POSITIVO
  - MECANISMO-SUPERVISAO-POSITIVO
  - MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
  - LIMITE-MODELAGEM-POSITIVO
  - MECANISMO-SOFTWARE-POSITIVO
  - REQUISITO-SUPERVISAO-NEUTRO
lido-em:
status: pendente
---

## O que diz


## O que me interessa


## Conexões

- [[]]

## Citação ABNT

```bibtex
@article{ART8,
  author  = {},
  title   = {},
  journal = {},
  year    = {},
}
```


>%%
>```annotation-json
>{"created":"2026-06-09T19:38:06.591Z","text":"Aqui o artigo justifica tecnicamente por que monitoramento manual é inviável. A anomalia não é tratada como um problema isolado de algoritmo, mas como consequência de escala operacional: muitos sistemas, muitos sinais e muita heterogeneidade.","updated":"2026-06-09T19:38:06.591Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":259,"end":499},{"type":"TextQuoteSelector","exact":"onsists of over 600 heterogeneous industrial control systems with around 45 million deployed sensors, actuators and control objects. Therefore, it is evident that the monitoring of such huge system represents a challenging and complex task.","prefix":"CERN automation infrastructure c","suffix":" This paper describes three diff"}]}]}
>```
>%%
>*%%PREFIX%%CERN automation infrastructure c%%HIGHLIGHT%% ==onsists of over 600 heterogeneous industrial control systems with around 45 million deployed sensors, actuators and control objects. Therefore, it is evident that the monitoring of such huge system represents a challenging and complex task.== %%POSTFIX%%This paper describes three diff*
>%%LINK%%[[#^zjvod2cr8e9|show annotation]]
>%%COMMENT%%
>Aqui o artigo justifica tecnicamente por que monitoramento manual é inviável. A anomalia não é tratada como um problema isolado de algoritmo, mas como consequência de escala operacional: muitos sistemas, muitos sinais e muita heterogeneidade.
>%%TAGS%%
>#REQUISITO-SUPERVISAO-POSITIVO
^zjvod2cr8e9


>%%
>```annotation-json
>{"created":"2026-06-09T20:34:46.108Z","text":"Este é o núcleo da ideia de “falta de padrão”: uma anomalia não precisa ser uma falha explícita, basta uma divergência consistente em relação ao comportamento histórico esperado. No meu projeto, isso pode virar uma condição observada pelo supervisor.","updated":"2026-06-09T20:34:46.108Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":885,"end":1429},{"type":"TextQuoteSelector","exact":"The presented methods can be categorized as dynamic unsupervised anomaly detection; “dynamic” since the be-haviour of the system and the evolution of its attributes are observed and changing in time. They are “unsupervised” because we are trying to predict faulty events without ex-amples in the data history. So, the described strategies in-volve monitoring the evolution of sensors values over time in the historical data. Indeed, consistent deviations from the historical evolutions can be seen as warning signs of a possible future anomaly;","prefix":"t faulty sensors measurements.  ","suffix":" these warning signs have been u"}]}]}
>```
>%%
>*%%PREFIX%%t faulty sensors measurements.%%HIGHLIGHT%% ==The presented methods can be categorized as dynamic unsupervised anomaly detection; “dynamic” since the be-haviour of the system and the evolution of its attributes are observed and changing in time. They are “unsupervised” because we are trying to predict faulty events without ex-amples in the data history. So, the described strategies in-volve monitoring the evolution of sensors values over time in the historical data. Indeed, consistent deviations from the historical evolutions can be seen as warning signs of a possible future anomaly;== %%POSTFIX%%these warning signs have been u*
>%%LINK%%[[#^nhoofw5a48|show annotation]]
>%%COMMENT%%
>Este é o núcleo da ideia de “falta de padrão”: uma anomalia não precisa ser uma falha explícita, basta uma divergência consistente em relação ao comportamento histórico esperado. No meu projeto, isso pode virar uma condição observada pelo supervisor.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^nhoofw5a48


>%%
>```annotation-json
>{"created":"2026-06-09T20:38:50.450Z","text":"O artigo transforma incoerência de sinal em alarme. No meu caso, esse alarme pode ser modelado como evento/estado observado em uma arquitetura tipo Kubernetes, por exemplo uma condição Anomalous=True associada a uma malha ou grupo de sinais.","updated":"2026-06-09T20:38:50.450Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":1465,"end":1597},{"type":"TextQuoteSelector","exact":"to trigger a generic anomaly alarm for the specific in-coherent sensors, requiring further checks by system ex-perts and operators. ","prefix":"se warning signs have been used ","suffix":"The paper also presents some res"}]}]}
>```
>%%
>*%%PREFIX%%se warning signs have been used%%HIGHLIGHT%% ==to trigger a generic anomaly alarm for the specific in-coherent sensors, requiring further checks by system ex-perts and operators.== %%POSTFIX%%The paper also presents some res*
>%%LINK%%[[#^087w9wtm8vif|show annotation]]
>%%COMMENT%%
>O artigo transforma incoerência de sinal em alarme. No meu caso, esse alarme pode ser modelado como evento/estado observado em uma arquitetura tipo Kubernetes, por exemplo uma condição Anomalous=True associada a uma malha ou grupo de sinais.
>%%TAGS%%
>#MECANISMO-SUPERVISAO-POSITIVO
^087w9wtm8vif


>%%
>```annotation-json
>{"created":"2026-06-09T20:39:34.761Z","text":"Esse trecho justifica usar telemetria industrial como base para supervisão. O dado de controle não serve apenas para plotar gráfico; ele carrega informação sobre estado, estabilidade e desempenho do processo.","updated":"2026-06-09T20:39:34.761Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":2691,"end":2884},{"type":"TextQuoteSelector","exact":"The generated controls data, after a proper analysis, con-stitutes a source of useful information about the current state of the processes, their performance, stability and over-all behaviour. ","prefix":"rder to reduce the data flow.   ","suffix":"Obviously, an extensive analysis"}]}]}
>```
>%%
>*%%PREFIX%%rder to reduce the data flow.%%HIGHLIGHT%% ==The generated controls data, after a proper analysis, con-stitutes a source of useful information about the current state of the processes, their performance, stability and over-all behaviour.== %%POSTFIX%%Obviously, an extensive analysis*
>%%LINK%%[[#^221f4p6tc1o|show annotation]]
>%%COMMENT%%
>Esse trecho justifica usar telemetria industrial como base para supervisão. O dado de controle não serve apenas para plotar gráfico; ele carrega informação sobre estado, estabilidade e desempenho do processo.
>%%TAGS%%
>#REQUISITO-SUPERVISAO-POSITIVO
^221f4p6tc1o


>%%
>```annotation-json
>{"created":"2026-06-09T20:40:21.602Z","text":"Esse trecho é perfeito para defender detecção de mudança de regime. A pergunta supervisória passa a ser: o comportamento atual ainda pertence ao padrão histórico esperado ou entrou em outro regime dinâmico?","updated":"2026-06-09T20:40:21.602Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":4182,"end":4436},{"type":"TextQuoteSelector","exact":" In the systems analysed, the change point or anomaly detection from data streams was an unsupervised learning task, which aimed at deciding  whether  the  new  generated  sensors’  measure-ments showed a different trend from the historical refer-ence.  ","prefix":" multivariate time series data. ","suffix":"  In this paper, we address the "}]}]}
>```
>%%
>*%%PREFIX%%multivariate time series data.%%HIGHLIGHT%% ==In the systems analysed, the change point or anomaly detection from data streams was an unsupervised learning task, which aimed at deciding  whether  the  new  generated  sensors’  measure-ments showed a different trend from the historical refer-ence.== %%POSTFIX%%In this paper, we address the*
>%%LINK%%[[#^r3osxqt60ib|show annotation]]
>%%COMMENT%%
>Esse trecho é perfeito para defender detecção de mudança de regime. A pergunta supervisória passa a ser: o comportamento atual ainda pertence ao padrão histórico esperado ou entrou em outro regime dinâmico?
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^r3osxqt60ib


>%%
>```annotation-json
>{"created":"2026-06-09T20:40:59.166Z","text":"Aqui aparece a ponte com Kubernetes: não é análise offline eventual; é uma tarefa contínua de monitoramento. Isso se aproxima conceitualmente de um controller loop observando continuamente o estado real do sistema.","updated":"2026-06-09T20:40:59.166Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":4563,"end":4782},{"type":"TextQuoteSelector","exact":"this paper describes three different algorithms for online detection of faulty measurements that have been de-veloped and integrated into the CERN control system as a continuous monitoring task of the machine operation.","prefix":"ime-series data. Spe-cifically, ","suffix":" Once these analyses have been d"}]}]}
>```
>%%
>*%%PREFIX%%ime-series data. Spe-cifically,%%HIGHLIGHT%% ==this paper describes three different algorithms for online detection of faulty measurements that have been de-veloped and integrated into the CERN control system as a continuous monitoring task of the machine operation.== %%POSTFIX%%Once these analyses have been d*
>%%LINK%%[[#^3qbf5x491m8|show annotation]]
>%%COMMENT%%
>Aqui aparece a ponte com Kubernetes: não é análise offline eventual; é uma tarefa contínua de monitoramento. Isso se aproxima conceitualmente de um controller loop observando continuamente o estado real do sistema.
>%%TAGS%%
>#MECANISMO-SUPERVISAO-POSITIVO
^3qbf5x491m8


>%%
>```annotation-json
>{"created":"2026-06-09T20:42:15.194Z","text":"Esse é um trecho fundamental. A anomalia é detectada por quebra de relações esperadas: relações físicas entre sensores próximos e relações lógicas entre entradas e saídas de malhas de controle. Isso é mais forte que limite fixo de alarme.","updated":"2026-06-09T20:42:15.194Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":7699,"end":8025},{"type":"TextQuoteSelector","exact":"in 2 main categories: •  Physical  relationships:  two  or  more  sensors  de-ployed in the same sector or even in the same cell should not differ much in value (like to temperature sensors in contiguous cells). •  Logical  relationship:  the  control  loops  regulate some output signals as a function of some input sig-nals.","prefix":"ela-tionships can be classified ","suffix":"  Both classes of these relation"}]}]}
>```
>%%
>*%%PREFIX%%ela-tionships can be classified%%HIGHLIGHT%% ==in 2 main categories: •  Physical  relationships:  two  or  more  sensors  de-ployed in the same sector or even in the same cell should not differ much in value (like to temperature sensors in contiguous cells). •  Logical  relationship:  the  control  loops  regulate some output signals as a function of some input sig-nals.== %%POSTFIX%%Both classes of these relation*
>%%LINK%%[[#^c0di8cqp1l|show annotation]]
>%%COMMENT%%
>Esse é um trecho fundamental. A anomalia é detectada por quebra de relações esperadas: relações físicas entre sensores próximos e relações lógicas entre entradas e saídas de malhas de controle. Isso é mais forte que limite fixo de alarme.
>%%TAGS%%
>#MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^c0di8cqp1l


>%%
>```annotation-json
>{"created":"2026-06-09T20:43:44.617Z","text":"Aqui está o argumento de modelo aprendido: primeiro se constrói uma referência do comportamento normal; depois se detecta ponto de mudança. Para meu projeto, isso sustenta um supervisor que compara estado observado contra um padrão esperado.","updated":"2026-06-09T20:43:44.617Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":8092,"end":8246},{"type":"TextQuoteSelector","exact":"the controls data in order to make a model of the system. The latter can be then used to detect change points that are distance from the reference state. ","prefix":"ps need to be discovered within ","suffix":"It is worth noting that the cryo"}]}]}
>```
>%%
>*%%PREFIX%%ps need to be discovered within%%HIGHLIGHT%% ==the controls data in order to make a model of the system. The latter can be then used to detect change points that are distance from the reference state.== %%POSTFIX%%It is worth noting that the cryo*
>%%LINK%%[[#^gf39nxg83vw|show annotation]]
>%%COMMENT%%
>Aqui está o argumento de modelo aprendido: primeiro se constrói uma referência do comportamento normal; depois se detecta ponto de mudança. Para meu projeto, isso sustenta um supervisor que compara estado observado contra um padrão esperado.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^gf39nxg83vw


>%%
>```annotation-json
>{"created":"2026-06-09T20:45:04.757Z","text":"Esse trecho é importante porque evita uma premissa fraca: o padrão normal não é fixo. Em sistemas dinâmicos industriais, o modelo de normalidade precisa acompanhar o modo operacional.","updated":"2026-06-09T20:45:04.757Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":8640,"end":8768},{"type":"TextQuoteSelector","exact":"On the contrary, the machine learn-ing process must continuously keep the model in line with the dynamic of the control system. ","prefix":"chine runs (or time intervals). ","suffix":"As it will be described in the f"}]}]}
>```
>%%
>*%%PREFIX%%chine runs (or time intervals).%%HIGHLIGHT%% ==On the contrary, the machine learn-ing process must continuously keep the model in line with the dynamic of the control system.== %%POSTFIX%%As it will be described in the f*
>%%LINK%%[[#^yiezzqgy9xc|show annotation]]
>%%COMMENT%%
>Esse trecho é importante porque evita uma premissa fraca: o padrão normal não é fixo. Em sistemas dinâmicos industriais, o modelo de normalidade precisa acompanhar o modo operacional.
>%%TAGS%%
>#LIMITE-MODELAGEM-POSITIVO
^yiezzqgy9xc


>%%
>```annotation-json
>{"created":"2026-06-09T20:46:00.716Z","text":"Esse trecho sustenta a arquitetura: histórico → extração de padrão → comparação com stream online → detecção. Em termos de Kubernetes, isso pode virar um reconciler que observa continuamente medições e atualiza o estado da malha.","updated":"2026-06-09T20:46:00.716Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":9255,"end":9359},{"type":"TextQuoteSelector","exact":"these patterns are then compared against the input stream of measurements for online anomaly detection. ","prefix":"terns from the historical data; ","suffix":"Anomaly Detection by Sensors Cor"}]}]}
>```
>%%
>*%%PREFIX%%terns from the historical data;%%HIGHLIGHT%% ==these patterns are then compared against the input stream of measurements for online anomaly detection.== %%POSTFIX%%Anomaly Detection by Sensors Cor*
>%%LINK%%[[#^1j7rfkmrlxv|show annotation]]
>%%COMMENT%%
>Esse trecho sustenta a arquitetura: histórico → extração de padrão → comparação com stream online → detecção. Em termos de Kubernetes, isso pode virar um reconciler que observa continuamente medições e atualiza o estado da malha.
>%%TAGS%%
>#MECANISMO-SOFTWARE-POSITIVO
^1j7rfkmrlxv


>%%
>```annotation-json
>{"created":"2026-06-09T20:46:43.238Z","text":"Esse é o melhor trecho visual para “falta de padrão”. O problema não é o valor absoluto do sinal, mas sua perda de coordenação com sinais que historicamente se moviam juntos.","updated":"2026-06-09T20:46:43.238Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":24924,"end":25060},{"type":"TextQuoteSelector","exact":"The anomaly was detected because one of the signals (the one in black) starts moving in an uncoordinated way with re-spect to the others","prefix":" to their historical behaviour. ","suffix":".   Figure 2: Flipping fault det"}]}]}
>```
>%%
>*%%PREFIX%%to their historical behaviour.%%HIGHLIGHT%% ==The anomaly was detected because one of the signals (the one in black) starts moving in an uncoordinated way with re-spect to the others== %%POSTFIX%%.   Figure 2: Flipping fault det*
>%%LINK%%[[#^9a3ew06y8bm|show annotation]]
>%%COMMENT%%
>Esse é o melhor trecho visual para “falta de padrão”. O problema não é o valor absoluto do sinal, mas sua perda de coordenação com sinais que historicamente se moviam juntos.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^9a3ew06y8bm


>%%
>```annotation-json
>{"created":"2026-06-09T20:47:22.597Z","text":"Esse trecho é muito útil para seu TCC: mudança manual, override ou alteração operacional pode aparecer como anomalia no processo de controle. Isso abre espaço para tratar mudança de estratégia como evento supervisório observável.","updated":"2026-06-09T20:47:22.597Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":25449,"end":25559},{"type":"TextQuoteSelector","exact":"Even in this case, the necessary human manual  action  can  be  interpreted  as  a  control  process anomaly. ","prefix":"ng the pro-cess control output. ","suffix":"   Figure 3: Step fault detectio"}]}]}
>```
>%%
>*%%PREFIX%%ng the pro-cess control output.%%HIGHLIGHT%% ==Even in this case, the necessary human manual  action  can  be  interpreted  as  a  control  process anomaly.== %%POSTFIX%%Figure 3: Step fault detectio*
>%%LINK%%[[#^2g553s99yn2|show annotation]]
>%%COMMENT%%
>Esse trecho é muito útil para seu TCC: mudança manual, override ou alteração operacional pode aparecer como anomalia no processo de controle. Isso abre espaço para tratar mudança de estratégia como evento supervisório observável.
>%%TAGS%%
>#MECANISMO-SUPERVISAO-POSITIVO
^2g553s99yn2


>%%
>```annotation-json
>{"created":"2026-06-09T20:48:00.882Z","text":"Aqui o artigo conecta anomalia com instabilidade/oscilações de controle. Para seu projeto, isso pode justificar uma condição supervisória do tipo: se uma malha entra em oscilação persistente, o supervisor pode recomendar ou aplicar outra configuração de controle.","updated":"2026-06-09T20:48:00.882Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":25701,"end":25838},{"type":"TextQuoteSelector","exact":"Figure  4  clearly  depicts  this  situation where the valve shows an unstable oscillatory behaviour to control the temperature process. ","prefix":"ilities have been  discovered.  ","suffix":"Obviously if this faulty os-cill"}]}]}
>```
>%%
>*%%PREFIX%%ilities have been  discovered.%%HIGHLIGHT%% ==Figure  4  clearly  depicts  this  situation where the valve shows an unstable oscillatory behaviour to control the temperature process.== %%POSTFIX%%Obviously if this faulty os-cill*
>%%LINK%%[[#^z8wgqi5t2sh|show annotation]]
>%%COMMENT%%
>Aqui o artigo conecta anomalia com instabilidade/oscilações de controle. Para seu projeto, isso pode justificar uma condição supervisória do tipo: se uma malha entra em oscilação persistente, o supervisor pode recomendar ou aplicar outra configuração de controle.
>%%TAGS%%
>#MECANISMO-SUPERVISAO-POSITIVO
^z8wgqi5t2sh


>%%
>```annotation-json
>{"created":"2026-06-09T20:48:38.263Z","text":"Esse trecho impõe um limite importante. O artigo não resolve diagnóstico causal nem decisão automática. Ele detecta anomalia; a decisão sobre trocar estratégia ou parâmetro precisa ser uma camada adicional do seu projeto.","updated":"2026-06-09T20:48:38.263Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":26935,"end":27138},{"type":"TextQuoteSelector","exact":". The algorithms detect the operational anom-aly but they are not able to identify the root cause; a direct intervention from the system expert is necessary to fully understand the nature of the problem.","prefix":"a wrong mechanical valve setting","suffix":"   Figure 5: Faulty signal ampli"}]}]}
>```
>%%
>*%%PREFIX%%a wrong mechanical valve setting%%HIGHLIGHT%% ==. The algorithms detect the operational anom-aly but they are not able to identify the root cause; a direct intervention from the system expert is necessary to fully understand the nature of the problem.== %%POSTFIX%%Figure 5: Faulty signal ampli*
>%%LINK%%[[#^9kxq5hz85uh|show annotation]]
>%%COMMENT%%
>Esse trecho impõe um limite importante. O artigo não resolve diagnóstico causal nem decisão automática. Ele detecta anomalia; a decisão sobre trocar estratégia ou parâmetro precisa ser uma camada adicional do seu projeto.
>%%TAGS%%
>#LIMITE-MODELAGEM-POSITIVO
^9kxq5hz85uh


>%%
>```annotation-json
>{"created":"2026-06-09T20:49:12.159Z","text":"Esse trecho sustenta integração com camada supervisória. No CERN, o resultado analítico volta para o SCADA; no seu projeto, pode voltar como estado observado em uma API/CRD inspirada em Kubernetes.","updated":"2026-06-09T20:49:12.159Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":28045,"end":28247},{"type":"TextQuoteSelector","exact":"Furthermore a specialized reporting tool has been designed and implemented in order to show the analytical results directly into the SCADA (Supervisory Control and Data Acquisition) applications at CERN","prefix":"ers and oper-ators can consult. ","suffix":" [17]. The detection of these an"}]}]}
>```
>%%
>*%%PREFIX%%ers and oper-ators can consult.%%HIGHLIGHT%% ==Furthermore a specialized reporting tool has been designed and implemented in order to show the analytical results directly into the SCADA (Supervisory Control and Data Acquisition) applications at CERN== %%POSTFIX%%[17]. The detection of these an*
>%%LINK%%[[#^7oxfmbq6vgj|show annotation]]
>%%COMMENT%%
>Esse trecho sustenta integração com camada supervisória. No CERN, o resultado analítico volta para o SCADA; no seu projeto, pode voltar como estado observado em uma API/CRD inspirada em Kubernetes.
>%%TAGS%%
>#MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^7oxfmbq6vgj


>%%
>```annotation-json
>{"created":"2026-06-09T20:49:28.389Z","text":"Esse é o trecho mais próximo da sua ideia de mudar parâmetros. Mas cuidado: no artigo, quem melhora a sintonia são os engenheiros, não um algoritmo automático. Você pode usar isso como justificativa para evoluir de detecção para recomendação ou reconciliação de parâmetros","updated":"2026-06-09T20:49:28.389Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":28287,"end":28407},{"type":"TextQuoteSelector","exact":"has allowed engineers to improve the tuning of thousands of regulation loops and reduce undesirable mechanical movements","prefix":"he detection of these anomalies ","suffix":" (e.g. wearing of valves due to "}]}]}
>```
>%%
>*%%PREFIX%%he detection of these anomalies%%HIGHLIGHT%% ==has allowed engineers to improve the tuning of thousands of regulation loops and reduce undesirable mechanical movements== %%POSTFIX%%(e.g. wearing of valves due to*
>%%LINK%%[[#^5e6chgipwpn|show annotation]]
>%%COMMENT%%
>Esse é o trecho mais próximo da sua ideia de mudar parâmetros. Mas cuidado: no artigo, quem melhora a sintonia são os engenheiros, não um algoritmo automático. Você pode usar isso como justificativa para evoluir de detecção para recomendação ou reconciliação de parâmetros
>%%TAGS%%
>#MECANISMO-SUPERVISAO-POSITIVO
^5e6chgipwpn


>%%
>```annotation-json
>{"created":"2026-06-09T20:51:55.872Z","text":"O artigo transforma correlação entre sensores em uma geometria: sensores historicamente correlacionados ficam “próximos” em um grafo. A distância usada é d_ij=−ln * a_ij, onde a_ij é a correlação de Pearson. Se dois sinais eram fortemente correlacionados e passam a divergir, a distância efetiva entre eles aumenta. Assim, a anomalia é identificada como uma quebra da vizinhança esperada entre sinais. Isso é útil para uma arquitetura supervisória porque a “falta de padrão” pode ser formalizada como perda de coerência entre sinais relacionados, não apenas como violação de setpoint.","updated":"2026-06-09T20:51:55.872Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":10949,"end":11186},{"type":"TextQuoteSelector","exact":"The proposed method adopts a similar approach by defining a K-Nearest-Neigh-bour graph [10] based on the computed correlation coeffi-cients; precisely the distance between signals, represented by the graph edges, is calculated as follows","prefix":"rity between a pair of signals. ","suffix":":  16th Int. Conf. on Accelerato"}]}]}
>```
>%%
>*%%PREFIX%%rity between a pair of signals.%%HIGHLIGHT%% ==The proposed method adopts a similar approach by defining a K-Nearest-Neigh-bour graph [10] based on the computed correlation coeffi-cients; precisely the distance between signals, represented by the graph edges, is calculated as follows== %%POSTFIX%%:  16th Int. Conf. on Accelerato*
>%%LINK%%[[#^ma4hff8wq6q|show annotation]]
>%%COMMENT%%
>O artigo transforma correlação entre sensores em uma geometria: sensores historicamente correlacionados ficam “próximos” em um grafo. A distância usada é d_ij=−ln * a_ij, onde a_ij é a correlação de Pearson. Se dois sinais eram fortemente correlacionados e passam a divergir, a distância efetiva entre eles aumenta. Assim, a anomalia é identificada como uma quebra da vizinhança esperada entre sinais. Isso é útil para uma arquitetura supervisória porque a “falta de padrão” pode ser formalizada como perda de coerência entre sinais relacionados, não apenas como violação de setpoint.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^ma4hff8wq6q


>%%
>```annotation-json
>{"created":"2026-06-09T20:53:45.400Z","text":"O artigo transforma correlação entre sensores em uma geometria: sensores historicamente correlacionados ficam “próximos” em um grafo. A distância usada é d_ij=−ln * a_ij, onde a_ij é a correlação de Pearson. Se dois sinais eram fortemente correlacionados e passam a divergir, a distância efetiva entre eles aumenta. Assim, a anomalia é identificada como uma quebra da vizinhança esperada entre sinais. Isso é útil para uma arquitetura supervisória porque a “falta de padrão” pode ser formalizada como perda de coerência entre sinais relacionados, não apenas como violação de setpoint.","updated":"2026-06-09T20:53:45.400Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":11605,"end":11737},{"type":"TextQuoteSelector","exact":"Therefore, the distance between highly correlated sig-nals will be close to zero and for uncorrelated signals will tend to infinity.","prefix":"OI.Data Analytics݀௜௝ =−lnหܽ௜௝ห  ","suffix":" ‘K’ represents the dimension of"}]}]}
>```
>%%
>*%%PREFIX%%OI.Data Analytics݀௜௝ =−lnหܽ௜௝ห%%HIGHLIGHT%% ==Therefore, the distance between highly correlated sig-nals will be close to zero and for uncorrelated signals will tend to infinity.== %%POSTFIX%%‘K’ represents the dimension of*
>%%LINK%%[[#^7fvhg1ifx1k|show annotation]]
>%%COMMENT%%
>O artigo transforma correlação entre sensores em uma geometria: sensores historicamente correlacionados ficam “próximos” em um grafo. A distância usada é d_ij=−ln * a_ij, onde a_ij é a correlação de Pearson. Se dois sinais eram fortemente correlacionados e passam a divergir, a distância efetiva entre eles aumenta. Assim, a anomalia é identificada como uma quebra da vizinhança esperada entre sinais. Isso é útil para uma arquitetura supervisória porque a “falta de padrão” pode ser formalizada como perda de coerência entre sinais relacionados, não apenas como violação de setpoint.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^7fvhg1ifx1k


>%%
>```annotation-json
>{"created":"2026-06-09T20:54:52.758Z","updated":"2026-06-09T20:54:52.758Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":12484,"end":12619},{"type":"TextQuoteSelector","exact":"In order to evaluate each significant change in the signals (change point analysis), the following dissimilarity func-tion was defined:","prefix":"y correlated pairs of signals.  ","suffix":" ܧ(݀௜)=∑ ݌௜௝∗݀(݆|݅)௞௝ୀଵ ,  where"}]}]}
>```
>%%
>*%%PREFIX%%y correlated pairs of signals.%%HIGHLIGHT%% ==In order to evaluate each significant change in the signals (change point analysis), the following dissimilarity func-tion was defined:== %%POSTFIX%%ܧ(݀௜)=∑ ݌௜௝∗݀(݆|݅)௞௝ୀଵ ,  where*
>%%LINK%%[[#^fogf2ookdr9|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^fogf2ookdr9


>%%
>```annotation-json
>{"created":"2026-06-09T20:54:57.505Z","text":"A identificação da anomalia ocorre por uma métrica de dissimilaridade esperada. O artigo calcula algo como E(d_i) = Soma p(j|i)d_ij, isto é, uma distância média ponderada entre um sinal e seus vizinhos esperados. Se essa dissimilaridade passa de um limiar, o sinal é considerado anômalo. O ponto importante é que o sistema não pergunta apenas “qual é o valor do sensor?”, mas “esse sensor ainda se comporta como seus vizinhos históricos?”. Para meu projeto, isso pode alimentar um estado observado da malha, como","updated":"2026-06-09T20:54:57.505Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":13877,"end":14203},{"type":"TextQuoteSelector","exact":"The faulty sensor detection was achieved by detecting any change exceeding a predefined threshold in the dissim-ilarity function for each KNNi graph. Due to the high dy-namic of the system, the learning process continuously up-dates the KNN-based model, which is used as a reference during the online fault detection analysis.","prefix":"d as: =)݅|݆(݌ ݁ିௗ೔ೕ1+∑ ݁ିௗ೔ೕ௝   ","suffix":" Anomaly Detection by Stochastic"}]}]}
>```
>%%
>*%%PREFIX%%d as: =)݅|݆(݌ ݁ିௗ೔ೕ1+∑ ݁ିௗ೔ೕ௝%%HIGHLIGHT%% ==The faulty sensor detection was achieved by detecting any change exceeding a predefined threshold in the dissim-ilarity function for each KNNi graph. Due to the high dy-namic of the system, the learning process continuously up-dates the KNN-based model, which is used as a reference during the online fault detection analysis.== %%POSTFIX%%Anomaly Detection by Stochastic*
>%%LINK%%[[#^omzs8yb521b|show annotation]]
>%%COMMENT%%
>A identificação da anomalia ocorre por uma métrica de dissimilaridade esperada. O artigo calcula algo como E(d_i) = Soma p(j|i)d_ij, isto é, uma distância média ponderada entre um sinal e seus vizinhos esperados. Se essa dissimilaridade passa de um limiar, o sinal é considerado anômalo. O ponto importante é que o sistema não pergunta apenas “qual é o valor do sensor?”, mas “esse sensor ainda se comporta como seus vizinhos históricos?”. Para meu projeto, isso pode alimentar um estado observado da malha, como
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^omzs8yb521b


>%%
>```annotation-json
>{"created":"2026-06-09T20:56:29.272Z","updated":"2026-06-09T20:56:29.272Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":14405,"end":14614},{"type":"TextQuoteSelector","exact":" The clustering is based on K-Means [11] method by splitting the historical data sets into time windows; by limiting the size of the signals analysed the computational load and the execution time are reduced. ","prefix":" their histori-cal measurements.","suffix":" Due to the presence of differen"}]}]}
>```
>%%
>*%%PREFIX%%their histori-cal measurements.%%HIGHLIGHT%% ==The clustering is based on K-Means [11] method by splitting the historical data sets into time windows; by limiting the size of the signals analysed the computational load and the execution time are reduced.== %%POSTFIX%%Due to the presence of differen*
>%%LINK%%[[#^6kas2jy2h8a|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^6kas2jy2h8a


>%%
>```annotation-json
>{"created":"2026-06-09T20:56:52.911Z","text":"O segundo método identifica padrões por agrupamento estatístico. Primeiro, os sinais são padronizados em cada janela temporal, removendo diferença de escala e calibração. Depois, o K-Means agrupa sinais com comportamento semelhante. A recorrência desses clusters ao longo das janelas vira um modelo probabilístico. Se a frequência esperada de um cluster muda além de um limiar, o artigo gera alarme. Em termos de controle supervisório, isso permite detectar mudança de regime: a planta não apenas mudou de valor, ela mudou a estrutura estatística do comportamento observado.","updated":"2026-06-09T20:56:52.911Z","document":{"title":"Model Learning Algorithms for Anomaly Detection in CERN Control SystemsModel Learning Algorithms for Anomaly Detection in CERN Control Systems","link":[{"href":"urn:x-pdf:82924ab786d8a7dc9e12e085f805a8bd"},{"href":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf"}],"documentFingerprint":"82924ab786d8a7dc9e12e085f805a8bd"},"uri":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","target":[{"source":"vault:/notes/articles/art8_Model-Learning-Algorithms-for-Anomaly-Detection-in-CERN-Control-Systems_Tilaro_Bradu_Berges_Varela_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":17760,"end":17896},{"type":"TextQuoteSelector","exact":"If the expected value of the binomial distribution of any cluster is changing more than a defined threshold then an alarm is generated. ","prefix":"݇௝ =ܺ൫ܲ݊݇ቁ∗ܲ൫݃௝൯௞∗(1−ܲ൫݃௝൯)௡ି௞  ","suffix":"Anomaly Detection Based on Exper"}]}]}
>```
>%%
>*%%PREFIX%%݇௝ =ܺ൫ܲ݊݇ቁ∗ܲ൫݃௝൯௞∗(1−ܲ൫݃௝൯)௡ି௞%%HIGHLIGHT%% ==If the expected value of the binomial distribution of any cluster is changing more than a defined threshold then an alarm is generated.== %%POSTFIX%%Anomaly Detection Based on Exper*
>%%LINK%%[[#^vq807zavj|show annotation]]
>%%COMMENT%%
>O segundo método identifica padrões por agrupamento estatístico. Primeiro, os sinais são padronizados em cada janela temporal, removendo diferença de escala e calibração. Depois, o K-Means agrupa sinais com comportamento semelhante. A recorrência desses clusters ao longo das janelas vira um modelo probabilístico. Se a frequência esperada de um cluster muda além de um limiar, o artigo gera alarme. Em termos de controle supervisório, isso permite detectar mudança de regime: a planta não apenas mudou de valor, ela mudou a estrutura estatística do comportamento observado.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^vq807zavj
