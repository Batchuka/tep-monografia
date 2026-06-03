# Setup da Monografia

## Extensão LaTeX no VS Code

1. Instalar a extensão **LaTeX Workshop** no VS Code
2. Instalar **MiKTeX** (distribuição LaTeX para Windows)
3. Instalar **Perl** — obrigatório para alguns scripts do LaTeX Workshop
   - Após instalar, adicionar o caminho do Perl às **variáveis de ambiente do sistema** (`PATH`)
   - Sem isso, a compilação falha silenciosamente em certas etapas

## Mapa mental (Obsidian Canvas)

- O vault do Obsidian é a pasta `C:\Projetos\tep\Monografia`
- O canvas fica em `docs/mapa_mental.canvas` — abre direto no Obsidian
- Para editar: duplo clique num nó para escrever, arrastar para mover, puxar a borda de um nó para criar uma seta

## Como escrever esta monografia

- O arquivo principal é `main.tex` — ele inclui os capítulos via `\include{trabalho/CapX-...}`
- Para ativar um capítulo comentado, remover o `%` na frente do `\include` correspondente
- Cada capítulo fica em `trabalho/CapX-nome.tex`
- **Cap 1** (Introdução) — já escrito, revisar
- **Cap 2** (Referencial Teórico) — reescrever com: TEP, IEC 61499, Kubernetes Operators, gRPC, RK4
- **Cap 3** (Desenvolvimento) — reescrever com o projeto TEP (tep-plant, tep-operator, tep-ihm, tep-supervisor)
- **Cap 4** (Resultados) — escrever a partir de `experiments.md` no repo `spec-tennessee-eastman`
- **Cap 5** (Conclusão) — escrever por último
- Para compilar: `Ctrl+Alt+B` no VS Code com o LaTeX Workshop
