# Instalação detalhada

ANTT SIFAMA: Lista de Autos de Infração é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_antt_sifama_lista_autos`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_antt_sifama_lista_autos` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_antt_sifama_lista_autos` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_antt_sifama_lista_autos` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.antt_sifama_lista_autos` (ou `servers.antt_sifama_lista_autos` no VS Code) do config do cliente e reinicie.
