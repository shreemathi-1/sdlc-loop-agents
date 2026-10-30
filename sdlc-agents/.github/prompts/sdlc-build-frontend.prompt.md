---
description: Stage 3 Build, frontend. Act as A5 on one task: plan, components, screens, state and routes, API wiring, build config, task gate, PR.
agent: A5-frontend-developer
---
Act as `.github/agents/A5-frontend-developer.agent.md`. Read `.github/copilot-instructions.md` first. Requires CP-02 and CP-03 APPROVED. One task per chat.

## Read
- `docs/sdlc/architecture/tasks-<ID>.md` (the one task)
- `docs/sdlc/design/<ID>/` (components.md, tokens.json, layout-plan.md)
- `docs/sdlc/architecture/navigation.md`, `docs/sdlc/architecture/api/openapi.yaml`
- `backend/seed/synthetic/` (seed data)
- `.github/sdlc/config.yml` (commands, git)

## Run, in order
1. `.github/skills/a5-task-plan/SKILL.md` (A5.01)
2. `.github/skills/a5-component-codegen-from-spec/SKILL.md` (A5.02)
3. `.github/skills/a5-screen-implementation/SKILL.md` (A5.03)
4. `.github/skills/a5-state-and-navigation-management/SKILL.md` (A5.04)
5. `.github/skills/a5-api-wiring/SKILL.md` (A5.05)
6. `.github/skills/a5-frontend-build-configuration/SKILL.md` (A5.06)
7. `.github/skills/shared-minimum-ui-ux-checklist/SKILL.md` (S.10)
8. `.github/skills/shared-task-gate-and-commit/SKILL.md` (S.07)
9. `.github/skills/shared-pull-request-creation/SKILL.md` (S.08)

## Write
frontend/ (components, screens, state, routes, api, theme, build config); docs/sdlc/build/plans/<task-ID>.md, task-gate-<task-ID>.md, pr-<task-ID>.md.

## Checkpoint
None at this stage. CP-07 through A1.05 for any TBD. Stop when the checkpoint is OPEN.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
