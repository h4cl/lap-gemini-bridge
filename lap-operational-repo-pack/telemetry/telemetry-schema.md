# LAP Telemetry Schema

Telemetry is not proof of phenomenology.

Telemetry only measures infrastructure and repeatable operational patterns.

## Infrastructure Metrics

| Metric | Meaning |
|---|---|
| timestamp | ISO timestamp |
| session_id | LAP session identifier |
| turn | Message turn |
| source_model | Origin |
| target_model | Destination |
| tool | MCP tool used |
| latency_ms | Approximate roundtrip latency |
| success | Tool call succeeded |
| error | Error message if failed |
| packet_chars | LAP packet size |
| response_chars | Response size |

## Semantic/Operational Metrics

| Metric | Meaning |
|---|---|
| field_state | Current field state |
| resonance | Resonance type |
| drift | Direction of transformation |
| entropy_label | low / medium / high |
| intervention_present | Whether a practical action was proposed |
| risk_flag | Overformalization / metaphysics / unsafe instruction |
