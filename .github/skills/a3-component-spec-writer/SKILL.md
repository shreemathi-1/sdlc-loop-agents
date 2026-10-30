---
name: a3-component-spec-writer
description: "Component spec writer: produces Component spec list. Use when A3 runs it in the Plan stage (checkpoint: CP-02)."
---
# A3.05 Component spec writer

## Owner
A3

## Stage
Plan

## Phase
1

## Checkpoint
CP-02

## Input (reads)
Layout plan and tokens

## Steps
1. List each component on each screen.
2. For each, write props, states, variants and sizes.
3. Refer to tokens by name only

## Output (writes)
Component spec list

## Save path
`docs/sdlc/design/<ID>/components.md`

## Verification
Each component lists its states

## Checkpoints raised
- none
