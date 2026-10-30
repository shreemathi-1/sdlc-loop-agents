---
name: a2-scope-check-against-input
description: "Scope check against input: produces Scope check table: story, input ID, status. Use when A2 runs it in the Understand stage."
---
# A2.11 Scope check against input

## Owner
A2

## Stage
Understand

## Phase
1

## Checkpoint
—

## Input (reads)
Stories and input manifest

## Steps
1. Map each story to an input ID.
2. Flag any story without a source.
3. Move suggested extra features to a decision request (S.03), not into scope

## Output (writes)
Scope check table: story, input ID, status

## Save path
`docs/sdlc/stories/<ID>/scope-check.md`

## Verification
Every story has an input ID or a flag

## Checkpoints raised
- none
