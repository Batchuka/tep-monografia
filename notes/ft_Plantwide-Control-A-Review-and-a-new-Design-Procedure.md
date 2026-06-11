---
type: ft
annotation-target: notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf
titulo: Plantwide control — A review and a new design procedure
autor:
ano:
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
@article{PLANTWIDE_REVIEW,
  author  = {},
  title   = {Plantwide control --- A review and a new design procedure},
  journal = {},
  year    = {},
}
```



>%%
>```annotation-json
>{"created":"2026-06-08T20:49:26.748Z","text":"Este é o problema fundador do artigo: antes de projetar controlador, é preciso decidir a arquitetura de controle. A pergunta não é “qual PID usar?”, mas “qual variável merece setpoint, qual atuador deve ser usado e qual informação deve fechar a malha?”. Isso desloca o foco de controle como algoritmo para controle como estrutura de decisão da planta.","updated":"2026-06-08T20:49:26.748Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":240,"end":647},{"type":"TextQuoteSelector","exact":"Most(ifnotall)availablecontroltheoriesassumethatacontrolstructureisgivenat the outset. They therefore fail to answer some basic questions that a controlengineer regularly meets in practice (Foss 1973): ‘Which variables should be con-trolled,whichvariablesshouldbemeasured,whichinputsshouldbemanipulated,and which links should be made between them?’ These are the questions thatplantwidecontroltriestoanswer.","prefix":"nnessee Eastmanchallenge process","suffix":"There are two main approaches to"}]}]}
>```
>%%
>*%%PREFIX%%nnessee Eastmanchallenge process%%HIGHLIGHT%% ==Most(ifnotall)availablecontroltheoriesassumethatacontrolstructureisgivenat the outset. They therefore fail to answer some basic questions that a controlengineer regularly meets in practice (Foss 1973): ‘Which variables should be con-trolled,whichvariablesshouldbemeasured,whichinputsshouldbemanipulated,and which links should be made between them?’ These are the questions thatplantwidecontroltriestoanswer.== %%POSTFIX%%There are two main approaches to*
>%%LINK%%[[#^pn5ces8y618|show annotation]]
>%%COMMENT%%
>Este é o problema fundador do artigo: antes de projetar controlador, é preciso decidir a arquitetura de controle. A pergunta não é “qual PID usar?”, mas “qual variável merece setpoint, qual atuador deve ser usado e qual informação deve fechar a malha?”. Isso desloca o foco de controle como algoritmo para controle como estrutura de decisão da planta.
>%%TAGS%%
>
^pn5ces8y618


>%%
>```annotation-json
>{"created":"2026-06-08T20:52:16.004Z","text":"A ideia forte aqui é que uma planta pode ter muitas malhas funcionando individualmente e ainda assim ter uma estratégia ruim em nível global. O problema plantwide aparece quando as decisões locais precisam ser coerentes com produção, inventários, qualidade, restrições e economia da planta inteira.","updated":"2026-06-08T20:52:16.004Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":989,"end":1153},{"type":"TextQuoteSelector","exact":"plantwide control itisnot meantthetuningandbehaviorofeachoftheseloops,but ratherthe control philosophy ofthe overall plant withemphasis on the structuraldecisions. ","prefix":"rementsandcontrolloops.Bytheterm","suffix":"The structural decision include "}]}]}
>```
>%%
>*%%PREFIX%%rementsandcontrolloops.Bytheterm%%HIGHLIGHT%% ==plantwide control itisnot meantthetuningandbehaviorofeachoftheseloops,but ratherthe control philosophy ofthe overall plant withemphasis on the structuraldecisions.== %%POSTFIX%%The structural decision include*
>%%LINK%%[[#^dd9065guw2k|show annotation]]
>%%COMMENT%%
>A ideia forte aqui é que uma planta pode ter muitas malhas funcionando individualmente e ainda assim ter uma estratégia ruim em nível global. O problema plantwide aparece quando as decisões locais precisam ser coerentes com produção, inventários, qualidade, restrições e economia da planta inteira.
>%%TAGS%%
>
^dd9065guw2k


>%%
>```annotation-json
>{"created":"2026-06-08T20:53:38.225Z","text":"Este trecho é importante porque mostra que controle industrial real é hierárquico: otimização trabalha mais lentamente, controle regulatório trabalha continuamente, e os setpoints conectam as camadas. Para uma digital twin, isso é crucial: modelo dinâmico, integração numérica, controle regulatório e supervisão não devem ser misturados como se fossem a mesma coisa.","updated":"2026-06-08T20:53:38.225Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":3124,"end":3173},{"type":"TextQuoteSelector","exact":"Figure1. Typicalcontrolhierarchyinachemicalplant.","prefix":"torycontrol(seconds)Controllayer","suffix":"switches. Thus, model based cont"}]}]}
>```
>%%
>*%%PREFIX%%torycontrol(seconds)Controllayer%%HIGHLIGHT%% ==Figure1. Typicalcontrolhierarchyinachemicalplant.== %%POSTFIX%%switches. Thus, model based cont*
>%%LINK%%[[#^lz1m5umdbyq|show annotation]]
>%%COMMENT%%
>Este trecho é importante porque mostra que controle industrial real é hierárquico: otimização trabalha mais lentamente, controle regulatório trabalha continuamente, e os setpoints conectam as camadas. Para uma digital twin, isso é crucial: modelo dinâmico, integração numérica, controle regulatório e supervisão não devem ser misturados como se fossem a mesma coisa.
>%%TAGS%%
>
^lz1m5umdbyq


>%%
>```annotation-json
>{"created":"2026-06-08T20:58:50.159Z","text":"O ponto aqui é pragmático: centralizar tudo exige modelo dinâmico detalhado, manutenção pesada e maior exposição a incertezas. Feedback local funciona bem justamente porque usa menos modelo explícito e rejeita perturbações próximas da origem. Isso justifica arquiteturas em camadas, não por limitação computacional apenas, mas por custo de modelagem e robustez.","updated":"2026-06-08T20:58:50.159Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/notes/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":2088,"end":2468},{"type":"TextQuoteSelector","exact":"There are fundamental reasons why such asolution is not the best, even with todays and tomorrows computing power. Onefundamentalreasonisthecostofmodeling,andthefactthatfeedbackcontrol,withoutmuchneedformodels,isveryeffectivewhenperformedlocally.Infact,bycascadingfeed-back loops, it is possible to control large plants with thousands of variableswithouttheneedtodevelopanymodels.H","prefix":"n dynamic on-line optimization. ","suffix":"owever,thetraditionalsingle-loop"}]}]}
>```
>%%
>*%%PREFIX%%n dynamic on-line optimization.%%HIGHLIGHT%% ==There are fundamental reasons why such asolution is not the best, even with todays and tomorrows computing power. Onefundamentalreasonisthecostofmodeling,andthefactthatfeedbackcontrol,withoutmuchneedformodels,isveryeffectivewhenperformedlocally.Infact,bycascadingfeed-back loops, it is possible to control large plants with thousands of variableswithouttheneedtodevelopanymodels.H== %%POSTFIX%%owever,thetraditionalsingle-loop*
>%%LINK%%[[#^czrue9k1ftn|show annotation]]
>%%COMMENT%%
>O ponto aqui é pragmático: centralizar tudo exige modelo dinâmico detalhado, manutenção pesada e maior exposição a incertezas. Feedback local funciona bem justamente porque usa menos modelo explícito e rejeita perturbações próximas da origem. Isso justifica arquiteturas em camadas, não por limitação computacional apenas, mas por custo de modelagem e robustez.
>%%TAGS%%
>
^czrue9k1ftn
