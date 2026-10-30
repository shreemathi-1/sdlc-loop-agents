---
name: a3-screenshot-design-extraction
description: "Screenshot design extraction: produces Extracted design values, all marked estimated. Use when A3 runs it in the Plan stage (checkpoint: CP-02)."
---
# A3.02 Screenshot design extraction

## Owner
A3

## Stage
Plan

## Phase
1

## Checkpoint
CP-02

## Input (reads)
Screen inventory (A2.06) and screenshot files

## Steps
1. Read colours, font sizes, spacing and radius from each screenshot.
2. Record each value as estimated.
3. Group values into candidate tokens

## Output (writes)
Extracted design values, all marked estimated

## Save path
`docs/sdlc/design/<ID>/extracted-design.md`

## Verification
Every value is marked estimated and cites a region ID

## Checkpoints raised
- none
