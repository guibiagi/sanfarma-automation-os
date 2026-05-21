# Sanfarma Automation OS

> Infraestrutura como Código Organizacional — Central de governança, padrões e registro dos sistemas de automação da Sanfarma.

## O que é este repositório?

Este é o **centro de governança** de todos os sistemas de automação, dados e inteligência operacional da **Sanfarma Indústria e Comércio Ltda.** e projetos de portfólio público de **Guilherme Biagi** (CFO → CEO).

**Não contém código de aplicação.** Contém:

- 📋 **Registro de todos os projetos** (`PROJECT_REGISTRY.md`)
- 📐 **Templates padronizados** (`templates/`)
- 🔒 **Política de segurança** (`SECURITY.md`)
- 📖 **Guia de contribuição** (`CONTRIBUTING.md`)

## Princípios

1. **Documentação é código.** Todo projeto tem README, arquitetura e roadmap.
2. **Dados reais são confidenciais.** Nenhum dado da Sanfarma é commitado.
3. **Estrutura previsível.** Projetos seguem templates padronizados.
4. **Manutenível sem o autor original.** Clareza > complexidade.
5. **Segurança em camadas.** `.env` nunca versionado, `.gitignore` robusto, credenciais isoladas.

## Projetos do ecossistema

| # | Projeto | Tipo | Stack | Status |
|---|---------|------|-------|--------|
| 1 | [frete-portal](https://github.com/guibiagi/frete-portal) | Portal logístico | FastAPI, HTMX, Docker | 🟢 Produção |
| 2 | [sanfarma-conciliacao](https://github.com/guibiagi/sanfarma-conciliacao) | Pipeline bancário | Python, Docker, LLM | 🟢 Produção |
| 3 | [fluxo-caixa-automatizado](https://github.com/guibiagi/fluxo-caixa-automatizado) | FP&A | FastAPI, PostgreSQL | 🟢 Produção |
| 4 | [sanfarma-inteligencia-comercial](https://github.com/guibiagi/sanfarma-inteligencia-comercial) | Sales Intelligence | Python, pandas, LLM | 🟢 Produção |
| 5 | [fpa-open-toolkit](https://github.com/guibiagi/fpa-open-toolkit) | FP&A Open Source | Python, Streamlit | 🅿️ Portfólio |
| 6 | [ml-automations](https://github.com/guibiagi/ml-automations) | ML Automações | Python, Mercado Livre API | 🚧 Protótipo |
| 7 | returns-portal | Portal B2B Devoluções | FastAPI, PostgreSQL | ⏳ Planejado |
| 8 | cortex-pme | Decision Layer | TBD | ⏳ Planejado |
| 9 | dashboard-producao-sanfarma | Dashboard Produção | FastAPI, Chart.js | ⏳ Planejado |

Detalhes completos em [PROJECT_REGISTRY.md](PROJECT_REGISTRY.md).

## Como usar este repositório

### Para criar um novo projeto

```bash
# 1. Clone o template de README
cp templates/README.template.md ../novo-projeto/README.md

# 2. Copie .gitignore base
cp templates/gitignore.template ../novo-projeto/.gitignore

# 3. Crie .env.example
cp templates/env.example.template ../novo-projeto/.env.example

# 4. Atualize o PROJECT_REGISTRY.md
```

### Para auditar um projeto existente

Compare com os checklists em `templates/` e a política em `SECURITY.md`.

## Autor

**Guilherme Biagi** — CFO da Sanfarma (em transição para CEO)

- GitHub: [@guibiagi](https://github.com/guibiagi)
- Empresa: Sanfarma Indústria e Comércio Ltda.
- Localização: Americana, SP, Brasil

---

*Este repositório é público para servir como vitrine de governança de engenharia. Projetos operacionais da Sanfarma são privados.*
