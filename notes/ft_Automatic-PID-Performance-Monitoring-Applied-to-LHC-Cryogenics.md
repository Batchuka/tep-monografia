---
type: resumo
annotation-target: notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf
titulo: Automatic Assessment of PID Controllers Applied to the LHC Cryogenic System
autor: Blanco Viñuela; Fernández Adiego; Gayet; Goddet
ano: "2013"
fonte: ICALEPCS 2013 — Proceedings
tema: qualidade de malhas PID; Índice de Preditividade; criogenia
conecta-com:
lido-em: 2026-06-06
tags:
  - control-loop-performance
  - predictability-index
  - PID-performance-monitoring
  - model-free-monitoring
  - data-driven-diagnostics
  - PID-tuning
status: lido
---


## O que diz
> *Os autores expõe uma técnica não baseada em métodos clássicos de avaliação — que segundo eles, produziam muitos dados e tornavam impossível a gestão dos loops. Eles implementaram um método numérico e estatístico que é mais objetivo. Esse método é o 'Predictability Index'*


## O que me interessa
> *Filtre o que é relevante para o TCC. Citações diretas com número de página.*


## Conexões
> *Links para outras notas, capítulos da monografia ou conceitos relacionados.*

- [[]]

## Citação ABNT
> *Cole aqui a referência formatada para usar no references.bib*

```bibtex
@inproceedings{CERN_WEAPL02,
  author    = {Blanco Viñuela, E. and Fernández Adiego, B. and Gayet, P. and Goddet, M.},
  title     = {Automatic Assessment of PID Controllers Applied to the {LHC} Cryogenic System},
  booktitle = {Proceedings of ICALEPCS 2013},
  year      = {2013},
  pages     = {WEAPL02},
  note      = {Disponível em:\url{https://cds.cern.ch/record/2305967/files/weapl02.pdf}}
}
```


