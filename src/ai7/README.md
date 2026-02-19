# AI7 – Implementation Notes

This directory is reserved for the **implementation** of AI7, the
constitutional kernel.

Suggested responsibilities:

- Load `constitution/primeforge.constitution.yaml`.
- Build an internal policy engine.
- Expose an API, e.g.:

  - `POST /ai7/evaluate-action`
  - Input: action object
  - Output: decision object

- Implement safe mode behavior as defined in the constitution.

Stack is up to you (Node, Python, etc.). The key is that AI7 **never**
bypasses the constitution and always returns explicit decisions with
rationales.
