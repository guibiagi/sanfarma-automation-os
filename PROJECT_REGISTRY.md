# Project Registry — Sanfarma Automation OS

Catálogo completo de todos os sistemas de automação, dados e inteligência operacional.

**Convenções:**
- 🟢 Produção | 🟡 Desenvolvimento ativo | 🚧 Protótipo | ⏳ Planejado | 🔒 Arquivado
- 🅿️ Portfólio público | 🔐 Operacional privado

---

## 1. frete-portal

| Campo | Valor |
|---|---|
| **Repositório** | [guibiagi/frete-portal](https://github.com/guibiagi/frete-portal) |
| **Visibilidade** | 🔐 Privado |
| **Status** | 🟢 Produção |
| **Propósito** | Portal de acompanhamento de frete em tempo real para logística. Substitui planilha Google Sheets por tracking automatizado com transportadoras. |
| **Stack** | FastAPI · SQLAlchemy · PostgreSQL · Jinja2 · HTMX · Tailwind CSS · Docker · Caddy |
| **URL produção** | `https://frete.sanfarma.com.br` |
| **Maturidade** | MÉDIA-ALTA |
| **README** | ✅ Completo (408 linhas) |
| **docs/** | ✅ Sim |
| **tests/** | ❌ Ausente |
| **CI** | ✅ GitHub Actions |
| **Docker** | ✅ docker-compose |
| **Dados reais** | ⚠️ Banco PostgreSQL com dados de produção |
| **Pendências** | Testes unitários/integração; pyproject.toml; requisitos explícitos |

---

## 2. sanfarma-conciliacao

| Campo | Valor |
|---|---|
| **Repositório** | [guibiagi/sanfarma-conciliacao](https://github.com/guibiagi/sanfarma-conciliacao) |
| **Visibilidade** | 🔐 Privado |
| **Status** | 🟢 Produção |
| **Propósito** | Pipeline automatizado de conciliação bancária multi-banco (BB, Itaú, Bradesco). Extrai extratos, classifica por regras + ERP + LLM, detecta anomalias e gera relatório consolidado XLSX. |
| **Stack** | Python 3.12 · PostgreSQL (ERP) · Docker · mTLS/OAuth 2.0 · OpenRouter/DeepSeek |
| **Maturidade** | ALTA |
| **README** | ✅ Excelente (648 linhas, diagrama ASCII, glossário) |
| **docs/** | ❌ Ausente |
| **tests/** | ❌ Ausente |
| **CI** | ✅ GitHub Actions |
| **Docker** | ✅ Dockerfile + docker-compose |
| **Dados reais** | ⚠️ Extratos bancários em `data/` (não versionado) |
| **Pendências** | Criar `docs/`; testes unitários para pipeline financeiro crítico |

---

## 3. fluxo-caixa-automatizado

| Campo | Valor |
|---|---|
| **Repositório** | [guibiagi/fluxo-caixa-automatizado](https://github.com/guibiagi/fluxo-caixa-automatizado) |
| **Visibilidade** | 🔐 Privado |
| **Status** | 🟢 Produção |
| **Propósito** | Ferramenta local que gera fluxo de caixa projetado a 90 dias do PostgreSQL (DB_SANFARMA), com dashboard web FastAPI e scrapers para portais Raia Drogasil e DPSP. |
| **Stack** | Python 3.11 · FastAPI · PostgreSQL · Playwright · Jinja2 · Chart.js |
| **Maturidade** | ALTA |
| **README** | ✅ Excelente (164 linhas, CI badge, roadmap) |
| **docs/** | ✅ Sim (db.md) |
| **tests/** | ✅ 37 testes |
| **CI** | ✅ GitHub Actions |
| **Docker** | ⚠️ docker-compose sem Dockerfile |
| **Dados reais** | ⚠️ Banco ERP e outputs XLSX locais (não versionados) |
| **Pendências** | Criar Dockerfile; decidir se extrai dashboard para repo próprio |

---

## 4. sanfarma-inteligencia-comercial

| Campo | Valor |
|---|---|
| **Repositório** | [guibiagi/sanfarma-inteligencia-comercial](https://github.com/guibiagi/sanfarma-inteligencia-comercial) |
| **Visibilidade** | 🔐 Privado |
| **Status** | 🟢 Produção |
| **Propósito** | Sistema de detecção de dormancy, recomendação de produtos, similaridade entre clientes, roteiro de visita via LLM e distribuição de ações comerciais via Excel por representante. |
| **Stack** | Python 3.12 · PostgreSQL · pandas · openpyxl · scikit-learn · OpenRouter/DeepSeek |
| **Maturidade** | MÉDIA |
| **README** | ✅ Bom (727 linhas) |
| **docs/** | ❌ Ausente (tem SPEC.md e PLANO_EVOLUCAO.md soltos) |
| **tests/** | ✅ 10 arquivos |
| **CI** | ❌ Ausente |
| **Docker** | ❌ Ausente |
| **Dados reais** | ⚠️ Conexão direta ao ERP (config não versionada) |
| **Pendências** | Docker; CI; migrar SPEC/PLANO para docs/ |

---

## 5. fpa-open-toolkit

| Campo | Valor |
|---|---|
| **Repositório** | [guibiagi/fpa-open-toolkit](https://github.com/guibiagi/fpa-open-toolkit) |
| **Visibilidade** | 🅿️ Público |
| **Status** | 🅿️ Portfólio / Open Source |
| **Propósito** | FP&A Open Toolkit — análise financeira open source para PMEs industriais. Ferramentas reutilizáveis de planejamento financeiro. |
| **Stack** | Python 3.11 · pandas · openpyxl · Streamlit · pytest |
| **Maturidade** | MÉDIA |
| **README** | ✅ Bom (169 linhas) |
| **docs/** | ✅ Sim |
| **tests/** | ✅ 7 arquivos |
| **CI** | ❌ Ausente |
| **LICENSE** | ✅ MIT |
| **Makefile** | ✅ Sim |
| **Dados reais** | ✅ Dados sintéticos (público) |
| **Pendências** | CI público; `.env.example` (✅ feito); confirmar dados 100% sintéticos |

---

## 6. ml-automations

| Campo | Valor |
|---|---|
| **Repositório** | [guibiagi/ml-automations](https://github.com/guibiagi/ml-automations) |
| **Visibilidade** | 🔐 Privado |
| **Status** | 🚧 Protótipo / Início |
| **Propósito** | Automações para Mercado Livre: visibilidade de anúncios, gestão de catálogo, precificação, reputação. Ecommerce segregado (CNPJ próprio Sanfarma). |
| **Stack** | Python · Mercado Livre API |
| **Maturidade** | BAIXA |
| **README** | ✅ Básico (105 linhas, roadmap inicial) |
| **docs/** | ❌ Ausente |
| **tests/** | ❌ Ausente |
| **CI** | ❌ Ausente |
| **Docker** | ❌ Ausente |
| **Pendências** | Implementar automações do roadmap; Docker; CI; testes |

---

## 7. returns-portal ⏳

| Campo | Valor |
|---|---|
| **Repositório** | *(não criado)* |
| **Visibilidade** | 🔐 Privado (planejado) |
| **Status** | ⏳ Planejado |
| **Propósito** | Portal B2B de devoluções — FastAPI + PostgreSQL + HTMX. Interface para clientes B2B gerenciarem processos de devolução. |
| **Stack** | FastAPI · PostgreSQL · HTMX (planejado) |
| **Pendências** | Criar repositório; definir escopo inicial |

---

## 8. cortex-pme ⏳

| Campo | Valor |
|---|---|
| **Repositório** | *(não criado)* |
| **Visibilidade** | 🅿️ Público (planejado) |
| **Status** | ⏳ Planejado |
| **Propósito** | Decision Layer para CEO/dono de PME, com briefing diário, fila de aprovação universal e visão consolidada de operações. |
| **Stack** | TBD |
| **Pendências** | Criar repositório; arquitetura inicial |

---

## 9. dashboard-producao-sanfarma ⏳

| Campo | Valor |
|---|---|
| **Repositório** | *(não criado)* |
| **Visibilidade** | 🔐 Privado (planejado) |
| **Status** | ⏳ Planejado |
| **Propósito** | Dashboard de produção da Sanfarma. Atualmente existe como submódulo dentro de `fluxo-caixa-automatizado/dashboard/`. |
| **Stack** | FastAPI · Jinja2 · Chart.js (a definir) |
| **Pendências** | Extrair do fluxo-caixa; criar repositório independente |

---

## Resumo de maturidade

| Projeto | README | Docs | Tests | CI | Docker | Maturidade |
|---|---|---|---|---|---|---|
| frete-portal | ✅ | ✅ | ❌ | ✅ | ✅ | MÉDIA-ALTA |
| sanfarma-conciliacao | ✅ | ❌ | ❌ | ✅ | ✅ | ALTA |
| fluxo-caixa | ✅ | ✅ | ✅ | ✅ | ⚠️ | ALTA |
| inteligencia-comercial | ✅ | ❌ | ✅ | ❌ | ❌ | MÉDIA |
| fpa-open-toolkit | ✅ | ✅ | ✅ | ❌ | ⚠️ | MÉDIA |
| ml-automations | ✅ | ❌ | ❌ | ❌ | ❌ | BAIXA |

---

*Última atualização: 2026-05-21 — Fase 1 do plano de reorganização GitHub*
