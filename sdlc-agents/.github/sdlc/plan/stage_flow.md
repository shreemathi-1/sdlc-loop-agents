# Stage flow

| Stage | Agent | Reads | Writes | Checkpoint | Kanban column |
|---|---|---|---|---|---|
| 0 Intake | A1 | docs/sdlc/inputs/<ID>/ (what the user drops in: story.md, epic.md, screenshots/*.png, figma.md) | kanban.md Backlog row; route to A2 | — | Backlog |
| 1 Understand | A2 | docs/sdlc/inputs/<ID>/ | docs/sdlc/stories/<ID>/: manifest.md, features.md (epic), stories.md, acceptance-criteria.md, scope.md, screen-inventory.md (screenshot), ux-states.md, ux-spec.md, scope-check.md, ready-report.md | CP-01 Ready | Backlog → Ready |
| 2 Plan: design | A3 | docs/sdlc/stories/<ID>/, screenshots | docs/sdlc/design/<ID>/: ui-baseline.md or extracted-design.md, layout-plan.md, tokens.json, components.md, responsive.md, ui-checklist.md; draft frontend/src/theme/ | CP-02 Design approval | Ready → Design |
| 2 Plan: architecture | A4 | docs/sdlc/stories/<ID>/, docs/sdlc/design/<ID>/ | docs/sdlc/architecture/: adr/ADR-*.md, stack-analysis.md, architecture.md, data-model.md, api/openapi.yaml, navigation.md, repo-structure.md, design-doc-<ID>.md, tasks-<ID>.md | CP-03 Architecture approval | Design |
| 3 Build: backend | A6 | tasks-<ID>.md, openapi.yaml, data-model.md | backend/ (migrations, api, validation, seed/synthetic, config, Dockerfile); docs/sdlc/build/plans, task-gate, pr files; docs/sdlc/tests/contract-<run>.md | — | Design → In Progress |
| 3 Build: frontend | A5 | tasks-<ID>.md, design/<ID>/, navigation.md, openapi.yaml, seed data | frontend/ (components, screens, state, routes, api, theme); docs/sdlc/build/plans, task-gate, pr files | — | In Progress |
| 4 Verify: tests | A7 | stories/<ID>/, PR branch, openapi.yaml | tests/, frontend/tests/, backend/tests/; docs/sdlc/tests/: test-plan, traceability, results, defects, quality-summary | CP-04 Quality GO | In Progress → Testing |
| 4 Verify: review | A8 | PR diff, CI results, ADRs, tokens.json | docs/sdlc/review/<PR>-*.md (review, summary, checklist, secrets, design, loops) | CP-06 if loop limit | Testing → Review |
| 5 Release | A8 | quality-summary (GO), review files, CHANGELOG | CHANGELOG.md, .github/workflows/ci.yml and deploy.yml, deploy/, docs/sdlc/release/checklist-<version>.md | CP-05 Release approval | Review → Release Ready → Done |

## Kanban columns (docs/sdlc/kanban.md)

| Column | Owner | Entry | Exit criteria | Human |
|---|---|---|---|---|
| Backlog | A1 | Input recorded in inputs/<ID>/ | Routed to A2 | No |
| Ready | A2 | Stories, criteria, scope, UX spec written | Definition of Ready passed; CP-01 APPROVED | CP-01 |
| Design | A3, A4 | Item is Ready | CP-02 and CP-03 APPROVED; tasks written | CP-02, CP-03 |
| In Progress | A5, A6 | Tasks exist | Every task: task gate passed, PR open, CI green | No |
| Testing | A7 | All PRs merged to the test branch | Traceability complete; CP-04 APPROVED | CP-04 |
| Review | A8 | CP-04 GO | No blocker or major open; loop count under limit | CP-06 only at limit |
| Release Ready | A8 | Review passed | Release checklist complete; CP-05 APPROVED | CP-05 |
| Done | A1 | CP-05 APPROVED | Deployed | No |
