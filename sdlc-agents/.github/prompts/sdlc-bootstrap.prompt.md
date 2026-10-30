---
description: Stage setup. Act as A1 and create the docs/sdlc/ tree from config.yml (skill A1.12). Run once per project.
agent: A1-orchestrator
---
Act as `.github/agents/A1-orchestrator.agent.md`. Read `.github/copilot-instructions.md` first.

## Read
- `.github/sdlc/config.yml` (filled by a human)
- `.github/sdlc/plan/stage_flow.md` (Kanban columns table: columns, owner, entry, exit criteria)

## Run, in order
1. `.github/skills/a1-project-bootstrap/SKILL.md` (A1.12). Stop if a required value in config.yml is missing and list it.

## Write
- `docs/sdlc/kanban.md` with the Columns table (8 columns) and an empty History table
- `docs/sdlc/inputs/`, `stories/`, `design/`, `architecture/`, `build/`, `tests/`, `review/`, `release/`, `checkpoints/`, `handoffs/`, `logs/`
- `docs/sdlc/README.md` naming the first prompt to run: `sdlc-intake`

## Checkpoint
None. Stop when the checkpoint is OPEN (none is raised here). If config.yml has a required value missing, stop and tell the human which field to fill.
