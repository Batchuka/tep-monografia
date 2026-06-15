---
annotation-target: articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf
titulo: Control structure design for complete chemical plants
autor: Skogestad, S.
ano:
fonte:
tema: politica_supervisao/espirito
---

## O que diz


## O que me interessa


## Conexões

- [[]]

## Citação ABNT

```bibtex
@article{SKOGESTAD_CONTROL_STRUCTURE,
  author  = {Skogestad, S.},
  title   = {Control structure design for complete chemical plants},
  journal = {},
  year    = {},
}
```












>%%
>```annotation-json
>{"created":"2026-06-15T20:33:02.044Z","text":"Mostra que o problema não é sintonia fina; é estrutura de controle. A planta não fica boa porque cada PID foi “bem ajustado”, mas porque alguém escolheu corretamente quais variáveis entram na arquitetura de controle.","updated":"2026-06-15T20:33:02.044Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":286,"end":678},{"type":"TextQuoteSelector","exact":" what to control and how to pair thevariables to form control loops. Although these are very important issues, these decisions are in most cases made in an ad hocfashion, based on experience and engineering insight, without considering the details of each problem. In the paper, a systematicprocedure for control structure design for complete chemical plants (plantwide control) is presented.","prefix":"of the control system, including","suffix":" It starts with carefully defini"}]}]}
>```
>%%
>*%%PREFIX%%of the control system, including%%HIGHLIGHT%% ==what to control and how to pair thevariables to form control loops. Although these are very important issues, these decisions are in most cases made in an ad hocfashion, based on experience and engineering insight, without considering the details of each problem. In the paper, a systematicprocedure for control structure design for complete chemical plants (plantwide control) is presented.== %%POSTFIX%%It starts with carefully defini*
>%%LINK%%[[#^16dvvhh36kb|show annotation]]
>%%COMMENT%%
>Mostra que o problema não é sintonia fina; é estrutura de controle. A planta não fica boa porque cada PID foi “bem ajustado”, mas porque alguém escolheu corretamente quais variáveis entram na arquitetura de controle.
>%%TAGS%%
>
^16dvvhh36kb


>%%
>```annotation-json
>{"created":"2026-06-15T20:34:02.373Z","text":"Excelente para defender que supervisão é uma camada própria, com escala de tempo e função diferente da camada regulatória. O PID atua em segundos; a supervisão decide setpoints e política operacional em escala mais lenta.","updated":"2026-06-15T20:34:02.373Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":1261,"end":1546},{"type":"TextQuoteSelector","exact":"In practice, the control systemis usually divided into several layers, separated by timescale, including (see Fig. 1):. scheduling (weeks),. site-wide optimization (days),. local optimization (hours),. supervisory (predictive, advanced) control (minutes),. regulatory control (seconds)","prefix":"easure-ments and control loops. ","suffix":"Here, we consider the lower thre"}]}]}
>```
>%%
>*%%PREFIX%%easure-ments and control loops.%%HIGHLIGHT%% ==In practice, the control systemis usually divided into several layers, separated by timescale, including (see Fig. 1):. scheduling (weeks),. site-wide optimization (days),. local optimization (hours),. supervisory (predictive, advanced) control (minutes),. regulatory control (seconds)== %%POSTFIX%%Here, we consider the lower thre*
>%%LINK%%[[#^ojwd4nbeit|show annotation]]
>%%COMMENT%%
>Excelente para defender que supervisão é uma camada própria, com escala de tempo e função diferente da camada regulatória. O PID atua em segundos; a supervisão decide setpoints e política operacional em escala mais lenta.
>%%TAGS%%
>
^ojwd4nbeit


>%%
>```annotation-json
>{"created":"2026-06-15T20:35:10.164Z","text":"Essa é uma passagem forte porque coloca o tipo de controlador — PID, MPC, LQG etc. — como apenas o último item. Antes disso vem a arquitetura: entradas, saídas, medições e pareamento.","updated":"2026-06-15T20:35:10.164Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":2114,"end":2571},{"type":"TextQuoteSelector","exact":"1. selection of manipulated variables m (‘‘inputs’’);2. selection of controlled variables (‘‘outputs’’; vari-ables with setpoints);3. selection of (extra) measurements (for controlpurposes including stabilization);4. selection of control configuration (the structure ofthe overall controller that interconnects the con-trolled, manipulated and measured variables);5. selection of controller type (control law specifica-tion, e.g. PID, decoupler, LQG, etc.).","prefix":"kogestad & Postlethwaite, 1996):","suffix":"Control structure design for com"}]}]}
>```
>%%
>*%%PREFIX%%kogestad & Postlethwaite, 1996):%%HIGHLIGHT%% ==1. selection of manipulated variables m (‘‘inputs’’);2. selection of controlled variables (‘‘outputs’’; vari-ables with setpoints);3. selection of (extra) measurements (for controlpurposes including stabilization);4. selection of control configuration (the structure ofthe overall controller that interconnects the con-trolled, manipulated and measured variables);5. selection of controller type (control law specifica-tion, e.g. PID, decoupler, LQG, etc.).== %%POSTFIX%%Control structure design for com*
>%%LINK%%[[#^ch83fnlngw6|show annotation]]
>%%COMMENT%%
>Essa é uma passagem forte porque coloca o tipo de controlador — PID, MPC, LQG etc. — como apenas o último item. Antes disso vem a arquitetura: entradas, saídas, medições e pareamento.
>%%TAGS%%
>
^ch83fnlngw6


>%%
>```annotation-json
>{"created":"2026-06-15T20:35:59.689Z","text":"Plantwide control deve começar de cima, pelos objetivos econômicos e graus de liberdade, e só depois descer para a camada regulatória. Isso sustenta que supervisão não é ajuste local.","updated":"2026-06-15T20:35:59.689Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":5504,"end":5859},{"type":"TextQuoteSelector","exact":"The procedure is divided intwo main parts:I. Top-down analysis, including definition of opera-tional objectives and consideration of degrees offreedom available to meet these (tasks 1 and 2above; steps 1 \u0002/4 in Table 1).II. Bottom-up design of the control system, startingwith the stabilizing control layer (tasks 3, 4 and 5above; steps 5 \u0002/8 in Table 1).","prefix":"n thesupervisory control layer. ","suffix":"The procedure is generally itera"}]}]}
>```
>%%
>*%%PREFIX%%n thesupervisory control layer.%%HIGHLIGHT%% ==The procedure is divided intwo main parts:I. Top-down analysis, including definition of opera-tional objectives and consideration of degrees offreedom available to meet these (tasks 1 and 2above; steps 1 /4 in Table 1).II. Bottom-up design of the control system, startingwith the stabilizing control layer (tasks 3, 4 and 5above; steps 5 /8 in Table 1).== %%POSTFIX%%The procedure is generally itera*
>%%LINK%%[[#^n1gdxsucbhh|show annotation]]
>%%COMMENT%%
>Plantwide control deve começar de cima, pelos objetivos econômicos e graus de liberdade, e só depois descer para a camada regulatória. Isso sustenta que supervisão não é ajuste local.
>%%TAGS%%
>
^n1gdxsucbhh


>%%
>```annotation-json
>{"created":"2026-06-15T20:37:20.910Z","text":"Skogestad basicamente diz: mesmo com poder computacional, um “controlador mágico” não é a melhor solução, por custo de modelagem, sintonia e complexidade.","updated":"2026-06-15T20:37:20.910Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":11435,"end":12016},{"type":"TextQuoteSelector","exact":"Most of the steps in Table 1 could be avoided bydesigning a single optimizing controller that stabilizesthe process and at the same time perfectly coordinatesall the manipulated variables based on dynamic on-lineoptimization. There are fundamental reasons why such asolution is not the best, even with tomorrows computingpower. One fundamental reason is the cost of modelingand tuning this controller, which must be balancedagainst the fact that the hierarchical structuring pro-posed in this paper, without much need for models, isused effectively to control most chemical plants.","prefix":"le big multivariable controller?","suffix":"3. Definition of operational obj"}]}]}
>```
>%%
>*%%PREFIX%%le big multivariable controller?%%HIGHLIGHT%% ==Most of the steps in Table 1 could be avoided bydesigning a single optimizing controller that stabilizesthe process and at the same time perfectly coordinatesall the manipulated variables based on dynamic on-lineoptimization. There are fundamental reasons why such asolution is not the best, even with tomorrows computingpower. One fundamental reason is the cost of modelingand tuning this controller, which must be balancedagainst the fact that the hierarchical structuring pro-posed in this paper, without much need for models, isused effectively to control most chemical plants.== %%POSTFIX%%3. Definition of operational obj*
>%%LINK%%[[#^eg6pdby85nk|show annotation]]
>%%COMMENT%%
>Skogestad basicamente diz: mesmo com poder computacional, um “controlador mágico” não é a melhor solução, por custo de modelagem, sintonia e complexidade.
>%%TAGS%%
>
^eg6pdby85nk


>%%
>```annotation-json
>{"created":"2026-06-15T20:38:08.717Z","text":"Perfeito para argumentar que sem política operacional explícita não existe controle plantwide. A sintonia dos loops não sabe sozinha o que significa “operar bem”: custo, segurança, produção, restrições e qualidade precisam ser definidos antes.","updated":"2026-06-15T20:38:08.717Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":12079,"end":12538},{"type":"TextQuoteSelector","exact":"The operational objectives must be clearly definedbefore attempting to design a control system. Althoughthis seems obvious, this step is frequently overlooked.Preferably, the operational objectives should be com-bined into a scalar cost function J to be minimized. Inmany cases, J may be simply selected as the operationalcost, but there are many other possibilities. Otherobjectives, including safety constraints, should normallybe formulated as constraints.","prefix":"jectives and constraints(step 1)","suffix":"4. Selection of manipulated vari"}]}]}
>```
>%%
>*%%PREFIX%%jectives and constraints(step 1)%%HIGHLIGHT%% ==The operational objectives must be clearly definedbefore attempting to design a control system. Althoughthis seems obvious, this step is frequently overlooked.Preferably, the operational objectives should be com-bined into a scalar cost function J to be minimized. Inmany cases, J may be simply selected as the operationalcost, but there are many other possibilities. Otherobjectives, including safety constraints, should normallybe formulated as constraints.== %%POSTFIX%%4. Selection of manipulated vari*
>%%LINK%%[[#^o80zla8rb|show annotation]]
>%%COMMENT%%
>Perfeito para argumentar que sem política operacional explícita não existe controle plantwide. A sintonia dos loops não sabe sozinha o que significa “operar bem”: custo, segurança, produção, restrições e qualidade precisam ser definidos antes.
>%%TAGS%%
>
^o80zla8rb


>%%
>```annotation-json
>{"created":"2026-06-15T20:40:40.019Z","text":"Essa passagem é muito boa porque revela o ponto filosófico: muitas variáveis internas são controladas não porque tenham setpoint “natural”, mas porque mantêm a planta próxima do ótimo e estável. Isso é supervisão/estrutura, não mera sintonia.","updated":"2026-06-15T20:40:40.019Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":16584,"end":16889},{"type":"TextQuoteSelector","exact":"‘‘Why do we control all these variables in a chemicalplant, like internal temperatures, pressures or composi-tions, when there are no a priori specifications on manyof them?’’. The answer to this question is that we firstneed to control the variables directly related to ensuringoptimal economic operation","prefix":"t puzzled me for many years was:","suffix":" (these are the primarycontrolle"}]}]}
>```
>%%
>*%%PREFIX%%t puzzled me for many years was:%%HIGHLIGHT%% ==‘‘Why do we control all these variables in a chemicalplant, like internal temperatures, pressures or composi-tions, when there are no a priori specifications on manyof them?’’. The answer to this question is that we firstneed to control the variables directly related to ensuringoptimal economic operation== %%POSTFIX%%(these are the primarycontrolle*
>%%LINK%%[[#^cs24uqh0yy8|show annotation]]
>%%COMMENT%%
>Essa passagem é muito boa porque revela o ponto filosófico: muitas variáveis internas são controladas não porque tenham setpoint “natural”, mas porque mantêm a planta próxima do ótimo e estável. Isso é supervisão/estrutura, não mera sintonia.
>%%TAGS%%
>
^cs24uqh0yy8


>%%
>```annotation-json
>{"created":"2026-06-15T20:42:28.185Z","text":"Aqui está a negativa que você quer: manter uma política fixa tem loss. Não existe operação ótima automática sem sacrifício; a escolha das variáveis controladas define quanto se perde quando a planta é perturbada.","updated":"2026-06-15T20:42:28.185Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":18864,"end":19395},{"type":"TextQuoteSelector","exact":"‘‘we want to find a function c of the processvariables which when held constant, leads automaticallyto the optimal adjustments of the manipulated vari-ables.’’ To quantify this more precisely, we define the(economic) loss L as the difference between the actualvalue of the cost function and the truly optimal value,i.e. L \u001eJ(u; d) \u001cJopt(d) where u \u001ef (c;d):/Self-optimizing control (Skogestad, 2000) is achieved if a constant setpoint policy results inan acceptable loss L (without the need to reopti-mize when disturbances occur).","prefix":"ari et al. (1980) whowrite that ","suffix":"The main issue here is not to fi"}]}]}
>```
>%%
>*%%PREFIX%%ari et al. (1980) whowrite that%%HIGHLIGHT%% ==‘‘we want to find a function c of the processvariables which when held constant, leads automaticallyto the optimal adjustments of the manipulated vari-ables.’’ To quantify this more precisely, we define the(economic) loss L as the difference between the actualvalue of the cost function and the truly optimal value,i.e. L J(u; d) Jopt(d) where u f (c;d):/Self-optimizing control (Skogestad, 2000) is achieved if a constant setpoint policy results inan acceptable loss L (without the need to reopti-mize when disturbances occur).== %%POSTFIX%%The main issue here is not to fi*
>%%LINK%%[[#^75omkw368yc|show annotation]]
>%%COMMENT%%
>Aqui está a negativa que você quer: manter uma política fixa tem loss. Não existe operação ótima automática sem sacrifício; a escolha das variáveis controladas define quanto se perde quando a planta é perturbada.
>%%TAGS%%
>
^75omkw368yc


>%%
>```annotation-json
>{"created":"2026-06-15T20:45:33.809Z","text":"Essa passagem mostra que uma decisão supervisória — onde definir a taxa de produção — reorganiza o controle de inventário inteiro. A regra de definir a produção no gargalo principal da planta.","updated":"2026-06-15T20:45:33.809Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":26275,"end":26457},{"type":"TextQuoteSelector","exact":"As we increase the feedrate wereach a point where some flow variable E internally inthe plant reaches its constraint Emax and becomes abottleneck for further increase in production. ","prefix":" optimalto maximize production. ","suffix":"In addi-tion, as we reach the co"}]}]}
>```
>%%
>*%%PREFIX%%optimalto maximize production.%%HIGHLIGHT%% ==As we increase the feedrate wereach a point where some flow variable E internally inthe plant reaches its constraint Emax and becomes abottleneck for further increase in production.== %%POSTFIX%%In addi-tion, as we reach the co*
>%%LINK%%[[#^78vkvka6mns|show annotation]]
>%%COMMENT%%
>Essa passagem mostra que uma decisão supervisória — onde definir a taxa de produção — reorganiza o controle de inventário inteiro. A regra de definir a produção no gargalo principal da planta.
>%%TAGS%%
>
^78vkvka6mns



>%%
>```annotation-json
>{"created":"2026-06-15T20:52:20.377Z","text":"A camada supervisória existe para manter as variáveis primárias nos setpoints ótimos usando como graus de liberdade os setpoints da camada regulatória e manipuladas não usadas. Isso mostra que supervisão atua sobre a política operacional da planta, não apenas sobre válvulas ou ganhos PID.","updated":"2026-06-15T20:52:20.377Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":42708,"end":42929},{"type":"TextQuoteSelector","exact":"The purpose of the supervisor control layer is to keepthe (primary) controlled outputs c at their optimalsetpoints cs, using as degrees of freedom the setpointsy2s in the regulatory layer and any unused manipulatedinputs.","prefix":".8. Supervisory control (step 6)","suffix":" Which variables to control and "}]}]}
>```
>%%
>*%%PREFIX%%.8. Supervisory control (step 6)%%HIGHLIGHT%% ==The purpose of the supervisor control layer is to keepthe (primary) controlled outputs c at their optimalsetpoints cs, using as degrees of freedom the setpointsy2s in the regulatory layer and any unused manipulatedinputs.== %%POSTFIX%%Which variables to control and*
>%%LINK%%[[#^nm3m0mwehih|show annotation]]
>%%COMMENT%%
>A camada supervisória existe para manter as variáveis primárias nos setpoints ótimos usando como graus de liberdade os setpoints da camada regulatória e manipuladas não usadas. Isso mostra que supervisão atua sobre a política operacional da planta, não apenas sobre válvulas ou ganhos PID.
>%%TAGS%%
>
^nm3m0mwehih


>%%
>```annotation-json
>{"created":"2026-06-15T20:52:30.977Z","text":"Essa é uma passagem-chave: o supervisório não inventa setpoints localmente; ele executa uma decisão que vem de uma camada de otimização. Portanto, plantwide control exige uma cadeia: objetivo econômico → variáveis controladas → setpoints → camada regulatória.","updated":"2026-06-15T20:52:30.977Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":42930,"end":43023},{"type":"TextQuoteSelector","exact":"Which variables to control and their setpointsare determined by the optimization layer above.","prefix":"d any unused manipulatedinputs. ","suffix":" Notethat the variables to contr"}]}]}
>```
>%%
>*%%PREFIX%%d any unused manipulatedinputs.%%HIGHLIGHT%% ==Which variables to control and their setpointsare determined by the optimization layer above.== %%POSTFIX%%Notethat the variables to contr*
>%%LINK%%[[#^stxw97zhh2|show annotation]]
>%%COMMENT%%
>Essa é uma passagem-chave: o supervisório não inventa setpoints localmente; ele executa uma decisão que vem de uma camada de otimização. Portanto, plantwide control exige uma cadeia: objetivo econômico → variáveis controladas → setpoints → camada regulatória.
>%%TAGS%%
>
^stxw97zhh2


>%%
>```annotation-json
>{"created":"2026-06-15T20:53:20.252Z","text":"Aqui Skogestad define a questão estrutural da supervisão: escolher entre controle descentralizado e controle multivariável. Isso serve para argumentar que o problema supervisório não é “sintonizar melhor”, mas decidir qual arquitetura de coordenação é adequada para a planta","updated":"2026-06-15T20:53:20.252Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":43101,"end":43370},{"type":"TextQuoteSelector","exact":"For the supervisory control layer, the first structuralissue is deciding on whether to use decentralized ormultivariable control. Note that there is usually somedecentralization, that is, there is often a combination ofseveral multivariable and single-loop controllers.","prefix":"if the activeconstraints change.","suffix":"Decentralized single-loop contro"}]}]}
>```
>%%
>*%%PREFIX%%if the activeconstraints change.%%HIGHLIGHT%% ==For the supervisory control layer, the first structuralissue is deciding on whether to use decentralized ormultivariable control. Note that there is usually somedecentralization, that is, there is often a combination ofseveral multivariable and single-loop controllers.== %%POSTFIX%%Decentralized single-loop contro*
>%%LINK%%[[#^qsnl231dzqf|show annotation]]
>%%COMMENT%%
>Aqui Skogestad define a questão estrutural da supervisão: escolher entre controle descentralizado e controle multivariável. Isso serve para argumentar que o problema supervisório não é “sintonizar melhor”, mas decidir qual arquitetura de coordenação é adequada para a planta
>%%TAGS%%
>
^qsnl231dzqf


>%%
>```annotation-json
>{"created":"2026-06-15T20:54:03.472Z","text":"Essa passagem é ótima para mostrar o limite do controle descentralizado: ele é simples, exige pouco modelo e é fácil de ajustar, mas perde desempenho, exige pareamento e fica complicado quando restrições ativas mudam. Isso mata a ideia de que loops individuais bem sintonizados bastam para plantwide.","updated":"2026-06-15T20:54:03.472Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":43370,"end":43813},{"type":"TextQuoteSelector","exact":"Decentralized single-loop control is the simplest. It ispreferred for non-interacting process and cases whereactive constraints remain constant. Advantages withdecentralized control:. tuning may be done on-line;. no or minimal model requirements;. easy to fix and change.Disadvantages:. need to determine pairing;. performance loss compared to multivariable control;. complicated logic required for reconfiguration whenactive constraints move.","prefix":"ble and single-loop controllers.","suffix":"The decision on how to pair inpu"}]}]}
>```
>%%
>*%%PREFIX%%ble and single-loop controllers.%%HIGHLIGHT%% ==Decentralized single-loop control is the simplest. It ispreferred for non-interacting process and cases whereactive constraints remain constant. Advantages withdecentralized control:. tuning may be done on-line;. no or minimal model requirements;. easy to fix and change.Disadvantages:. need to determine pairing;. performance loss compared to multivariable control;. complicated logic required for reconfiguration whenactive constraints move.== %%POSTFIX%%The decision on how to pair inpu*
>%%LINK%%[[#^mh6tmrekrkt|show annotation]]
>%%COMMENT%%
>Essa passagem é ótima para mostrar o limite do controle descentralizado: ele é simples, exige pouco modelo e é fácil de ajustar, mas perde desempenho, exige pareamento e fica complicado quando restrições ativas mudam. Isso mata a ideia de que loops individuais bem sintonizados bastam para plantwide.
>%%TAGS%%
>
^mh6tmrekrkt


>%%
>```annotation-json
>{"created":"2026-06-15T20:55:00.478Z","text":"Esse é o bloco mais forte para sua proposta: controle multivariável/MPC é indicado para processos interativos e restrições móveis, porque coordena variáveis e lida melhor com restrições. Mas o artigo também freia a expectativa: exige modelo dinâmico, é difícil de sintonizar, menos transparente e mais sensível a incertezas.","updated":"2026-06-15T20:55:00.478Z","document":{"title":"doi:10.1016/j.compchemeng.2003.08.002","link":[{"href":"urn:x-pdf:c069c7c026c50215a7f0f80117423978"},{"href":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf"}],"documentFingerprint":"c069c7c026c50215a7f0f80117423978"},"uri":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","target":[{"source":"vault:/articles/art3_Control-Structure-Desing-for-Complete-Chemical-Plants_Skogestad.pdf","selector":[{"type":"TextPositionSelector","start":44457,"end":44783},{"type":"TextQuoteSelector","exact":"Multivariable control is preferred forinteracting processes and for processes with changesin active constraint. For the cases where theconstraints may change, one needs a multivariablecontroller with explicit constraint handling(e.g. MPC). This avoids the need for logic, andgives a smooth transition between activeconstraints","prefix":"if the active constraintschange.","suffix":". Advantages with multivariable "}]}]}
>```
>%%
>*%%PREFIX%%if the active constraintschange.%%HIGHLIGHT%% ==Multivariable control is preferred forinteracting processes and for processes with changesin active constraint. For the cases where theconstraints may change, one needs a multivariablecontroller with explicit constraint handling(e.g. MPC). This avoids the need for logic, andgives a smooth transition between activeconstraints== %%POSTFIX%%. Advantages with multivariable*
>%%LINK%%[[#^s3j8mvk7hyl|show annotation]]
>%%COMMENT%%
>Esse é o bloco mais forte para sua proposta: controle multivariável/MPC é indicado para processos interativos e restrições móveis, porque coordena variáveis e lida melhor com restrições. Mas o artigo também freia a expectativa: exige modelo dinâmico, é difícil de sintonizar, menos transparente e mais sensível a incertezas.
>%%TAGS%%
>
^s3j8mvk7hyl
