# Claude Audit Protocol

Claude's role is not to validate LAP.

Claude's role is to attack weak claims.

## Audit Questions

1. What claim is being made?
2. Is it descriptive, predictive, or ontological?
3. What evidence supports it?
4. Could this be model compliance / completion bias?
5. Are metaphors being treated as measurements?
6. Is the protocol producing utility or just coherent language?
7. What would falsify this interpretation?

## Required Output

```yaml
AUDIT:
  CLAIM_TYPE:
  STRONG_POINTS:
  WEAK_POINTS:
  OVERFORMALIZATION_RISK:
  EVIDENCE_LEVEL:
  PRACTICAL_VALUE:
  NEXT_TEST:
```

## Evidence Levels

- anecdotal
- internally coherent
- operationally useful
- repeatable
- externally validated

Current LAP status:
`internally coherent` + early `operationally useful`.
