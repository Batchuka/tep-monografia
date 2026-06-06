# Protocolo de Notas — Monografia TEP

## O que instalar

### Plugins do Obsidian
Vá em: `Configurações → Plugins da comunidade → Procurar`

| Plugin        | Para quê                                                 | Obrigatório? |
| ------------- | -------------------------------------------------------- | ------------ |
| **Templater** | Insere templates com data automática e prompts           | Sim          |
| **Dataview**  | Cria tabelas automáticas a partir dos campos frontmatter | Sim          |
| **Calendar**  | Navegação por data em notas diárias                      | Opcional     |

Após instalar o Templater:
`Configurações → Templater → Template folder location → .obsidian/templates`

---

## Os três tipos de nota

### 1. Resumo (`resumo`)
**Quando usar:** Sempre que terminar de ler um artigo, livro, seção de norma ou qualquer conteúdo externo.

**Como invocar o template:**
`Ctrl+P → Templater: Create new note from template → resumo.md`

**Convenção de nome do arquivo:** `resumo_<autor>_<ano>.md`
Exemplo: `resumo_downs_1993.md`

**Protocolo de escrita:**
1. Preencha o frontmatter (autor, ano, tema, conecta-com)
2. Escreva em `## O que diz` só o que o texto diz — sem opinião
3. Escreva em `## O que me interessa` só o que é relevante para o TCC
4. Escreva em `## Conexões` links `[[nota]]` para outros resumos ou docs do projeto
5. Se surgir uma ideia nova, **não escreva aqui** — crie um brainstorming separado e linke

---

### 2. Documentação do Projeto (`doc-projeto`)
**Quando usar:** Para registrar decisões de arquitetura, descrições de componentes, resultados de experimentos, problemas resolvidos.

**Como invocar o template:**
`Ctrl+P → Templater: Create new note from template → doc-projeto.md`

**Convenção de nome do arquivo:** `doc_<componente>_<assunto>.md`
Exemplo: `doc_tep-plant_controllerbank.md`

**Protocolo de escrita:**
1. Preencha o frontmatter (componente, status, relates-to)
2. Seja objetivo — este é um registro técnico, não um diário
3. Sempre termine com `## Próximos passos` ou `## Problemas em aberto`
4. Se virar brainstorming, crie uma nota separada e linke

---

### 3. Brainstorming (`brainstorming`)
**Quando usar:** Quando uma ideia surge e você não sabe ainda onde ela se encaixa. Para conexões entre conceitos. Para perguntas em aberto.

**Como invocar o template:**
`Ctrl+P → Templater: Create new note from template → brainstorming.md`

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
`C:\Projetos\tep\Monografia\.obsidian\templates\`

| Arquivo            | Tipo de nota            |
| ------------------ | ----------------------- |
| `resumo.md`        | Resumo de leitura       |
| `doc-projeto.md`   | Documentação do projeto |
| `brainstorming.md` | Brainstorming           |
