---
type: doc
componente: latex
assunto: setup e estrutura da monografia
status: atualizado
relates-to: []
tags: []
data: 2026-06-06
---

# doc_setup-latex-monografia

## Contexto
Registro do ambiente de escrita da monografia — o que foi instalado, como o projeto está organizado e como compilar.

## Instalação do ambiente LaTeX

1. **LaTeX Workshop** — extensão do VS Code (editor + compilador integrado)
2. **MiKTeX** — distribuição LaTeX para Windows (instala pacotes sob demanda)
3. **Perl** — obrigatório para scripts internos do LaTeX Workshop
   - Depois de instalar, adicionar o binário do Perl ao `PATH` nas variáveis de ambiente do sistema
   - Sem isso, a compilação falha silenciosamente em certas etapas

**Compilar:** `Ctrl+Alt+B` no VS Code

## Estrutura do projeto

```
Monografia/
├── main.tex              ← entry point LaTeX (nunca mover daqui)
├── ifes8.cls             ← classe da IFES (precisa ficar junto ao main.tex)
├── references.bib        ← bibliografia
├── latex/
│   ├── trabalho/         ← capítulos .tex (Cap0 a Cap5)
│   └── pdf/              ← PDFs incluídos (folha, aprovacao)
└── referencial/          ← vault Obsidian (notas + PDFs + config)
    ├── .obsidian/
    ├── articles/
    ├── books/
    ├── notes/
    └── standard/
```

## Capítulos

| Arquivo | Capítulo | Status |
|---------|----------|--------|
| `Cap0-resumo.tex` | Resumo (PT) | escrito |
| `Cap0-abstract.tex` | Abstract (EN) | escrito |
| `Cap1-introducao.tex` | Introdução | escrito — revisar |
| `Cap2-referencialteorico.tex` | Referencial Teórico | escrito — lapidar |
| `Cap3-desenvolvimento.tex` | Desenvolvimento | escrito — lapidar |
| `Cap4-resultados.tex` | Resultados | escrito — lapidar |
| `Cap5-conclusao.tex` | Conclusão | escrito — lapidar |

Para ativar um capítulo comentado no `main.tex`: remover o `%` antes do `\include{}` correspondente.

## Decisões tomadas

| Decisão | Alternativa descartada | Motivo |
|---------|------------------------|--------|
| Capítulos em `latex/trabalho/` | raiz do projeto | separar LaTeX de notas Obsidian |
| `ifes8.cls` na raiz | dentro de `latex/` | LaTeX exige classe no mesmo diretório do `main.tex` |
| `main.pdf` no `.gitignore` | versionar o PDF | evita conflito de merge a cada compilação |

## Problemas em aberto / Próximos passos

- [ ] Arquivo `nota_setup_monografia.md` está desatualizado — este o substitui

## Referências internas

- [[]]
