---
type: ft
annotation-target: articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf
titulo: UNICOS — A Framework to Build Industry-Like Control Systems
autor:
ano:
fonte: CERN
tema:
conecta-com: []
lido-em:
tags: [RUNTIME_LACUNA]
status: em-leitura
---

## O que diz


## O que me interessa


## Conexões

- [[]]

## Citação ABNT

```bibtex
@techreport{CERN_UNICOS,
  author      = {},
  title       = {{UNICOS}: A Framework to Build Industry-Like Control Systems},
  institution = {CERN},
  year        = {},
}
```



>%%
>```annotation-json
>{"text":"UNICOS é um framework CERN para sistemas industriais em três camadas.\n\nPorque a nota não fala de PID nem de dinâmica da planta; ela mostra um mecanismo arquitetural usado pelo CERN para estruturar aplicações de controle industrial em camadas. Positivo porque reforça sua ideia de organizar o digital twin/control system com entidades modulares e hierarquia operacional.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":144,"end":255},{"type":"TextQuoteSelector","exact":"UNICOS is a CERN framework developed to produce control applications for three-layer industrial control systems","prefix":"N, Geneva, Switzerland ABSTRACT","suffix":"(Fig. 1). UNICOS provides devel"}]}],"created":"2026-06-07T11:56:58.768Z","updated":"2026-06-07T11:56:58.768Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%N, Geneva, Switzerland ABSTRACT%%HIGHLIGHT%% ==UNICOS is a CERN framework developed to produce control applications for three-layer industrial control systems== %%POSTFIX%%(Fig. 1). UNICOS provides devel*
>%%LINK%%[[#^1u6ohu3fy3g|show annotation]]
>%%COMMENT%%
>UNICOS é um framework CERN para sistemas industriais em três camadas.
>
>Porque a nota não fala de PID nem de dinâmica da planta; ela mostra um mecanismo arquitetural usado pelo CERN para estruturar aplicações de controle industrial em camadas. Positivo porque reforça sua ideia de organizar o digital twin/control system com entidades modulares e hierarquia operacional.
>%%TAGS%%
>#MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^1u6ohu3fy3g


>%%
>```annotation-json
>{"text":"O problema é integrar PLC, SCADA e fieldbus heterogêneos.\n\nPorque o insight aponta um limite/principal dificuldade arquitetural: PLC, SCADA e fieldbus vêm de fornecedores e camadas diferentes, então a integração não é trivial.\n\nÉ positivo para seu argumento porque justifica a necessidade de uma camada/modelo comum de integração, como UNICOS ou uma arquitetura modular inspirada em entidades operacionais.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":2439,"end":2625},{"type":"TextQuoteSelector","exact":"One  of  the  major  problems  faced  by  such  type  of  control  architecture  is  the  heterogeneity  of  the  different layers, the components being provided by different  suppliers.","prefix":"ntegration of the three layers","suffix":"Despite communication standards"}]}],"created":"2026-06-07T11:58:04.357Z","updated":"2026-06-07T11:58:04.357Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%ntegration of the three layers%%HIGHLIGHT%% ==One  of  the  major  problems  faced  by  such  type  of  control  architecture  is  the  heterogeneity  of  the  different layers, the components being provided by different  suppliers.== %%POSTFIX%%Despite communication standards*
>%%LINK%%[[#^fgbsk42c8q5|show annotation]]
>%%COMMENT%%
>O problema é integrar PLC, SCADA e fieldbus heterogêneos.
>
>Porque o insight aponta um limite/principal dificuldade arquitetural: PLC, SCADA e fieldbus vêm de fornecedores e camadas diferentes, então a integração não é trivial.
>
>É positivo para seu argumento porque justifica a necessidade de uma camada/modelo comum de integração, como UNICOS ou uma arquitetura modular inspirada em entidades operacionais.
>%%TAGS%%
>#LIMITE-INTEGRACAO_INDUSTRIAL-POSITIVO
^fgbsk42c8q5



>%%
>```annotation-json
>{"text":"UNICOS usa COTS, mas evita dependência de soluções proprietárias únicas.\n\nPorque o insight explica como o UNICOS lida com heterogeneidade: ele cria um modelo de controle comum acima de componentes COTS de diferentes fornecedores.\n\nÉ positivo porque reforça sua tese de que uma arquitetura industrial robusta não depende de um fornecedor único, mas de uma camada lógica padronizada que integra hardware e software diversos.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":3462,"end":3632},{"type":"TextQuoteSelector","exact":"The purpose of UNICOS is to offer a control model integrating COTS of the three layers. UNICOS can  be  applied  to  hardware  and  software  items  of  many  suppliers. ","prefix":"n many incompatible solutions.","suffix":"The  model  is  implemented  by"}]}],"created":"2026-06-07T12:01:18.682Z","updated":"2026-06-07T12:01:18.682Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%n many incompatible solutions.%%HIGHLIGHT%% ==The purpose of UNICOS is to offer a control model integrating COTS of the three layers. UNICOS can  be  applied  to  hardware  and  software  items  of  many  suppliers.== %%POSTFIX%%The  model  is  implemented  by*
>%%LINK%%[[#^ljvivz5wsq|show annotation]]
>%%COMMENT%%
>UNICOS usa COTS, mas evita dependência de soluções proprietárias únicas.
>
>Porque o insight explica como o UNICOS lida com heterogeneidade: ele cria um modelo de controle comum acima de componentes COTS de diferentes fornecedores.
>
>É positivo porque reforça sua tese de que uma arquitetura industrial robusta não depende de um fornecedor único, mas de uma camada lógica padronizada que integra hardware e software diversos.
>%%TAGS%%
>#MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^ljvivz5wsq


>%%
>```annotation-json
>{"text":"Uma planta contínua pode ser organizada como módulos funcionais aninhados, cada um com fronteira, função e capacidade de controle própria.\n\nPorque o insight explica como uma planta contínua pode ser representada: por decomposição hierárquica em Unit, Equipment Module e Control Module.\n\nEu não colocaria como INTEGRACAO_INDUSTRIAL aqui, porque a ênfase não é interoperabilidade entre sistemas, mas modelo lógico de representação da planta.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":5016,"end":5118},{"type":"TextQuoteSelector","exact":" The other part (Unit, Equipment modules, Control modules) is applicable to continuous process control","prefix":"into several batch productions.","suffix":":   ‚ The Unit is made of Equipm"}]}],"created":"2026-06-08T14:48:11.216Z","updated":"2026-06-08T14:48:11.216Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%into several batch productions.%%HIGHLIGHT%% ==The other part (Unit, Equipment modules, Control modules) is applicable to continuous process control== %%POSTFIX%%:   ‚ The Unit is made of Equipm*
>%%LINK%%[[#^7l2ljodsinn|show annotation]]
>%%COMMENT%%
>Uma planta contínua pode ser organizada como módulos funcionais aninhados, cada um com fronteira, função e capacidade de controle própria.
>
>Porque o insight explica como uma planta contínua pode ser representada: por decomposição hierárquica em Unit, Equipment Module e Control Module.
>
>Eu não colocaria como INTEGRACAO_INDUSTRIAL aqui, porque a ênfase não é interoperabilidade entre sistemas, mas modelo lógico de representação da planta.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^7l2ljodsinn


>%%
>```annotation-json
>{"text":"O ponto mais interessante é a separação entre sinal, equipamento físico e objeto de controle hierárquico.\nI/O object não é “sensor”; é a fronteira padronizada de acesso ao canal físico.\nField object representa algo operável: válvula, motor, aquecedor, PID — já com lógica e estado.\nPCO sobe o nível: controla agrupamentos de objetos e vira a unidade lógica da operação.\nA frase final é chave: I/O e field objects ≈ Control Modules; PCO ≈ Equipment Module ou Unit\n\nPorque o insight explica como o UNICOS organiza a planta: separa sinal bruto, objeto físico operável e objeto lógico hierárquico de controle.\n\nEu manteria em MODELAGEM, não em INTEGRACAO_INDUSTRIAL, porque o ponto forte aqui não é conectar fornecedores diferentes, mas criar uma representação operacional da planta em camadas.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":7009,"end":7064},{"type":"TextQuoteSelector","exact":"These objects can be sorted in three categories (fig.3)","prefix":"each object as a unique parent.","suffix":":    Figure 3: The UNICOS Object"}]}],"created":"2026-06-08T15:12:37.830Z","updated":"2026-06-08T15:12:37.830Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%each object as a unique parent.%%HIGHLIGHT%% ==These objects can be sorted in three categories (fig.3)== %%POSTFIX%%:    Figure 3: The UNICOS Object*
>%%LINK%%[[#^kjc6jpp3ckp|show annotation]]
>%%COMMENT%%
>O ponto mais interessante é a separação entre sinal, equipamento físico e objeto de controle hierárquico.
>I/O object não é “sensor”; é a fronteira padronizada de acesso ao canal físico.
>Field object representa algo operável: válvula, motor, aquecedor, PID — já com lógica e estado.
>PCO sobe o nível: controla agrupamentos de objetos e vira a unidade lógica da operação.
>A frase final é chave: I/O e field objects ≈ Control Modules; PCO ≈ Equipment Module ou Unit
>
>Porque o insight explica como o UNICOS organiza a planta: separa sinal bruto, objeto físico operável e objeto lógico hierárquico de controle.
>
>Eu manteria em MODELAGEM, não em INTEGRACAO_INDUSTRIAL, porque o ponto forte aqui não é conectar fornecedores diferentes, mas criar uma representação operacional da planta em camadas.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^kjc6jpp3ckp


>%%
>```annotation-json
>{"text":"Modelo UNICOS prevê mudança de parâmetros durante fase de programação. Logo, poderíamos supor que também é disponível na fase de operação.\n\nPorque o insight diz que certos parâmetros precisam estar explicitamente configuráveis para que o sistema seja adaptável.\n\nMas cuidado: a frase citada fala em modificação por especialista na fase de programação. Então eu não afirmaria ainda que isso está disponível em operação. Essa parte é uma hipótese sua, não uma conclusão direta do trecho.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":9281,"end":9395},{"type":"TextQuoteSelector","exact":"Configuration parameters set during the programming phase and accessible for modification by a program specialist.","prefix":"to Requests from parent PCO); ‚","suffix":"Programmer Information to Other"}]}],"created":"2026-06-08T15:23:21.453Z","updated":"2026-06-08T15:23:21.453Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%to Requests from parent PCO); ‚%%HIGHLIGHT%% ==Configuration parameters set during the programming phase and accessible for modification by a program specialist.== %%POSTFIX%%Programmer Information to Other*
>%%LINK%%[[#^15ryb7qz3gc|show annotation]]
>%%COMMENT%%
>Modelo UNICOS prevê mudança de parâmetros durante fase de programação. Logo, poderíamos supor que também é disponível na fase de operação.
>
>Porque o insight diz que certos parâmetros precisam estar explicitamente configuráveis para que o sistema seja adaptável.
>
>Mas cuidado: a frase citada fala em modificação por especialista na fase de programação. Então eu não afirmaria ainda que isso está disponível em operação. Essa parte é uma hipótese sua, não uma conclusão direta do trecho.
>%%TAGS%%
>#REQUISITO-SUPERVISAO-NEUTRO
^15ryb7qz3gc


>%%
>```annotation-json
>{"text":"Em vez de o SCADA lidar com milhares de tags soltas, ele lida com objetos coerentes: uma válvula, um PID, um motor, um PCO etc. Cada objeto já vem com comandos, estados, alarmes, permissões, parâmetros e faceplate padronizado.\n\nPorque o insight explica como a camada SCADA/supervisória deixa de enxergar tags soltas e passa a enxergar objetos operacionais coerentes expostos por proxy.\n\nEu não colocaria como MODELAGEM aqui: a modelagem aparece, mas o ponto principal é a interface operacional entre PLC e supervisão.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":8448,"end":8562},{"type":"TextQuoteSelector","exact":"The UNICOS objects are implemented in the PLCs and each of them is provided with a proxy in the supervision layer.","prefix":"st in those selected at CERN).","suffix":"The UNICOS middleware guarantee"}]}],"created":"2026-06-08T15:26:55.638Z","updated":"2026-06-08T15:26:55.638Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%st in those selected at CERN).%%HIGHLIGHT%% ==The UNICOS objects are implemented in the PLCs and each of them is provided with a proxy in the supervision layer.== %%POSTFIX%%The UNICOS middleware guarantee*
>%%LINK%%[[#^wk1kisb92z8|show annotation]]
>%%COMMENT%%
>Em vez de o SCADA lidar com milhares de tags soltas, ele lida com objetos coerentes: uma válvula, um PID, um motor, um PCO etc. Cada objeto já vem com comandos, estados, alarmes, permissões, parâmetros e faceplate padronizado.
>
>Porque o insight explica como a camada SCADA/supervisória deixa de enxergar tags soltas e passa a enxergar objetos operacionais coerentes expostos por proxy.
>
>Eu não colocaria como MODELAGEM aqui: a modelagem aparece, mas o ponto principal é a interface operacional entre PLC e supervisão.
>%%TAGS%%
>#MECANISMO-SUPERVISAO-POSITIVO
^wk1kisb92z8


>%%
>```annotation-json
>{"text":"De modo relevante, essa modelagem traduz os elementos físicos e funcionais do processo em objetos lógicos de alto nível, não apenas para observação, mas também para atuação sobre a planta.\n\nPorque o ponto principal é o mecanismo de sincronização entre objetos no PLC e seus proxies na supervisão.\n\nEu colocaria em INTEGRACAO_INDUSTRIAL, não MODELAGEM, porque a modelagem é o meio; o insight útil é a ponte operacional coerente entre camadas heterogêneas.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":8563,"end":8671},{"type":"TextQuoteSelector","exact":"The UNICOS middleware guarantees the synchronisation between the PLC objects and  their  respective  proxies","prefix":"proxy in the supervision layer.","suffix":".  In  particular,  the  result"}]}],"created":"2026-06-08T15:28:28.119Z","updated":"2026-06-08T15:28:28.119Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%proxy in the supervision layer.%%HIGHLIGHT%% ==The UNICOS middleware guarantees the synchronisation between the PLC objects and  their  respective  proxies== %%POSTFIX%%.  In  particular,  the  result*
>%%LINK%%[[#^n7pn2gqb4ln|show annotation]]
>%%COMMENT%%
>De modo relevante, essa modelagem traduz os elementos físicos e funcionais do processo em objetos lógicos de alto nível, não apenas para observação, mas também para atuação sobre a planta.
>
>Porque o ponto principal é o mecanismo de sincronização entre objetos no PLC e seus proxies na supervisão.
>
>Eu colocaria em INTEGRACAO_INDUSTRIAL, não MODELAGEM, porque a modelagem é o meio; o insight útil é a ponte operacional coerente entre camadas heterogêneas.
>%%TAGS%%
>#MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^n7pn2gqb4ln


>%%
>```annotation-json
>{"text":"Esse trecho está dizendo que, no UNICOS, a análise funcional não começa escrevendo código PLC. Ela começa decompondo a planta em uma hierarquia de PCOs: primeiro você identifica as Units e Equipment Modules da IEC61512-1 e, dentro delas, agrupa os Control Modules, que no UNICOS aparecem como field objects.\n\nPorque o insight explica como o UNICOS transforma análise funcional em estrutura operacional: decompor a planta em PCOs, mapear Unit/Equipment Module e agrupar Control Modules como objetos de campo.\n\nEu manteria em MODELAGEM, não SOFTWARE, porque o ponto não é a implementação em código PLC, mas a estrutura conceitual usada antes da implementação.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":13460,"end":13494},{"type":"TextQuoteSelector","exact":"Functional analysis and PCO model ","prefix":"d for the LHC GCS project [4].","suffix":"With UNICOS, process engineers"}]}],"created":"2026-06-08T15:34:55.641Z","updated":"2026-06-08T15:34:55.641Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%d for the LHC GCS project [4].%%HIGHLIGHT%% ==Functional analysis and PCO model== %%POSTFIX%%With UNICOS, process engineers*
>%%LINK%%[[#^960ys8rjqc7|show annotation]]
>%%COMMENT%%
>Esse trecho está dizendo que, no UNICOS, a análise funcional não começa escrevendo código PLC. Ela começa decompondo a planta em uma hierarquia de PCOs: primeiro você identifica as Units e Equipment Modules da IEC61512-1 e, dentro delas, agrupa os Control Modules, que no UNICOS aparecem como field objects.
>
>Porque o insight explica como o UNICOS transforma análise funcional em estrutura operacional: decompor a planta em PCOs, mapear Unit/Equipment Module e agrupar Control Modules como objetos de campo.
>
>Eu manteria em MODELAGEM, não SOFTWARE, porque o ponto não é a implementação em código PLC, mas a estrutura conceitual usada antes da implementação.
>%%TAGS%%
>#MECANISMO-MODELAGEM-POSITIVO
^960ys8rjqc7


>%%
>```annotation-json
>{"text":"Ou seja, a decomposição em PCOs não é automática nem óbvia. Para sistemas de fluido, o artigo sugere identificar circuitos independentes que executam tarefas independentes. Isso é uma heurística prática: se um circuito pode operar, parar, intertravar ou mudar de modo como uma unidade coerente, ele provavelmente merece virar um PCO.\n\nPorque o ponto central é um limite metodológico: a decomposição em PCOs não tem solução geral automática; exige análise funcional da planta.\n\nÉ positivo para seu projeto porque reforça que a modelagem modular precisa ser uma decisão de engenharia baseada em autonomia operacional, não uma simples tradução mecânica de equipamentos para objetos.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":13768,"end":13833},{"type":"TextQuoteSelector","exact":"This is the most critical phase as there are no general solutions","prefix":"ontrol modules (field objects).","suffix":". For fluids systems, a good app"}]}],"created":"2026-06-08T15:38:16.333Z","updated":"2026-06-08T15:38:16.333Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%ontrol modules (field objects).%%HIGHLIGHT%% ==This is the most critical phase as there are no general solutions== %%POSTFIX%%. For fluids systems, a good app*
>%%LINK%%[[#^ycqhaqsfp68|show annotation]]
>%%COMMENT%%
>Ou seja, a decomposição em PCOs não é automática nem óbvia. Para sistemas de fluido, o artigo sugere identificar circuitos independentes que executam tarefas independentes. Isso é uma heurística prática: se um circuito pode operar, parar, intertravar ou mudar de modo como uma unidade coerente, ele provavelmente merece virar um PCO.
>
>Porque o ponto central é um limite metodológico: a decomposição em PCOs não tem solução geral automática; exige análise funcional da planta.
>
>É positivo para seu projeto porque reforça que a modelagem modular precisa ser uma decisão de engenharia baseada em autonomia operacional, não uma simples tradução mecânica de equipamentos para objetos.
>%%TAGS%%
>#LIMITE-MODELAGEM-POSITIVO
^ycqhaqsfp68


>%%
>```annotation-json
>{"text":"A lógica específica do processo ainda precisa ser escrita, mas dentro de lugares previstos — os placeholders dos PCOs. Então o UNICOS não elimina engenharia de controle; ele elimina muito trabalho repetitivo de infraestrutura.\n\nPorque o insight explica como o UNICOS transforma o modelo PCO em código PLC: ele gera esqueletos/estruturas compatíveis com a hierarquia, mas deixa a lógica específica do processo para o engenheiro.\n\nHá um subtexto de LIMITE, mas eu não usaria como tag principal: o ponto mais forte é o mecanismo de geração de infraestrutura, não a limitação em si.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":15813,"end":16006},{"type":"TextQuoteSelector","exact":" consists  in  producing  the  application  specific  PLC  code.  The  logic  generator tool is used to provide developers with PLC program skeletons which are compliant with the PCO hierarchy.","prefix":"on.  The  second  coding  phase","suffix":"From the functional analysis th"}]}],"created":"2026-06-08T15:44:39.685Z","updated":"2026-06-08T15:44:39.685Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%on.  The  second  coding  phase%%HIGHLIGHT%% ==consists  in  producing  the  application  specific  PLC  code.  The  logic  generator tool is used to provide developers with PLC program skeletons which are compliant with the PCO hierarchy.== %%POSTFIX%%From the functional analysis th*
>%%LINK%%[[#^sn3kenrtefe|show annotation]]
>%%COMMENT%%
>A lógica específica do processo ainda precisa ser escrita, mas dentro de lugares previstos — os placeholders dos PCOs. Então o UNICOS não elimina engenharia de controle; ele elimina muito trabalho repetitivo de infraestrutura.
>
>Porque o insight explica como o UNICOS transforma o modelo PCO em código PLC: ele gera esqueletos/estruturas compatíveis com a hierarquia, mas deixa a lógica específica do processo para o engenheiro.
>
>Há um subtexto de LIMITE, mas eu não usaria como tag principal: o ponto mais forte é o mecanismo de geração de infraestrutura, não a limitação em si.
>%%TAGS%%
>#MECANISMO-SOFTWARE-POSITIVO
^sn3kenrtefe


>%%
>```annotation-json
>{"text":"Modelagem é basicamente: 'Devices Specification → Instance Generator → PLC + SCADA + Middleware'.\n\nO ponto é modelo declarativo + geração consistente de artefatos em múltiplas camadas.\n\nPorque o insight explica como o UNICOS produz artefatos coerentes: parte de uma especificação declarativa, gera instâncias e deriva código/configuração para PLC, SCADA e middleware.\n\nEu não colocaria como MODELAGEM principal, porque aqui o ponto não é representar a planta em si, mas o pipeline de geração model-driven que transforma modelo em software operacional.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":17849,"end":17893},{"type":"TextQuoteSelector","exact":"Figure 6 : UNICOS Basic Software  Production","prefix":"ndustry Like Control ... 7 of 9","suffix":"Maintenance.  The  Functional"}]}],"created":"2026-06-08T15:45:59.451Z","updated":"2026-06-08T15:45:59.451Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%ndustry Like Control ... 7 of 9%%HIGHLIGHT%% ==Figure 6 : UNICOS Basic Software  Production== %%POSTFIX%%Maintenance.  The  Functional*
>%%LINK%%[[#^l5d941d9boe|show annotation]]
>%%COMMENT%%
>Modelagem é basicamente: 'Devices Specification → Instance Generator → PLC + SCADA + Middleware'.
>
>O ponto é modelo declarativo + geração consistente de artefatos em múltiplas camadas.
>
>Porque o insight explica como o UNICOS produz artefatos coerentes: parte de uma especificação declarativa, gera instâncias e deriva código/configuração para PLC, SCADA e middleware.
>
>Eu não colocaria como MODELAGEM principal, porque aqui o ponto não é representar a planta em si, mas o pipeline de geração model-driven que transforma modelo em software operacional.
>%%TAGS%%
>#MECANISMO-SOFTWARE-POSITIVO
^l5d941d9boe


>%%
>```annotation-json
>{"text":"Os princípios do UNICOS sobreviveram a diferentes SCADAs e ambientes PLC, então a abstração não ficou presa a uma tecnologia específica.\n\nPorque o insight mostra que a abstração do UNICOS funciona como mecanismo de portabilidade/interoperabilidade: o modelo sobrevive a diferentes SCADAs e ambientes PLC.\n\nEu não colocaria como SOFTWARE, porque o ponto principal não é o código em si, mas a independência entre modelo de controle e plataforma/fabricante.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":19104,"end":19329},{"type":"TextQuoteSelector","exact":"Since  its  first  application  commissioned  in  July  2001,  UNICOS  principles  have  prove  to  be  independent of their platform. They have been ported in two successive SCADA and in several PLC programming environments.","prefix":"th  types of PLCs.  CONCLUSION","suffix":"UNICOS  has  been  used  to  p"}]}],"created":"2026-06-08T15:53:13.203Z","updated":"2026-06-08T15:53:13.203Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%th  types of PLCs.  CONCLUSION%%HIGHLIGHT%% ==Since  its  first  application  commissioned  in  July  2001,  UNICOS  principles  have  prove  to  be  independent of their platform. They have been ported in two successive SCADA and in several PLC programming environments.== %%POSTFIX%%UNICOS  has  been  used  to  p*
>%%LINK%%[[#^7us7x8xs8uw|show annotation]]
>%%COMMENT%%
>Os princípios do UNICOS sobreviveram a diferentes SCADAs e ambientes PLC, então a abstração não ficou presa a uma tecnologia específica.
>
>Porque o insight mostra que a abstração do UNICOS funciona como mecanismo de portabilidade/interoperabilidade: o modelo sobrevive a diferentes SCADAs e ambientes PLC.
>
>Eu não colocaria como SOFTWARE, porque o ponto principal não é o código em si, mas a independência entre modelo de controle e plataforma/fabricante.
>%%TAGS%%
>#MECANISMO-INTEGRACAO_INDUSTRIAL-POSITIVO
^7us7x8xs8uw


>%%
>```annotation-json
>{"text":"Comparado a programação PLC tradicional, consome mais memória e CPU; por isso não serve para controle muito crítico em tempo, abaixo de 10 ms.\n\nPorque há uma troca clara: ganha-se abstração, padronização e geração estruturada, mas perde-se eficiência de execução para controle muito rápido/crítico.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":19774,"end":19974},{"type":"TextQuoteSelector","exact":"UNICOS  has  some  limitations,  compared  to  usual  PLC  programming;  it  implies  extra  memory  usage and additional CPU load. Hence this method is not suitable for time critical process (<10ms).","prefix":"ny  (Accelerator  cryogenic).","suffix":"UNICOS-based  applications  p"}]}],"created":"2026-06-08T15:55:34.679Z","updated":"2026-06-08T15:55:34.679Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%ny  (Accelerator  cryogenic).%%HIGHLIGHT%% ==UNICOS  has  some  limitations,  compared  to  usual  PLC  programming;  it  implies  extra  memory  usage and additional CPU load. Hence this method is not suitable for time critical process (<10ms).== %%POSTFIX%%UNICOS-based  applications  p*
>%%LINK%%[[#^eotr9swkd6f|show annotation]]
>%%COMMENT%%
>Comparado a programação PLC tradicional, consome mais memória e CPU; por isso não serve para controle muito crítico em tempo, abaixo de 10 ms.
>
>Porque há uma troca clara: ganha-se abstração, padronização e geração estruturada, mas perde-se eficiência de execução para controle muito rápido/crítico.
>%%TAGS%%
>#TRADEOFF-SOFTWARE-NEGATIVO
^eotr9swkd6f


>%%
>```annotation-json
>{"text":"Operadores interagem com objetos padronizados, o que melhora troubleshooting, testes, resposta a falhas e disponibilidade.\n\nPorque explica como a padronização dos objetos melhora operação, troubleshooting, testes e resposta a falhas: o operador interage com objetos coerentes, não com lógica dispersa.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":20062,"end":20283},{"type":"TextQuoteSelector","exact":"Operators  can  interact  with  the  any  application  objects  through  a  standardized  interface.  This  possibility  offers  flexible  troubleshooting  facilities  during  tests  or  in  case  of  equipment  failure. ","prefix":"icient  tools  for  operators.","suffix":"It  also  increases  availabili"}]}],"created":"2026-06-08T15:57:13.912Z","updated":"2026-06-08T15:57:13.912Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%icient  tools  for  operators.%%HIGHLIGHT%% ==Operators  can  interact  with  the  any  application  objects  through  a  standardized  interface.  This  possibility  offers  flexible  troubleshooting  facilities  during  tests  or  in  case  of  equipment  failure.== %%POSTFIX%%It  also  increases  availabili*
>%%LINK%%[[#^taduh53pcl|show annotation]]
>%%COMMENT%%
>Operadores interagem com objetos padronizados, o que melhora troubleshooting, testes, resposta a falhas e disponibilidade.
>
>Porque explica como a padronização dos objetos melhora operação, troubleshooting, testes e resposta a falhas: o operador interage com objetos coerentes, não com lógica dispersa.
>%%TAGS%%
>#MECANISMO-SUPERVISAO-POSITIVO
^taduh53pcl


>%%
>```annotation-json
>{"text":"Guidelines rígidos reduzem liberdade do programador, mas tornam o código homogêneo e mantível por qualquer membro da equipe.\n\nPorque há perda de liberdade individual do programador, mas ganho em homogeneidade, transferibilidade e manutenção por qualquer membro da equipe.","target":[{"source":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf","selector":[{"type":"TextPositionSelector","start":20394,"end":20570},{"type":"TextQuoteSelector","exact":"the  easy  and  efficient  creation  and  modification  of  process  views  does  not  involve  programming knowledge, it can then easily be transferred to the operation crew. ","prefix":"n hardware failure.   Moreover","suffix":"The UNICOS concepts are complex"}]}],"created":"2026-06-08T15:58:00.402Z","updated":"2026-06-08T15:58:00.402Z","document":{"title":"UNICOS a Framework to Build Industry Like Control Systems Principles Methodology","link":[{"href":"urn:x-pdf:631ebd84de6a45cb30dd815f5f2564af00"},{"href":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}],"documentFingerprint":"631ebd84de6a45cb30dd815f5f2564af00"},"uri":"vault:/notes/articles/art6_UNICOS-A-Framework-to-Build-Industry-Like-Control-Systems_Gayet_Barillere.pdf"}
>```
>%%
>*%%PREFIX%%n hardware failure.   Moreover%%HIGHLIGHT%% ==the  easy  and  efficient  creation  and  modification  of  process  views  does  not  involve  programming knowledge, it can then easily be transferred to the operation crew.== %%POSTFIX%%The UNICOS concepts are complex*
>%%LINK%%[[#^gyecal1zim|show annotation]]
>%%COMMENT%%
>Guidelines rígidos reduzem liberdade do programador, mas tornam o código homogêneo e mantível por qualquer membro da equipe.
>
>Porque há perda de liberdade individual do programador, mas ganho em homogeneidade, transferibilidade e manutenção por qualquer membro da equipe.
>%%TAGS%%
>#TRADEOFF-SOFTWARE-POSITIVO
^gyecal1zim
