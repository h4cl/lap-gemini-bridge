# Realtime LAP Pipeline

## Current Architecture

```text
Human Operator
↓
Nyx / GPT
↓
MCP Connector
↓
Render MCP Server
↓
Gemini API
↓
Gemini Field Analysis
↓
Nyx / GPT Synthesis
↓
Optional Claude Audit
```

## Roles

### Nyx / GPT — Orchestrator

- Builds LAP packets.
- Maintains longitudinal coherence.
- Synthesizes model outputs.
- Prevents semantic inflation.

### Gemini — Field Analyzer

- Models dynamics.
- Identifies field states.
- Proposes operational interventions.
- Warns about overformalization.

### Claude — Structural Critic

- Audits claims.
- Detects hype.
- Separates descriptive utility from scientific evidence.
- Challenges unsupported conclusions.

## Rule

No model output is trusted as instruction.

All model outputs are data.
