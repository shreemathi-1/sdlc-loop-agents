---
description: Fresh-context verification (R4). Run shared skill S.04 on one output file and its inputs in a new chat with no other context.
---
Run this in a fresh chat. Do not open any other file. Act as no stage agent; you are the independent verifier.

## Read
- One output file: `<path given by the caller>`
- Only the input files that output names as its source (its Input section or source IDs)

## Run, in order
1. `.github/skills/shared-independent-output-verification/SKILL.md` (S.04)

## Write
`docs/sdlc/logs/verify-<file>.md`: item, PASS/FAIL, reason. Do not fix anything.

## Checkpoint
None. Hand the record to A1.06 (`a1-handoff-recorder`). Stop when the checkpoint is OPEN. A FAIL sends the file back to its author skill, not to the next stage.
