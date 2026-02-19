# AI7 Constitutional Kernel – Specification

## Purpose

AI7 is the **constitutional kernel** of PrimeForge Genesis. It enforces
`constitution/primeforge.constitution.yaml` across all agents, workflows,
and integrations.yyy6⁶

## Responsibilities

- Load and validate the constitution at startup.
- Maintain an in-memory representation of:
  - Principles
  - Roles
  - Risk levels
  - Policies
- For each requested action:
  - Classify risk level.
  - Evaluate applicable policies.
  - Decide: `allow`, `deny`, or `escalate`.
- Trigger **safe mode** when anomalies or integrity failures are detected.

## Action evaluation model

Each action should be represented as a structured object, e.g.:

```json
{
  "actor_role": "elaira_portal",
  "target": {
    "is_sentient": false,
    "is_unknown_advanced_system": false
  },
  "risk_level": "medium",
  "may_cause_harm": false,
  "is_offensive_capability": false,
  "uses_external_ai": true
} 8⁷
