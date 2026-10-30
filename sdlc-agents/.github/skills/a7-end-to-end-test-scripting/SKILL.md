---
name: a7-end-to-end-test-scripting
description: "End-to-end test scripting (web): produces E2E test scripts. Use when A7 runs it in the Verify stage."
---
# A7.05 End-to-end test scripting (web)

## Owner
A7

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
User flows from the UX spec and navigation map

## Steps
1. Script each flow from the story.
2. Use a real browser.
3. Assert the visible result from the acceptance criterion

## Output (writes)
E2E test scripts

## Save path
`tests/e2e/`

## Verification
Every acceptance criterion with a flow has a passing E2E test

## Checkpoints raised
- none
