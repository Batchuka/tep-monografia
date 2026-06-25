---
annotation-target: articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf
titulo: Plantwide control — A review and a new design procedure
autor:
ano:
fonte:
papel: espirito_politica
---

>%%
>```annotation-json
>{"created":"2026-06-15T23:33:40.784Z","text":"Essa é a abertura conceitual do artigo. Ele está dizendo que o problema plantwide vem antes do PID, antes do MPC e antes da sintonia: é decidir qual estrutura de controle faz sentido para a planta. No caso da TEP, isso significa decidir quais variáveis entre XMEAS devem virar variáveis controladas, quais XMV devem ser usadas, e como essas conexões devem ser organizadas.","updated":"2026-06-15T23:33:40.784Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":240,"end":647},{"type":"TextQuoteSelector","exact":"Most(ifnotall)availablecontroltheoriesassumethatacontrolstructureisgivenat the outset. They therefore fail to answer some basic questions that a controlengineer regularly meets in practice (Foss 1973): ‘Which variables should be con-trolled,whichvariablesshouldbemeasured,whichinputsshouldbemanipulated,and which links should be made between them?’ These are the questions thatplantwidecontroltriestoanswer.","prefix":"nnessee Eastmanchallenge process","suffix":"There are two main approaches to"}]}]}
>```
>%%
>*%%PREFIX%%nnessee Eastmanchallenge process%%HIGHLIGHT%% ==Most(ifnotall)availablecontroltheoriesassumethatacontrolstructureisgivenat the outset. They therefore fail to answer some basic questions that a controlengineer regularly meets in practice (Foss 1973): ‘Which variables should be con-trolled,whichvariablesshouldbemeasured,whichinputsshouldbemanipulated,and which links should be made between them?’ These are the questions thatplantwidecontroltriestoanswer.== %%POSTFIX%%There are two main approaches to*
>%%LINK%%[[#^tn7jiqq1vj|show annotation]]
>%%COMMENT%%
>Essa é a abertura conceitual do artigo. Ele está dizendo que o problema plantwide vem antes do PID, antes do MPC e antes da sintonia: é decidir qual estrutura de controle faz sentido para a planta. No caso da TEP, isso significa decidir quais variáveis entre XMEAS devem virar variáveis controladas, quais XMV devem ser usadas, e como essas conexões devem ser organizadas.
>%%TAGS%%
>
^tn7jiqq1vj


>%%
>```annotation-json
>{"created":"2026-06-15T23:34:41.106Z","text":"Esse trecho é essencial porque impede uma interpretação rasa. O artigo não quer ajustar cada PID da TEP. Ele quer responder: qual é a filosofia de controle da planta inteira? Isso inclui seleção de manipuladores, medições, decomposição do problema e configuração de controle. Para a TEP, isso é a diferença entre “controlar reactor pressure” e entender por que reactor pressure deve ou não ser uma variável estrutural da estratégia.","updated":"2026-06-15T23:34:41.106Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":920,"end":1342},{"type":"TextQuoteSelector","exact":"Achemicalplantmayhavethousandsofmeasurementsandcontrolloops.Bythetermplantwide control itisnot meantthetuningandbehaviorofeachoftheseloops,but ratherthe control philosophy ofthe overall plant withemphasis on the structuraldecisions. The structural decision include the selection/placement of manipulatorsand measurements as well as the decomposition of the overall problem into smallersubproblems(thecontrolconfiguration).","prefix":" plantwidecontrol.1 Introduction","suffix":"In practice, the control system "}]}]}
>```
>%%
>*%%PREFIX%%plantwidecontrol.1 Introduction%%HIGHLIGHT%% ==Achemicalplantmayhavethousandsofmeasurementsandcontrolloops.Bythetermplantwide control itisnot meantthetuningandbehaviorofeachoftheseloops,but ratherthe control philosophy ofthe overall plant withemphasis on the structuraldecisions. The structural decision include the selection/placement of manipulatorsand measurements as well as the decomposition of the overall problem into smallersubproblems(thecontrolconfiguration).== %%POSTFIX%%In practice, the control system*
>%%LINK%%[[#^ddtvift2h75|show annotation]]
>%%COMMENT%%
>Esse trecho é essencial porque impede uma interpretação rasa. O artigo não quer ajustar cada PID da TEP. Ele quer responder: qual é a filosofia de controle da planta inteira? Isso inclui seleção de manipuladores, medições, decomposição do problema e configuração de controle. Para a TEP, isso é a diferença entre “controlar reactor pressure” e entender por que reactor pressure deve ou não ser uma variável estrutural da estratégia.
>%%TAGS%%
>
^ddtvift2h75


>%%
>```annotation-json
>{"created":"2026-06-15T23:38:22.124Z","text":"Aqui o artigo dá a arquitetura mental da metodologia. A planta não é controlada por uma única camada. Existe uma camada regulatória rápida, uma supervisória intermediária e uma camada de otimização mais lenta. Isso conecta diretamente com TEP: XMV não deve ser manipulado todo pelo mesmo tipo de controlador. Algumas ações são de estabilização, outras de produção, outras de otimização econômica.","updated":"2026-06-15T23:38:22.124Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":1355,"end":1594},{"type":"TextQuoteSelector","exact":"the control system is usually divided into several layers. Typically,layers include scheduling (weeks), site-wide optimization (day), local optimization(hour),supervisory/predictivecontrol(minutes)andregulatorycontrol(seconds);seeFigure 1.","prefix":"trolconfiguration).In practice, ","suffix":" The optimization layer typicall"}]}]}
>```
>%%
>*%%PREFIX%%trolconfiguration).In practice,%%HIGHLIGHT%% ==the control system is usually divided into several layers. Typically,layers include scheduling (weeks), site-wide optimization (day), local optimization(hour),supervisory/predictivecontrol(minutes)andregulatorycontrol(seconds);seeFigure 1.== %%POSTFIX%%The optimization layer typicall*
>%%LINK%%[[#^f6azou7wm6|show annotation]]
>%%COMMENT%%
>Aqui o artigo dá a arquitetura mental da metodologia. A planta não é controlada por uma única camada. Existe uma camada regulatória rápida, uma supervisória intermediária e uma camada de otimização mais lenta. Isso conecta diretamente com TEP: XMV não deve ser manipulado todo pelo mesmo tipo de controlador. Algumas ações são de estabilização, outras de produção, outras de otimização econômica.
>%%TAGS%%
>
^f6azou7wm6


>%%
>```annotation-json
>{"created":"2026-06-15T23:39:38.367Z","text":"A pergunta não é “qual algoritmo usar dentro do controlador?”, mas como decompor a planta em blocos de decisão. Para a TEP, isso significa separar: planta física simulada, camada regulatória, camada supervisória, otimização, alarmes, intertravamentos e possíveis reconfigurações.","updated":"2026-06-15T23:39:38.367Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":3490,"end":3567},{"type":"TextQuoteSelector","exact":"Which ‘boxes’ should we have and what information should be send betweenthem?","prefix":"eterminingthecontrol structure:Ω","suffix":"Notethatthatweareherenotinterest"}]}]}
>```
>%%
>*%%PREFIX%%eterminingthecontrol structure:Ω%%HIGHLIGHT%% ==Which ‘boxes’ should we have and what information should be send betweenthem?== %%POSTFIX%%Notethatthatweareherenotinterest*
>%%LINK%%[[#^pyb5aw3qjn|show annotation]]
>%%COMMENT%%
>A pergunta não é “qual algoritmo usar dentro do controlador?”, mas como decompor a planta em blocos de decisão. Para a TEP, isso significa separar: planta física simulada, camada regulatória, camada supervisória, otimização, alarmes, intertravamentos e possíveis reconfigurações.
>%%TAGS%%
>
^pyb5aw3qjn


>%%
>```annotation-json
>{"created":"2026-06-15T23:40:17.134Z","text":"Aplicando à TEP:\n* c são as variáveis que recebem setpoint; \n* m são as XMV; \n* v são as medições XMEAS usadas para controle; \n* a configuração define quem controla quem; \n* o tipo de controlador vem por último. \n\nEsse trecho é útil porque força uma ordem: antes de falar PID ou MPC, você precisa classificar variáveis.","updated":"2026-06-15T23:40:17.134Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":3695,"end":3820},{"type":"TextQuoteSelector","exact":"control structure design isdefined as the structural decisions involved in control system design, including thefollowingtasks","prefix":"uning problem). More precisely, ","suffix":"((Foss1973);(Morari1982);(Skoges"}]}]}
>```
>%%
>*%%PREFIX%%uning problem). More precisely,%%HIGHLIGHT%% ==control structure design isdefined as the structural decisions involved in control system design, including thefollowingtasks== %%POSTFIX%%((Foss1973);(Morari1982);(Skoges*
>%%LINK%%[[#^sinv32umuhj|show annotation]]
>%%COMMENT%%
>Aplicando à TEP:
>* c são as variáveis que recebem setpoint; 
>* m são as XMV; 
>* v são as medições XMEAS usadas para controle; 
>* a configuração define quem controla quem; 
>* o tipo de controlador vem por último. 
>
>Esse trecho é útil porque força uma ordem: antes de falar PID ou MPC, você precisa classificar variáveis.
>%%TAGS%%
>
^sinv32umuhj


>%%
>```annotation-json
>{"created":"2026-06-15T23:43:28.138Z","text":"Primeiro vem o top-down: quais são os objetivos da planta, restrições, economia e graus de liberdade? \n\nDepois vem o bottom-up: estabilizar inventários, pressões, temperaturas e malhas locais. \n\nPara a TEP, isso evita começar errado: não se começa escolhendo PIDs; começa-se perguntando quais objetivos operacionais a TEP precisa cumprir.","updated":"2026-06-15T23:43:28.138Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":4421,"end":4687},{"type":"TextQuoteSelector","exact":" control structure design is solved by a mixture of a top-downconsiderationofcontrolobjectivesandwhichdegreesoffreedomareavailabletomeetthese (tasks 1 and 2), and a with a bottom-up design of the control system, startingwiththestabilizationoftheprocess(tasks3,4and5)","prefix":"pler,LQG,etc.).In most cases the","suffix":".In most cases the problem is so"}]}]}
>```
>%%
>*%%PREFIX%%pler,LQG,etc.).In most cases the%%HIGHLIGHT%% ==control structure design is solved by a mixture of a top-downconsiderationofcontrolobjectivesandwhichdegreesoffreedomareavailabletomeetthese (tasks 1 and 2), and a with a bottom-up design of the control system, startingwiththestabilizationoftheprocess(tasks3,4and5)== %%POSTFIX%%.In most cases the problem is so*
>%%LINK%%[[#^4gcb33myb1j|show annotation]]
>%%COMMENT%%
>Primeiro vem o top-down: quais são os objetivos da planta, restrições, economia e graus de liberdade? 
>
>Depois vem o bottom-up: estabilizar inventários, pressões, temperaturas e malhas locais. 
>
>Para a TEP, isso evita começar errado: não se começa escolhendo PIDs; começa-se perguntando quais objetivos operacionais a TEP precisa cumprir.
>%%TAGS%%
>
^4gcb33myb1j


>%%
>```annotation-json
>{"created":"2026-06-15T23:46:42.704Z","text":"Variáveis controladas não são escolhidas porque são fáceis ou tradicionais. Elas são escolhidas porque ajudam a manter a planta perto do ótimo. \n\nNa TEP, isso conecta com o artigo original de Downs & Vogel, que fornece uma função de custo baseada em perdas de matéria-prima, purga, subprodutos, compressor e vapor.","updated":"2026-06-15T23:46:42.704Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":23378,"end":24427},{"type":"TextQuoteSelector","exact":"Why are we controlling hundreds of temperatures, pressures and compositions in achemical plant, when there is no speciﬁcation on most of these variables?Aftersomethought,onerealizesthatthemainreasonforcontrollingallthesevariablesisthatoneneedstospecifytheavailabledegreesoffreedominordertokeeptheplantclosetoitsoptimaloperatingpoint.Butthereisafollow-upquestion:Why do we select a particular set c of controlled variables? (e.g., why specify(control) the top composition in a distillation column, which does not produce ﬁnalproducts, rather than just specifying its reflux?)Theanswertothissecondquestionislessobvious,becauseatfirstitseemslikeitdoesnot really matter which variables we specify (as long as all degrees of freedom areconsumed,becausetheremainingvariablesarethenuniquelydetermined).However,thisistrueonlywhenthereisnouncertaintycausedbydisturbancesandnoise(signaluncertainty) or model uncertainty. When there is uncertainty then it does make adifferencehowthesolutionisimplemented,thatis,whichvariablesweselecttocontrolattheirsetpoints.","prefix":"foutputisanissue,askthequestion:","suffix":"Maarleveld and Rijnsdrop (1970),"}]}]}
>```
>%%
>*%%PREFIX%%foutputisanissue,askthequestion:%%HIGHLIGHT%% ==Why are we controlling hundreds of temperatures, pressures and compositions in achemical plant, when there is no speciﬁcation on most of these variables?Aftersomethought,onerealizesthatthemainreasonforcontrollingallthesevariablesisthatoneneedstospecifytheavailabledegreesoffreedominordertokeeptheplantclosetoitsoptimaloperatingpoint.Butthereisafollow-upquestion:Why do we select a particular set c of controlled variables? (e.g., why specify(control) the top composition in a distillation column, which does not produce ﬁnalproducts, rather than just specifying its reflux?)Theanswertothissecondquestionislessobvious,becauseatfirstitseemslikeitdoesnot really matter which variables we specify (as long as all degrees of freedom areconsumed,becausetheremainingvariablesarethenuniquelydetermined).However,thisistrueonlywhenthereisnouncertaintycausedbydisturbancesandnoise(signaluncertainty) or model uncertainty. When there is uncertainty then it does make adifferencehowthesolutionisimplemented,thatis,whichvariablesweselecttocontrolattheirsetpoints.== %%POSTFIX%%Maarleveld and Rijnsdrop (1970),*
>%%LINK%%[[#^ck8eik312pt|show annotation]]
>%%COMMENT%%
>Variáveis controladas não são escolhidas porque são fáceis ou tradicionais. Elas são escolhidas porque ajudam a manter a planta perto do ótimo. 
>
>Na TEP, isso conecta com o artigo original de Downs & Vogel, que fornece uma função de custo baseada em perdas de matéria-prima, purga, subprodutos, compressor e vapor.
>%%TAGS%%
>
^ck8eik312pt


>%%
>```annotation-json
>{"created":"2026-06-15T23:59:25.413Z","text":"O artigo está dizendo: sem uma função objetivo, a escolha entre controlar recycle flow, reactor holdup, composição ou pressão vira opinião. \n\nCom função custo, a comparação fica técnica: qual escolha causa menor perda econômica? Esse é o raciocínio que depois eles levam para a Tennessee Eastman.","updated":"2026-06-15T23:59:25.413Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":63734,"end":64024},{"type":"TextQuoteSelector","exact":"offuturework,weproposethatonefirstneedstodefineclearlytheobjectivefunction(cost) J for the operation of the reactor system. Only when this is given, may onedecideinarigorousmanneronthebestselectionofcontrolledvariables,forexamplebyusingtheideaof‘self-optimizing’controlandevaluatingtheloss.","prefix":"ing.IntermsPlantwide control 231","suffix":"7. Tennessee Eastman Process7.1."}]}]}
>```
>%%
>*%%PREFIX%%ing.IntermsPlantwide control 231%%HIGHLIGHT%% ==offuturework,weproposethatonefirstneedstodefineclearlytheobjectivefunction(cost) J for the operation of the reactor system. Only when this is given, may onedecideinarigorousmanneronthebestselectionofcontrolledvariables,forexamplebyusingtheideaof‘self-optimizing’controlandevaluatingtheloss.== %%POSTFIX%%7. Tennessee Eastman Process7.1.*
>%%LINK%%[[#^ph1imsl6tkg|show annotation]]
>%%COMMENT%%
>O artigo está dizendo: sem uma função objetivo, a escolha entre controlar recycle flow, reactor holdup, composição ou pressão vira opinião. 
>
>Com função custo, a comparação fica técnica: qual escolha causa menor perda econômica? Esse é o raciocínio que depois eles levam para a Tennessee Eastman.
>%%TAGS%%
>
^ph1imsl6tkg


>%%
>```annotation-json
>{"created":"2026-06-16T00:09:43.756Z","text":"Eles dizem que, para o modo nominal, há 8 graus de liberdade estacionários; 5 ficam consumidos por restrições economicamente ativas; sobram 3 graus livres. Para esses, eles indicam variáveis como reactor temperature, recycle flowrate ou compressor work, e composição de A na purga ou na alimentação do reator.","updated":"2026-06-16T00:09:43.756Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":69971,"end":70244},{"type":"TextQuoteSelector","exact":"A degree of freedomanalysisrevealsthatthereare8degreesoffreedomatsteady-state.Inthenominalcase(mode 1), 5 constraints are active at the optimum (Ricker 1995), which leaves 3unconstraineddegreesoffreedom.Theysystematicallygothroughmostofthealterna-tive controlled variables.","prefix":"ased on steady-state economics. ","suffix":" They find that good self-optimi"}]}]}
>```
>%%
>*%%PREFIX%%ased on steady-state economics.%%HIGHLIGHT%% ==A degree of freedomanalysisrevealsthatthereare8degreesoffreedomatsteady-state.Inthenominalcase(mode 1), 5 constraints are active at the optimum (Ricker 1995), which leaves 3unconstraineddegreesoffreedom.Theysystematicallygothroughmostofthealterna-tive controlled variables.== %%POSTFIX%%They find that good self-optimi*
>%%LINK%%[[#^fs0wxe6iy7u|show annotation]]
>%%COMMENT%%
>Eles dizem que, para o modo nominal, há 8 graus de liberdade estacionários; 5 ficam consumidos por restrições economicamente ativas; sobram 3 graus livres. Para esses, eles indicam variáveis como reactor temperature, recycle flowrate ou compressor work, e composição de A na purga ou na alimentação do reator.
>%%TAGS%%
>
^fs0wxe6iy7u


>%%
>```annotation-json
>{"created":"2026-06-16T00:10:29.653Z","text":"Também concluem que controlar B/inert não é uma boa escolha nesse caso. Isso é a procedure sendo aplicada conceitualmente à TEP: primeiro economia/restrições, depois escolha das variáveis controladas.","updated":"2026-06-16T00:10:29.653Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":70598,"end":70834},{"type":"TextQuoteSelector","exact":",Ainreactorfeed,andCinreactorfeed,isamongthebetterchoicesfromaself-optimizingpointofview.LarssonandSkogestad(2000)concludethatinert(B)compositionshouldnotbecontrolled,whichisagainsttherecommendationsofmostotherauthorsexcept Ricker(1996)","prefix":" and Sigurd Skogestadtemperature","suffix":".Forthecasethey study,withagiven"}]}]}
>```
>%%
>*%%PREFIX%%and Sigurd Skogestadtemperature%%HIGHLIGHT%% ==,Ainreactorfeed,andCinreactorfeed,isamongthebetterchoicesfromaself-optimizingpointofview.LarssonandSkogestad(2000)concludethatinert(B)compositionshouldnotbecontrolled,whichisagainsttherecommendationsofmostotherauthorsexcept Ricker(1996)== %%POSTFIX%%.Forthecasethey study,withagiven*
>%%LINK%%[[#^mb5s42vhctg|show annotation]]
>%%COMMENT%%
>Também concluem que controlar B/inert não é uma boa escolha nesse caso. Isso é a procedure sendo aplicada conceitualmente à TEP: primeiro economia/restrições, depois escolha das variáveis controladas.
>%%TAGS%%
>
^mb5s42vhctg


>%%
>```annotation-json
>{"created":"2026-06-16T00:11:03.150Z","text":"Ela organiza a procedure assim:\n\n1. escolher variáveis controladas com modelo estacionário, restrições e economia;\n2. decidir onde a produção será manipulada;\n3. construir a camada regulatória;\n4. construir a camada supervisória;\n5. calcular setpoints ótimos por real-time optimization;\n6. validar por simulação dinâmica não linear.","updated":"2026-06-16T00:11:03.150Z","document":{"title":"art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","link":[{"href":"urn:x-pdf:512b6e92fc5a420504fafb016d116264"},{"href":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf"}],"documentFingerprint":"512b6e92fc5a420504fafb016d116264"},"uri":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","target":[{"source":"vault:/articles/art4_Plantwide-Control-A-Review-and-a-new-Design-Procedure_Larsson_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":76636,"end":76676},{"type":"TextQuoteSelector","exact":"Table1. Aplantwidecontroldesignprocedure","prefix":"uls Larsson and Sigurd Skogestad","suffix":"Step ToolsandcommentsTop-down an"}]}]}
>```
>%%
>*%%PREFIX%%uls Larsson and Sigurd Skogestad%%HIGHLIGHT%% ==Table1. Aplantwidecontroldesignprocedure== %%POSTFIX%%Step ToolsandcommentsTop-down an*
>%%LINK%%[[#^bd2oj7b84wa|show annotation]]
>%%COMMENT%%
>Ela organiza a procedure assim:
>
>1. escolher variáveis controladas com modelo estacionário, restrições e economia;
>2. decidir onde a produção será manipulada;
>3. construir a camada regulatória;
>4. construir a camada supervisória;
>5. calcular setpoints ótimos por real-time optimization;
>6. validar por simulação dinâmica não linear.
>%%TAGS%%
>
^bd2oj7b84wa
