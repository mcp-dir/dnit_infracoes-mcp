# Instalação rápida

DNIT: Infrações é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_dnit_infracoes`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `DNIT: Infrações` / `https://api.mcp.ai/p_dnit_infracoes`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "dnit_infracoes": { "type": "http", "url": "https://api.mcp.ai/p_dnit_infracoes" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=dnit_infracoes&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9kbml0X2luZnJhY29lcyJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "dnit_infracoes": { "url": "https://api.mcp.ai/p_dnit_infracoes" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=dnit_infracoes&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_dnit_infracoes%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "dnit_infracoes": { "type": "http", "url": "https://api.mcp.ai/p_dnit_infracoes" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_dnit_infracoes
```

Dúvidas? [dnit_infracoes@mcp.ai](mailto:dnit_infracoes@mcp.ai)
