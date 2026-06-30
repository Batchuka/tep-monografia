---
annotation-target: books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf
titulo: Model Building in Mathematical Programming
autor: H. Paul Williams
ano: 2013
fonte: Wiley / London School of Economics
tags: otimizacao_matematica
---

>%%
>```annotation-json
>{"created":"2026-06-30T00:00:00.000Z","text":"Livro de referência em programação matemática (LP, MIP, não-linear). Estrutura em três partes:\n- Parte I: teoria e construção de modelos (caps 1–11)\n- Parte II: enunciados de 29 problemas clássicos (cap 12)\n- Parte III: formulação e discussão dos mesmos problemas (cap 13)\n\nAplicações industriais relevantes ao projeto estão em 5.1.2 (indústria química) e 12.6/13.6 (otimização de refinaria). O cap. 11 trata da implementação de um sistema de planejamento por programação matemática em contexto organizacional — relevante para pensar o supervisor plant-wide como um solver de PL/PLIM.\n\nRelação com o projeto: a camada supervisória baseada em Kubernetes pode eventualmente delegar decisões de setpoint a um solver de programação matemática. O livro fornece o arcabouço formal para modelar essas decisões como problemas de LP/MIP, com restrições de capacidade, balanço de massa e objetivos conflitantes — todos presentes no TEP.","updated":"2026-06-30T00:00:00.000Z","document":{"title":"Model Building in Mathematical Programming, 5th ed.","link":[{"href":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}],"documentFingerprint":"book3_williams_mbmp_5ed"},"uri":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}
>```
>%%
>*Visão geral do livro e relação com o projeto*
>
>Livro de referência em programação matemática (LP, MIP, não-linear). Estrutura em três partes:
>- Parte I: teoria e construção de modelos (caps 1–11)
>- Parte II: enunciados de 29 problemas clássicos (cap 12)
>- Parte III: formulação e discussão dos mesmos problemas (cap 13)
>
>Aplicações industriais relevantes ao projeto estão em §5.1.2 (indústria química) e §12.6/13.6 (otimização de refinaria). O cap. 11 trata da implementação de um sistema de planejamento por programação matemática em contexto organizacional — relevante para pensar o supervisor plant-wide como um solver de PL/PLIM.
>
>**Relação com o projeto:** a camada supervisória baseada em Kubernetes pode eventualmente delegar decisões de setpoint a um solver de programação matemática. O livro fornece o arcabouço formal para modelar essas decisões como problemas de LP/MIP, com restrições de capacidade, balanço de massa e objetivos conflitantes — todos presentes no TEP.
>%%TAGS%%
>
^overview-williams-mbmp


