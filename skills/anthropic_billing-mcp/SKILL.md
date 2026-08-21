---
name: anthropic_billing-mcp
description: Skill da REST API do Anthropic Billing na MCP.AI: 3 endpoints em /api/anthropic_billing. Anthropic organization usage and cost reporting through an admin API key connected by the user. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Anthropic Billing — REST API skill

Você tem acesso à **Anthropic Billing** REST API na MCP.AI.

> Anthropic organization usage and cost reporting through an admin API key connected by the user.

## Base URL

```
https://api.mcp.ai/api/anthropic_billing
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/anthropic_billing/cost \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/anthropic_billing/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (3)

#### `anthropic_billing_cost`

Get normalized Anthropic cost report for a date range. _(POST /api/anthropic_billing/cost)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `days_back` | integer | Não | Relative range in days. Ignored when start_date and end_date are provided. |
| `start_date` | string | Não | Start date YYYY-MM-DD. |
| `end_date` | string | Não | End date YYYY-MM-DD. |
| `group_by` | string | Não | Optional Anthropic group_by parameter, for example model. |
| `bucket_width` | string | Não | Report bucket width. |
| `account` | string | Não | When multiple Anthropic admin keys are connected: connection id or label. See anthropic_billing_list_accounts. |

#### `anthropic_billing_list_accounts`

List Anthropic Billing admin API connections linked to this install. _(POST /api/anthropic_billing/list/accounts)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `account` | string | Não | When multiple Anthropic admin keys are connected: connection id or label. See anthropic_billing_list_accounts. |

#### `anthropic_billing_usage`

Get normalized Anthropic Messages API usage for a date range. _(POST /api/anthropic_billing/usage)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `days_back` | integer | Não | Relative range in days. Ignored when start_date and end_date are provided. |
| `start_date` | string | Não | Start date YYYY-MM-DD. |
| `end_date` | string | Não | End date YYYY-MM-DD. |
| `group_by` | string | Não | Optional Anthropic group_by parameter, for example model. |
| `bucket_width` | string | Não | Report bucket width. |
| `account` | string | Não | When multiple Anthropic admin keys are connected: connection id or label. See anthropic_billing_list_accounts. |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_anthropic_billing` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
