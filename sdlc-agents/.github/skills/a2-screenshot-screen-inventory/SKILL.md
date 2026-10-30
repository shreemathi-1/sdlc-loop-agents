---
name: a2-screenshot-screen-inventory
description: "Screenshot screen inventory: produces Screen inventory: screen ID, region IDs, visible text, controls. Use when A2 runs it in the Understand stage."
---
# A2.06 Screenshot screen inventory

## Owner
A2

## Stage
Understand

## Phase
1

## Checkpoint
—

## Input (reads)
Screenshot files (SS-01…)

## Steps
1. Open each screenshot.
2. Name each screen and region with an ID (SS-01-R1).
3. List visible text, buttons, inputs and navigation.
4. Mark values read from pixels as estimated

## Output (writes)
Screen inventory: screen ID, region IDs, visible text, controls

## Save path
`docs/sdlc/stories/<ID>/screen-inventory.md`

## Verification
Every screen has a screenshot region ID; estimates are labelled

## Checkpoints raised
- none