>%%
>```annotation-json
>{"created":"2026-06-30T19:35:21.068Z","text":"Williams diz que modelos de programação matemática envolvem otimização e que a quantidade a maximizar ou minimizar é chamada de função objetivo.","updated":"2026-06-30T19:35:21.068Z","document":{"title":"Model Building in Mathematical Programming","link":[{"href":"urn:x-pdf:c4f07b23d54b07acd8c624814f1c909e"},{"href":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}],"documentFingerprint":"c4f07b23d54b07acd8c624814f1c909e"},"uri":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","target":[{"source":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","selector":[{"type":"TextPositionSelector","start":30323,"end":30558},{"type":"TextQuoteSelector","exact":"The common feature that mathematical programming models have is that theyall involve optimization. We wish to maximize something or minimize something.The quantity that we wish to maximize or minimize is known as an objectivefunction. ","prefix":" should, however, be understood.","suffix":"Unfortunately, the realization t"}]}]}
>```
>%%
>*%%PREFIX%%should, however, be understood.%%HIGHLIGHT%% ==The common feature that mathematical programming models have is that theyall involve optimization. We wish to maximize something or minimize something.The quantity that we wish to maximize or minimize is known as an objectivefunction.== %%POSTFIX%%Unfortunately, the realization t*
>%%LINK%%[[#^slanqd80md|show annotation]]
>%%COMMENT%%
>Williams diz que modelos de programação matemática envolvem otimização e que a quantidade a maximizar ou minimizar é chamada de função objetivo.
>%%TAGS%%
>
^slanqd80md


>%%
>```annotation-json
>{"created":"2026-06-30T19:38:01.346Z","text":"Ele discute exatamente o problema conceitual: dado um mesmo conjunto de restrições, diferentes objetivos podem levar a diferentes soluções ótimas. \n\nEle também lista exemplos típicos: maximizar lucro, minimizar custo, maximizar utilidade, maximizar valor presente líquido, maximizar robustez etc. \n\nIsso é muito aderente ao meu uso em plantwide control, porque a função objetivo não é “uma equação natural da planta”; ela é uma escolha de formulação que traduz uma política operacional.\n\nEm programação matemática, a função objetivo representa a quantidade escalar que se deseja maximizar ou minimizar, sujeita às restrições do modelo. Williams destaca que a definição do objetivo afeta diretamente a solução obtida e que objetivos usuais incluem maximização de lucro, minimização de custo e critérios compostos de desempenho. No contexto plantwide, essa formulação ganha significado operacional: a função J não descreve apenas uma variável física da planta, mas expressa uma política de operação, ponderando custos, produção, qualidade, consumo energético, perdas e restrições.","updated":"2026-06-30T19:38:01.346Z","document":{"title":"Model Building in Mathematical Programming","link":[{"href":"urn:x-pdf:c4f07b23d54b07acd8c624814f1c909e"},{"href":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}],"documentFingerprint":"c4f07b23d54b07acd8c624814f1c909e"},"uri":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","target":[{"source":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","selector":[{"type":"TextPositionSelector","start":66402,"end":66425},{"type":"TextQuoteSelector","exact":"3.2 Defining objectives","prefix":"tally respectablerepresentation.","suffix":"With a given set of constraints,"}]}]}
>```
>%%
>*%%PREFIX%%tally respectablerepresentation.%%HIGHLIGHT%% ==3.2 Defining objectives== %%POSTFIX%%With a given set of constraints,*
>%%LINK%%[[#^plwnrwyqi3b|show annotation]]
>%%COMMENT%%
>Ele discute exatamente o problema conceitual: dado um mesmo conjunto de restrições, diferentes objetivos podem levar a diferentes soluções ótimas. 
>
>Ele também lista exemplos típicos: maximizar lucro, minimizar custo, maximizar utilidade, maximizar valor presente líquido, maximizar robustez etc. 
>
>Isso é muito aderente ao meu uso em plantwide control, porque a função objetivo não é “uma equação natural da planta”; ela é uma escolha de formulação que traduz uma política operacional.
>
>Em programação matemática, a função objetivo representa a quantidade escalar que se deseja maximizar ou minimizar, sujeita às restrições do modelo. Williams destaca que a definição do objetivo afeta diretamente a solução obtida e que objetivos usuais incluem maximização de lucro, minimização de custo e critérios compostos de desempenho. No contexto plantwide, essa formulação ganha significado operacional: a função J não descreve apenas uma variável física da planta, mas expressa uma política de operação, ponderando custos, produção, qualidade, consumo energético, perdas e restrições.
>%%TAGS%%
>
^plwnrwyqi3b


>%%
>```annotation-json
>{"created":"2026-06-30T19:41:14.430Z","text":"Assim como no problema de otimização de refinaria apresentado por Williams, a TEP pode ser vista, no nível econômico-supervisório, como uma rede de transformação material sujeita a restrições de capacidade, qualidade e disponibilidade. \n\nA função objetivo não descreve a dinâmica física da planta, mas traduz uma política operacional: maximizar retorno ou minimizar custo dado um conjunto de restrições industriais.","updated":"2026-06-30T19:41:14.430Z","document":{"title":"Model Building in Mathematical Programming","link":[{"href":"urn:x-pdf:c4f07b23d54b07acd8c624814f1c909e"},{"href":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}],"documentFingerprint":"c4f07b23d54b07acd8c624814f1c909e"},"uri":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","target":[{"source":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","selector":[{"type":"TextPositionSelector","start":622177,"end":622203},{"type":"TextQuoteSelector","exact":"13.6 Refinery optimization","prefix":"gramming on its right-hand side.","suffix":"The petroleum industry is the ma"}]}]}
>```
>%%
>*%%PREFIX%%gramming on its right-hand side.%%HIGHLIGHT%% ==13.6 Refinery optimization== %%POSTFIX%%The petroleum industry is the ma*
>%%LINK%%[[#^ka92oknz159|show annotation]]
>%%COMMENT%%
>Assim como no problema de otimização de refinaria apresentado por Williams, a TEP pode ser vista, no nível econômico-supervisório, como uma rede de transformação material sujeita a restrições de capacidade, qualidade e disponibilidade. 
>
>A função objetivo não descreve a dinâmica física da planta, mas traduz uma política operacional: maximizar retorno ou minimizar custo dado um conjunto de restrições industriais.
>%%TAGS%%
>
^ka92oknz159


>%%
>```annotation-json
>{"created":"2026-06-30T19:43:24.557Z","text":"O exemplo de blending também é útil, mas é mais limitado. Ele envolve refinar óleos crus, misturá-los, respeitar uma restrição tecnológica de qualidade — dureza entre 3 e 6 — e maximizar lucro líquido. A formulação inclui custos dos insumos, receita do produto, restrições de capacidade de refino, restrições de qualidade e balanço de massa.","updated":"2026-06-30T19:43:24.557Z","document":{"title":"Model Building in Mathematical Programming","link":[{"href":"urn:x-pdf:c4f07b23d54b07acd8c624814f1c909e"},{"href":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}],"documentFingerprint":"c4f07b23d54b07acd8c624814f1c909e"},"uri":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","target":[{"source":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","selector":[{"type":"TextPositionSelector","start":47670,"end":48246},{"type":"TextQuoteSelector","exact":"This problem was converted into a model involving five constraints and sixvariables. It is convenient to name the variables VEG 1, VEG 2, OIL 1, OIL 2,OIL 3 and PROD. The objective is conveniently named PROF (profit) and theconstraints VVEG (vegetable refining), NVEG (non-vegetable refining), UHAR(upper hardness), LHAR (lower hardness) and CONT (continuity). The data areconveniently drawn up in the matrix presented in Table 2.1. It will be seen that theright-hand side coefficients are regarded as a column and named CAP (capacity).Blank cells indicate a zero coefficient.","prefix":"hich a model might be presented.","suffix":"Table 2.1VEG 1 VEG 2 OIL 1 OIL 2"}]}]}
>```
>%%
>*%%PREFIX%%hich a model might be presented.%%HIGHLIGHT%% ==This problem was converted into a model involving five constraints and sixvariables. It is convenient to name the variables VEG 1, VEG 2, OIL 1, OIL 2,OIL 3 and PROD. The objective is conveniently named PROF (profit) and theconstraints VVEG (vegetable refining), NVEG (non-vegetable refining), UHAR(upper hardness), LHAR (lower hardness) and CONT (continuity). The data areconveniently drawn up in the matrix presented in Table 2.1. It will be seen that theright-hand side coefficients are regarded as a column and named CAP (capacity).Blank cells indicate a zero coefficient.== %%POSTFIX%%Table 2.1VEG 1 VEG 2 OIL 1 OIL 2*
>%%LINK%%[[#^kfyrq6rk0a|show annotation]]
>%%COMMENT%%
>O exemplo de blending também é útil, mas é mais limitado. Ele envolve refinar óleos crus, misturá-los, respeitar uma restrição tecnológica de qualidade — dureza entre 3 e 6 — e maximizar lucro líquido. A formulação inclui custos dos insumos, receita do produto, restrições de capacidade de refino, restrições de qualidade e balanço de massa.
>%%TAGS%%
>
^kfyrq6rk0a


>%%
>```annotation-json
>{"created":"2026-06-30T19:44:20.492Z","text":"Uma função objetivo plantwide aparece quando a decisão ótima não pode ser obtida pela soma de ótimos locais. A presença de recursos compartilhados, reciclos, restrições globais e metas econômicas força uma formulação sistêmica.","updated":"2026-06-30T19:44:20.492Z","document":{"title":"Model Building in Mathematical Programming","link":[{"href":"urn:x-pdf:c4f07b23d54b07acd8c624814f1c909e"},{"href":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}],"documentFingerprint":"c4f07b23d54b07acd8c624814f1c909e"},"uri":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","target":[{"source":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","selector":[{"type":"TextPositionSelector","start":116388,"end":116433},{"type":"TextQuoteSelector","exact":"4.1 Multiple plant, product and period models","prefix":"uctured linearprogramming models","suffix":"The purpose of this section is t"}]}]}
>```
>%%
>*%%PREFIX%%uctured linearprogramming models%%HIGHLIGHT%% ==4.1 Multiple plant, product and period models== %%POSTFIX%%The purpose of this section is t*
>%%LINK%%[[#^342h5ts6q6m|show annotation]]
>%%COMMENT%%
>Uma função objetivo plantwide aparece quando a decisão ótima não pode ser obtida pela soma de ótimos locais. A presença de recursos compartilhados, reciclos, restrições globais e metas econômicas força uma formulação sistêmica.
>%%TAGS%%
>
^342h5ts6q6m


>%%
>```annotation-json
>{"created":"2026-06-30T19:46:23.965Z","text":"A função objetivo original da TEP, em Downs & Vogel, é mais estreita: ela considera principalmente custo operacional instantâneo, com perdas de matérias-primas no purge, perdas no produto, formação de subproduto F, trabalho do compressor e vapor no stripper. Ou seja: não há planejamento de manutenção nela. Mas ela pode ser formulada como função objetivo plantwide estendida ou função objetivo supervisória. Aí entram múltiplas dimensões:\n\n$$ \nJ =\nJ_{\\text{operação}}\n+\nJ_{\\text{qualidade}}\n+\nJ_{\\text{energia}}\n+\nJ_{\\text{risco}}\n+\nJ_{\\text{manutenção}}\n+\nJ_{\\text{produção perdida}}\n$$\n\n\n\nA função objetivo do TEP, conforme proposta originalmente, representa uma métrica econômica de operação. Entretanto, em uma formulação plantwide ou supervisória, essa função pode ser ampliada para incorporar múltiplos critérios, como qualidade, produção, energia, risco operacional e planejamento de manutenção. Nesse caso, a função J deixa de representar apenas o custo instantâneo da planta e passa a expressar uma política de operação em horizonte de tempo, combinando variáveis contínuas de processo com decisões discretas de planejamento.\n\n\n","updated":"2026-06-30T19:46:23.965Z","document":{"title":"Model Building in Mathematical Programming","link":[{"href":"urn:x-pdf:c4f07b23d54b07acd8c624814f1c909e"},{"href":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf"}],"documentFingerprint":"c4f07b23d54b07acd8c624814f1c909e"},"uri":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","target":[{"source":"vault:/books/book3_Model-Building-in-Mathematical-Programming_H.Paul-Williams.pdf","selector":[{"type":"TextPositionSelector","start":551275,"end":551298},{"type":"TextQuoteSelector","exact":"12.4 Factory planning 2","prefix":"rothers (which no longerexists).","suffix":"Instead of stipulating when each"}]}]}
>```
>%%
>*%%PREFIX%%rothers (which no longerexists).%%HIGHLIGHT%% ==12.4 Factory planning 2== %%POSTFIX%%Instead of stipulating when each*
>%%LINK%%[[#^qmdjr1rqm6|show annotation]]
>%%COMMENT%%
>A função objetivo original da TEP, em Downs & Vogel, é mais estreita: ela considera principalmente custo operacional instantâneo, com perdas de matérias-primas no purge, perdas no produto, formação de subproduto F, trabalho do compressor e vapor no stripper. Ou seja: não há planejamento de manutenção nela. Mas ela pode ser formulada como função objetivo plantwide estendida ou função objetivo supervisória. Aí entram múltiplas dimensões:
>
>$$ 
>J =
>J_{\text{operação}}
>+
>J_{\text{qualidade}}
>+
>J_{\text{energia}}
>+
>J_{\text{risco}}
>+
>J_{\text{manutenção}}
>+
>J_{\text{produção perdida}}
>$$
>
>
>
>A função objetivo do TEP, conforme proposta originalmente, representa uma métrica econômica de operação. Entretanto, em uma formulação plantwide ou supervisória, essa função pode ser ampliada para incorporar múltiplos critérios, como qualidade, produção, energia, risco operacional e planejamento de manutenção. Nesse caso, a função J deixa de representar apenas o custo instantâneo da planta e passa a expressar uma política de operação em horizonte de tempo, combinando variáveis contínuas de processo com decisões discretas de planejamento.
>
>
>
>%%TAGS%%
>
^qmdjr1rqm6
