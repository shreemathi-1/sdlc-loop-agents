---
name: a1-kanban-consistency-check
description: "Kanban consistency check: produces Consistency report listing violations (empty if none). Use when A1 runs it in any stage."
---
# A1.02 Kanban consistency check

## Owner
A1

## Stage
All

## Phase
1

## Checkpoint
—

## Input (reads)
docs/sdlc/kanban.md

## Steps
1. Check each item appears in one column only.
2. Check every move has a History row.
3. Check each 'Awaiting approval' has a matching checkpoint file

## Output (writes)
Consistency report listing violations (empty if none)

## Save path
`docs/sdlc/logs/consistency-<date>.md`

## Verification
Report has zero violations or lists each one

## Checkpoints raised
- none
