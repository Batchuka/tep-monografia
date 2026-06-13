# Monografia TEP — Protocolo de Notas e Referências

## Big Picture

![Big picture da monografia TEP](referencial/big_picture_tcc_tep.svg)

---

## Inventário de Referências

### Artigos

| Título                                                                                      | Autores                                                       | Ano  |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ---- |
| A plant-wide industrial process control problem                                             | Downs, J.J.; Vogel, E.F.                                      | 1993 |
| An Expert Knowledge Based Methodology for Online Detection of Signal Oscillations           | Tilaro, F.; Bradu, B.; Berges, A.; Roshchin, M.               | —    |
| Assessment of control loop performance                                                      | Burns, W.L.                                                   | 2016 |
| Automatic Assessment of PID Controllers Applied to the LHC Cryogenic System                 | Blanco Viñuela; Fernández Adiego; Gayet; Goddet               | 2013 |
| Borg, Omega, and Kubernetes                                                                 | Verma, A. et al. (Google)                                     | 2015 |
| Control structure design for complete chemical plants                                       | Skogestad, S.                                                 | —    |
| Model Learning Algorithms for Anomaly Detection in CERN Control Systems                     | Tilaro, F.; Bradu, B.; Berges, A.; Varela, C.; Roshchin, M.   | —    |
| Plantwide control — A review and a new design procedure                                     | Larsson; Skogestad                                            | —    |
| UNICOS — A Framework to Build Industry-Like Control Systems                                 | Gayet; Barilliere                                             | —    |
| Kubernetes Orchestration of High Availability Distributed Control Systems                   | Johansson, B.; Rågebrergi, M.; Nolte, T.; Papadopoulos, A. V. | —    |
| Design of an IoT-PLC - A containerized programmeble logical controller for the Industry 4.0 | Mellado, J.; Núñez, F.                                        | 2021 |

### Normas / Standards

| Título                                                               | Organização                                                      | Versão    |
| -------------------------------------------------------------------- | ---------------------------------------------------------------- | --------- |
| Batch process control — Part 1: Models and Terminology (IEC 61512-1) | International Electrotechnical Commission (IEC)                  | 2015      |
| Batch control (ISA-88 / S88) (IEC 61512)                             | International Electrotechnical Commission (IEC)                  | 1997–2017 |
| OPC Unified Architecture (OPC UA) (IEC 62541)                        | International Electrotechnical Commission (IEC) / OPC Foundation | 2009–2026 |

### Livros

| Título                                                                                    | Autores                                               | Ano  | Editora  |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------- | ---- | -------- |
| Mechatronic Futures: Challenges and Solutions for Mechatronic Systems and their Designers | Peter Hehenberger, David Bradley (Editors)            | 2016 | Springer |
| OPC Unified Architecture                                                                  | Wolfgang Mahnke, Stefan-Helmut Leitner, Matthias Damm | 2009 | Springer |

**Resumo**: 11 artigos + 3 normas + 2 livros = **16 fontes no total**

---

## Estrutura do referencial (`referencial/`)

Todos os arquivos do vault Obsidian — notas, artigos, livros, normas e o big picture — estão centralizados em `referencial/`. Não há subpastas espalhadas pelo repositório.

```
referencial/
├── .obsidian/          # configuração interna do Obsidian (plugins, graph, temas)
├── articles/           # PDFs de artigos vinculados via Annotator
├── books/              # PDFs de livros e normas
├── notes/              # todas as notas (ft_, nt_, doc_, bs_)
├── standard/           # PDFs de normas separados por clareza
└── big_picture_tcc_tep.svg
```

---

## O campo `tema` — classificação das fontes

Cada nota de fonte (`ft_`) carrega no frontmatter um campo `tema` que indica **onde aquela fonte se encaixa no argumento da monografia**. É a única classificação da fonte como um todo — não há mais tags de viés.

O campo segue o formato `<categoria>_<subcategoria>` quando há subcategoria, ou apenas `<categoria>` quando não há:

| Valor do `tema`        | Significado                                                                      |
| ---------------------- | -------------------------------------------------------------------------------- |
| `problema`             | Estabelece o problema de origem — por que supervisão industrial é necessária     |
| `politica_espirito`    | Fundamento teórico e conceitual da política de supervisão                        |
| `politica_tecnica`     | Derivado do espírito: abordagem aplicada, método, framework de decisão           |
| `runtime_espirito`     | Infraestrutura e plataforma — o que sustenta a execução do controle supervisório |
| `runtime_tecnica`      | Implementação concreta do runtime: orquestrador, operador, serviço               |
| `integracao_espirito`  | Comunicação, padrões e normas — o que conecta os componentes                     |
| `implementacao`        | O que foi construído neste projeto — o próprio digital twin TEP                  |

**Exemplo de frontmatter:**

```yaml
---
annotation-target: articles/art1_...pdf
titulo: A plant-wide industrial process control problem
autor: Downs, J.J.; Vogel, E.F.
ano: 1993
fonte: Computers & Chemical Engineering, v.17, n.3
tema: problema
---
```

---

## Graph View — Grupos por Tema

O grafo do Obsidian (`Ctrl+G`) exibe os nós agrupados e coloridos por valor do campo `tema`. As cores foram escolhidas para comunicar a posição de cada fonte no argumento:

