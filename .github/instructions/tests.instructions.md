---
applyTo: "tests/**"
---
# Rules for tests/**

- Only A7 (`.github/agents/A7-test-engineer.agent.md`) writes here; A7 changes no application source beyond test files.
- Every test carries the ID of the acceptance criterion it covers, so `docs/sdlc/tests/traceability-<ID>.md` can map criterion to test (A7.06).
- Every acceptance criterion with a flow has an E2E test that asserts the visible result (A7.05).
- Use the test runner and commands in `.github/sdlc/config.yml` (A7.02).
- A failed test gets a defect report from `.github/sdlc/templates/defect.md` (A7.07).
- Test results totals match the runner output; attach the output (R7, A7.08).
- A7 never records GO or NO-GO; that is CP-04, decided by the approver in config.yml (R5).
