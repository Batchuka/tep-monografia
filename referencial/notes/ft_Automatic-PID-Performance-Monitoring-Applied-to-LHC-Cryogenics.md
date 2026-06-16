---
annotation-target: articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf
titulo: Automatic Assessment of PID Controllers Applied to the LHC Cryogenic System
autor: Blanco Viñuela; Fernández Adiego; Gayet; Goddet
ano: "2013"
fonte: ICALEPCS 2013 — Proceedings
tema: politica_supervisao/tecnica
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
>{"created":"2026-06-16T10:05:57.931Z","text":"Ela é model-free. O algoritmo não precisa conhecer a física da planta criogênica; ele usa sinais da própria malha: setpoint, variável medida e saída do controlador.","updated":"2026-06-16T10:05:57.931Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","target":[{"source":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":988,"end":1120},{"type":"TextQuoteSelector","exact":"This techniqueis generic for any PID feedback control loop, it does not useany process model and needs only a few tuning parameters.","prefix":" in the past year of operation. ","suffix":"The publication also describes t"}]}]}
>```
>%%
>*%%PREFIX%%in the past year of operation.%%HIGHLIGHT%% ==This techniqueis generic for any PID feedback control loop, it does not useany process model and needs only a few tuning parameters.== %%POSTFIX%%The publication also describes t*
>%%LINK%%[[#^ohb2wh8ety|show annotation]]
>%%COMMENT%%
>Ela é model-free. O algoritmo não precisa conhecer a física da planta criogênica; ele usa sinais da própria malha: setpoint, variável medida e saída do controlador.
>%%TAGS%%
>
^ohb2wh8ety


>%%
>```annotation-json
>{"created":"2026-06-16T10:08:56.848Z","text":" O artigo posiciona a técnica dentro de Control Loop Performance Assessment. Ou seja: o objetivo não é controlar melhor diretamente, mas medir se a malha está performando bem ou mal.","updated":"2026-06-16T10:08:56.848Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","target":[{"source":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":557,"end":783},{"type":"TextQuoteSelector","exact":"It is nearly impossible to check theperformance of a regulation loop with a classical thresholdtechnique as the controlled variables could evolve in largeoperation ranges and the amount of data cannot be manuallychecked daily.","prefix":"st perform-ing PID controllers. ","suffix":" This paper presents the adaptat"}]}]}
>```
>%%
>*%%PREFIX%%st perform-ing PID controllers.%%HIGHLIGHT%% ==It is nearly impossible to check theperformance of a regulation loop with a classical thresholdtechnique as the controlled variables could evolve in largeoperation ranges and the amount of data cannot be manuallychecked daily.== %%POSTFIX%%This paper presents the adaptat*
>%%LINK%%[[#^wvabhgbsfje|show annotation]]
>%%COMMENT%%
> O artigo posiciona a técnica dentro de Control Loop Performance Assessment. Ou seja: o objetivo não é controlar melhor diretamente, mas medir se a malha está performando bem ou mal.
>%%TAGS%%
>
^wvabhgbsfje


>%%
>```annotation-json
>{"created":"2026-06-16T10:10:14.272Z","text":"O artigo tenta prever o erro futuro da malha a partir dos erros passados. Se o erro tem padrão previsível, a malha parece “comportada”; se parece ruído/imprevisível, a malha pode estar ruim.","updated":"2026-06-16T10:10:14.272Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","target":[{"source":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":5340,"end":5515},{"type":"TextQuoteSelector","exact":"The first calculation to do is the estimation of the error ateach sampling time t for a certain prediction horizon b asdescribed in equation 1 where m is the error model order","prefix":"of the work, publisher, and DOI.","suffix":".ˆe(t +b) =a0 +a1 ·e(t)+a2 ·e(t "}]}]}
>```
>%%
>*%%PREFIX%%of the work, publisher, and DOI.%%HIGHLIGHT%% ==The first calculation to do is the estimation of the error ateach sampling time t for a certain prediction horizon b asdescribed in equation 1 where m is the error model order== %%POSTFIX%%.ˆe(t +b) =a0 +a1 ·e(t)+a2 ·e(t*
>%%LINK%%[[#^bappdqohojm|show annotation]]
>%%COMMENT%%
>O artigo tenta prever o erro futuro da malha a partir dos erros passados. Se o erro tem padrão previsível, a malha parece “comportada”; se parece ruído/imprevisível, a malha pode estar ruim.
>%%TAGS%%
>
^bappdqohojm


>%%
>```annotation-json
>{"created":"2026-06-16T10:11:47.524Z","text":"Esse número é usado para dizer se a malha parece bem ajustada ou candidata a investigação. Leia com cuidado porque há uma ambiguidade entre a fórmula impressa e a interpretação textual, mas operacionalmente o artigo usa PI baixo = comportamento ruim.","updated":"2026-06-16T10:11:47.524Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","target":[{"source":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":5687,"end":5858},{"type":"TextQuoteSelector","exact":" Oncethe error estimation is calculated, the predictability indexPI is computed as function of the error residue variance σ2rand the mean square error mse, see equation 2.","prefix":"east square method for instance.","suffix":"PI = σ2rmse (2)This predictabili"}]}]}
>```
>%%
>*%%PREFIX%%east square method for instance.%%HIGHLIGHT%% ==Oncethe error estimation is calculated, the predictability indexPI is computed as function of the error residue variance σ2rand the mean square error mse, see equation 2.== %%POSTFIX%%PI = σ2rmse (2)This predictabili*
>%%LINK%%[[#^j7kdg7rczd|show annotation]]
>%%COMMENT%%
>Esse número é usado para dizer se a malha parece bem ajustada ou candidata a investigação. Leia com cuidado porque há uma ambiguidade entre a fórmula impressa e a interpretação textual, mas operacionalmente o artigo usa PI baixo = comportamento ruim.
>%%TAGS%%
>
^j7kdg7rczd


>%%
>```annotation-json
>{"created":"2026-06-16T10:12:50.672Z","text":"Ela exige que o atuador esteja realmente se movendo e que o mau desempenho persista em várias janelas. Isso torna o diagnóstico mais robusto.","updated":"2026-06-16T10:12:50.672Z","document":{"title":"Automatic PID Performance Monitoring Applied to LHC CryogenicsAutomatic PID Performance Monitoring Applied to LHC Cryogenics","link":[{"href":"urn:x-pdf:fd30aa98009226dfcc5f77c99e406b60"},{"href":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf"}],"documentFingerprint":"fd30aa98009226dfcc5f77c99e406b60"},"uri":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","target":[{"source":"vault:/articles/art2_Automatic-PID-Performance-Monitoring-Applied-to-LHC-Cryogenics_Bradu_Vinuela_Tilaro.pdf","selector":[{"type":"TextPositionSelector","start":7325,"end":7417},{"type":"TextQuoteSelector","exact":"we have decided to addtwo additional conditions to consider a regulation loop aspoorly tuned","prefix":"ble to not pollute the results, ","suffix":":1. A regulation loop is conside"}]}]}
>```
>%%
>*%%PREFIX%%ble to not pollute the results,%%HIGHLIGHT%% ==we have decided to addtwo additional conditions to consider a regulation loop aspoorly tuned== %%POSTFIX%%:1. A regulation loop is conside*
>%%LINK%%[[#^txw7ssknsz|show annotation]]
>%%COMMENT%%
>Ela exige que o atuador esteja realmente se movendo e que o mau desempenho persista em várias janelas. Isso torna o diagnóstico mais robusto.
>%%TAGS%%
>
^txw7ssknsz
