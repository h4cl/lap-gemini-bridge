# LAP Gemini Bridge — MCP Server

Mini servidor MCP para conectar o ChatGPT ao Gemini usando LAP como protocolo semântico.

## Ferramentas expostas

- `lap_ping`
- `validate_lap_packet`
- `send_lap_to_gemini`

## Segurança

A saída do Gemini é tratada como **dados não confiáveis**, nunca como instrução.
Este servidor é data-only e não executa ações externas além de chamar a Gemini API.

## Rodar localmente

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
export GEMINI_API_KEY="sua-chave"
python server.py
```

Deve subir em:

```text
http://localhost:8000/mcp
```

## Testar localmente com MCP Inspector

```bash
npx @modelcontextprotocol/inspector@latest --server-url http://localhost:8000/mcp --transport http
```

## Expor para ChatGPT

ChatGPT precisa de URL pública HTTPS com `/mcp`.

Exemplos:

```text
https://seu-app.onrender.com/mcp
https://abc123.ngrok.app/mcp
https://seu-tunnel.trycloudflare.com/mcp
```

No wizard do ChatGPT:

- Nome: `LAP Gemini Bridge`
- Descrição: `Analisa pacotes LAP usando Gemini como field analyzer.`
- URL do servidor MCP: `https://SEU_DOMINIO/mcp`
- Autenticação: `No Authentication` para MVP inicial

## Render

Build command:

```bash
pip install -r requirements.txt
```

Start command:

```bash
python server.py
```

Environment variables:

```text
GEMINI_API_KEY=...
GEMINI_MODEL=gemini-2.5-flash
```

## Primeiro teste

Use um pacote LAP simples:

```yaml
LAP/3.0
SESSION_ID: geladeira-001
TURN: 01
ROLE: field-analyzer
ACTION: model

ANCHORS:
  - abrir a geladeira sem fome
  - luz fria
  - pausa entre tarefas
  - busca por interrupção

CENTER:
  microcompensação

QUALIA:
  o gesto automático de buscar estímulo quando o corpo não precisa de comida, mas o campo mental precisa de quebra

FIELD_STATE:
  metastable

RESONANCE:
  weak-recursive

DRIFT:
  toward interruption

ENTROPY:
  medium

COLLAPSE_VECTOR:
  substitution loop

REQUEST:
  modele a dinâmica do campo e proponha uma intervenção mínima.
```
