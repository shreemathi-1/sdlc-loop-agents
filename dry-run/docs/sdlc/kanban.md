# Kanban (dry run): written only by A1

Columns from `config.scratch.yml` kanban.columns (scratch copy of `.github/sdlc/config.yml`).

## Columns

| Column | Owner | Exit criteria | Checkpoint |
|---|---|---|---|
| Backlog | A1 | Routed to A2 | none |
| Ready | A2 | Definition of Ready passed; all CP-07 for the item APPROVED; CP-01 APPROVED | CP-01 |
| Design | A3, A4 | CP-02 and CP-03 APPROVED; tasks written | CP-02, CP-03 |
| In Progress | A5, A6 | Every task: task gate passed, PR open, CI green | none |
| Testing | A7 | Traceability complete; CP-04 APPROVED | CP-04 |
| Review | A8 | No blocker or major open; loop count under fix_loop_max | CP-06 at limit |
| Release Ready | A8 | Release checklist complete; CP-05 APPROVED | CP-05 |
| Done | A1 | Deployed | none |

## Items

| ID | Column | Status | Handoff | Checkpoint |
|---|---|---|---|---|
| T-01 | Backlog | Blocked. Awaiting approval: Product Owner (5 CP-07 OPEN); A2.09 FAIL, CP-01 not requested | docs/sdlc/handoffs/T-01-A1-to-A2.md | docs/sdlc/checkpoints/CP-07-*.md (OPEN) |

## History

| Date | ID | From | To | Evidence |
|---|---|---|---|---|
| 2026-10-30 | T-01 | — | Backlog | docs/sdlc/inputs/T-01/story.md (intake, A1.01) |
| 2026-10-30 | T-01 | Backlog | Backlog (blocked: 5 CP-07 OPEN) | docs/sdlc/checkpoints/CP-07-*.md (A1.05) |
| 2026-10-30 | T-01 | Backlog | Backlog (not moved: Ready exit needs all CP-07 APPROVED and CP-01 APPROVED) | docs/sdlc/stories/T-01/ready-report.md (A1.01, end of Understand) |

## Checkpoints raised
- none
