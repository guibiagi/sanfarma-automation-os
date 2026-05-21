# Contribuindo — Sanfarma Automation OS

## Para Desenvolvedores Futuros

Este ecossistema foi projetado para ser **mantido sem depender 100% da memória do autor original.**

Se você está assumindo a manutenção destes sistemas:

1. **Leia primeiro** — Comece por este repositório (`sanfarma-automation-os`), depois pelo README do projeto específico.
2. **Siga o fluxo** — Todo projeto tem um `README.md` com setup, uso e arquitetura.
3. **Audite segurança** — Leia `SECURITY.md` antes de commitar qualquer coisa.
4. **Não quebre o que funciona** — Altere lógica de negócio crítica somente com plano documentado.

## Padrões de Código

- **Linguagem:** Python 3.11+ para novos projetos
- **Formatação:** Black (line-length 100)
- **Lint:** Ruff
- **Tipagem:** Type hints obrigatórios em funções públicas
- **Commits:** [Conventional Commits](https://www.conventionalcommits.org/) — `feat:`, `fix:`, `chore:`, `docs:`, `test:`

## Fluxo de Trabalho

1. **Issue primeiro** — Descreva o problema ou feature
2. **Branch:** `feat/descricao` ou `fix/descricao`
3. **PR:** Pequeno, focado, com descrição clara
4. **Review:** CI passa → merge com squash

## Templates

Use os templates em `templates/` para criar novos projetos ou padronizar existentes:

- `templates/README.template.md` — Estrutura padrão de README
- `templates/SECURITY.template.md` — Template de política de segurança
- `templates/gitignore.template` — `.gitignore` base para Python
- `templates/env.example.template` — Template de variáveis de ambiente

## Dúvidas?

Consulte o [PROJECT_REGISTRY.md](PROJECT_REGISTRY.md) para o catálogo completo de projetos e seus responsáveis.
