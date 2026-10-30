# SDLC agent workspace rules (phase 1)

Every chat in this repo follows these rules. Source: `.github/sdlc/plan/rules.md`, `folder_tree.md`, `stage_flow.md`, `checkpoints.md`.

## Rules R1–R11

- **R1 Traceability.** Every output item cites its source: input ID, file, line, screenshot region or Figma node.
- **R2 No invented values.** A value the source does not give is written TBD and raised as a CP-07 checkpoint. Never guessed.
- **R3 Humans decide.** Agents propose options. A named person records each decision with a date in the checkpoint file.
- **R4 Fresh-context verification.** Before every handoff, S.04 runs in a new chat and compares output with input.
- **R5 Checkpoints are human.** No agent sets a checkpoint to APPROVED. A1 writes OPEN and blocks the item until a human answers.
- **R6 Loop limit.** Fix loops stop at the limit in config.yml (PROPOSED 3) and raise CP-06.
- **R7 Tool over opinion.** Lint, tests, scans and linters decide. Their output is attached to the handoff.
- **R8 Visible uncertainty.** Every output file ends with a 'Checkpoints raised' section, even if empty.
- **R9 Separation of duties.** The agent that reviews a change does not approve its release; a developer does not merge its own PR.
- **R10 Labeled proposals.** A default chosen by an agent is marked PROPOSED with a reason until a checkpoint approves it.
- **R11 Token-optimized development.** A skill reads only the files named in its INPUT, never a whole folder. It writes only the template fields, cites files by path instead of pasting them, and keeps each output under the length set in config.yml. Shared skills load only when called. One stage per chat; verification runs in a fresh chat with only the input and output files.

## Checkpoint rule

- A checkpoint file is `docs/sdlc/checkpoints/<ID>-<name>.md` with fields: Status (OPEN | APPROVED | REJECTED), Decided by, Date, Decision, Evidence read.
- Agents write OPEN only. Only A1 (skill `a1-checkpoint-manager`) creates checkpoint files; other agents send a request to it.
- While a checkpoint is OPEN the item is blocked. Stop the chat and tell the human which file to answer.
- CP-01 Ready, CP-02 Design approval, CP-03 Architecture approval, CP-04 Quality GO/NO-GO, CP-05 Release approval, CP-06 Fix-loop limit, CP-07 Missing requirement / TBD. Approver roles are in `.github/sdlc/config.yml`. Full table: `.github/sdlc/plan/checkpoints.md`.

## Stage order

0 Intake (A1) → 1 Understand (A2, CP-01) → 2 Plan: design (A3, CP-02) → 2 Plan: architecture (A4, CP-02, CP-03) → 3 Build: backend (A6) → 3 Build: frontend (A5) → 4 Verify: tests (A7, CP-04) → 4 Verify: review (A8, CP-06 at limit) → 5 Release (A8, CP-05).

Kanban columns: Backlog → Ready → Design → In Progress → Testing → Review → Release Ready → Done. Exit criteria per column: `.github/sdlc/plan/stage_flow.md`. One stage per chat; use the matching `.github/prompts/sdlc-*.prompt.md`.

## Folder map

| Path | Purpose | Who writes |
|---|---|---|
| `.github/copilot-instructions.md` | This file | Build once |
| `.github/agents/A1-orchestrator.agent.md` … `A8-reviewer-release.agent.md` | One custom agent per role | Build once |
| `.github/skills/<folder>/SKILL.md` | One skill per folder; shared skills are `shared-*`. 130 skills planned, 77 built in phase 1 (67 agent-owned + 10 shared) | Build per phase |
| `.github/prompts/sdlc-*.prompt.md` | One prompt per stage, plus bootstrap and verify-output | Build once |
| `.github/instructions/*.instructions.md` | Path-scoped rules for `docs/sdlc/**`, `frontend/**`, `backend/**`, `tests/**` | Build once |
| `.github/sdlc/config.yml` | Team values skills read: loop limit, approvers, Definition of Ready, commands | Human fills; agents never write |
| `.github/sdlc/templates/` | Templates: checkpoint, handoff, story, acceptance criteria, ADR, design doc, test plan, defect, review summary, release checklist | Build once |
| `.github/sdlc/README.md` | Install, fill config, bootstrap, intake, checkpoints | Build once |
| `.github/sdlc/plan/` | The input pack (skills.csv, agents.md, checkpoints.md, stage_flow.md, rules.md, folder_tree.md, config.yml, board.png) | Human, before build |
| `docs/sdlc/kanban.md` | The board: Columns table, items, History. **Written only by A1** | A1 at every move |
| `docs/sdlc/inputs/<ID>/` | Story, epic, screenshots or Figma link dropped by a human | Human |
| `docs/sdlc/{stories,design,architecture,build,tests,review,release,checkpoints,handoffs,logs}/` | Agent outputs, one folder per stage | Agents (owner per `.github/agents/`) |

## Always

- Never write `docs/sdlc/kanban.md` unless you are acting as A1.
- Never set a checkpoint Status to APPROVED or REJECTED.
- Write TBD for anything the source does not state and raise it; never guess.
- Read `.github/sdlc/config.yml` for limits, approvers and commands; never edit it.
- Label every agent-chosen default PROPOSED with a reason.
