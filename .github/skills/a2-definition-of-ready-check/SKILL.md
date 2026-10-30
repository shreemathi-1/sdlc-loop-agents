---
name: a2-definition-of-ready-check
description: "Definition of Ready check: produces Ready report: story, check, pass/fail, evidence. Use when A2 runs it in the Understand stage (checkpoint: CP-01)."
---
# A2.09 Definition of Ready check

## Owner
A2

## Stage
Understand

## Phase
1

## Checkpoint
CP-01

## Input (reads)
Stories, criteria, scope, UX spec, checkpoint log (S.02)

## Steps
1. Check each story against the Definition of Ready in .github/sdlc/config.yml.
2. Record pass or fail per story with evidence.
3. If any CP-07 for this item is not APPROVED, mark the check FAIL, list the open CP-07 files, and stop; do not request CP-01.
4. If all pass, request CP-01 through A1.05

## Output (writes)
Ready report: story, check, pass/fail, evidence

## Save path
`docs/sdlc/stories/<ID>/ready-report.md`

## Verification
Every story has a pass or fail result with evidence

## Checkpoints raised
- none
