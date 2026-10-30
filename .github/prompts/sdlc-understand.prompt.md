---
description: Stage 1 Understand. Act as A2, turn the input into stories, criteria, scope and UX spec; end with a CP-01 request.
agent: A2-requirements-analyst
---
Act as `.github/agents/A2-requirements-analyst.agent.md`. Read `.github/copilot-instructions.md` first.

## Read
- `docs/sdlc/inputs/<ID>/` (only the files named in each skill's Input)
- `.github/sdlc/config.yml` (definition_of_ready, approvers)
- Templates: `.github/sdlc/templates/story.md`, `acceptance-criteria.md`

## Run, in order (skip a skill whose input type is absent)
1. `.github/skills/a2-input-intake-and-type-detection/SKILL.md` (A2.01)
2. `.github/skills/a2-epic-decomposition/SKILL.md` (A2.02) — epic input only
3. `.github/skills/a2-user-story-writing/SKILL.md` (A2.03)
4. `.github/skills/a2-acceptance-criteria/SKILL.md` (A2.04)
5. `.github/skills/a2-platform-and-scope-definition/SKILL.md` (A2.05)
6. `.github/skills/a2-screenshot-screen-inventory/SKILL.md` (A2.06) — screenshot input only
7. `.github/skills/a2-ux-state-definition/SKILL.md` (A2.07)
8. `.github/skills/a2-ux-spec-writing/SKILL.md` (A2.08)
9. `.github/skills/a2-scope-check-against-input/SKILL.md` (A2.11)
10. `.github/skills/a2-clarifying-question-and-checkpoint-builder/SKILL.md` (A2.10) — one CP-07 request per TBD
11. `.github/skills/a2-definition-of-ready-check/SKILL.md` (A2.09)

## Write
`docs/sdlc/stories/<ID>/`: manifest.md, features.md (epic), stories.md, acceptance-criteria.md, scope.md, screen-inventory.md (screenshot), ux-states.md, ux-spec.md, scope-check.md, ready-report.md. CP-07 requests go to A1.05, not to kanban.md.

## Checkpoint
Request CP-01 Ready through A1.05 (`a1-checkpoint-manager`) when the ready report passes. Stop when the checkpoint is OPEN. Do not mark Ready.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
