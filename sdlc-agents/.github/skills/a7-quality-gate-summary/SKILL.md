---
name: a7-quality-gate-summary
description: "Quality gate summary: produces Quality summary and CP-04 request. Use when A7 runs it in the Verify stage (checkpoint: CP-04)."
---
# A7.09 Quality gate summary

## Owner
A7

## Stage
Verify

## Phase
1

## Checkpoint
CP-04

## Input (reads)
Test plan, traceability, results, coverage, defects

## Steps
1. Summarise results, coverage, open defects.
2. List open risks.
3. Request CP-04 GO or NO-GO from the named approver.
4. Do not record the decision

## Output (writes)
Quality summary and CP-04 request

## Save path
`docs/sdlc/tests/quality-summary-<ID>.md`

## Verification
Summary cites each figure to its file

## Checkpoints raised
- none