| Grupo                 | Cor         | Motivação                                                          |
| --------------------- | ----------- | ------------------------------------------------------------------ |
| `problema`            | Vermelho    | Ponto de tensão — o que motiva tudo                                |
| `politica_espirito`   | Azul escuro | Fundamento teórico e conceitual                                    |
| `politica_tecnica`    | Azul claro  | Derivado do espírito, mais aplicado                                |
| `runtime_espirito`    | Verde escuro| Infraestrutura e plataforma                                        |
| `runtime_tecnica`     | Verde claro | Implementação concreta do runtime                                  |
| `integracao_espirito` | Roxo        | Comunicação, padrão, norma                                         |
| `implementacao`       | Laranja     | O que você construiu                                               |

Os grupos são configurados em **Settings → Graph view → Groups**, com filtros por propriedade `tema`.

---

## Protocolo de Tags — Classificação de Insights

Dentro das notas de fonte, highlights individuais podem receber tags no formato **TIPO-TEMA-POLARIDADE**. Essas tags vinculam fragmentos de conhecimento entre artigos diferentes — dois highlights de fontes distintas com a mesma tag formam uma aresta no grafo.

> Não descrevem a fonte como um todo (isso é papel do campo `tema`). Descrevem aquele fragmento específico.

### Tipo da Tag

| Tipo      | Quando usar                                                                |
| --------- | -------------------------------------------------------------------------- |
| TRADEOFF  | Quando melhorar X implica piorar Y — há tensão entre dois objetivos        |
| LIMITE    | Quando existe um teto ou piso teórico que nenhuma solução consegue superar |
| PARADOXO  | Quando o resultado contraria a intuição — o esperado não acontece          |
| REQUISITO | Quando algo é condição necessária para outra coisa funcionar               |
| MECANISMO | Quando o insight explica *por que* algo acontece — a causa, não o efeito   |
| METRICA   | Quando o insight define uma forma de medir, avaliar ou comparar algo       |

### Tema da Tag

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

### Polaridade da Tag

| Polaridade | Quando usar                                                           |
| ---------- | --------------------------------------------------------------------- |
| POSITIVO   | O insight reforça ou justifica uma decisão do seu projeto             |
| NEGATIVO   | O insight contradiz, limita ou critica uma decisão do seu projeto     |
| NEUTRO     | O insight é relevante mas não tem posição clara em relação ao projeto |

### Regras de Construção

- **Tipo fechado** — se não encaixa, o insight não é atômico. Quebre em dois.
- **Tema semi-aberto** — novo tema só com justificativa registrada aqui no README.
- **Código final**: `TIPO-TEMA-POLARIDADE` → ex: `TRADEOFF-CONTROLE_AUTOMATICO-NEGATIVO`

---

## Os Quatro Tipos de Nota

### 1. Nota de Fonte (`ft_`)

**Quando usar:** Sempre que estiver lendo um artigo, livro, seção de norma ou qualquer conteúdo externo. Vincula o PDF via Annotator.

**Convenção de nome:** `ft_<titulo-resumido>.md`
Exemplo: `ft_A-Plantwide-Industrial-Process-Control-Problem.md`

**Frontmatter obrigatório:**

```yaml
---
annotation-target: articles/<arquivo>.pdf
titulo: <título completo>
autor: <autores>
ano: <ano>
fonte: <periódico / editora / norma>
tema: <valor do tema>
---
```

---

### 2. Nota Atômica de Conceito (`nt_`)

**Quando usar:** Quando você aprende um conceito novo — uma ideia, um método, uma definição. Uma nota por conceito. É o que alimenta o Graph View (`Ctrl+G`).

**Convenção de nome:** `nt_<conceito>.md`
Exemplo: `nt_harris-index.md`, `nt_predictability-index.md`, `nt_controle-discreto.md`

**Protocolo de escrita:**
1. `conceito` — nome do conceito em uma ou duas palavras
2. `origem` — nota `ft_` de onde veio (ex: `[[ft_harris_1989]]`)
3. `conecta-com` — outros conceitos relacionados, mesmo sem saber como ainda
4. `## O que é` — apenas uma frase direta
5. `## Como se conecta ao projeto` — onde isso aparece no TCC

---

### 3. Documentação do Projeto (`doc_`)

**Quando usar:** Para registrar decisões de arquitetura, descrições de componentes, resultados de experimentos, problemas resolvidos.

**Convenção de nome:** `doc_<componente>_<assunto>.md`
Exemplo: `doc_tep-plant_controllerbank.md`

**Protocolo de escrita:**
1. Preencha o frontmatter (componente, relates-to)
2. Seja objetivo — este é um registro técnico, não um diário
3. Sempre termine com `## Próximos passos` ou `## Problemas em aberto`
4. Se virar brainstorming, crie uma nota separada e linke

---

### 4. Brainstorming (`bs_`)

**Quando usar:** Quando uma ideia surge e você não sabe ainda onde ela se encaixa. Para conexões entre conceitos. Para perguntas em aberto.

**Convenção de nome:** `bs_<tema>_<data>.md`
Exemplo: `bs_opcua_supervisor_20260606.md`

**Protocolo de escrita:**
1. Escreva sem filtro em `## Ideia bruta`
2. Depois tente responder: "Isso vai para qual capítulo da monografia?"
3. Se souber, linke o canvas da monografia e o capítulo correspondente
4. Se não souber ainda, deixe em `status: incubando`

---

## Infraestrutura Obsidian

Para instruções sobre setup de plugins, como usar o Annotator, e convenções do Obsidian, ver: **[`docs/doc_obsidian_setup.md`](docs/doc_obsidian_setup.md)**
