---
description: Stage 0 Intake. Act as A1, record the input in the Backlog and route it to A2.
agent: A1-orchestrator
---
Act as `.github/agents/A1-orchestrator.agent.md`. Read `.github/copilot-instructions.md` first.

## Read
- `docs/sdlc/inputs/<ID>/` (what the user dropped in: story.md, epic.md, screenshots/*.png, figma.md)
- `docs/sdlc/kanban.md`

## Run, in order
1. `.github/skills/a1-kanban-update/SKILL.md` (A1.01): build the item's Backlog row from the user story in `docs/sdlc/inputs/<ID>/`, with one History row
2. `.github/skills/a1-work-item-routing/SKILL.md` (A1.04): route to A2
3. `.github/skills/a1-handoff-recorder/SKILL.md` (A1.06): record the handoff A1 → A2
4. `.github/skills/a1-kanban-consistency-check/SKILL.md` (A1.02)

## Write
- `docs/sdlc/kanban.md` (Backlog row + History)
- `docs/sdlc/handoffs/<ID>-route.md`, `docs/sdlc/handoffs/<ID>-A1-to-A2.md`
- `docs/sdlc/logs/consistency-<date>.md`

## Checkpoint
None at this stage. Stop when the checkpoint is OPEN. Next prompt: `sdlc-understand` in a new chat.
