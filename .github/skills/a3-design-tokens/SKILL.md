---
name: a3-design-tokens
description: "Design tokens (extracted or PROPOSED): produces tokens.json with reason and source per token. Use when A3 runs it in the Plan stage (checkpoint: CP-02)."
---
# A3.04 Design tokens (extracted or PROPOSED)

## Owner
A3

## Stage
Plan

## Phase
1

## Checkpoint
CP-02

## Input (reads)
Extracted design values (A3.02) or PROPOSED defaults

## Steps
1. Set colour, type scale, spacing and radius tokens.
2. Give each token a reason or source.
3. Check text contrast against 4.5:1 with a tool.
4. Save as JSON

## Output (writes)
tokens.json with reason and source per token

## Save path
`docs/sdlc/design/<ID>/tokens.json`

## Verification
Every text colour pair passes 4.5:1 per the tool output

## Checkpoints raised
- none
