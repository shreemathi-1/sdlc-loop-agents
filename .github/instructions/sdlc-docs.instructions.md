---
applyTo: "docs/sdlc/**"
---
# Rules for docs/sdlc/**

- Only A1 (`.github/agents/A1-orchestrator.agent.md`) writes `docs/sdlc/kanban.md`, `checkpoints/`, `handoffs/`, `logs/`.
- Every value the source does not give is written `TBD` and raised as CP-07 (R2). Never guess.
- Every default chosen by an agent carries the label `PROPOSED` with a reason (R10).
- Every item cites its source: input ID, file, line, screenshot region or Figma node (R1).
- Every file ends with a `## Checkpoints raised` section, even if it only says `- none` (R8).
- Checkpoint files use `.github/sdlc/templates/checkpoint.md`. Status is `OPEN` when an agent writes it. Only a named human writes `APPROVED` or `REJECTED` with a date (R5).
- Fill templates from `.github/sdlc/templates/`; add no fields the template lacks (S.05).
- Keep each file under `limits.output_max_lines` in `.github/sdlc/config.yml`; cite files by path instead of pasting them (R11).
- Write only the folder your agent is permitted to write (see the agent file's Permissions).
