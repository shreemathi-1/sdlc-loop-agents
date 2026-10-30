---
description: Stage 5 Release. Act as A8: CI workflow, deploy workflow, version and changelog, release checklist; request CP-05.
agent: A8-reviewer-release
---
Act as `.github/agents/A8-reviewer-release.agent.md`. Read `.github/copilot-instructions.md` first. Requires review passed (no blocker or major open) and CP-04 GO.

## Read
- `docs/sdlc/tests/quality-summary-<ID>.md` (GO)
- `docs/sdlc/review/<PR>-*.md`
- `CHANGELOG.md`; merged PRs since the last release
- `.github/sdlc/config.yml` (commands, git)
- Template: `.github/sdlc/templates/release-checklist.md`

## Run, in order
1. `.github/skills/a8-ci-pipeline-configuration/SKILL.md` (A8.07)
2. `.github/skills/a8-build-and-deploy-automation/SKILL.md` (A8.08)
3. `.github/skills/a8-versioning-and-changelog/SKILL.md` (A8.09)
4. `.github/skills/a8-release-checklist/SKILL.md` (A8.10)

## Write
`.github/workflows/ci.yml`, `.github/workflows/deploy.yml`, `deploy/`, `CHANGELOG.md`, `docs/sdlc/release/checklist-<version>.md`.

## Checkpoint
Request CP-05 Release approval through A1.05. Stop when the checkpoint is OPEN. Nothing ships until a named approver writes APPROVED.

Last step, as A1: run `.github/skills/a1-kanban-update/SKILL.md` (A1.01) with this stage's status event, then link `docs/sdlc/kanban.md` in each checkpoint file so the approver can approve or edit the board with it. Only A1 writes kanban.md.
