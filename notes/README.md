# Protocolo de Notas — Monografia TEP

## Plugins do Obsidian — O que instalar

Vá em: `Configurações → Plugins da comunidade → Procurar`

| Plugin        | Para quê                                                 | Obrigatório? |
| ------------- | -------------------------------------------------------- | ------------ |
| **Templater** | Insere templates com data automática e prompts           | Sim          |
| **Dataview**  | Cria tabelas automáticas a partir dos campos frontmatter | Sim          |
| **Annotator** | Lê PDFs com highlight e salva anotações como Markdown    | Sim          |
| **Calendar**  | Navegação por data em notas diárias                      | Opcional     |

Após instalar o Templater:
`Configurações → Templater → Template folder location → .obsidian/templates`


## Como usar o Annotator

O **Annotator** é um leitor de PDF dentro do Obsidian que vincula highlights a notas Markdown.

### Abrir um PDF com o Annotator
A nota de resumo tem o campo `annotation-target` no frontmatter. Quando preenchido, a nota abre automaticamente como leitor de PDF.

### Fazer um highlight
1. Selecione o texto no PDF
2. Clique no botão **"** (aspas) que aparece
3. Escolha a cor do highlight (amarelo, vermelho, verde, azul)
4. Adicione um comentário — **é aqui que as conexões são criadas** (ver abaixo)
5. O highlight fica salvo automaticamente na nota

### Sistemática de comentário nos highlights

O comentário do highlight **é indexado pelo Obsidian** — wikilinks e tags escritos ali aparecem no Graph View. Use isso para criar conexões durante a leitura, sem sair do PDF.

**No campo de comentário escreva:**

```
[[nt_nome-do-conceito]]  #tag-existente
```

**Regras:**
- `[[nt_nome]]` — use mesmo que a nota `nt_` ainda não exista; ela aparece como nó órfão no grafo e você preenche depois
- `#tag` — use **apenas tags já existentes** nos frontmatter das `ft_`; não invente tags novas durante a leitura
- Você pode combinar: `[[nt_three-layer-control]] #cern #controle-industrial`

**Após a leitura (5 min):**
1. Abra `Ctrl+G` (Graph View)
2. Identifique os nós órfãos (cinza, sem arestas) criados pelos seus links `[[nt_]]`
3. Para cada nó que merece existir: crie a nota `nt_` via `Alt+N → nt.md`
4. Para os que eram só marcadores descartáveis: ignore — ficam no grafo mas não atrapalham

### Alternar entre PDF e Markdown
- **Ver o PDF:** a nota abre no modo Annotator por padrão
- **Ver o Markdown:** clique nos `...` (três pontos) no canto superior direito → **Open as Markdown**
- Os highlights ficam registrados no Markdown como blocos com o trecho destacado e um link de volta à posição no PDF

### Cores sugeridas
| Cor      | Uso                                           |
| -------- | --------------------------------------------- |
| Amarelo  | Informação geral importante                   |
| Vermelho | Contradiz algo que eu pensava / ponto crítico |
| Verde    | Diretamente usável na monografia              |
| Azul     | Referência a citar                            |

## Protocolo desse projeto

**Tipo** da Tag

| Tipo      | Quando usar                                                                |
| --------- | -------------------------------------------------------------------------- |
| TRADEOFF  | Quando melhorar X implica piorar Y — há tensão entre dois objetivos        |
| LIMITE    | Quando existe um teto ou piso teórico que nenhuma solução consegue superar |
| PARADOXO  | Quando o resultado contraria a intuição — o esperado não acontece          |
| REQUISITO | Quando algo é condição necessária para outra coisa funcionar               |
| MECANISMO | Quando o insight explica *por que* algo acontece — a causa, não o efeito   |
| METRICA   | Quando o insight define uma forma de medir, avaliar ou comparar algo       |

---

**Tema** da Tag

| Tema                  | Quando usar                                                              |
| --------------------- | ------------------------------------------------------------------------ |
| CONTROLE_AUTOMATICO   | Malhas PID, sintonia, resposta a distúrbios, estabilidade                |
| SISTEMAS_DINAMICOS    | Modelagem matemática, equações diferenciais, análise de comportamento    |
| SUPERVISAO            | Camada acima dos loops — decisão, coordenação, metacontrole              |
| DIAGNOSTICO           | Detecção de falhas, sensores ruins, malhas degradadas                    |
| INSTRUMENTACAO        | Sensores, atuadores, condicionamento de sinal, leitura de dados          |
| INTEGRACAO_INDUSTRIAL | Integração de sistemas de controle, interoperabilidade entre componentes |
| COMUNICACAO           | Protocolos, latência, gRPC, OPC-UA, troca de dados                       |
| MODELAGEM             | Gêmeo digital, simulação, representação matemática da planta             |
| CALCULO_NUMERICO      | Métodos numéricos, soluções iterativas, precisão e estabilidade          |
| SOFTWARE              | Padrões de código, arquitetura, implementação, frameworks, tooling       |
| BENCHMARKING          | Índices de desempenho, limites teóricos, comparação entre soluções       |

---

**Polaridade** da Tag

| Polaridade | Quando usar                                                           |
| ---------- | --------------------------------------------------------------------- |
| POSITIVO   | O insight reforça ou justifica uma decisão do seu projeto             |
| NEGATIVO   | O insight contradiz, limita ou critica uma decisão do seu projeto     |
| NEUTRO     | O insight é relevante mas não tem posição clara em relação ao projeto |

