---
name: shared-git-operations
description: "Git operations: produces Branch, commit, PR link, CI status. Use when any of A1,A5,A6,A8 runs it in any stage."
---
# S.06 Git operations

## Owner
Shared (used by: A1,A5,A6,A8)

## Stage
All

## Phase
1

## Checkpoint
—

## Input (reads)
Branch, commit or PR request

## Steps
1. Create the branch named <type>/<task-ID>.
2. Commit with a conventional message.
3. Open the PR.
4. Read CI status. Only A1 commits docs/sdlc/kanban.md

## Output (writes)
Branch, commit, PR link, CI status

## Save path
`git (no file)`

## Verification
CI status is recorded in the handoff file

## Checkpoints raised
- none
