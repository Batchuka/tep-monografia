---
annotation-target: articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf
titulo: An Expert Knowledge Based Methodology for Online Detection of Signal Oscillations
autor: Tilaro, F.; Bradu, B.; Berges, A.; Roshchin, M.
ano:
fonte:
papel: tecnica_diagnostico
---

>%%
>```annotation-json
>{"created":"2026-06-18T00:02:47.155Z","text":"A análise automática não é apenas 'pós-processamento', quando está integrada à operação, ela passa a compor o próprio sistema de controle. \n\nEntão, nesse artigo já há uma análise continua integrada ao ambiente de produção. Isso é um dos efeitos que quero causar com o k8s. Isso é um controller supervisório. ","updated":"2026-06-18T00:02:47.155Z","document":{"title":"An expert knowledge based methodology for online detection of signal oscillations","link":[{"href":"urn:x-pdf:608346e615b41a43407e015b9ebaa419"},{"href":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf"}],"documentFingerprint":"608346e615b41a43407e015b9ebaa419"},"uri":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","target":[{"source":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":2456,"end":3098},{"type":"TextQuoteSelector","exact":" It  is  obvious  that  an  extensive  analysis  of  this  massive data flow cannot be achieved manually by operators;  on  the  contrary  it  is  necessary  to  develop  and  deploy  specialized  frameworks  which  are  able  to  provide  analytical services and handle the big datasets. The presented algorithm  has  been  developed  in  line  with  this  vision  of  industrial analytical services; the automatic detection of signal oscillation has been, indeed, integrated as a continuous monitoring task into the machine operation. Once the analysis can be applied to solve a control problem, it becomes part of the control system itself","prefix":"stability and overall behavior. ","suffix":" making possible to raise awaren"}]}]}
>```
>%%
>*%%PREFIX%%stability and overall behavior.%%HIGHLIGHT%% ==It  is  obvious  that  an  extensive  analysis  of  this  massive data flow cannot be achieved manually by operators;  on  the  contrary  it  is  necessary  to  develop  and  deploy  specialized  frameworks  which  are  able  to  provide  analytical services and handle the big datasets. The presented algorithm  has  been  developed  in  line  with  this  vision  of  industrial analytical services; the automatic detection of signal oscillation has been, indeed, integrated as a continuous monitoring task into the machine operation. Once the analysis can be applied to solve a control problem, it becomes part of the control system itself== %%POSTFIX%%making possible to raise awaren*
>%%LINK%%[[#^e773z1lxzl6|show annotation]]
>%%COMMENT%%
>A análise automática não é apenas 'pós-processamento', quando está integrada à operação, ela passa a compor o próprio sistema de controle. 
>
>Então, nesse artigo já há uma análise continua integrada ao ambiente de produção. Isso é um dos efeitos que quero causar com o k8s. Isso é um controller supervisório. 
>%%TAGS%%
>
^e773z1lxzl6


>%%
>```annotation-json
>{"created":"2026-06-18T00:17:26.089Z","text":"O artigo está dando luz em uma coisa e a análise online teoricamente consegue captar esse conhecimento tácito. O k8s iria além... além de identificar, ele iria saber se a política de alto nível é aplicável.\n\n## Exemplo — do julgamento humano à supervisão online\n\nNo PLC, a malha de temperatura do reator continua executando o PID normalmente: ela mede `XMEAS(9)` — temperatura do reator — e atua em `XMV(10)` — vazão de água de resfriamento. Essa camada não muda: o controle regulatório continua no PLC.\n\nO problema está acima disso. Em uma operação tradicional, parte da supervisão depende do julgamento do operador ou do especialista da planta. Ele olha a tendência da válvula, reconhece pela experiência que aquele padrão de abertura e fechamento “não está normal” e conclui que a malha pode estar degradada.\n\nO artigo propõe transformar esse julgamento tácito em uma análise online. A série temporal da válvula deixa de depender da interpretação visual do especialista e passa por uma metodologia automática: detecção espectral, comparação com limites definidos a partir do conhecimento operacional, verificação de regularidade e classificação da oscilação.\n\nAssim, o sistema não entrega apenas valores crus como:\n\n`XMV(10) = 42%`\n\nEle entrega uma condição interpretada:\n\n`ReactorCoolingLoop/OscillationDetected = true`\n`amplitude = 8%`\n`period = 33 s`\n`regularity = valid`\n`condition = degraded`\n\nNesse ponto entra a camada inspirada em Kubernetes. Ela não precisa controlar a válvula nem interpretar manualmente o gráfico. Ela consome a condição já produzida pela análise online e verifica se a política operacional ainda é válida.\n\nPor exemplo:\n\n`Alta produção só é permitida se a malha de resfriamento do reator estiver saudável.`\n\nSe o estado observado diz que a malha está degradada, o supervisor conclui que a política de alta produção não é aplicável naquele momento. A reconciliação não é “mexer no PID diretamente”, mas impedir uma transição operacional insegura, manter a planta em modo conservador, gerar alerta ou solicitar uma ação autorizada de diagnóstico e retuning.\n\nO ponto central é que a peculiaridade que antes ficava na experiência do especialista passa a ser capturada como condição observável da planta. O Kubernetes, ou uma camada inspirada nele, usaria essa condição para decidir se uma política de alto nível pode ou não ser aplicada.\n","updated":"2026-06-18T00:17:26.089Z","document":{"title":"An expert knowledge based methodology for online detection of signal oscillations","link":[{"href":"urn:x-pdf:608346e615b41a43407e015b9ebaa419"},{"href":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf"}],"documentFingerprint":"608346e615b41a43407e015b9ebaa419"},"uri":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","target":[{"source":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":3748,"end":4133},{"type":"TextQuoteSelector","exact":"While  the  experts  are  knowledgeable  about  their  domain,  they  are  not  skilled  to  perform these data analysis or computing problems tasks. In this context, formalizing expert knowledge means translating the  correct  operational  conditions,  known  by  the  machine  expert, into simple equations, parameters that can be used as input in the oscillation detection analysis.","prefix":"edge  and  spectrum  analysis.  ","suffix":" Then all the analytical  proces"}]}]}
>```
>%%
>*%%PREFIX%%edge  and  spectrum  analysis.%%HIGHLIGHT%% ==While  the  experts  are  knowledgeable  about  their  domain,  they  are  not  skilled  to  perform these data analysis or computing problems tasks. In this context, formalizing expert knowledge means translating the  correct  operational  conditions,  known  by  the  machine  expert, into simple equations, parameters that can be used as input in the oscillation detection analysis.== %%POSTFIX%%Then all the analytical  proces*
>%%LINK%%[[#^ol8aj9zy3dk|show annotation]]
>%%COMMENT%%
>O artigo está dando luz em uma coisa e a análise online teoricamente consegue captar esse conhecimento tácito. O k8s iria além... além de identificar, ele iria saber se a política de alto nível é aplicável.
>
>## Exemplo — do julgamento humano à supervisão online
>
>No PLC, a malha de temperatura do reator continua executando o PID normalmente: ela mede `XMEAS(9)` — temperatura do reator — e atua em `XMV(10)` — vazão de água de resfriamento. Essa camada não muda: o controle regulatório continua no PLC.
>
>O problema está acima disso. Em uma operação tradicional, parte da supervisão depende do julgamento do operador ou do especialista da planta. Ele olha a tendência da válvula, reconhece pela experiência que aquele padrão de abertura e fechamento “não está normal” e conclui que a malha pode estar degradada.
>
>O artigo propõe transformar esse julgamento tácito em uma análise online. A série temporal da válvula deixa de depender da interpretação visual do especialista e passa por uma metodologia automática: detecção espectral, comparação com limites definidos a partir do conhecimento operacional, verificação de regularidade e classificação da oscilação.
>
>Assim, o sistema não entrega apenas valores crus como:
>
>`XMV(10) = 42%`
>
>Ele entrega uma condição interpretada:
>
>`ReactorCoolingLoop/OscillationDetected = true`
>`amplitude = 8%`
>`period = 33 s`
>`regularity = valid`
>`condition = degraded`
>
>Nesse ponto entra a camada inspirada em Kubernetes. Ela não precisa controlar a válvula nem interpretar manualmente o gráfico. Ela consome a condição já produzida pela análise online e verifica se a política operacional ainda é válida.
>
>Por exemplo:
>
>`Alta produção só é permitida se a malha de resfriamento do reator estiver saudável.`
>
>Se o estado observado diz que a malha está degradada, o supervisor conclui que a política de alta produção não é aplicável naquele momento. A reconciliação não é “mexer no PID diretamente”, mas impedir uma transição operacional insegura, manter a planta em modo conservador, gerar alerta ou solicitar uma ação autorizada de diagnóstico e retuning.
>
>O ponto central é que a peculiaridade que antes ficava na experiência do especialista passa a ser capturada como condição observável da planta. O Kubernetes, ou uma camada inspirada nele, usaria essa condição para decidir se uma política de alto nível pode ou não ser aplicada.
>
>%%TAGS%%
>
^ol8aj9zy3dk


>%%
>```annotation-json
>{"created":"2026-06-18T00:19:48.859Z","updated":"2026-06-18T00:19:48.859Z","document":{"title":"An expert knowledge based methodology for online detection of signal oscillations","link":[{"href":"urn:x-pdf:608346e615b41a43407e015b9ebaa419"},{"href":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf"}],"documentFingerprint":"608346e615b41a43407e015b9ebaa419"},"uri":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","target":[{"source":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":3942,"end":3943},{"type":"TextQuoteSelector","exact":"e","prefix":"ext, formalizing expert knowledg","suffix":" means translating the  correct "}]}]}
>```
>%%
>*%%PREFIX%%ext, formalizing expert knowledg%%HIGHLIGHT%% ==e== %%POSTFIX%%means translating the  correct*
>%%LINK%%[[#^yjvklz88gn|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^yjvklz88gn


>%%
>```annotation-json
>{"created":"2026-06-18T00:42:34.799Z","text":"Do artigo: sensores e atuadores geram séries temporais que carregam informação sobre estabilidade, falhas e desempenho.\n\nUm supervisor k8s não deveria ler só alarmes discretos; ele deveria consumir abstrações derivadas de telemetria, como `oscillation_detected`, `dominant_period`, `amplitude`, `confidence`.","updated":"2026-06-18T00:42:34.799Z","document":{"title":"An expert knowledge based methodology for online detection of signal oscillations","link":[{"href":"urn:x-pdf:608346e615b41a43407e015b9ebaa419"},{"href":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf"}],"documentFingerprint":"608346e615b41a43407e015b9ebaa419"},"uri":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","target":[{"source":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":8820,"end":9023},{"type":"TextQuoteSelector","exact":"The  analysis  cannot  rely  on  control  alarms  or  logs  since  an oscillatory behavior can take place even when the system is operating in nominal state, so without triggering any control  threshold.","prefix":" operations from the experts.   ","suffix":"  For  instance,  in  the  cryog"}]}]}
>```
>%%
>*%%PREFIX%%operations from the experts.%%HIGHLIGHT%% ==The  analysis  cannot  rely  on  control  alarms  or  logs  since  an oscillatory behavior can take place even when the system is operating in nominal state, so without triggering any control  threshold.== %%POSTFIX%%For  instance,  in  the  cryog*
>%%LINK%%[[#^09c3sc53t5qp|show annotation]]
>%%COMMENT%%
>Do artigo: sensores e atuadores geram séries temporais que carregam informação sobre estabilidade, falhas e desempenho.
>
>Um supervisor k8s não deveria ler só alarmes discretos; ele deveria consumir abstrações derivadas de telemetria, como `oscillation_detected`, `dominant_period`, `amplitude`, `confidence`.
>%%TAGS%%
>
^09c3sc53t5qp


>%%
>```annotation-json
>{"created":"2026-06-18T00:45:54.470Z","text":"O algoritmo usa janela deslizante, DFT, detecção de pico espectral, filtro passa-faixa, zero-crossing e checagem de regularidade. O sinal cru deixa de ser apenas uma curva e vira um objeto interpretável: frequência dominante, amplitude, período e regularidade da oscilação.\n\nDo artigo: existe um mecanismo matemático para converter telemetria em diagnóstico de comportamento.\n\nEsse diagnóstico pode virar uma condição observada no supervisor, análoga a PodReady, mas aplicada à malha: LoopStable, OscillationDetected, ValveChattering, PerformanceDegraded.","updated":"2026-06-18T00:45:54.470Z","document":{"title":"An expert knowledge based methodology for online detection of signal oscillations","link":[{"href":"urn:x-pdf:608346e615b41a43407e015b9ebaa419"},{"href":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf"}],"documentFingerprint":"608346e615b41a43407e015b9ebaa419"},"uri":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","target":[{"source":"vault:/articles/art7_An-Expert-Knowledge-Based-Methodology-for-Online-Detection-of-Signal-Oscillations_Tilaro_Bradu_Berges_Roshchin.pdf","selector":[{"type":"TextPositionSelector","start":9849,"end":10692},{"type":"TextQuoteSelector","exact":"The analysis flow is represented in the figure below. The developed algorithm consists of a univariate time series analysis which combines both spectral and time-domain analysis.  In  order  to  reduce  the  computational  load  and  be  able  to  run  the  analysis  in  online  mode  a  sliding  window  mechanism  is  used.  Once  new  signal  samples  arrive,  the  Discrete Fourier Transform (DFT) is calculated, on an incremental step, to detect possible peaks in the spectrum. As many  references  stated  [6],  [7],  [8]  this  represents  a  well-known and validated procedure for oscillation detection. Actually  the  frequency  components  are  compared  against  a  specific  threshold.  The  latter  is  calculated  on  the  base  of  expert  knowledge  according  to  the  procedure  described  in  the following of the document.","prefix":"rbation. B.  The analysis flow  ","suffix":"   Fig. 1. Analysis flow of the "}]}]}
>```
>%%
>*%%PREFIX%%rbation. B.  The analysis flow%%HIGHLIGHT%% ==The analysis flow is represented in the figure below. The developed algorithm consists of a univariate time series analysis which combines both spectral and time-domain analysis.  In  order  to  reduce  the  computational  load  and  be  able  to  run  the  analysis  in  online  mode  a  sliding  window  mechanism  is  used.  Once  new  signal  samples  arrive,  the  Discrete Fourier Transform (DFT) is calculated, on an incremental step, to detect possible peaks in the spectrum. As many  references  stated  [6],  [7],  [8]  this  represents  a  well-known and validated procedure for oscillation detection. Actually  the  frequency  components  are  compared  against  a  specific  threshold.  The  latter  is  calculated  on  the  base  of  expert  knowledge  according  to  the  procedure  described  in  the following of the document.== %%POSTFIX%%Fig. 1. Analysis flow of the*
>%%LINK%%[[#^jd3kmk42ojb|show annotation]]
>%%COMMENT%%
>O algoritmo usa janela deslizante, DFT, detecção de pico espectral, filtro passa-faixa, zero-crossing e checagem de regularidade. O sinal cru deixa de ser apenas uma curva e vira um objeto interpretável: frequência dominante, amplitude, período e regularidade da oscilação.
>
>Do artigo: existe um mecanismo matemático para converter telemetria em diagnóstico de comportamento.
>
>Esse diagnóstico pode virar uma condição observada no supervisor, análoga a PodReady, mas aplicada à malha: LoopStable, OscillationDetected, ValveChattering, PerformanceDegraded.
>%%TAGS%%
>
^jd3kmk42ojb
