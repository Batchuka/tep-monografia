---
annotation-target: articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf
titulo: Assessment of control loop performance
autor: Burns, W.L.
ano: 2016
fonte:
tags: tecnica_diagnostico
---

>%%
>```annotation-json
>{"created":"2026-06-17T23:23:47.853Z","text":"Isso é uma abstração supervisória, podemos dizer que é uma espécie de 'Loop Performance State'.\n```\nloop.performance = good | degraded | poor\n```\nExemplo:\n\n```yaml\nloop:\n  name: reactor_pressure_control\n  desiredPerformance: near_minimum_variance\n```\nobservado:\n``` yaml\nobserved:\n  harris_ratio: 2.8\n  status: degraded\n```\n\ndaí a ação de reconciliação é gerar um alerta ou solicitar diagnóstico de sintonia, sem k8s atuar diretamente no PID. \n\nNão acho que a ideia se restrinja apenas a mexer no PID, podem haver outros elementos associados as quais o k8s também orquestra algo.\n","updated":"2026-06-17T23:23:47.853Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":1616,"end":1839},{"type":"TextQuoteSelector","exact":"Regardless ofthè control strategy , it is important to have some benchmarkagainst which its performance can be evaluated. The theo-retical ‘best achievable’ control, as measured by thè meansquare error, is such a benchmark.","prefix":"d linear quadratic controllers. ","suffix":" If thè theoretical bestachievab"}]}]}
>```
>%%
>*%%PREFIX%%d linear quadratic controllers.%%HIGHLIGHT%% ==Regardless ofthè control strategy , it is important to have some benchmarkagainst which its performance can be evaluated. The theo-retical ‘best achievable’ control, as measured by thè meansquare error, is such a benchmark.== %%POSTFIX%%If thè theoretical bestachievab*
>%%LINK%%[[#^ogx4bci2fp|show annotation]]
>%%COMMENT%%
>Isso é uma abstração supervisória, podemos dizer que é uma espécie de 'Loop Performance State'.
>```
>loop.performance = good | degraded | poor
>```
>Exemplo:
>
>```yaml
>loop:
>  name: reactor_pressure_control
>  desiredPerformance: near_minimum_variance
>```
>observado:
>``` yaml
>observed:
>  harris_ratio: 2.8
>  status: degraded
>```
>
>daí a ação de reconciliação é gerar um alerta ou solicitar diagnóstico de sintonia, sem k8s atuar diretamente no PID. 
>
>Não acho que a ideia se restrinja apenas a mexer no PID, podem haver outros elementos associados as quais o k8s também orquestra algo.
>
>%%TAGS%%
>
^ogx4bci2fp


>%%
>```annotation-json
>{"created":"2026-06-17T23:27:41.225Z","text":"Isso é bem bacana, esse método é coletado em tempo real sobre a operação nominal da planta. É perfeito para o k8s; ele meio que continuaria consumindo a telemetria da planta enquanto o controlador só está lá. \n\n```yaml\ntelemetry:\n  xmeas: reactor_temperature\n  xmv: reactor_cooling_water_flow\n  samplingTime: 1s\n  loopMode: automatic\n```\n\nÉ objetivamente legal né, porque a sintonia da planta muitas vezes requer 'resposta ao degrau', não é o caso aqui.","updated":"2026-06-17T23:27:41.225Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":3196,"end":3372},{"type":"TextQuoteSelector","exact":"It is then shown that thè theoretical best achiev-able performance in thè mean square sense can be estimatedfrom process data collected under ‘normal’ closed loop condi-tions. ","prefix":"nder minimum var-iance control. ","suffix":"A method for estimating this mea"}]}]}
>```
>%%
>*%%PREFIX%%nder minimum var-iance control.%%HIGHLIGHT%% ==It is then shown that thè theoretical best achiev-able performance in thè mean square sense can be estimatedfrom process data collected under ‘normal’ closed loop condi-tions.== %%POSTFIX%%A method for estimating this mea*
>%%LINK%%[[#^hhml4vrs6zw|show annotation]]
>%%COMMENT%%
>Isso é bem bacana, esse método é coletado em tempo real sobre a operação nominal da planta. É perfeito para o k8s; ele meio que continuaria consumindo a telemetria da planta enquanto o controlador só está lá. 
>
>```yaml
>telemetry:
>  xmeas: reactor_temperature
>  xmv: reactor_cooling_water_flow
>  samplingTime: 1s
>  loopMode: automatic
>```
>
>É objetivamente legal né, porque a sintonia da planta muitas vezes requer 'resposta ao degrau', não é o caso aqui.
>%%TAGS%%
>
^hhml4vrs6zw


>%%
>```annotation-json
>{"created":"2026-06-17T23:31:42.092Z","text":"Sob controle de variância mínima, a saída da malha é o erro de previsão da perturbação. Se a malha está no limite, o que sobra em $Y$ é aquilo que não podia ser previsto e compensado.\n\nIsso é bem bacana porque saber se há margem para sintonia fica tangível, pode ser traduzido para algo como \"ainda existe estrutura previsível sobrando na variável controlada?\" Se existe, a malha pode estar deixando desempenho disponível. Por exemplo:\n\nEstado observado:\n```yaml\nloop:\n  observedPattern:\n    residualPredictability: high\n    autocorrelationAfterDelay: significant\n```\nPolítica:\n```yaml\npolicy:\n  requireResidualPredictability: low\n```\n\n","updated":"2026-06-17T23:31:42.092Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":9990,"end":10113},{"type":"TextQuoteSelector","exact":"Under minimum variance control, thè process output isthè error in forecasting thè disturbance, i.e., D t + b -D t + h / t .","prefix":"ing for Minimum Variance Control","suffix":" This error is a moving average "}]}]}
>```
>%%
>*%%PREFIX%%ing for Minimum Variance Control%%HIGHLIGHT%% ==Under minimum variance control, thè process output isthè error in forecasting thè disturbance, i.e., D t + b -D t + h / t .== %%POSTFIX%%This error is a moving average*
>%%LINK%%[[#^24cf002v2az|show annotation]]
>%%COMMENT%%
>Sob controle de variância mínima, a saída da malha é o erro de previsão da perturbação. Se a malha está no limite, o que sobra em $Y$ é aquilo que não podia ser previsto e compensado.
>
>Isso é bem bacana porque saber se há margem para sintonia fica tangível, pode ser traduzido para algo como "ainda existe estrutura previsível sobrando na variável controlada?" Se existe, a malha pode estar deixando desempenho disponível. Por exemplo:
>
>Estado observado:
>```yaml
>loop:
>  observedPattern:
>    residualPredictability: high
>    autocorrelationAfterDelay: significant
>```
>Política:
>```yaml
>policy:
>  requireResidualPredictability: low
>```
>
>
>%%TAGS%%
>
^24cf002v2az


>%%
>```annotation-json
>{"created":"2026-06-17T23:45:57.906Z","text":"Outro ponto bem objetivo para o k8s se apropriar. Podemos dizer que se a autocorrelação da variável controlada continua significativa depois do atraso esperado, então a malha pode estar degradada. Exemplo:\n\nNo TEP, uma malha de pressão do reator tem atraso discreto estimado f = 3. Se a autocorrelação continua significativa em lag > 3, o diagnóstico publica:\n\n```yaml\nloopHealth: degraded\nreason: predictable_residual_after_deadtime\n```","updated":"2026-06-17T23:45:57.906Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":10308,"end":10559},{"type":"TextQuoteSelector","exact":"A moving average process of order/has thè property thatits autocorrelation function is zero beyond lag /. This propertyenables one to check whether a n y control strategy is givingminimum variance control (Astrom, 1970; Astrom and Wit-tenmark , 1973).","prefix":" ( 1 + V' i + . . . 4- t f ) o2a","suffix":" The sample autocorrelations can"}]}]}
>```
>%%
>*%%PREFIX%%( 1 + V' i + . . . 4- t f ) o2a%%HIGHLIGHT%% ==A moving average process of order/has thè property thatits autocorrelation function is zero beyond lag /. This propertyenables one to check whether a n y control strategy is givingminimum variance control (Astrom, 1970; Astrom and Wit-tenmark , 1973).== %%POSTFIX%%The sample autocorrelations can*
>%%LINK%%[[#^6hc67qx35ef|show annotation]]
>%%COMMENT%%
>Outro ponto bem objetivo para o k8s se apropriar. Podemos dizer que se a autocorrelação da variável controlada continua significativa depois do atraso esperado, então a malha pode estar degradada. Exemplo:
>
>No TEP, uma malha de pressão do reator tem atraso discreto estimado f = 3. Se a autocorrelação continua significativa em lag > 3, o diagnóstico publica:
>
>```yaml
>loopHealth: degraded
>reason: predictable_residual_after_deadtime
>```
>%%TAGS%%
>
^6hc67qx35ef


>%%
>```annotation-json
>{"created":"2026-06-17T23:49:59.663Z","text":"É um jeito tão tangível de identificar se a malha está no seu máximo de controle que pode-se usar para avaliar que ela precisa de outra intervenção, é como se fosse um controle estatístico mesmo — na verdade é exatamente isso.\n\nO k8s poderia classificar o problema em:\n- sintonia\n- atraso\n- estrutura de controle\n- perturbação\n- saturação\n- variável controlada\n\nEu penso no k8s fazendo consultas em camadas:\n1. A malha está degradada? \n→ PI / Predictability Index / métrica de qualidade\n\n2. A degradação parece corrigível por feedback?\n→ Harris Benchmark / Minimum Variance Benchmark\n\n3. Se for corrigível, é sintonia, oscilação, saturação ou agressividade?\n→ autocorrelação, variância de XMV, saturação, modo da malha\n\n4. Se não for corrigível por feedback, é problema estrutural?\n→ atraso, feedforward ausente, variável manipulada ruim, perturbação forte, sensor ruim\n\n---\n\n###  \"A malha está saudável\"\n```yaml\nPI: acceptable\nharris_ratio: close_to_1\nautocorrelation_after_delay: low\nxmv_saturation: false\n```\n**Conclusão**: a variável controlada não apresenta padrão previsível relevante sobrando, e a variância observada está perto do limite estimado.\n**Ação**: não retunar. Apenas continuar monitorando.\n\n\n### “A malha está degradada e há espaço para melhorar por controle”\n```yaml\nPI: poor\nharris_ratio: high\nautocorrelation_after_delay: high\n```\n**Conclusão**: a saída ainda contém estrutura previsível além do atraso. Isso sugere que o controlador não está extraindo todo o desempenho possível.\nAção: abrir diagnóstico de sintonia PID, revisão de parâmetros, oscilação ou estratégia de controle.\n\nAqui sim o Harris ajuda a dizer: talvez seja controle/sintonia.\n\n### “A malha está ruim, mas não parece ser problema de sintonia”\n\n```yaml\nPI: poor\nharris_ratio: close_to_1\nminimum_variance: high\n```\n\n**Conclusão**: a malha está perto do melhor desempenho possível para aquela estrutura, mas esse “melhor possível” ainda é ruim.\n**Ação**: não insistir em retuning. Investigar redução de atraso, feedforward, troca de variável manipulada, sensor, pareamento ou fonte da perturbação.`\n\n### “O controlador tenta corrigir, mas o atuador está no limite”\n```yaml\nPI: poor\nharris_ratio: high\nxmv_saturation: true\nxmv_variability: high\n```\n\n**Conclusão**: existe desempenho perdido, mas o controlador pode estar limitado por saturação, restrição de válvula ou falta de autoridade da variável manipulada.\n**Ação**: não só retunar. Verificar limites de XMV, capacidade do atuador e restrições operacionais.\n\nNo TEP: válvula de água de resfriamento próxima de 100% enquanto a temperatura do reator continua fora do alvo.\n\n### “A malha está oscilando”\n```yaml\nPI: poor\nautocorrelation_pattern: oscillatory\nspectrum_peak: present\nharris_ratio: high\n```\n\n**Conclusão**: a saída tem padrão periódico previsível. Isso pode indicar sintonia agressiva, interação com outra malha ou perturbação periódica.\n**Ação**: classificar como oscilação; depois investigar PID, acoplamento entre malhas ou perturbação externa.\n\n\n### “O problema é atraso”\n```yaml\nPI: poor\nharris_ratio: close_to_1\ndeadtime_fraction: high\nminimum_variance: high\n```\n\n**Conclusão**: o feedback chega tarde demais. Mesmo um controlador bom não consegue remover a variabilidade antes que o atraso passe.\n**Ação**: reduzir atraso de medição/analisador, mudar ponto de medição, usar inferência, ou adicionar feedforward.\n\nNo TEP isso é muito plausível para analisadores de composição, porque há atraso de amostragem/medição.\n\n### “O problema é perturbação não medida”\n```yaml\nPI: poor\nharris_ratio: close_to_1\ndisturbance_activity: high\nfeedforward: absent\n```\n\n**Conclusão**: a malha responde depois que a perturbação já afetou a saída. O feedback sozinho está fazendo o possível.\n**Ação**: criar caminho feedforward ou medir a perturbação antes que ela afete a variável controlada.\n\n## Conclusão aqui\n\nO supervisor tipo Kubernetes não deveria ter uma regra simplista: `if loop_degraded -> retune PID`\n\ntem que ser algo:\n\n```\nif loop_degraded:\n    estimate_minimum_variance()\n    classify_degradation_cause()\n    choose_authorized_action()\n``` ","updated":"2026-06-17T23:49:59.663Z","document":{"title":"Assessment of control loop performance","link":[{"href":"urn:x-pdf:74e243065d2ababf171208423d1f4f1b"},{"href":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf"}],"documentFingerprint":"74e243065d2ababf171208423d1f4f1b"},"uri":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","target":[{"source":"vault:/articles/art9_Assessment-of-Control-Loop-Performance_Harris.pdf","selector":[{"type":"TextPositionSelector","start":11040,"end":11336},{"type":"TextQuoteSelector","exact":"Further reductions can only beachieved through process modifications, such as reducingthè inherent variability <j2a, reducing thè deadtime, incor-porating feedforward control, eliminating thè source of dis-turbances or possibly finding another manipulated variableto control thè process variable.","prefix":"hthè existing control strategy. ","suffix":"U , = -G C ( Z ~' )Y, (11)(10)Su"}]}]}
>```
>%%
>*%%PREFIX%%hthè existing control strategy.%%HIGHLIGHT%% ==Further reductions can only beachieved through process modifications, such as reducingthè inherent variability <j2a, reducing thè deadtime, incor-porating feedforward control, eliminating thè source of dis-turbances or possibly finding another manipulated variableto control thè process variable.== %%POSTFIX%%U , = -G C ( Z ~' )Y, (11)(10)Su*
>%%LINK%%[[#^i93oz2f8tt|show annotation]]
>%%COMMENT%%
>É um jeito tão tangível de identificar se a malha está no seu máximo de controle que pode-se usar para avaliar que ela precisa de outra intervenção, é como se fosse um controle estatístico mesmo — na verdade é exatamente isso.
>
>O k8s poderia classificar o problema em:
>- sintonia
>- atraso
>- estrutura de controle
>- perturbação
>- saturação
>- variável controlada
>
>Eu penso no k8s fazendo consultas em camadas:
>1. A malha está degradada? 
>→ PI / Predictability Index / métrica de qualidade
>
>2. A degradação parece corrigível por feedback?
>→ Harris Benchmark / Minimum Variance Benchmark
>
>3. Se for corrigível, é sintonia, oscilação, saturação ou agressividade?
>→ autocorrelação, variância de XMV, saturação, modo da malha
>
>4. Se não for corrigível por feedback, é problema estrutural?
>→ atraso, feedforward ausente, variável manipulada ruim, perturbação forte, sensor ruim
>
>---
>
>###  "A malha está saudável"
>```yaml
>PI: acceptable
>harris_ratio: close_to_1
>autocorrelation_after_delay: low
>xmv_saturation: false
>```
>**Conclusão**: a variável controlada não apresenta padrão previsível relevante sobrando, e a variância observada está perto do limite estimado.
>**Ação**: não retunar. Apenas continuar monitorando.
>
>
>### “A malha está degradada e há espaço para melhorar por controle”
>```yaml
>PI: poor
>harris_ratio: high
>autocorrelation_after_delay: high
>```
>**Conclusão**: a saída ainda contém estrutura previsível além do atraso. Isso sugere que o controlador não está extraindo todo o desempenho possível.
>Ação: abrir diagnóstico de sintonia PID, revisão de parâmetros, oscilação ou estratégia de controle.
>
>Aqui sim o Harris ajuda a dizer: talvez seja controle/sintonia.
>
>### “A malha está ruim, mas não parece ser problema de sintonia”
>
>```yaml
>PI: poor
>harris_ratio: close_to_1
>minimum_variance: high
>```
>
>**Conclusão**: a malha está perto do melhor desempenho possível para aquela estrutura, mas esse “melhor possível” ainda é ruim.
>**Ação**: não insistir em retuning. Investigar redução de atraso, feedforward, troca de variável manipulada, sensor, pareamento ou fonte da perturbação.`
>
>### “O controlador tenta corrigir, mas o atuador está no limite”
>```yaml
>PI: poor
>harris_ratio: high
>xmv_saturation: true
>xmv_variability: high
>```
>
>**Conclusão**: existe desempenho perdido, mas o controlador pode estar limitado por saturação, restrição de válvula ou falta de autoridade da variável manipulada.
>**Ação**: não só retunar. Verificar limites de XMV, capacidade do atuador e restrições operacionais.
>
>No TEP: válvula de água de resfriamento próxima de 100% enquanto a temperatura do reator continua fora do alvo.
>
>### “A malha está oscilando”
>```yaml
>PI: poor
>autocorrelation_pattern: oscillatory
>spectrum_peak: present
>harris_ratio: high
>```
>
>**Conclusão**: a saída tem padrão periódico previsível. Isso pode indicar sintonia agressiva, interação com outra malha ou perturbação periódica.
>**Ação**: classificar como oscilação; depois investigar PID, acoplamento entre malhas ou perturbação externa.
>
>
>### “O problema é atraso”
>```yaml
>PI: poor
>harris_ratio: close_to_1
>deadtime_fraction: high
>minimum_variance: high
>```
>
>**Conclusão**: o feedback chega tarde demais. Mesmo um controlador bom não consegue remover a variabilidade antes que o atraso passe.
>**Ação**: reduzir atraso de medição/analisador, mudar ponto de medição, usar inferência, ou adicionar feedforward.
>
>No TEP isso é muito plausível para analisadores de composição, porque há atraso de amostragem/medição.
>
>### “O problema é perturbação não medida”
>```yaml
>PI: poor
>harris_ratio: close_to_1
>disturbance_activity: high
>feedforward: absent
>```
>
>**Conclusão**: a malha responde depois que a perturbação já afetou a saída. O feedback sozinho está fazendo o possível.
>**Ação**: criar caminho feedforward ou medir a perturbação antes que ela afete a variável controlada.
>
>## Conclusão aqui
>
>O supervisor tipo Kubernetes não deveria ter uma regra simplista: `if loop_degraded -> retune PID`
>
>tem que ser algo:
>
>```
>if loop_degraded:
>    estimate_minimum_variance()
>    classify_degradation_cause()
>    choose_authorized_action()
>``` 
>%%TAGS%%
>
^i93oz2f8tt
