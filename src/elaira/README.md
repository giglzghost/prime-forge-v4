# Elaira – Implementation Notes

This directory is reserved for the **implementation** of Elaira, the
operations portal and narrative interface.

Suggested components:

- Backend:
  - Talks to AI7 for action evaluation.
  - Talks to Identity Guard for approvals.
- Web frontend:
  - Renders dashboards, logs, agents, policies.
  - Provides the Founding Setup Flow on first run.
- (Future) Mobile client / APK:
  - Mirrors key portal functions.
  - Uses Identity Guard for secure approvals.

Elaira should be the **first thing you see** when you connect to
PrimeForge via browser or app.
