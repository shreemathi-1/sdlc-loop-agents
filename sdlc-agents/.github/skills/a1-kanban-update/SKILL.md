---
name: a1-kanban-update
description: "Kanban update: produces Updated kanban.md with one new History row. Use when A1 runs it in any stage."
---
# A1.01 Kanban update

## Owner
A1

## Stage
All

## Phase
1

## Checkpoint
—

## Input (reads)
Status event from an agent: item ID, from-column, to-column, evidence file path

## Steps
1. Read the event.
2. Check the exit criteria for the current column (stage gate check).
3. If all pass, move the item and add one History row.
4. If a human gate applies, write 'Awaiting approval: <role>' and do not move.
5. Commit: kanban: <ID> <from> → <to>

## Output (writes)
Updated kanban.md with one new History row

## Save path
`docs/sdlc/kanban.md`

## Verification
Every move has one History row with evidence path

## Checkpoints raised
- none
