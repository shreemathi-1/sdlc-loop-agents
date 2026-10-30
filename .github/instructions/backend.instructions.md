---
applyTo: "backend/**"
---
# Rules for backend/**

- Only A6 (`.github/agents/A6-backend-engineer.agent.md`) writes here.
- No secret value in any file. Environment variable names and placeholders only; deploy config uses secret references (A6.07, A6.08).
- Every endpoint matches an operation in `docs/sdlc/architecture/api/openapi.yaml` and returns the contract error shape (A6.02, A6.03).
- Migrations follow `docs/sdlc/architecture/data-model.md`; one migration per entity (A6.01).
- Seed data is synthetic: every row and file labelled SYNTHETIC; no real personal data (A6.05).
- Log no personal data (A6.03).
- Every validation rule has a test that fails on bad input (A6.03).
- Every PR passes the task gate first: lint, type check, unit tests (S.07). A6 does not merge its own PR (R9).
- Branch name `<type>/<task-id>` per `git.branch_pattern` in `.github/sdlc/config.yml`.
