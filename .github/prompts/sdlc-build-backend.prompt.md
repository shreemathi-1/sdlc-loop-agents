---
description: Stage 3 Build, backend. Act as A6 on one task: migrations, endpoints, validation, seed data, config, container, contract report, task gate, PR.
agent: A6-backend-engineer
---
Act as `.github/agents/A6-backend-engineer.agent.md`. Read `.github/copilot-instructions.md` first. Requires CP-03 APPROVED. One task per chat.

## Read
- `docs/sdlc/architecture/tasks-<ID>.md` (the one task)
- `docs/sdlc/architecture/api/openapi.yaml`
- `docs/sdlc/architecture/data-model.md`
- `.github/sdlc/config.yml` (commands, git)

## Run, in order
1. `.github/skills/a6-data-model-and-migrations/SKILL.md` (A6.01)
2. `.github/skills/a6-api-endpoint-implementation/SKILL.md` (A6.02)
3. `.github/skills/a6-validation-and-error-responses/SKILL.md` (A6.03)
4. `.github/skills/a6-mock-data-generation/SKILL.md` (A6.05)
5. `.github/skills/a6-backend-environment-config-and-seed/SKILL.md` (A6.07)
6. `.github/skills/a6-backend-container-and-deploy-config/SKILL.md` (A6.08)
7. `.github/skills/a6-api-contract-validator/SKILL.md` (A6.06)
8. `.github/skills/shared-task-gate-and-commit/SKILL.md` (S.07)
9. `.github/skills/shared-pull-request-creation/SKILL.md` (S.08)

## Write
backend/ (migrations, api, validation, seed/synthetic, config), deploy/backend/ (Dockerfile); docs/sdlc/build/plans, task-gate-<task-ID>.md, pr-<task-ID>.md; docs/sdlc/tests/contract-<run>.md.

## Checkpoint
None at this stage. CP-07 through A1.05 for any TBD. Stop when the checkpoint is OPEN.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
