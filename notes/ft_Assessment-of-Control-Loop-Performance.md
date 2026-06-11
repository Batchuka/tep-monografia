---
type: ft
annotation-target: notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf
titulo: Assessment of control loop performance
autor: Burns, W.L.
ano: 2016
fonte:
tema:
conecta-com: []
tags:
lido-em:
status: pendente
---

## O que diz


## O que me interessa


## Conexões

- [[]]

## Citação ABNT

```bibtex
@article{BURNS2016,
  author  = {Burns, W. L.},
  title   = {Assessment of control loop performance},
  journal = {},
  year    = {2016},
}
```



>%%
>```annotation-json
>{"created":"2026-06-10T00:39:09.656Z","text":"Aqui Harris estabelece uma ideia fundamental: antes de trocar controlador, retunar PID ou propor uma arquitetura supervisória, é preciso ter uma referência objetiva de desempenho. Sem benchmark, qualquer melhora percebida pode ser apenas impressão visual da resposta temporal.\n\nNo meu TCC, isso justifica que a camada supervisória não deve agir apenas porque “parece ruim”. Ela precisa comparar o desempenho observado da malha com algum limite ou referência formal de desempenho.\n\n","updated":"2026-06-10T00:39:09.656Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":1616,"end":1739},{"type":"TextQuoteSelector","exact":"Regardless ofthè control strategy , it is important to have some benchmarkagainst which its performance can be evaluated. T","prefix":"d linear quadratic controllers. ","suffix":"he theo-retical ‘best achievable"}]}]}
>```
>%%
>*%%PREFIX%%d linear quadratic controllers.%%HIGHLIGHT%% ==Regardless ofthè control strategy , it is important to have some benchmarkagainst which its performance can be evaluated. T== %%POSTFIX%%he theo-retical ‘best achievable*
>%%LINK%%[[#^qf04ncgd319|show annotation]]
>%%COMMENT%%
>Aqui Harris estabelece uma ideia fundamental: antes de trocar controlador, retunar PID ou propor uma arquitetura supervisória, é preciso ter uma referência objetiva de desempenho. Sem benchmark, qualquer melhora percebida pode ser apenas impressão visual da resposta temporal.
>
>No meu TCC, isso justifica que a camada supervisória não deve agir apenas porque “parece ruim”. Ela precisa comparar o desempenho observado da malha com algum limite ou referência formal de desempenho.
>
>
>%%TAGS%%
>
^qf04ncgd319


>%%
>```annotation-json
>{"created":"2026-06-10T00:39:32.612Z","text":"O artigo define desempenho de controle em termos de variância/erro quadrático médio da saída. Isso desloca a avaliação da malha de uma percepção qualitativa para uma métrica estatística: quanto a variável controlada oscila ao redor do setpoint.\n\nPara o Tennessee Eastman, posso avaliar uma malha não apenas por overshoot ou settling time, mas também pela variabilidade residual da variável controlada durante operação contínua.","updated":"2026-06-10T00:39:32.612Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":1782,"end":1839},{"type":"TextQuoteSelector","exact":"as measured by thè meansquare error, is such a benchmark.","prefix":"ical ‘best achievable’ control, ","suffix":" If thè theoretical bestachievab"}]}]}
>```
>%%
>*%%PREFIX%%ical ‘best achievable’ control,%%HIGHLIGHT%% ==as measured by thè meansquare error, is such a benchmark.== %%POSTFIX%%If thè theoretical bestachievab*
>%%LINK%%[[#^a8foveplqev|show annotation]]
>%%COMMENT%%
>O artigo define desempenho de controle em termos de variância/erro quadrático médio da saída. Isso desloca a avaliação da malha de uma percepção qualitativa para uma métrica estatística: quanto a variável controlada oscila ao redor do setpoint.
>
>Para o Tennessee Eastman, posso avaliar uma malha não apenas por overshoot ou settling time, mas também pela variabilidade residual da variável controlada durante operação contínua.
>%%TAGS%%
>
^a8foveplqev


>%%
>```annotation-json
>{"created":"2026-06-10T00:45:22.535Z","text":"Comentário:\nHarris usa o controle de variância mínima como referência teórica de melhor desempenho. O ponto não é necessariamente implementar esse controlador, mas usar seu desempenho como limite inferior para comparar uma malha real.\n\nEu posso tratar o Harris Benchmark como uma régua de comparação para os PIDs simulados: não para substituir o PID imediatamente, mas para medir se ele está muito distante do melhor desempenho possível.\n\nHarris propõe estimar o desempenho possível usando dados coletados durante operação normal em malha fechada. Isso é muito relevante industrialmente, porque evita forçar testes invasivos na planta.\n\nConclusão para meu TCC:\nIsso conversa diretamente com o meu TCC: o digital twin pode gerar dados contínuos de operação e permitir que o supervisor avalie malhas sem precisar interromper ou perturbar artificialmente a planta.","updated":"2026-06-10T00:45:22.535Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":3037,"end":3540},{"type":"TextQuoteSelector","exact":"This is followed by a briefderivation of a minimum variance controller, and of thèresulting properties of a process operating under minimum var-iance control. It is then shown that thè theoretical best achiev-able performance in thè mean square sense can be estimatedfrom process data collected under ‘normal’ closed loop condi-tions. A method for estimating this mean square performanceis discussed. This is followed by a Monte-Carlo simulation toillustrate thè statistical properties of thè estimator.","prefix":"è process description is given. ","suffix":" Finally, thistechnique is appli"}]}]}
>```
>%%
>*%%PREFIX%%è process description is given.%%HIGHLIGHT%% ==This is followed by a briefderivation of a minimum variance controller, and of thèresulting properties of a process operating under minimum var-iance control. It is then shown that thè theoretical best achiev-able performance in thè mean square sense can be estimatedfrom process data collected under ‘normal’ closed loop condi-tions. A method for estimating this mean square performanceis discussed. This is followed by a Monte-Carlo simulation toillustrate thè statistical properties of thè estimator.== %%POSTFIX%%Finally, thistechnique is appli*
>%%LINK%%[[#^m6gi5eb406|show annotation]]
>%%COMMENT%%
>Comentário:
>Harris usa o controle de variância mínima como referência teórica de melhor desempenho. O ponto não é necessariamente implementar esse controlador, mas usar seu desempenho como limite inferior para comparar uma malha real.
>
>Eu posso tratar o Harris Benchmark como uma régua de comparação para os PIDs simulados: não para substituir o PID imediatamente, mas para medir se ele está muito distante do melhor desempenho possível.
>
>Harris propõe estimar o desempenho possível usando dados coletados durante operação normal em malha fechada. Isso é muito relevante industrialmente, porque evita forçar testes invasivos na planta.
>
>Conclusão para meu TCC:
>Isso conversa diretamente com o meu TCC: o digital twin pode gerar dados contínuos de operação e permitir que o supervisor avalie malhas sem precisar interromper ou perturbar artificialmente a planta.
>%%TAGS%%
>
^m6gi5eb406



>%%
>```annotation-json
>{"created":"2026-06-10T00:51:16.168Z","text":"Comentário\n\nA formulação matemática de Harris é mais importante do que parece. Ele escreve a saída controlada como a soma de dois efeitos: a dinâmica causada pela variável manipulada e a perturbação que entra no processo. Em termos conceituais, isso separa o que o controlador consegue influenciar diretamente daquilo que chega como excitação externa ou incerteza dinâmica.\n\nA equação tem a forma de um modelo discreto entrada-saída: a função de transferência em z^-1 representa a dinâmica da planta, U representa a ação manipulada, b representa o atraso inteiro do processo, e D representa a perturbação. Isso transforma o problema de desempenho de controle em uma pergunta matemática precisa: quanto da variabilidade de Y vem de uma perturbação que poderia ser prevista e compensada, e quanto vem de uma parte inevitável por causa do atraso e do ruído?\n\nO ponto forte é que Harris não precisa abrir a planta em estados internos físicos. Ele trabalha com uma decomposição externa: saída, entrada manipulada e perturbação. Depois, a perturbação é modelada como uma série temporal ARIMA, isto é, como ruído branco passando por uma dinâmica estatística. Assim, o problema de controle vira também um problema de previsão: se a perturbação tem estrutura temporal, parte dela pode ser prevista; se não pode ser prevista dentro do horizonte imposto pelo atraso, ela vira erro inevitável.\n\nO Monte Carlo entra justamente para dar peso estatístico a essa ideia. Harris não apenas propõe uma decomposição matemática; ele testa, por simulação repetida, se o estimador do desempenho mínimo se comporta bem quando os dados vêm de um processo estocástico conhecido. Ou seja, ele gera várias realizações da mesma planta com diferentes sequências de ruído e observa se o método consegue recuperar de forma confiável a variância mínima esperada.\n\nConclusão para meu TCC\n\nNo meu TCC, essa equação justifica uma separação arquitetural e matemática essencial: a planta simulada não deve ser tratada como uma caixa única onde tudo é “sinal”. Eu preciso distinguir estado interno da planta, variável manipulada, variável medida e perturbação. Para o Tennessee Eastman, isso significa tratar XMV como ação de controle, XMEAS como observação da planta e IDV como fonte explícita de perturbação.\n\nEssa separação também sustenta a futura camada supervisória. O supervisor não deve olhar apenas para a saída e concluir que a malha está ruim. Ele precisa perguntar: a variabilidade observada vem de má atuação do controlador, de uma perturbação previsível não compensada, de atraso inevitável ou de ruído estatístico? O valor do digital twin é justamente permitir repetir esse experimento várias vezes, como um Monte Carlo controlado, mudando sementes, perturbações e janelas de observação para testar se o diagnóstico da malha é robusto.","updated":"2026-06-10T00:51:16.168Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":1300,"end":1340},{"type":"TextQuoteSelector","exact":"Y, = w ( z -' ) / 8 ( z -' ) U , _ b + D","prefix":"lysis, control loop performance.","suffix":",T here are many techniques avai"}]}]}
>```
>%%
>*%%PREFIX%%lysis, control loop performance.%%HIGHLIGHT%% ==Y, = w ( z -' ) / 8 ( z -' ) U , _ b + D== %%POSTFIX%%,T here are many techniques avai*
>%%LINK%%[[#^324iz2ep1xm|show annotation]]
>%%COMMENT%%
>Comentário
>
>A formulação matemática de Harris é mais importante do que parece. Ele escreve a saída controlada como a soma de dois efeitos: a dinâmica causada pela variável manipulada e a perturbação que entra no processo. Em termos conceituais, isso separa o que o controlador consegue influenciar diretamente daquilo que chega como excitação externa ou incerteza dinâmica.
>
>A equação tem a forma de um modelo discreto entrada-saída: a função de transferência em z^-1 representa a dinâmica da planta, U representa a ação manipulada, b representa o atraso inteiro do processo, e D representa a perturbação. Isso transforma o problema de desempenho de controle em uma pergunta matemática precisa: quanto da variabilidade de Y vem de uma perturbação que poderia ser prevista e compensada, e quanto vem de uma parte inevitável por causa do atraso e do ruído?
>
>O ponto forte é que Harris não precisa abrir a planta em estados internos físicos. Ele trabalha com uma decomposição externa: saída, entrada manipulada e perturbação. Depois, a perturbação é modelada como uma série temporal ARIMA, isto é, como ruído branco passando por uma dinâmica estatística. Assim, o problema de controle vira também um problema de previsão: se a perturbação tem estrutura temporal, parte dela pode ser prevista; se não pode ser prevista dentro do horizonte imposto pelo atraso, ela vira erro inevitável.
>
>O Monte Carlo entra justamente para dar peso estatístico a essa ideia. Harris não apenas propõe uma decomposição matemática; ele testa, por simulação repetida, se o estimador do desempenho mínimo se comporta bem quando os dados vêm de um processo estocástico conhecido. Ou seja, ele gera várias realizações da mesma planta com diferentes sequências de ruído e observa se o método consegue recuperar de forma confiável a variância mínima esperada.
>
>Conclusão para meu TCC
>
>No meu TCC, essa equação justifica uma separação arquitetural e matemática essencial: a planta simulada não deve ser tratada como uma caixa única onde tudo é “sinal”. Eu preciso distinguir estado interno da planta, variável manipulada, variável medida e perturbação. Para o Tennessee Eastman, isso significa tratar XMV como ação de controle, XMEAS como observação da planta e IDV como fonte explícita de perturbação.
>
>Essa separação também sustenta a futura camada supervisória. O supervisor não deve olhar apenas para a saída e concluir que a malha está ruim. Ele precisa perguntar: a variabilidade observada vem de má atuação do controlador, de uma perturbação previsível não compensada, de atraso inevitável ou de ruído estatístico? O valor do digital twin é justamente permitir repetir esse experimento várias vezes, como um Monte Carlo controlado, mudando sementes, perturbações e janelas de observação para testar se o diagnóstico da malha é robusto.
>%%TAGS%%
>
^324iz2ep1xm


>%%
>```annotation-json
>{"created":"2026-06-10T00:53:55.832Z","text":"Comentário:\nO artigo mostra que o feedback não consegue corrigir a saída antes que o atraso do processo tenha passado. Isso é importante porque parte do erro não é culpa da sintonia: é consequência da dinâmica temporal da planta.\n\nConclusão para meu TCC:\nMinha camada supervisória não pode interpretar toda variabilidade como falha de controle. Em processos com atraso, existe uma parcela inevitável de erro que nenhum controlador feedback consegue remover instantaneamente.","updated":"2026-06-10T00:53:55.832Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":13066,"end":13455},{"type":"TextQuoteSelector","exact":"The key feature to note fromEquation (12) is that thè first / moving average terms ofthè closed loop transfer function are not affected by anyform of feedback. The invariance of these parameters tofeedback is simply a recognition that a feedback controlstrategy , linear or nonlinear, cannot return thè processoutput to its target value until thè process deadtime ortime delay has elapsed.","prefix":"quiva-lenti a t -j , for j > /. ","suffix":" The significance of this result"}]}]}
>```
>%%
>*%%PREFIX%%quiva-lenti a t -j , for j > /.%%HIGHLIGHT%% ==The key feature to note fromEquation (12) is that thè first / moving average terms ofthè closed loop transfer function are not affected by anyform of feedback. The invariance of these parameters tofeedback is simply a recognition that a feedback controlstrategy , linear or nonlinear, cannot return thè processoutput to its target value until thè process deadtime ortime delay has elapsed.== %%POSTFIX%%The significance of this result*
>%%LINK%%[[#^cnd1ljt24uv|show annotation]]
>%%COMMENT%%
>Comentário:
>O artigo mostra que o feedback não consegue corrigir a saída antes que o atraso do processo tenha passado. Isso é importante porque parte do erro não é culpa da sintonia: é consequência da dinâmica temporal da planta.
>
>Conclusão para meu TCC:
>Minha camada supervisória não pode interpretar toda variabilidade como falha de controle. Em processos com atraso, existe uma parcela inevitável de erro que nenhum controlador feedback consegue remover instantaneamente.
>%%TAGS%%
>
^cnd1ljt24uv


>%%
>```annotation-json
>{"created":"2026-06-10T08:42:01.015Z","text":"Comentário:\nO artigo valoriza uma abordagem passiva de diagnóstico: observar a saída da malha e estimar o desempenho possível sem injetar sinais externos. Isso torna o método mais adequado para operação industrial contínua.\n\nConclusão para meu TCC:\nNo meu projeto, isso sustenta a ideia de monitoramento online: o sistema pode observar XMEAS e XMV ao longo do tempo e inferir qualidade de controle sem executar experimentos agressivos na planta.","updated":"2026-06-10T08:42:01.015Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":13810,"end":14085},{"type":"TextQuoteSelector","exact":"Consequently , i) it isnot necessary to perturb thè manipulated variable to obtaininformation about thè process dynamics and ii) it is notnecessary to insist on any ‘identifiability’ restrictions (Boxand MacGregor, 1976), as is usually thè case for closed loopidentification.","prefix":"ime series fit only to thè Y s. ","suffix":" If a nonlinear controller is us"}]}]}
>```
>%%
>*%%PREFIX%%ime series fit only to thè Y s.%%HIGHLIGHT%% ==Consequently , i) it isnot necessary to perturb thè manipulated variable to obtaininformation about thè process dynamics and ii) it is notnecessary to insist on any ‘identifiability’ restrictions (Boxand MacGregor, 1976), as is usually thè case for closed loopidentification.== %%POSTFIX%%If a nonlinear controller is us*
>%%LINK%%[[#^w6y5d5gr6nr|show annotation]]
>%%COMMENT%%
>Comentário:
>O artigo valoriza uma abordagem passiva de diagnóstico: observar a saída da malha e estimar o desempenho possível sem injetar sinais externos. Isso torna o método mais adequado para operação industrial contínua.
>
>Conclusão para meu TCC:
>No meu projeto, isso sustenta a ideia de monitoramento online: o sistema pode observar XMEAS e XMV ao longo do tempo e inferir qualidade de controle sem executar experimentos agressivos na planta.
>%%TAGS%%
>
^w6y5d5gr6nr


>%%
>```annotation-json
>{"created":"2026-06-10T09:08:10.723Z","text":"Depois de escrever a planta como função de transferência discreta, ele define b como o atraso inteiro em número de períodos de amostragem/controle.\n\nOu seja: transforma o atraso físico τ_d em atraso discreto usando o intervalo de controle T.","updated":"2026-06-10T09:08:10.723Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/notes/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":3846,"end":3878},{"type":"TextQuoteSelector","exact":"b = 1 + / = 1 + integer (r^ / F)","prefix":" process and is calculated as(2)","suffix":"T is thè control interval and is"}]}]}
>```
>%%
>*%%PREFIX%%process and is calculated as(2)%%HIGHLIGHT%% ==b = 1 + / = 1 + integer (r^ / F)== %%POSTFIX%%T is thè control interval and is*
>%%LINK%%[[#^48n1xtlaaws|show annotation]]
>%%COMMENT%%
>Depois de escrever a planta como função de transferência discreta, ele define b como o atraso inteiro em número de períodos de amostragem/controle.
>
>Ou seja: transforma o atraso físico τ_d em atraso discreto usando o intervalo de controle T.
>%%TAGS%%
>
^48n1xtlaaws