---

**Regras**

- Tipo fechado — se não encaixa, o insight não é atômico. Quebre em dois.
- Tema semi-aberto — novo tema só com justificativa registrada aqui no README.
- Código final: `TIPO-TEMA-POLARIDADE` → ex: `TRADEOFF-CONTROLE-PROCESSOS-NEGATIVO`


## Os quatro tipos de nota

### 1. Nota de fonte (`ft`)
**Quando usar:** Sempre que estiver lendo ou for ler um artigo, livro, seção de norma ou qualquer conteúdo externo. Vincula o PDF via Annotator.

**Como invocar o template:**
`Ctrl+P → Templater: Create new note from template → ft.md`

**Convenção de nome do arquivo:** `ft_<autor>_<ano>.md`
Exemplo: `ft_downs_1993.md`

---

### 2. Nota atômica de conceito (`nt`)
**Quando usar:** Quando você aprende um conceito novo — uma ideia, um método, uma definição. Uma nota por conceito. É isso que alimenta o Graph View (`Ctrl+G`).

**Como invocar o template:**
`Ctrl+P → Templater: Create new note from template → nt.md`

**Convenção de nome do arquivo:** `nt_<conceito>.md`
Exemplo: `nt_harris-index.md`, `nt_predictability-index.md`, `nt_controle-discreto.md`

**Protocolo de escrita:**
1. Preencha `conceito` com o nome do conceito em uma ou duas palavras
2. Preencha `origem` com a nota `ft_` de onde veio (ex: `[[ft_harris_1989]]`)
3. Preencha `conecta-com` com outros conceitos relacionados — mesmo sem saber ainda como
4. Escreva em `## O que é` apenas uma frase direta
5. Escreva em `## Como se conecta ao projeto` onde isso aparece no TCC

**Protocolo de escrita:**
1. Preencha o frontmatter (autor, ano, tema, conecta-com)
2. Preencha `annotation-target` com o caminho relativo do PDF — ex: `notes/articles/art2_....pdf`
3. Salve — a nota vira leitor de PDF com o Annotator
4. Leia o PDF, faça highlights e comentários diretamente nele
5. Para escrever o resumo em texto: clique nos `...` no canto superior direito → **Open as Markdown**
6. Escreva em `## O que diz` só o que o texto diz — sem opinião
7. Escreva em `## O que me interessa` só o que é relevante para o TCC
8. Escreva em `## Conexões` links `[[nota]]` para outros resumos ou docs do projeto
9. Se surgir uma ideia nova, **não escreva aqui** — crie um brainstorming separado e linke

---
[]()
### 3. Documentação do Projeto (`doc-projeto`)
**Quando usar:** Para registrar decisões de arquitetura, descrições de componentes, resultados de experimentos, problemas resolvidos.

**Como invocar o template:**
`Ctrl+P → Templater: Create new note from template → doc.md`

**Convenção de nome do arquivo:** `doc_<componente>_<assunto>.md`
Exemplo: `doc_tep-plant_controllerbank.md`

**Protocolo de escrita:**
1. Preencha o frontmatter (componente, status, relates-to)
2. Seja objetivo — este é um registro técnico, não um diário
3. Sempre termine com `## Próximos passos` ou `## Problemas em aberto`
4. Se virar brainstorming, crie uma nota separada e linke

---

### 4. Brainstorming (`brainstorming`)
**Quando usar:** Quando uma ideia surge e você não sabe ainda onde ela se encaixa. Para conexões entre conceitos. Para perguntas em aberto.

**Como invocar o template:**
`Ctrl+P → Templater: Create new note from template → br.md`

**Convenção de nome do arquivo:** `bs_<tema>_<data>.md`
Exemplo: `bs_opcua_supervisor_20260606.md`

**Protocolo de escrita:**
1. Escreva sem filtro em `## Ideia bruta`
2. Depois tente responder: "Isso vai para qual capítulo da monografia?"
3. Se souber, linke o canvas da monografia e o capítulo correspondente
4. Se não souber ainda, deixe em `status: incubando`

---

## Convenção de cores no Canvas

| Cor      | Significado                                 |
| -------- | ------------------------------------------- |
| Verde    | Conteúdo já incorporado à monografia        |
| Amarelo  | Ideia em desenvolvimento / incubando        |
| Vermelho | Problema em aberto / blocker                |
| Roxo     | Referência externa (artigo, livro, norma)   |
| Sem cor  | Nó estrutural (capítulo, seção, componente) |

---

## Ritual semanal (15 min)
1. Abra o canvas `mapa_mental.canvas`
2. Para cada nota de resumo criada na semana: existe um nó no canvas que se beneficia dela? Se sim, puxe uma seta e anote a conexão
3. Para cada brainstorming com `status: incubando`: já tem destino? Mova para o canvas correto ou descarte
4. Atualize as cores dos nós do canvas conforme o estado atual

---

## Onde ficam os templates

`C:\Projetos\tep\Monografia\notes\templates\`

| Template                  | Prefixo | Tipo de nota                       |
| ------------------------- | ------- | ---------------------------------- |
| [[templates/ft\|ft.md]]   | `ft_`   | Nota de fonte (artigo/livro + PDF) |
| [[templates/nt\|nt.md]]   | `nt_`   | Nota atômica de conceito           |
| [[templates/doc\|doc.md]] | `doc_`  | Documentação do projeto            |
| [[templates/br\|br.md]]   | `bs_`   | Brainstorming                      |
