---
description: Stage 4 Verify, tests. Act as A7: test plan, unit, component, integration and E2E tests, traceability, defects, results, quality summary; request CP-04.
agent: A7-test-engineer
---
Act as `.github/agents/A7-test-engineer.agent.md`. Read `.github/copilot-instructions.md` first. Requires all PRs merged to the test branch (config.yml git.test_branch).

## Read
- `docs/sdlc/stories/<ID>/` (stories.md, acceptance-criteria.md, ux-spec.md)
- The PR branch; `docs/sdlc/architecture/api/openapi.yaml`; `docs/sdlc/architecture/navigation.md`
- `.github/sdlc/config.yml` (commands, coverage_threshold)
- Templates: `.github/sdlc/templates/test-plan.md`, `defect.md`

## Run, in order
1. `.github/skills/a7-test-plan-creation/SKILL.md` (A7.01)
2. `.github/skills/a7-unit-test-writing/SKILL.md` (A7.02)
3. `.github/skills/a7-component-testing/SKILL.md` (A7.03)
4. `.github/skills/a7-integration-testing/SKILL.md` (A7.04)
5. `.github/skills/a7-end-to-end-test-scripting/SKILL.md` (A7.05)
6. `.github/skills/a7-requirement-to-test-traceability/SKILL.md` (A7.06)
7. `.github/skills/a7-defect-report-writing/SKILL.md` (A7.07) — per failed test
8. `.github/skills/a7-test-results-writer/SKILL.md` (A7.08)
9. `.github/skills/a7-quality-gate-summary/SKILL.md` (A7.09)

## Write
tests/e2e/, frontend/tests/, backend/tests/; docs/sdlc/tests/: test-plan-<ID>.md, traceability-<ID>.md, results-<run>.md, defects/BUG-<n>.md, quality-summary-<ID>.md.

## Checkpoint
Request CP-04 Quality GO / NO-GO through A1.05. Do not record GO or NO-GO. Stop when the checkpoint is OPEN.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
