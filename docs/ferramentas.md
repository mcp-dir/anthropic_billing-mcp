# Ferramentas

Anthropic Billing expõe 3 ferramentas (todas somente leitura).

### 1. `anthropic_billing_list_accounts`
**Input**: `account` (opcional)

List Anthropic Billing admin API connections linked to this install.

### 2. `anthropic_billing_usage`
**Input**: `days_back` (opcional), `start_date` (opcional), `end_date` (opcional), `group_by` (opcional), `bucket_width` (opcional), `account` (opcional)

Get normalized Anthropic Messages API usage for a date range.

### 3. `anthropic_billing_cost`
**Input**: `days_back` (opcional), `start_date` (opcional), `end_date` (opcional), `group_by` (opcional), `bucket_width` (opcional), `account` (opcional)

Get normalized Anthropic cost report for a date range.

## Prompts de exemplo

```
Show Anthropic usage for the last 30 days
What did Anthropic cost this month?
Break down Anthropic message tokens by day
```
