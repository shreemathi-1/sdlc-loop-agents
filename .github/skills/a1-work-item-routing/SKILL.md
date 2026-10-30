---
name: a1-work-item-routing
description: "Work item routing: produces Routing decision: next agent and reason. Use when A1 runs it in the Understand stage."
---
# A1.04 Work item routing

## Owner
A1

## Stage
Understand

## Phase
1

## Checkpoint
—

## Input (reads)
Item in Backlog or Ready, with its type (story, task, bug)

## Steps
1. Read item type.
2. Look up the next agent in the agent table.
3. Write the handoff request

## Output (writes)
Routing decision: next agent and reason

## Save path
`docs/sdlc/handoffs/<ID>-route.md`

## Verification
Routing matches the agent table in .github/sdlc/config.yml

## Checkpoints raised
- none
