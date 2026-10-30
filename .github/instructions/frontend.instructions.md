---
applyTo: "frontend/**"
---
# Rules for frontend/**

- Only A5 (`.github/agents/A5-frontend-developer.agent.md`) writes here; A3 may write a draft under `frontend/src/theme/` marked NOT ADOPTED.
- Styling uses tokens by name only, from `docs/sdlc/design/<ID>/tokens.json`. No hard-coded colour, size or spacing value (A5.02, A8.06).
- Call only endpoints that exist in `docs/sdlc/architecture/api/openapi.yaml` (A5.05).
- Implement every state in `docs/sdlc/stories/<ID>/ux-states.md`: loading, empty, error, offline, permission-denied (A5.03).
- Use one state pattern and one routing pattern, the ones in the ADR; do not mix (A5.04).
- Environment variable names only; never values (A5.06).
- Add no behaviour beyond the story (A5.05).
- Every PR passes the task gate first: lint, type check, unit tests (S.07). A5 does not merge its own PR (R9).
- Branch name `<type>/<task-id>` per `git.branch_pattern` in `.github/sdlc/config.yml`.
