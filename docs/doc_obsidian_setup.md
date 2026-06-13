---
type: doc-projeto
componente: Obsidian Setup
assunto: Configuração de plugins e infraestrutura do Obsidian para o projeto
status: ativo
relates-to: []
tags: []
data: 2026-06-12
---

# Infraestrutura Obsidian — Setup e Plugins

## Plugins do Obsidian — O que instalar

Vá em: `Configurações → Plugins da comunidade → Procurar`

| Plugin       | Para quê                                                 | Obrigatório? |
| ------------ | -------------------------------------------------------- | ------------ |
| **Dataview** | Cria tabelas automáticas a partir dos campos frontmatter | Sim          |
| **Annotator**| Lê PDFs com highlight e salva anotações como Markdown    | Sim          |
| **Calendar** | Navegação por data em notas diárias                      | Opcional     |

---

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
3. Para cada nó que merece existir: crie a nota `nt_` (novo arquivo em `referencial/notes/`)
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

## Estrutura do vault

Todos os arquivos ficam em `referencial/`:

```
referencial/
├── .obsidian/      # configuração interna do Obsidian
├── articles/       # PDFs de artigos
├── books/          # PDFs de livros
├── notes/          # todas as notas (ft_, nt_, doc_, bs_)
└── standard/       # PDFs de normas
```

Não há templates — as notas são criadas manualmente seguindo as convenções documentadas no README.
