# Decisions — P-2026-001-saudi-hotels

Every decision, change and gate result, newest at the bottom of each section. Written by `/ba-approve`; you can also add entries by hand using the same format. Never delete an entry: if a decision is reversed, add a new one that says so.

## Decision log (DEC)

<!--
### DEC-001 · Approved REQ-014, REQ-015
- date: 2026-09-28
- decided-by: (your name)
- decision: What was decided, in one or two lines.
- items: REQ-014 (AI-CHECKED → APPROVED), REQ-015 (REVIEWED → APPROVED)
- reason: Why.
- evidence: Sources or answers relied on.
- alternatives: Options considered and not taken, or "none".
- impact: What this changes.
-->

### DEC-001 · Approved the project profile
- date: 2026-09-28
- decided-by: the BA
- decision: Approved `profile.md` as updated with the client's round 1 and round 2 answers: basics, size `complex` (suggested), depth per phase, domain notes, extra checks and stakeholders.
- items: profile.md (AI-DRAFT → APPROVED)
- reason: not stated
- evidence: `checks/check-2-2026-09-28.md` (finding C2-11); `inputs/client-answers-2026-09-28.md`; `inputs/client-answers-round-2-2026-09-28.md`
- alternatives: none
- impact: Gate 1 criterion "Size and depth in `profile.md` are reviewed" is now met. The gate itself is not recorded yet; that needs `/ba-approve gate 1 <result>`.

### DEC-002 · Reviewed 02-discover.md section "Stakeholders"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Stakeholders" section of `02-discover.md` as refreshed after round 3.
- items: 02-discover.md "Stakeholders" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `inputs/client-answers-round-3-2026-09-28.md`; `items.md` (REQ-064, DEP-009 to DEP-012)
- alternatives: none
- impact: One of the 8 Discover sections is now reviewed. Check 3 finding C3-16 stays open until `/ba-check` is run again.

### DEC-003 · Reviewed 02-discover.md section "Current state"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Current state" section of `02-discover.md` as refreshed after round 3.
- items: 02-discover.md "Current state" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `inputs/client-answers-round-3-2026-09-28.md`; `items.md` (PRB-004, PRB-006, ASM-003, REQ-055, RULE-034, RULE-035)
- alternatives: none
- impact: Two of the 8 Discover sections are now reviewed. Check 3 finding C3-16 stays open until `/ba-check` is run again.

### DEC-004 · Reviewed 02-discover.md section "Current workflows"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Current workflows" section of `02-discover.md` as refreshed after round 3.
- items: 02-discover.md "Current workflows" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `inputs/client-answers-round-3-2026-09-28.md`; `items.md` (PRB-004, PRB-005, PRB-006, RULE-034, RULE-035, RISK-001, RISK-008)
- alternatives: none
- impact: Three of the 8 Discover sections are now reviewed. Check 3 finding C3-16 stays open until `/ba-check` is run again.

### DEC-005 · Reviewed 02-discover.md section "Current systems, data and integrations"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Current systems, data and integrations" section of `02-discover.md` as refreshed after round 3.
- items: 02-discover.md "Current systems, data and integrations" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `inputs/client-answers-round-3-2026-09-28.md`; `items.md` (PRB-004, PRB-006, RULE-011, DEP-005, Q-045, Q-068, Q-069)
- alternatives: none
- impact: Four of the 8 Discover sections are now reviewed. Check 3 finding C3-16 stays open until `/ba-check` is run again.

### DEC-006 · Reviewed 03-define.md section "Problem statement"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Problem statement" section of `03-define.md`.
- items: 03-define.md "Problem statement" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `inputs/client-answers-round-3-2026-09-28.md`; `items.md` (PRB-003, PRB-004, PRB-005, PRB-006, ASM-003, NEED-003, GOAL-004)
- alternatives: none
- impact: One of the 11 Define sections is now reviewed. Gate 3 also needs a goal with a success measure to be `REVIEWED`; GOAL-004 is still `AI-DRAFT` and its 50% is not yet confirmed with the client (check 4, C4-02).

### DEC-007 · Reviewed 03-define.md section "Root causes"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Root causes" section of `03-define.md`, including its `UNKNOWN` (why guests choose the booking sites) and its inferred cause (double bookings).
- items: 03-define.md "Root causes" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `items.md` (PRB-003, PRB-004, PRB-005, PRB-006, RISK-001, ASM-003)
- alternatives: none
- impact: Two of the 11 Define sections are now reviewed. Why guests choose the booking sites over the client's own site is still `UNKNOWN`; no question about it is in `items.md` yet.

### DEC-008 · Reviewed 03-define.md section "Desired future state"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Desired future state" section of `03-define.md`, including its proposed December list.
- items: 03-define.md "Desired future state" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `items.md` (GOAL-004, NEED-003, REQ-002, REQ-003, REQ-009, REQ-019, REQ-026, REQ-028, REQ-030, REQ-048, REQ-053, REQ-064, REQ-065, REQ-066)
- alternatives: none
- impact: Three of the 11 Define sections are now reviewed. The December list is still proposed (Q-070 open) and the 50% target (GOAL-004) is not yet confirmed with the client.

