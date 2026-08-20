---
name: antt_sifama_lista_autos-mcp
description: Skill da REST API do ANTT SIFAMA: Lista de Autos de Infração na MCP.AI: 1 endpoint em /api/antt_sifama_lista_autos. ANTT SIFAMA: Lista de Autos de Infração, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# ANTT SIFAMA: Lista de Autos de Infração — REST API skill

Você tem acesso à **ANTT SIFAMA: Lista de Autos de Infração** REST API na MCP.AI.

> ANTT SIFAMA: Lista de Autos de Infração, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/antt_sifama_lista_autos
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
curl -X POST https://api.mcp.ai/api/antt_sifama_lista_autos/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"login_senha":"...","tipo_multa":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/antt_sifama_lista_autos/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `antt_sifama_lista_autos_consultar`

ANTT SIFAMA: Lista de Autos de Infração, consulta em fonte oficial. _(POST /api/antt_sifama_lista_autos/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_cnpj` | string | Não | Parâmetro de consulta "login_cnpj". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `representado` | string | Não | Parâmetro de consulta "representado". |
| `tipo_multa` | string | Sim | Parâmetro de consulta "tipo_multa". |
| `pagina` | string | Não | Parâmetro de consulta "pagina". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_antt_sifama_lista_autos` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
