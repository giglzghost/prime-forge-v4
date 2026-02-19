# PrimeForge Bootstrap – First Run Playbook

This document describes how PrimeForge should conceptually "become itself"
on first run. Actual implementation is up to your chosen stack.

## Sequence

1. **Start AI7**
   - Load `constitution/primeforge.constitution.yaml`.
   - Validate structure and integrity.
   - Expose an internal API for action evaluation.

2. **Start Identity Guard**
   - Initialize Founder identity (David Berry).
   - Set up secure approval channel(s).
   - Expose an API for approval requests.

3. **Start Elaira**
   - Connect to AI7 and Identity Guard.
   - Detect "first run" state (no prior Founder confirmation).
   - Launch Founding Setup Flow in the web portal.

4. **Founding Setup Flow**
   - Verify you via Identity Guard.
   - Present constitution summary.
   - Let you confirm or adjust non-critical settings.
   - Confirm system is now "live" under the constitution.

From that point, PrimeForge operates as an AI-native OS with:

- AI7 enforcing the constitution
- Elaira providing visibility and orchestration
- Identity Guard anchoring your authority
