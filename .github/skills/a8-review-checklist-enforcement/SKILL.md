---
name: a8-review-checklist-enforcement
description: "Review checklist enforcement: produces Checklist result. Use when A8 runs it in the Verify stage."
---
# A8.03 Review checklist enforcement

## Owner
A8

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
PR checklist and review checklist from config

## Steps
1. Check each checklist item.
2. Mark present or missing.
3. Block the PR if a required item is missing

## Output (writes)
Checklist result

## Save path
`docs/sdlc/review/<PR>-checklist.md`

## Verification
Every item is marked present or missing

## Checkpoints raised
- none
