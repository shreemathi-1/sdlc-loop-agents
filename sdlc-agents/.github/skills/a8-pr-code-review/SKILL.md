---
name: a8-pr-code-review
description: "PR code review: produces Review comments. Use when A8 runs it in the Verify stage."
---
# A8.01 PR code review

## Owner
A8

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
PR diff, conventions, ADRs

## Steps
1. Read the diff.
2. Check logic, naming and convention rules.
3. Write each comment with its file and line

## Output (writes)
Review comments

## Save path
`docs/sdlc/review/<PR>-review.md`

## Verification
Every comment cites a file and line

## Checkpoints raised
- none
