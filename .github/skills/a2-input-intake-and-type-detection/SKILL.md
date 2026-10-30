---
name: a2-input-intake-and-type-detection
description: "Input intake and type detection: produces Input manifest: ID, type, file path, date received. Use when A2 runs it in the Understand stage."
---
# A2.01 Input intake and type detection

## Owner
A2

## Stage
Understand

## Phase
1

## Checkpoint
—

## Input (reads)
Raw input in docs/sdlc/inputs/<ID>/: text story, epic text, screenshot files (PNG/JPG), Figma link (phase 2)

## Steps
1. List every input file or link.
2. Assign an ID: T-01 text, SS-01 screenshot, FIG-01 Figma.
3. Detect type: story, epic, screenshot, Figma, mixed.
4. Write the manifest

## Output (writes)
Input manifest: ID, type, file path, date received

## Save path
`docs/sdlc/stories/<ID>/manifest.md`

## Verification
Every input has an ID, type and file path

## Checkpoints raised
- none
