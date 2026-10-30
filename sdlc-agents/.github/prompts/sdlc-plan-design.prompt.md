---
description: Stage 2 Plan, design. Act as A3, write the UI baseline or extracted design, layout plan, tokens, components, responsive rules and checklist for CP-02.
agent: A3-ui-ux-designer
---
Act as `.github/agents/A3-ui-ux-designer.agent.md`. Read `.github/copilot-instructions.md` first. Requires CP-01 APPROVED in `docs/sdlc/checkpoints/CP-01-ready.md`.

## Read
- `docs/sdlc/stories/<ID>/` (stories.md, ux-spec.md, screen-inventory.md, scope.md)
- Screenshots in `docs/sdlc/inputs/<ID>/screenshots/` if any

## Run, in order
1. `.github/skills/a3-text-only-ux-baseline/SKILL.md` (A3.01) — text input, or
   `.github/skills/a3-screenshot-design-extraction/SKILL.md` (A3.02) — screenshot input
2. `.github/skills/a3-baseline-ui-layout-plan/SKILL.md` (A3.03)
3. `.github/skills/a3-design-tokens/SKILL.md` (A3.04)
4. `.github/skills/a3-component-spec-writer/SKILL.md` (A3.05)
5. `.github/skills/a3-responsive-layout-rules/SKILL.md` (A3.06)
6. `.github/skills/shared-minimum-ui-ux-checklist/SKILL.md` (S.10)
7. `.github/skills/a3-design-system-bootstrap/SKILL.md` (A3.07)

## Write
`docs/sdlc/design/<ID>/`: ui-baseline.md or extracted-design.md, layout-plan.md, tokens.json, components.md, responsive.md, ui-checklist.md; draft `frontend/src/theme/` marked NOT ADOPTED.

## Checkpoint
CP-02 Design approval. Per `.github/sdlc/plan/checkpoints.md` it is raised by A4.10 in `sdlc-plan-architecture`; this stage prepares its evidence. Stop when the checkpoint is OPEN.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
