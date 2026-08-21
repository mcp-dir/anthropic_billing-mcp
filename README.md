# Anthropic Billing

### Anthropic Billing para Claude, ChatGPT e agentes de IA

Anthropic organization usage and cost reporting through an admin API key connected by the user.

- 📊 **3 ferramentas**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Anthropic Billing` e **URL** `https://api.mcp.ai/p_anthropic_billing`.

### Cursor

[➕ Instalar Anthropic Billing no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=anthropic_billing&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9hbnRocm9waWNfYmlsbGluZyJ9)

### VS Code (Copilot Chat)

[➕ Instalar Anthropic Billing no VS Code](vscode:mcp/install?name=anthropic_billing&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_anthropic_billing%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_anthropic_billing
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Show Anthropic usage for the last 30 days
What did Anthropic cost this month?
Break down Anthropic message tokens by day
```

---

## 3 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `anthropic_billing_list_accounts` | List Anthropic Billing admin API connections linked to this install. |
| `anthropic_billing_usage` | Get normalized Anthropic Messages API usage for a date range. |
| `anthropic_billing_cost` | Get normalized Anthropic cost report for a date range. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_anthropic_billing`.


---

## Suporte

- 📧 [anthropic_billing@mcp.ai](mailto:anthropic_billing@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/anthropic_billing-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_anthropic_billing` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
