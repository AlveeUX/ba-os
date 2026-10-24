# Glossary

| Term | Meaning in BA-OS |
| --- | --- |
| Active project | The project named in `projects/active.md`; every `/ba-` command works on it |
| Baseline | The set of `APPROVED` items at the end of Shape and Commit; changes after it need a `CHG` |
| CHG | A change-log entry in `decisions.md` |
| Check | A run of `/ba-check`: a critic review plus a gate readiness check, saved in `checks/` |
| Compliance table | The table at the end of an RFP response listing every RFP requirement and evaluation criterion with our answer (`templates/exports/rfp-response.md`) |
| Cut-over | The switch from the old system or process to the new one: side-by-side running, pilot, launch-day data and fallback |
| DEC | A decision-log entry in `decisions.md` |
| Deliverable expected | What the client expects to receive from us (proposal, RFP response, estimate only…), recorded in `profile.md` |
| Depth | How much of a phase is done: `skip`, `light`, `standard`, `deep` |
| Evidence | The `source` and `quote` on an item; there is no separate evidence register |
| Finding (check) | A problem reported by `/ba-check`, numbered `C<run>-<n>`, for example `C3-07` |
| Finding (research) | A research result in `research/`, numbered `F-001` |
| Gate | The quality decision at the end of a phase: `PASS`, `PARTIAL`, `FAIL`, `BLOCKED` |
| GATE | A gate record in `decisions.md` |
| Input type | What the client gave us: rough idea, existing website or app, Figma file, specification, or an RFP / RFQ / tender, recorded in `profile.md` |
| Item | Anything tracked in `items.md`: GOAL, PRB, NEED, REQ, RULE, FEAT, ASM, Q, RISK, DEP |
| Label | How sure we are: `KNOWN`, `ASSUMPTION`, `UNKNOWN`, `CONFLICT` |
| Lesson | A reusable learning in `knowledge/lessons.md`, numbered `L-001`; drafted by `/ba-learn`, approved with `/ba-approve lesson` |
| Lite mode | The Simple-size setup with fewer stage files and fields |
| Orphan | An item whose `parent` is missing or points to an item that does not exist |
| Phase | One of the six working phases: Intake, Discover, Define, Shape, Commit, Deliver and learn |
| Profile | `profile.md`: type, size, depth, privacy, domain notes for one project |
| Screen inventory | The list of screens in `04-shape.md`, with role, FEAT, states and S/M/L complexity; UX and UI estimates use it |
| Skill | A `/ba-` command, defined in `.claude/skills/<name>/SKILL.md` |
| Stage | One of the 15 reasoning steps (Qualify … Loop) inside the phases |
| Status | Who has checked an item: `AI-DRAFT` → `AI-CHECKED` → `REVIEWED` → `CONFIRMED` → `APPROVED` |
| Trace chain | GOAL → PRB → NEED → REQ → FEAT, followed through `parent` fields |
