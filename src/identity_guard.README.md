# Identity Guard – Implementation Notes

This directory is reserved for the **implementation** of Identity Guard.

Suggested responsibilities:

- Manage Founder identity and any additional authorized identities.
- Provide an API, e.g.:
  - `POST /identity/approve`
  - Input: action summary, risk level, metadata
  - Output: signed approval/denial
- Integrate with:
  - Web portal authentication
  - (Future) Mobile client / APK for push approvals

Identity Guard is the **root-of-trust**. Keep it minimal, hardened, and
auditable
