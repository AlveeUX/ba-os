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
