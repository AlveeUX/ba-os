# Lessons

Lessons from projects, without client names, prices or personal data. Newest at the bottom.

- `/ba-learn` drafts lessons here as `AI-DRAFT`, from a BA-OS project or a project done outside BA-OS. It can run at any gate, not only at the end.
- You approve or reject them with `/ba-approve lesson <IDs> approved` (or `rejected "<reason>"`).
- `/ba-start` lists `APPROVED` lessons whose `applies-when` matches a new project in its profile. `/ba-check` asks the `check-question` of every `APPROVED` lesson listed in the profile.
- Never change the text of an `APPROVED` lesson. Add new evidence to it, or write a new lesson.

<!--
### L-000 · One-line lesson title
- status: AI-DRAFT | APPROVED | REJECTED
- date:
- project type:
- applies-when: the situation in which this lesson matters (so /ba-start can match it)
- evidence: project ID with item, finding, DEC or GATE IDs; or an outside project and its file paths
- lesson: what to do differently, in one to three lines
- check-question: one question /ba-check can ask on a future project
- proposed-change: the BA-OS file and the text to add or change
- change made to BA-OS: (file and date, or "none yet")
- history:
  - <date> drafted by /ba-learn from <source>
-->

### L-001 · Target numbers hide disagreements about definitions
- status: AI-DRAFT
- date: 2026-10-24
- project type: hotel booking website; hotel-group KPI and reporting
- applies-when: a GOAL or KPI has a numeric target, or several locations or teams report the same number
- evidence: P-2026-001 — direct-booking share was about 10% by number of bookings (ASM-003) but 8–10% by money (Q-062); the goal had to be restated by money (GOAL-004 superseding GOAL-002 and GOAL-003), and "direct" needed its own rule (RULE-029). Outside practice project (hotel-group KPI reporting RFP, portfolio repository) — the properties calculated occupancy differently, so the real problem was the definition, not the data.
- lesson: Before Define closes, record each target number's formula, unit (count, nights or money), what it includes, and who owns the definition. When locations define a number differently, treat that as a root cause, not a reporting detail.
- check-question: For each GOAL or KPI with a number, are the formula, unit and definition owner recorded?
- proposed-change: question in `knowledge/patterns/common-gaps.md` (Content and data); KPI questions in `knowledge/patterns/hospitality.md`
- change made to BA-OS: `common-gaps.md` and `hospitality.md`, 2026-10-24
- history:
  - 2026-10-24 drafted from P-2026-001 and an outside practice project

### L-002 · Replacement projects need a cut-over plan
- status: AI-DRAFT
- date: 2026-10-24
- project type: hotel booking website; hotel-group KPI and reporting
- applies-when: the product replaces an existing website, spreadsheet, system or manual process
- evidence: P-2026-001 — the old site is switched off on launch day with no side-by-side running (REQ-054), and no fallback was described in any check from check 2 to check 8 (C8-07); a shared spreadsheet is today's single source of truth (PRB-004). Outside practice project — the plan ran a pilot alongside the existing process for a full monthly cycle before rollout.
- lesson: Ask early how the switch happens: side-by-side running, a pilot, the data that must exist on launch day, the fallback if launch fails, and who decides to use it.
- check-question: Does the project replace something, and if so, is there a cut-over plan with a fallback?
- proposed-change: "Launch and cut-over" section in `knowledge/patterns/common-gaps.md`
- change made to BA-OS: `common-gaps.md`, 2026-10-24
- history:
  - 2026-10-24 drafted from P-2026-001 and an outside practice project

### L-003 · Know which side of the RFP you are on
- status: AI-DRAFT
- date: 2026-10-24
- project type: hotel-group KPI and reporting (RFP)
- applies-when: the input is an RFP, RFQ or tender, or the client mentions one
- evidence: Outside practice project — a full client-side RFP was prepared when the job needed the agency's response to an RFP; the response had to be built afterwards as a separate deliverable with a different structure and voice (folders 06-rfp-and-commercial and 09-rfp-response).
- lesson: At Intake, confirm whether we write the RFP for the client or respond to it, and what the client expects back. A response follows the RFP's own structure and answers every requirement and evaluation criterion.
- check-question: Are the input type and the expected deliverable recorded, and for an RFP, which side we are on?
- proposed-change: profile fields, `/ba-start` question 4, an Intake section, a Gate 1 criterion, and `templates/exports/rfp-response.md`
- change made to BA-OS: `templates/profile.md`, `.claude/skills/ba-start/SKILL.md`, `templates/stages/01-intake.md`, `method/phases.md`, `templates/exports/rfp-response.md`, 2026-10-24
- history:
  - 2026-10-24 drafted from an outside practice project

### L-004 · An open build-or-buy decision makes the estimate conditional
- status: AI-DRAFT
- date: 2026-10-24
- project type: hotel-group KPI and reporting (RFP)
- applies-when: before Commit, on any project where an existing product could meet the need
- evidence: Outside practice project — the client had not decided between buying a configurable platform and a bespoke build; the response could only be scoped for a build and had to warn that a buy decision would change almost everything downstream.
- lesson: Make build, buy or configure an explicit, recorded decision in Shape. Do not estimate until it is made, or estimate each option separately.
- check-question: Is build, buy or configure recorded as a DEC before the estimate?
- proposed-change: first row of Solution options in `templates/stages/04-shape.md`; a stop rule in Readiness to estimate in `templates/stages/05-commit.md`; a question in `common-gaps.md`
- change made to BA-OS: `04-shape.md`, `05-commit.md`, `common-gaps.md`, 2026-10-24
- history:
  - 2026-10-24 drafted from an outside practice project

### L-005 · An answer promised twice is a risk, not a question
- status: AI-DRAFT
- date: 2026-10-24
- project type: hotel booking website
- applies-when: a Q or DEP item stays open across two or more client rounds
- evidence: P-2026-001 — the accountant's contact details (DEP-012, Q-049) were promised in rounds 3, 4 and 5 without arriving; three gates closed `PARTIAL` with the same tax and e-invoicing risk carried forward (GATE-001 C2-03, GATE-002 C4-01, GATE-003 C8-01), and each check only suggested chasing again.
- lesson: After two rounds, change approach: raise a RISK with its impact, offer research, price the unknown as a separate line or exclude it, and agree a decision date with the client.
- check-question: Is any Q or DEP still open after two or more client rounds?
- proposed-change: a stale-item rule in `.claude/skills/ba-check/SKILL.md`; a question in `common-gaps.md`
- change made to BA-OS: `ba-check/SKILL.md`, `common-gaps.md`, 2026-10-24
- history:
  - 2026-10-24 drafted from P-2026-001
