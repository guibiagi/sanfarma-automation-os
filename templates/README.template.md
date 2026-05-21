# Nome do Projeto

> Uma frase descrevendo o propósito principal do projeto e que problema resolve.

**Status:** 🟢 Produção | 🚧 Protótipo | ⏳ Planejado  
**Tipo:** 🔐 Operacional privado Sanfarma | 🅿️ Portfólio público  
**Stack:** Python 3.x · Framework · Banco · Infra

---

## Índice

1. [Visão Geral](#visão-geral)
2. [Arquitetura](#arquitetura)
3. [Estrutura do Projeto](#estrutura-do-projeto)
4. [Setup](#setup)
5. [Uso](#uso)
6. [Configuração](#configuração)
7. [Roadmap](#roadmap)
8. [Segurança](#segurança)

---

## Visão Geral

Descreva o problema que o projeto resolve. Quem usa? Qual o fluxo principal?

### Funcionalidades principais

- ✨ Feature 1
- ✨ Feature 2
- ✨ Feature 3

---

## Arquitetura

```
┌──────────┐     ┌──────────┐     ┌──────────┐
│ Entrada  │────▶│ Processo │────▶│  Saída   │
└──────────┘     └──────────┘     └──────────┘
```

Descreva o fluxo de dados e componentes principais.

---

## Estrutura do Projeto

```
src/
  modulo_a/        # descrição
  modulo_b/        # descrição
data/              # dados (não versionado se real)
  snapshots/       # cache local
docs/              # documentação
  arquitetura.md
tests/             # pytest
```

---

## Setup

```bash
# 1. Clone
git clone https://github.com/guibiagi/nome-do-projeto.git
cd nome-do-projeto

# 2. Virtualenv
python -m venv .venv && source .venv/bin/activate

# 3. Dependências
pip install -r requirements.txt

# 4. Configurar
cp .env.example .env
# Editar .env com as variáveis necessárias
```

### Pré-requisitos

- Python 3.11+
- PostgreSQL 15 (opcional)
- Docker (opcional)

---

## Uso

```bash
source .venv/bin/activate
python main.py
```

### Testes

```bash
pytest -q
ruff check .
```

---

## Configuração

Variáveis de ambiente (ver `.env.example`):

| Variável | Descrição | Obrigatória |
|---|---|---|
| `DB_HOST` | Host do PostgreSQL | Sim |
| `DB_USER` | Usuário (somente leitura) | Sim |
| `TELEGRAM_BOT_TOKEN` | Token do bot Telegram | Não |

---

## Roadmap

- [ ] Milestone 1 — descrição (issues #X, #Y)
- [ ] Milestone 2 — descrição
- [ ] Milestone 3 — descrição

---

## Segurança

- 🔒 Dados reais da Sanfarma **nunca** são commitados
- 🔒 `.env` está no `.gitignore`
- 🔒 Credenciais injetadas via variáveis de ambiente
- Veja [SECURITY.md](SECURITY.md) para política completa

---

## Autor

**Guilherme Biagi** — CFO Sanfarma

- GitHub: [@guibiagi](https://github.com/guibiagi)
- Empresa: Sanfarma Indústria e Comércio Ltda.
