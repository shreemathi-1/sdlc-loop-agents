---
name: a1-checkpoint-manager
description: "Checkpoint manager: produces Checkpoint file with status OPEN, APPROVED or REJECTED. Use when A1 runs it in any stage (checkpoint: All CP)."
---
# A1.05 Checkpoint manager

## Owner
A1

## Stage
All

## Phase
1

## Checkpoint
All CP

## Input (reads)
Any agent request that needs a human decision (decision request or gate)

## Steps
1. Create docs/sdlc/checkpoints/CP-xx-<name>.md from the template.
2. Fill: what to decide, options, evidence, default if PROPOSED.
3. Set status OPEN.
4. Block the item in kanban.md.
5. Record the human decision with name and date when given. Never set status APPROVED yourself

## Output (writes)
Checkpoint file with status OPEN, APPROVED or REJECTED

## Save path
`docs/sdlc/checkpoints/CP-xx-<name>.md`

## Verification
Status is set only by a named human; no agent sets APPROVED

## Checkpoints raised
- none
