---
name: a8-release-checklist
description: "Release checklist: produces Release checklist and CP-05 request. Use when A8 runs it in the Release stage (checkpoint: CP-05)."
---
# A8.10 Release checklist

## Owner
A8

## Stage
Release

## Phase
1

## Checkpoint
CP-05

## Input (reads)
Quality summary (CP-04 GO), security results, changelog, deploy config

## Steps
1. Check each item: tests green, CP-04 GO recorded, secrets scan clean, config reviewed, rollback plan written.
2. Mark evidence per item.
3. Request CP-05 from the named approver

## Output (writes)
Release checklist and CP-05 request

## Save path
`docs/sdlc/release/checklist-<version>.md`

## Verification
Every item has evidence; the agent does not approve

## Checkpoints raised
- none
