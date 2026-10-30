# Checkpoints

| ID | Name | Stage | Who decides | Raised when | Decides | Evidence | If unanswered |
|---|---|---|---|---|---|---|---|
| CP-01 | Ready | Understand | Product Owner | After A2.09 Definition of Ready check passes | Stories, acceptance criteria and scope are correct and complete enough to design from | docs/sdlc/stories/<ID>/ready-report.md and the files it lists | Item stays in Backlog |
| CP-02 | Design approval | Plan | Product Owner (plus a designer if one exists) | After A4.10 sends the request with the UI baseline or extracted design | UI/UX baseline or extracted design, tokens, layout plan, navigation map; adoption of the theme file | docs/sdlc/design/<ID>/ and docs/sdlc/architecture/navigation.md | Design stays PROPOSED; no code uses it |
| CP-03 | Architecture approval | Plan | Tech Lead (or Product Owner if none) | After A4.08 design doc and A4.09 tasks are written | Stack ADR, architecture, data model, API contract, repo structure, task breakdown | docs/sdlc/architecture/design-doc-<ID>.md and ADRs | No build task starts |
| CP-04 | Quality GO / NO-GO | Verify | QA Lead (or Product Owner if none) | After A7.09 quality summary | Whether test results, traceability and open defects allow release preparation | docs/sdlc/tests/quality-summary-<ID>.md | Item stays in Testing |
| CP-05 | Release approval | Release | Product Owner | After A8.10 release checklist is complete | Whether the version ships, and the rollout plan | docs/sdlc/release/checklist-<version>.md | Nothing ships |
| CP-06 | Fix-loop limit reached | Verify | Tech Lead | When A8.04 loop count reaches the limit in config (PROPOSED 3) | Continue fixing, accept with a note, or send the item back to Design | docs/sdlc/review/<PR>-loops.md | PR stays blocked |
| CP-07 | Missing requirement / TBD | Any | Product Owner | When any skill finds a gap in the source and logs a TBD | The missing value, chosen from the options listed | docs/sdlc/checkpoints/CP-07-<topic>.md | Value stays TBD; dependent items stay blocked |
| CP-08 | Figma access (phase 2) | Understand | Repo owner | Before A2.14 reads a Figma file | Grant read access to the file; confirm the file is the source of truth | Figma link in the manifest | Figma skills do not run; screenshot path is used |
| CP-09 | Security and privacy sign-off (phase 2) | Verify | Security owner (or Tech Lead) | After A8.12 and A8.14 findings and S.12 checklist | Whether findings are accepted, fixed, or block release | docs/sdlc/review/<PR>-security.md, <PR>-pii.md, <ID>-compliance.md | Release blocked |

A checkpoint file is `docs/sdlc/checkpoints/<ID>-<name>.md` with fields: Status (OPEN | APPROVED | REJECTED), Decided by, Date, Decision, Evidence read. Agents write OPEN only.
