---
name: a7-unit-test-writing
description: "Unit test writing: produces Unit test files. Use when A7 runs it in the Verify stage."
---
# A7.02 Unit test writing

## Owner
A7

## Stage
Verify

## Phase
1

## Checkpoint
—

## Input (reads)
Source files from the PR

## Steps
1. Write a test for each branch and state.
2. Use the test runner in config.
3. Run the tests

## Output (writes)
Unit test files

## Save path
`frontend/tests/unit/, backend/tests/unit/`

## Verification
Tests pass in the task gate (S.07)

## Checkpoints raised
- none
