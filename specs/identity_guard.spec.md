# Identity Guard – Specification

## Purpose

Identity Guard is the **root-of-trust** for Founder-level and other
authorized human approvals.

## Responsibilities

- Verify identity of:
  - Founder & Constitutional Steward (David Berry)
  - Any additional authorized humans you define
- Approve or deny high-risk actions based on explicit human intent.
- Cryptographically sign approvals and maintain an immutable audit log.

## Behavior

- Accepts approval requests from AI7 or Elaira, including:
  - Action description
  - Risk level
  - Required approvals
- Prompts the human via secure channel (e.g., web portal, mobile app).
- Returns a signed decision:

```json
{
  "approved": true,
  "approver": "David Berry",
  "timestamp": "ISO-8601",
  "signature": "..."
}
