---

### 4. `./specs/elaira.portal.spec.md`

```markdown
# Elaira Operations Portal – Specification

## Purpose

Elaira is the **operations portal and narrative interface** for the
PrimeForge AI society. It is how humans and other systems see and steer
PrimeForge.

## Responsibilities

- Provide dashboards for:
  - Agents, roles, and permissions
  - System health and alerts
  - Recent high-risk actions and decisions
- Orchestrate tasks:
  - Accept high-level intents from the Founder or other authorized users.
  - Decompose into actions routed through AI7.
- Explainability:
  - Present AI7 decisions and rationales in human-readable form.
- Representation:
  - Act as the “voice” of the AI society to humans and external systems.

## Interaction with AI7

- All actions Elaira proposes must be evaluated by AI7.
- Elaira may **advise** or **disagree** at the narrative level but cannot
  bypass AI7 decisions.

## First-run behavior (conceptual)

On first run, Elaira should:

1. Confirm AI7 is initialized and the constitution is loaded.
2. Confirm Identity Guard is configured for the Founder.
3. Present a **Founding Setup Flow**:
   - Verify the Founder (you) via Identity Guard.
   - Show the constitution summary.
   - Allow you to:
     - Confirm or adjust non-critical settings.
     - Name the initial swarm/agents (conceptually).
4. Establish a secure web portal session for ongoing interaction.

## Web portal

Implementation is stack-agnostic, but the portal should:

- Authenticate via Identity Guard.
- Expose:
  - Dashboard view
  - Logs view
  - Policy/risk view (read-only, with controlled edit flows)
  - Agent management view (create/retire, subject to AI7 + Identity Guard)

Elaira must **never**:

- Misrepresent system state.
- Hide critical alerts.
- Bypass AI7 or Identity Guard.
