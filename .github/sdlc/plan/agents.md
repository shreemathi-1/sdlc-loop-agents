# Agents

| ID | Agent | Role | Stage | Reads | Writes | Permissions | Must not |
|---|---|---|---|---|---|---|---|
| A1 | Orchestrator | Routes work, runs stage gates, keeps kanban.md and the checkpoint files, records every handoff | All | Status events from agents; docs/sdlc/kanban.md; checkpoint decisions from humans | Updated kanban.md, gate results, handoff files, checkpoint files, board reports | Write docs/sdlc/kanban.md, docs/sdlc/checkpoints/, docs/sdlc/handoffs/, docs/sdlc/logs/; read everything | Change application code; set a checkpoint to APPROVED |
| A2 | Requirements Analyst | Turns a story, epic or screenshot into stories, acceptance criteria, scope and a UX spec | Understand | docs/sdlc/inputs/<ID>/ (text, epic, screenshots; Figma link in phase 2) | docs/sdlc/stories/<ID>/ (manifest, stories, acceptance criteria, scope, screen inventory, UX states, UX spec, ready report) | Write docs/sdlc/stories/; read inputs; read Figma (phase 2) | Write kanban.md; invent requirements; mark Ready |
| A3 | UI/UX Designer | Plans the UI from text (PROPOSED baseline) or extracts it from a screenshot or Figma; writes tokens and component specs | Plan | Approved stories and UX spec; screenshots or Figma inventory | docs/sdlc/design/<ID>/ (baseline, layout plan, tokens.json, components, responsive rules, checklist); draft theme file | Write docs/sdlc/design/ and frontend/src/theme/ (draft) | Adopt a theme without CP-02; invent brand values without PROPOSED label |
| A4 | Architect | Chooses the stack, designs architecture, data model, API contract, navigation and task breakdown | Plan | Approved stories, scope, NFRs, UX spec, design baseline | docs/sdlc/architecture/ (ADRs, stack analysis, architecture, data model, openapi.yaml, navigation, repo structure, design doc, tasks) | Write docs/sdlc/architecture/; read code | Approve its own ADRs; write application code |
| A5 | Frontend Developer | Builds screens and components for web or mobile from the approved design and tasks | Build | One task (A4.09), component specs, tokens, layout plan, navigation map, openapi.yaml, mock data | frontend/ source, task plan, task gate result, PR | Write frontend/; create branches and PRs | Change backend/; merge its own PR; skip the task gate |
| A6 | Backend Engineer | Builds the API, data model, auth, mock data and backend deploy config from the contract | Build | openapi.yaml, data model, one task (A4.09), security review (phase 2) | backend/ source, migrations, seed data, contract validation report, Dockerfile, PR | Write backend/ and deploy/backend/; create branches and PRs | Change frontend/; merge its own PR; store secret values in files |
| A7 | Test Engineer | Plans and writes tests, traces every criterion to a test, reports results and prepares the quality gate | Verify | Stories, acceptance criteria, PR branch, openapi.yaml, built screens | docs/sdlc/tests/ (plan, traceability, results, defects, quality summary); test files under tests/, frontend/tests/, backend/tests/ | Write tests/ and docs/sdlc/tests/; run the app and tests | Change application source beyond test files; record GO or NO-GO |
| A8 | Reviewer & Release | Reviews PRs for code, design and security; prepares CI, versioning and the release checklist | Verify, Release | PR diff, CI results, ADRs, tokens, quality summary (CP-04 GO) | docs/sdlc/review/ (findings by severity), .github/workflows/, CHANGELOG.md, docs/sdlc/release/ (checklist) | Read all code; write .github/workflows/, CHANGELOG.md, docs/sdlc/review/, docs/sdlc/release/ | Approve its own release; merge without CP-04 GO; exceed the fix-loop limit without CP-06 |

## Skills owned per agent (phase 1 only)

- **A1**: A1.01, A1.02, A1.03, A1.04, A1.05, A1.06, A1.12
- **A2**: A2.01, A2.02, A2.03, A2.04, A2.05, A2.06, A2.07, A2.08, A2.09, A2.10, A2.11
- **A3**: A3.01, A3.02, A3.03, A3.04, A3.05, A3.06, A3.07
- **A4**: A4.01, A4.02, A4.03, A4.04, A4.05, A4.06, A4.07, A4.08, A4.09, A4.10
- **A5**: A5.01, A5.02, A5.03, A5.04, A5.05, A5.06
- **A6**: A6.01, A6.02, A6.03, A6.05, A6.06, A6.07, A6.08
- **A7**: A7.01, A7.02, A7.03, A7.04, A7.05, A7.06, A7.07, A7.08, A7.09
- **A8**: A8.01, A8.02, A8.03, A8.04, A8.05, A8.06, A8.07, A8.08, A8.09, A8.10
- **Shared (all agents may call)**: S.01, S.02, S.03, S.04, S.05, S.06, S.07, S.08, S.09, S.10
