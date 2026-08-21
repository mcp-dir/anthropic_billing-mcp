# Anthropic Billing

### Anthropic Billing for Claude, ChatGPT and AI agents

Anthropic organization usage and cost reporting through an admin API key connected by the user.

- 📊 **3 tools**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Anthropic Billing`, URL `https://api.mcp.ai/p_anthropic_billing`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=anthropic_billing&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9hbnRocm9waWNfYmlsbGluZyJ9)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=anthropic_billing&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_anthropic_billing%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_anthropic_billing
```

---

## 3 tools

| Tool | Description |
|---|---|
| `anthropic_billing_list_accounts` | List Anthropic Billing admin API connections linked to this install. |
| `anthropic_billing_usage` | Get normalized Anthropic Messages API usage for a date range. |
| `anthropic_billing_cost` | Get normalized Anthropic cost report for a date range. |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_anthropic_billing` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