### DEC-009 · Reviewed 03-define.md section "Non-goals"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Non-goals" section of `03-define.md`. The client has stated no non-goals himself; the section is built from his "not now" and "no" answers.
- items: 03-define.md "Non-goals" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `items.md` (REQ-005, REQ-007, REQ-032, REQ-033, REQ-034, REQ-035, REQ-039, REQ-054, RULE-009, REQ-059)
- alternatives: none
- impact: Four of the 11 Define sections are now reviewed. The December exclusions stay proposals until Q-070 is answered.

### DEC-010 · Reviewed 03-define.md section "Business rules"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Business rules" section of `03-define.md`, which lists all 32 active RULE items by kind, including rules still in conflict or with open questions.
- items: 03-define.md "Business rules" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `items.md` (RULE-001 to RULE-035, active ones)
- alternatives: none
- impact: Five of the 11 Define sections are now reviewed. RULE-007 and RULE-027 (date changes) and RULE-020 and RULE-028 (data deletion) are still in conflict (Q-040, Q-041); RULE-006, RULE-016, RULE-021, RULE-023 and RULE-033 have open questions.

### DEC-011 · Reviewed 03-define.md section "Integrations"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Integrations" section of `03-define.md`, including its `UNKNOWN` failure behaviours.
- items: 03-define.md "Integrations" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `items.md` (DEP-001, DEP-004, DEP-006, REQ-013, REQ-029, REQ-036, REQ-038, REQ-042, REQ-045, REQ-051, REQ-052, REQ-063, RULE-011, RULE-017, RISK-001, RISK-007)
- alternatives: none
- impact: Six of the 11 Define sections are now reviewed. The payment provider, the sync method and the domain are not decided yet (DEP-001, RISK-007, REQ-063), and most failure behaviours are `UNKNOWN`.

### DEC-012 · Reviewed 03-define.md section "Future workflows"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Future workflows" section of `03-define.md`, including cells that say "Not stated" and the phone and walk-in payment steps flagged in check 4 (C4-27).
- items: 03-define.md "Future workflows" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `items.md` (PRB-004, PRB-005, PRB-006, REQ-002, REQ-003, REQ-007, REQ-026, REQ-028, REQ-029, REQ-030, REQ-031, REQ-039, REQ-045, REQ-050, REQ-054, REQ-057, REQ-063, RULE-011, RULE-012, RULE-016, RULE-024, RULE-033, RULE-034, RULE-035, DEP-011)
- alternatives: none
- impact: Seven of the 11 Define sections are now reviewed. Several "today" cells are `Not stated`, and whether the phone and walk-in payment steps describe today's practice or the new platform is still open (check 4, C4-27).

### DEC-013 · Reviewed 03-define.md section "Key journeys"
- date: 2026-09-28
- decided-by: the BA
- decision: Reviewed the "Key journeys" section of `03-define.md` (eight journeys, each with at least one failure path), including steps and failure paths that are still `UNKNOWN`.
- items: 03-define.md "Key journeys" (AI-DRAFT → REVIEWED)
- reason: not stated
- evidence: `items.md` (REQ-002, REQ-003, REQ-009, REQ-013, REQ-016, REQ-017, REQ-019, REQ-028, REQ-029, REQ-030, REQ-031, REQ-036, REQ-040, REQ-047, REQ-048, REQ-049, REQ-050, REQ-064, REQ-065, REQ-066, REQ-068, REQ-073, REQ-074, REQ-075, RULE-006, RULE-007, RULE-012, RULE-014, RULE-015, RULE-016, RULE-017, RULE-018, RULE-027, RULE-033, RULE-034, RULE-035)
- alternatives: none
- impact: Eight of the 11 Define sections are now reviewed. Who takes phone bookings after launch, a declined card, staff password reset and the booking-site double-booking rule are still `UNKNOWN`; J3 and J4 rest on the phone and walk-in answer flagged in check 4 (C4-27).

## Change log (CHG)

<!--
### CHG-001 · Refund window changed from 48h to 24h
- date:
- type: CLARIFICATION | BUG | SCOPE CHANGE | NEW REQUIREMENT | TECHNICAL CONSTRAINT | DESIGN DECISION | BUSINESS DECISION
- requested-by:
- change:
- reason:
- impact: items affected, effort, timeline, cost
- decision: accepted | rejected | deferred
- approved-by:
- items: new and superseded item IDs
-->

## Gate records (GATE)

<!--
### GATE-001 · Phase 1 Intake — PASS
- date:
- decided-by:
- result: PASS | PARTIAL | FAIL | BLOCKED
- reason:
- open-risks: (for PARTIAL)
- go-back-to: (for FAIL)
- waiting-on: (for BLOCKED)
- check-report: checks/<file>
-->

### GATE-001 · Phase 1 Intake — PARTIAL
- date: 2026-09-28
- decided-by: the BA
- result: PARTIAL
- reason: not stated
- open-risks: C2-01 (first-year goal is 30% or 50%, and the starting share is a guess); C2-02 (staff roles and permissions contradict each other); C2-03 (Saudi rules on VAT, ZATCA invoicing and privacy are unknown)
- check-report: checks/check-2-2026-09-28.md

### GATE-002 · Phase 2 Discover — PARTIAL
- date: 2026-09-28
- decided-by: the BA
- result: PARTIAL
- reason: not stated
- open-risks: C4-01 (Saudi rules on VAT, ZATCA e-invoicing, privacy and card handling are unknown; waiting on the accountant, Q-049 and DEP-012)
- check-report: checks/check-4-2026-09-28.md
