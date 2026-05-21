# Política de Segurança — Sanfarma Automation OS

## Princípios Fundamentais

1. **Dados reais da Sanfarma jamais são commitados.** Nenhum dado de produção, extrato bancário, planilha financeira, dump de banco ou informação de clientes.
2. **Credenciais são injetadas em runtime.** Via variáveis de ambiente, nunca hardcoded.
3. **`.env` nunca é versionado.** Sempre coberto por `.gitignore`.
4. **Todo projeto tem `.env.example`** com placeholders, para orientar setup.
5. **Projetos públicos usam exclusivamente dados sintéticos.**

## Checklist de Segurança por Projeto

Ao criar ou auditar um repositório, verifique:

### 🔒 Commits
- [ ] `.env` está no `.gitignore`
- [ ] `.env.example` existe com placeholders
- [ ] Nenhum arquivo `.csv`, `.xlsx`, `.json` com dados reais está trackeado
- [ ] Nenhum token, chave API, senha está hardcoded no código fonte
- [ ] Histórico do git não contém dados sensíveis

### 🔒 Código
- [ ] Configurações de banco lidas de variáveis de ambiente (não hardcoded)
- [ ] Fallbacks em config usam placeholders, não valores reais
- [ ] Tokens de API nunca logados em produção
- [ ] `.env.example` reflete fielmente as variáveis necessárias

### 🔒 Infraestrutura
- [ ] Dockerfiles não expõem secrets em ARG/ENV
- [ ] GitHub Actions secrets usados para tokens, não hardcoded
- [ ] `.dockerignore` exclui `.env`, `data/`, backups

## Como Reportar Vulnerabilidades

**NÃO crie issues públicas** para vulnerabilidades de segurança.

Entre em contato diretamente:
- **Email:** guilherme@sanfarma.com.br
- **Telegram:** DM para @guibiagi

## Dados Sensíveis — O que NUNCA commitar

| Tipo | Exemplos |
|---|---|
| Credenciais | Senhas, API keys, tokens OAuth, certificados mTLS |
| Dados financeiros | Extratos bancários, fluxo de caixa, conciliações |
| Dados de clientes | CNPJ, razão social, histórico de compras, contratos |
| Dados internos | Planilhas de preços, margens, comissões, estoque |
| Infraestrutura | IPs internos, topologia de rede, chaves SSH |

## Resposta a Incidentes

Se dados sensíveis forem detectados em um repositório:

1. **Imediatamente:** Tornar o repo privado (se público)
2. **Rotacionar:** Invalidar todas as credenciais expostas
3. **Remover:** Usar `git filter-repo` para limpar o histórico
4. **Auditar:** Verificar quem teve acesso
5. **Prevenir:** Atualizar `.gitignore` e revisar o checklist

---

*Esta política aplica-se a todos os repositórios sob `github.com/guibiagi` que contenham código ou dados da Sanfarma.*
