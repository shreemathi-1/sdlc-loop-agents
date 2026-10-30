---
description: Stage 2 Plan, architecture. Act as A4, write ADRs, architecture, data model, API contract, navigation, repo structure, design doc and tasks; request CP-02 and CP-03.
agent: A4-architect
---
Act as `.github/agents/A4-architect.agent.md`. Read `.github/copilot-instructions.md` first. Requires CP-01 APPROVED.

## Read
- `docs/sdlc/stories/<ID>/` (stories.md, acceptance-criteria.md, scope.md, ux-spec.md, screen-inventory.md)
- `docs/sdlc/design/<ID>/` (ui-baseline.md or extracted-design.md)
- `.github/sdlc/config.yml` (project.platform, commands)
- Templates: `.github/sdlc/templates/adr.md`, `design-doc.md`

## Run, in order
1. `.github/skills/a4-stack-selection-analysis/SKILL.md` (A4.02), which calls
2. `.github/skills/a4-adr-writing/SKILL.md` (A4.01) for each decision
3. `.github/skills/a4-data-model-design/SKILL.md` (A4.04)
4. `.github/skills/a4-api-contract-design/SKILL.md` (A4.05)
5. `.github/skills/a4-navigation-and-flow-design/SKILL.md` (A4.06)
6. `.github/skills/a4-application-architecture-design/SKILL.md` (A4.03) — stack is PROPOSED until CP-03
7. `.github/skills/a4-repository-structure-plan/SKILL.md` (A4.07)
8. `.github/skills/a4-design-doc-writer/SKILL.md` (A4.08)
9. `.github/skills/a4-task-breakdown/SKILL.md` (A4.09)
10. `.github/skills/a4-design-approval-request/SKILL.md` (A4.10)

## Write
`docs/sdlc/architecture/`: adr/ADR-*.md, stack-analysis.md, architecture.md, data-model.md, api/openapi.yaml, navigation.md, repo-structure.md, design-doc-<ID>.md, tasks-<ID>.md.

## Checkpoint
Request CP-02 Design approval and CP-03 Architecture approval through A1.05. Stop when the checkpoint is OPEN.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