>%%
>```annotation-json
>{"text":"Já há uma demanda por uma técnica que consiga dar à supervisão uma visão holística do quão bem ajustadas estão as malhas de controle.\n\nPorque a nota aponta a necessidade de uma forma genérica de avaliar e comparar desempenho de malhas, independente da técnica de controle usada.\n\nSe você quiser enfatizar a camada acima das malhas, também caberia 'SUPERVISAO'","target":[{"source":"vault:/notes/articles/art2_Automatic%20PID%20Performance%20Monitoring%20Applied%20to%20LHC%20Cryogenics.pdf","selector":[{"type":"TextPositionSelector","start":4283,"end":4434},{"type":"TextQuoteSelector","exact":"Since 1980, there has been a lot of research to evaluate, ina generic way, the performance of a regulation loop, what-ever is the regulation technique.","prefix":"LATION LOOP PERFORMANCEINDICATOR","suffix":"Some methods use thevariance of"}]}],"created":"2026-06-06T17:54:12.194Z","updated":"2026-06-06T17:54:12.194Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic%20PID%20Performance%20Monitoring%20Applied%20to%20LHC%20Cryogenics.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic%20PID%20Performance%20Monitoring%20Applied%20to%20LHC%20Cryogenics.pdf"}
>```
>%%
>*%%PREFIX%%LATION LOOP PERFORMANCEINDICATOR%%HIGHLIGHT%% ==Since 1980, there has been a lot of research to evaluate, ina generic way, the performance of a regulation loop, what-ever is the regulation technique.== %%POSTFIX%%Some methods use thevariance of*
>%%LINK%%[[#^u9izq95yr7e|show annotation]]
>%%COMMENT%%
>Já há uma demanda por uma técnica que consiga dar à supervisão uma visão holística do quão bem ajustadas estão as malhas de controle.
>
>Porque a nota aponta a necessidade de uma forma genérica de avaliar e comparar desempenho de malhas, independente da técnica de controle usada.
>
>Se você quiser enfatizar a camada acima das malhas, também caberia 'SUPERVISAO'
>%%TAGS%%
>#REQUISITO-BENCHMARKING-POSITIVO, #REQUISITO-SUPERVISAO-POSITIVO
^u9izq95yr7e


>%%
>```annotation-json
>{"text":"O CERN faz, obviamente, o uso intensivo de um padrão de controle chamado UNICOS. É baseado no WinCC.\n\nPorque a nota mostra que o CERN não opera esses PIDs como lógicas isoladas: eles estão dentro de um framework industrial padronizado, o UNICOS, que organiza controle, operação e infraestrutura.","target":[{"source":"vault:/notes/articles/art2_Automatic%20PID%20Performance%20Monitoring%20Applied%20to%20LHC%20Cryogenics.pdf","selector":[{"type":"TextPositionSelector","start":1380,"end":1469},{"type":"TextQuoteSelector","exact":"12 years of operation using the CERN controlframework UNICOS (UNIfied COntrol System) [1]","prefix":"ow very mature af-ter more than","suffix":". Nev-ertheless, the cryogenic o"}]}],"created":"2026-06-06T18:01:35.369Z","updated":"2026-06-06T18:01:35.369Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic%20PID%20Performance%20Monitoring%20Applied%20to%20LHC%20Cryogenics.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic%20PID%20Performance%20Monitoring%20Applied%20to%20LHC%20Cryogenics.pdf"}
>```
>%%
>*%%PREFIX%%ow very mature af-ter more than%%HIGHLIGHT%% ==12 years of operation using the CERN controlframework UNICOS (UNIfied COntrol System) [1]== %%POSTFIX%%. Nev-ertheless, the cryogenic o*
>%%LINK%%[[#^v3l8hdyvkdh|show annotation]]
>%%COMMENT%%
>O CERN faz, obviamente, o uso intensivo de um padrão de controle chamado UNICOS. É baseado no WinCC.
>
>Porque a nota mostra que o CERN não opera esses PIDs como lógicas isoladas: eles estão dentro de um framework industrial padronizado, o UNICOS, que organiza controle, operação e infraestrutura.
>%%TAGS%%
>#MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^v3l8hdyvkdh


>%%
>```annotation-json
>{"text":"O problema não é “como sintonizar um PID”, mas como descobrir, entre milhares de malhas, quais merecem atenção humana.\n\nPorque a nota diz que a escala de 5000 PIDs torna necessário um mecanismo automático de diagnóstico/priorização. \n\nEla reforça seu argumento: em operação industrial real, não basta controlar; é preciso detectar quais malhas estão degradadas.","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":199,"end":221},{"type":"TextQuoteSelector","exact":"employs about 5000 PID","prefix":"adron Collider) cryogenicsystem","suffix":"(Proportional IntegralDerivativ"}]}],"created":"2026-06-08T16:12:23.331Z","updated":"2026-06-08T16:12:23.331Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%adron Collider) cryogenicsystem%%HIGHLIGHT%% ==employs about 5000 PID== %%POSTFIX%%(Proportional IntegralDerivativ*
>%%LINK%%[[#^0lvl58wpi36|show annotation]]
>%%COMMENT%%
>O problema não é “como sintonizar um PID”, mas como descobrir, entre milhares de malhas, quais merecem atenção humana.
>
>Porque a nota diz que a escala de 5000 PIDs torna necessário um mecanismo automático de diagnóstico/priorização. 
>
>Ela reforça seu argumento: em operação industrial real, não basta controlar; é preciso detectar quais malhas estão degradadas.
>%%TAGS%%
>#REQUISITO-DIAGNOSTICO-POSITIVO
^0lvl58wpi36


>%%
>```annotation-json
>{"text":"Uma malha pode não ultrapassar alarmes e ainda assim estar ruim. Ou seja: “sem alarme” não significa “bom controle”\n\nPorque a nota mostra um limite do diagnóstico baseado em threshold: uma malha pode estar degradada sem disparar alarme. \n\nIsso reforça positivamente seu argumento de que é preciso monitorar desempenho, não apenas violação de limites.","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":557,"end":652},{"type":"TextQuoteSelector","exact":"It is nearly impossible to check theperformance of a regulation loop with a classical threshold","prefix":"st perform-ing PID controllers.","suffix":"technique as the controlled vari"}]}],"created":"2026-06-08T16:13:04.309Z","updated":"2026-06-08T16:13:04.309Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%st perform-ing PID controllers.%%HIGHLIGHT%% ==It is nearly impossible to check theperformance of a regulation loop with a classical threshold== %%POSTFIX%%technique as the controlled vari*
>%%LINK%%[[#^6hdihaz6de7|show annotation]]
>%%COMMENT%%
>Uma malha pode não ultrapassar alarmes e ainda assim estar ruim. Ou seja: “sem alarme” não significa “bom controle”
>
>Porque a nota mostra um limite do diagnóstico baseado em threshold: uma malha pode estar degradada sem disparar alarme. 
>
>Isso reforça positivamente seu argumento de que é preciso monitorar desempenho, não apenas violação de limites.
>%%TAGS%%
>#LIMITE-DIAGNOSTICO-POSITIVO
^6hdihaz6de7


>%%
>```annotation-json
>{"text":"Eles montam um modelo regressivo simples: erro futuro estimado como combinação linear de erros anteriores. Isso transforma controle em problema de séries temporais.\n\nPorque a fórmula explica o mecanismo matemático usado para construir um índice de desempenho da malha: prever o erro futuro e usar essa previsibilidade como critério de avaliação.\n\nMas eu prefiro BENCHMARKING, porque o foco da nota é o cálculo do indicador, não ainda a decisão operacional de diagnosticar uma malha ruim.","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":5517,"end":5572},{"type":"TextQuoteSelector","exact":"e(t +b) =a0 +a1 ·e(t)+a2 ·e(t −1)+...+am ·e(t −m−1) (1)","prefix":"ere m is the error model order.ˆ","suffix":"Note that all coefficients ai ha"}]}],"created":"2026-06-08T16:17:19.770Z","updated":"2026-06-08T16:17:19.770Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%ere m is the error model order.ˆ%%HIGHLIGHT%% ==e(t +b) =a0 +a1 ·e(t)+a2 ·e(t −1)+...+am ·e(t −m−1) (1)== %%POSTFIX%%Note that all coefficients ai ha*
>%%LINK%%[[#^kpangmwo9vp|show annotation]]
>%%COMMENT%%
>Eles montam um modelo regressivo simples: erro futuro estimado como combinação linear de erros anteriores. Isso transforma controle em problema de séries temporais.
>
>Porque a fórmula explica o mecanismo matemático usado para construir um índice de desempenho da malha: prever o erro futuro e usar essa previsibilidade como critério de avaliação.
>
>Mas eu prefiro BENCHMARKING, porque o foco da nota é o cálculo do indicador, não ainda a decisão operacional de diagnosticar uma malha ruim.
>%%TAGS%%
>#MECANISMO-BENCHMARKING-POSITIVO, #MECANISMO-DIAGNOSTICO-POSITIVO
^kpangmwo9vp


>%%
>```annotation-json
>{"text":"eles não usam modelo físico da planta criogênica. Isso é importante: o diagnóstico vem dos sinais históricos da malha, não das equações do processo.\n\nPorque o insight é: o diagnóstico de desempenho da malha pode ser feito sem modelo físico da planta, usando apenas sinais históricos da malha.\n\nMas eu prefiro DIAGNOSTICO, porque a função prática da técnica é identificar malhas PID degradadas.","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":988,"end":1120},{"type":"TextQuoteSelector","exact":"This techniqueis generic for any PID feedback control loop, it does not useany process model and needs only a few tuning parameters.","prefix":"in the past year of operation.","suffix":"The publication also describes t"}]}],"created":"2026-06-08T16:21:31.629Z","updated":"2026-06-08T16:21:31.629Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%in the past year of operation.%%HIGHLIGHT%% ==This techniqueis generic for any PID feedback control loop, it does not useany process model and needs only a few tuning parameters.== %%POSTFIX%%The publication also describes t*
>%%LINK%%[[#^0pq9v8gwuykk|show annotation]]
>%%COMMENT%%
>eles não usam modelo físico da planta criogênica. Isso é importante: o diagnóstico vem dos sinais históricos da malha, não das equações do processo.
>
>Porque o insight é: o diagnóstico de desempenho da malha pode ser feito sem modelo físico da planta, usando apenas sinais históricos da malha.
>
>Mas eu prefiro DIAGNOSTICO, porque a função prática da técnica é identificar malhas PID degradadas.
>%%TAGS%%
>#MECANISMO-DIAGNOSTICO-POSITIVO, #MECANISMO-BENCHMARKING-POSITIVO
^0pq9v8gwuykk


>%%
>```annotation-json
>{"text":"O artigo reconhece que uma métrica automática pode gerar falsos positivos e, por isso, adiciona critérios operacionais extras antes de classificar uma malha como mal sintonizada. Isso reforça a ideia de que diagnóstico industrial precisa combinar índice matemático com regras de robustez operacional.\n\nPorque o trecho mostra como o algoritmo evita falsos positivos: ele não usa só o PI bruto, mas adiciona condições auxiliares antes de declarar uma malha como ruim.","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":7243,"end":7372},{"type":"TextQuoteSelector","exact":" in order to avoid false positives as much aspossible to not pollute the results, we have decided to addtwo additional conditions","prefix":"ofthe regulation loop.Moreover,","suffix":"to consider a regulation loop a"}]}],"created":"2026-06-08T16:24:15.908Z","updated":"2026-06-08T16:24:15.908Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%ofthe regulation loop.Moreover,%%HIGHLIGHT%% ==in order to avoid false positives as much aspossible to not pollute the results, we have decided to addtwo additional conditions== %%POSTFIX%%to consider a regulation loop a*
>%%LINK%%[[#^qqt0ygvmcd|show annotation]]
>%%COMMENT%%
>O artigo reconhece que uma métrica automática pode gerar falsos positivos e, por isso, adiciona critérios operacionais extras antes de classificar uma malha como mal sintonizada. Isso reforça a ideia de que diagnóstico industrial precisa combinar índice matemático com regras de robustez operacional.
>
>Porque o trecho mostra como o algoritmo evita falsos positivos: ele não usa só o PI bruto, mas adiciona condições auxiliares antes de declarar uma malha como ruim.
>%%TAGS%%
>#MECANISMO-DIAGNOSTICO-POSITIVO
^qqt0ygvmcd


>%%
>```annotation-json
>{"text":"A fórmula mede quanto do erro da malha permanece imprevisível depois de tentar prever seu comportamento a partir dos erros passados.\n\nPorque a nota define o que a métrica mede: a fração do erro da malha que permanece imprevisível após a predição.","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":5863,"end":5869},{"type":"TextQuoteSelector","exact":"σ2rmse","prefix":"error mse, see equation 2.PI =","suffix":"(2)This predictability index PI"}]}],"created":"2026-06-08T17:02:15.306Z","updated":"2026-06-08T17:02:15.306Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%error mse, see equation 2.PI =%%HIGHLIGHT%% ==σ2rmse== %%POSTFIX%%(2)This predictability index PI*
>%%LINK%%[[#^17x7pbz9h|show annotation]]
>%%COMMENT%%
>A fórmula mede quanto do erro da malha permanece imprevisível depois de tentar prever seu comportamento a partir dos erros passados.
>
>Porque a nota define o que a métrica mede: a fração do erro da malha que permanece imprevisível após a predição.
>%%TAGS%%
>#METRICA-BENCHMARKING-POSITIVO
^17x7pbz9h


>%%
>```annotation-json
>{"text":"O PID é sintonizado individualmente; o “detector de PID ruim” é parametrizado por grupos.\n\nPorque o insight central é o trade-off entre precisão individual e viabilidade operacional: parametrizar cada malha seria melhor, mas inviável em escala; agrupar por tipo torna o diagnóstico praticável.\n\nSe quiser uma segunda tag, menos central: diagnóstico","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":9959,"end":10164},{"type":"TextQuoteSelector","exact":"Ideally, each regulation loop should have its ownparametrization to calculate its predictability index depend-ing on its process dynamics but this is demanding too mucheffort for so many regulation loops. ","prefix":"d Tuning of the Moni-toring Tool","suffix":"Hence, the first taskconsists of"}]}],"created":"2026-06-08T17:06:08.799Z","updated":"2026-06-08T17:06:08.799Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%d Tuning of the Moni-toring Tool%%HIGHLIGHT%% ==Ideally, each regulation loop should have its ownparametrization to calculate its predictability index depend-ing on its process dynamics but this is demanding too mucheffort for so many regulation loops.== %%POSTFIX%%Hence, the first taskconsists of*
>%%LINK%%[[#^ma9cwtxr7os|show annotation]]
>%%COMMENT%%
>O PID é sintonizado individualmente; o “detector de PID ruim” é parametrizado por grupos.
>
>Porque o insight central é o trade-off entre precisão individual e viabilidade operacional: parametrizar cada malha seria melhor, mas inviável em escala; agrupar por tipo torna o diagnóstico praticável.
>
>Se quiser uma segunda tag, menos central: diagnóstico
>%%TAGS%%
>#TRADEOFF-DIAGNOSTICO-POSITIVO, #MECANISMO-DIAGNOSTICO-POSITIVO
^ma9cwtxr7os


>%%
>```annotation-json
>{"text":"Uma malha de controle pode ser operacionalmente melhor mesmo com pior erro de rastreamento, quando o objetivo real inclui suavizar atuadores, preservar equipamentos ou manter a variável apenas dentro de uma faixa aceitável.\n\nPorque o insight central é um trade-off de controle: melhorar o rastreamento do nível pode piorar o esforço/oscilação do atuador; suavizar o atuador pode piorar o erro da variável controlada.","target":[{"source":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":16339,"end":17309},{"type":"TextQuoteSelector","exact":"The second regulation loop represented in Figure 6 withidentifier \"QSRB-4-7LC240\" controls the liquid helium levelin the phase separator of a cryogenic refrigerator at 4.5 K.The actuator controlling this level is an electrical heaterevaporating the liquid to decrease the level. Until 9 am, thecontroller is considered \"good\" as it obtains a predictabilityindex of about 0.7 but the actuator is oscillating a lot and thisbehavior can cause several issues for a long term operation.Consequently, the cryogenic operators modified the PIDparameters of this loop and the actuator was clearly smootherbut, on the other hand, the level was oscillating more and thecontroller was declared as \"poorly tuned\" as its predictabilityindex was around 0.1, well below the setup threshold of 0.4.Nevertheless, the operation team prefered this last tuningover the former one because the level can oscillate slightlyif it stays above 50 % whereas the actuator oscillation canbe an issue.","prefix":"avoidingpotential future issues.","suffix":"These examples show that the pre"}]}],"created":"2026-06-08T17:11:47.043Z","updated":"2026-06-08T17:11:47.043Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/notes/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}
>```
>%%
>*%%PREFIX%%avoidingpotential future issues.%%HIGHLIGHT%% ==The second regulation loop represented in Figure 6 withidentifier "QSRB-4-7LC240" controls the liquid helium levelin the phase separator of a cryogenic refrigerator at 4.5 K.The actuator controlling this level is an electrical heaterevaporating the liquid to decrease the level. Until 9 am, thecontroller is considered "good" as it obtains a predictabilityindex of about 0.7 but the actuator is oscillating a lot and thisbehavior can cause several issues for a long term operation.Consequently, the cryogenic operators modified the PIDparameters of this loop and the actuator was clearly smootherbut, on the other hand, the level was oscillating more and thecontroller was declared as "poorly tuned" as its predictabilityindex was around 0.1, well below the setup threshold of 0.4.Nevertheless, the operation team prefered this last tuningover the former one because the level can oscillate slightlyif it stays above 50 % whereas the actuator oscillation canbe an issue.== %%POSTFIX%%These examples show that the pre*
>%%LINK%%[[#^35fk1zrjvo2|show annotation]]
>%%COMMENT%%
>Uma malha de controle pode ser operacionalmente melhor mesmo com pior erro de rastreamento, quando o objetivo real inclui suavizar atuadores, preservar equipamentos ou manter a variável apenas dentro de uma faixa aceitável.
>
>Porque o insight central é um trade-off de controle: melhorar o rastreamento do nível pode piorar o esforço/oscilação do atuador; suavizar o atuador pode piorar o erro da variável controlada.
>%%TAGS%%
>#TRADEOFF-CONTROLE_AUTOMATICO-POSITIVO, #TRADEOFF-INSTRUMENTACAO-POSITIVO
^35fk1zrjvo2
