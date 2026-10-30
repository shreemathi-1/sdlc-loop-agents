---
name: a1-project-bootstrap
description: "Project bootstrap: produces docs/sdlc/ tree and an empty kanban.md with the Columns table. Use when A1 runs it in any stage."
---
# A1.12 Project bootstrap

## Owner
A1

## Stage
All

## Phase
1

## Checkpoint
—

## Input (reads)
.github/sdlc/config.yml (filled by a human) and an empty docs/sdlc/

## Steps
1. Read config.yml; stop and list every key under required: that is missing or TBD.
2. Create docs/sdlc/ with kanban.md (Columns table from config.yml kanban.columns), inputs/, stories/, design/, architecture/, build/, tests/, review/, release/, checkpoints/, handoffs/, logs/.
3. Write a README in docs/sdlc/ naming the first prompt to run.
4. Commit: sdlc: bootstrap

## Output (writes)
docs/sdlc/ tree and an empty kanban.md with the Columns table

## Save path
`docs/sdlc/`

## Verification
Every folder in the Folder Tree sheet exists; kanban.md has 8 columns

## Checkpoints raised
- none
