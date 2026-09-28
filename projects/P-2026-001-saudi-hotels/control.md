# Control Center — P-2026-001-saudi-hotels

_Rebuilt by `/ba-status`. Do not edit by hand, except the Notes section at the bottom._

Last updated: 2026-09-28

## Right now

| | |
| --- | --- |
| Current phase | 1. Intake (gate not started) |
| Next required action | Resolve the top findings from check 2. The three high ones need answers from Yusuf: **C2-01** (goal 30% or 50%: Q-035, Q-057), **C2-02** (staff roles and permissions: Q-037, Q-038, Q-039, Q-033) and **C2-03** (Saudi rules: Q-049, for his accountant). Two quick fixes are yours: **C2-08** (which deadline counts: RULE-001 or RULE-010) and **C2-14** (RULE-009 states a guess as fact). Gate 1 can be recorded at any time with `/ba-approve gate 1 <result>`: criteria 1 to 4 are met, and the fifth is the gate decision itself. |
| Blockers | No gate is `BLOCKED` and no dependency blocks Phase 1. Three high findings from check 2 are open: **C2-01** (the headline goal is contested and its starting point is a guess), **C2-02** (the staff roles and permissions contradict each other, and the December booking list depends on them) and **C2-03** (Saudi rules on VAT, ZATCA invoicing and privacy are unknown, with no date for the accountant's answer). They do not block Gate 1 but must be resolved before Define and Shape. There are also 8 open `CONFLICT` items; each has a question (Q-033 to Q-042). |
| Overall confidence | low — 95 of 171 open items are `KNOWN` (56%) and every quote was checked against `inputs/`, but no item is `REVIEWED` yet (only the profile is approved), there are 8 open conflicts and 29 unanswered questions, 3 high findings are open, and 47 of 61 requirements have no priority. The December scope (Q-034) is not settled, and the 4-month and end-of-December deadlines are not yet reconciled (C2-08). |

## Project

| | |
| --- | --- |
| Project | saudi hotels |
| Client | Yusuf (company name UNKNOWN). Makes the final decisions (RULE-002). His team: Layla (translation and content, 5 hours a week), Fatima (his manager: testing and approval, 10 hours a week, day-to-day support after launch), Yusuf (about 5 hours a week) (DEP-009, DEP-010, DEP-011) |
| Type / size | Booking website with online payment, customer accounts and admin dashboard / complex (suggested; profile approved 2026-09-28, DEC-001) |
| Business objective | GOAL-002: increase direct bookings to 30% of all bookings within the first year. **GOAL-003 is an open conflict**: round 2 says 50% (Q-035). Direct share today is about 10%, a client estimate (ASM-003). Booking sites take 15% commission (PRB-005). Status `AI-DRAFT` |
| Deadline | End of December is the "hard deadline" and the go-live date (RULE-010, about 13 weeks from 2026-09-28, calculated). "4 months maximum" (RULE-001) is still on file and is later; the two are not yet reconciled (C2-08). Features can follow in January |
| Budget signal | About 120,000 SAR (~$32,000), "flexible if it's worth it" (RULE-003). It includes hosting, payment fees, translation, running the platform and first-year support (RULE-019). How it splits is not known (Q-048, RISK-005) |

## Gates

| Phase | Depth | Gate result | Date |
| --- | --- | --- | --- |
| 1. Intake | standard | PARTIAL | 2026-09-28 |
| 2. Discover | standard | not started | |
| 3. Define | standard | not started | |
| 4. Shape | deep | not started | |
| 5. Commit | standard | not started | |
| 6. Deliver and learn | standard | not started | |

## Items by status

| Status | Count |
| --- | --- |
| AI-DRAFT | 94 |
| AI-CHECKED | 77 |
| REVIEWED | 0 |
| CONFIRMED | 0 |
| APPROVED | 0 |
| REJECTED | 0 |
| SUPERSEDED | 12 |

Total: 183 items. The 94 `AI-DRAFT` items all went through check 2 and carry finding flags.

## Items by label (open items only)

| Label | Count |
| --- | --- |
| KNOWN | 95 |
| ASSUMPTION | 8 |
| UNKNOWN | 60 |
| CONFLICT | 8 |

Open items: 171. All 60 `UNKNOWN` are Q items. 31 of them have an answer recorded (Q-001 to Q-014, and 17 from round 2), and 29 have none: Q-019 and Q-033 to Q-060. The 8 `CONFLICT` items are GOAL-003, REQ-059, REQ-060, REQ-061, REQ-062, REQ-063, RULE-027 and RULE-028.

## Top open questions

MVP-related first. The MVP items are REQ-001, REQ-002, REQ-003, REQ-009, REQ-013 and, proposed, REQ-019 and REQ-028.

| ID | Question | Ask |
| --- | --- | --- |
| Q-034 | For December, do you also need Arabic pages, VAT invoices, staff logins and roles, a screen for staff to type in bookings, and guest reminders, or only "guests to book online, staff to see bookings in a simple list, and payment confirmation"? (sets the December scope, RULE-010) | Yusuf |
| Q-043 | For online bookings, when and how is the rest of the payment (after the 25% or 50% deposit) paid? (blocks REQ-003) | Yusuf |
| Q-044 | How do phone-booking and walk-in guests pay, and is that recorded as "deposit paid" or "paid in full"? (blocks REQ-003, RULE-013) | Yusuf |
| Q-019 | How fast is "fast" and how simple is "simple to use", for example a page load time or a maximum number of steps to book? (blocks REQ-001) | Yusuf |
| Q-037 | Which staff roles exist: head office, hotel manager and front desk (first answer), or guest, front desk and manager (second answer)? (conflict REQ-060; REQ-019 depends on it) | Yusuf |

Also important, but not MVP: Q-035 (30% or 50% target, conflict GOAL-003), Q-049 (VAT, ZATCA and invoices, for the accountant), Q-048 (how the budget splits) and Q-060 (which of the client's requests are in scope; the BA decides first).

## Top risks

| ID | Risk | Impact |
| --- | --- | --- |
| RISK-001 | Rooms could be double-booked if the platform and the booking sites do not share availability | high |
| RISK-002 | The hard deadline (now end of December) and the fixed budget may not fit the full wanted scope | high |
| RISK-005 | The 120,000 SAR budget also has to cover running costs, so less is left for building | high |
| RISK-006 | VAT, ZATCA registration and invoicing rules may add scope, time or cost that is not yet known | high |
| RISK-007 | Automatic sync with Booking.com and Agoda may need extra time, cost or a third-party service | high |

## Recent decisions

| ID | Date | Decision |
| --- | --- | --- |
| DEC-001 | 2026-09-28 | Approved the project profile (`profile.md` AI-DRAFT → APPROVED). Reason not stated |

## Input log

| File in `inputs/` | Received | Extracted on |
| --- | --- | --- |
| brief-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-round-2-2026-09-28.md | 2026-09-28 | 2026-09-28 |

## Last check

Run 2 · 2026-09-28 · Phase 1 (Intake) · 24 findings (high 3, medium 12, low 9) · 51 items became AI-CHECKED · Gate suggestion: ready to PASS once the profile is reviewed and approved and you record the gate decision · Report: `checks/check-2-2026-09-28.md` (run 1: `checks/check-1-2026-09-28.md`). The profile has been approved since (DEC-001); the gate decision is still to be recorded.

## Notes

(Your own notes. `/ba-status` keeps this section as it is.)
