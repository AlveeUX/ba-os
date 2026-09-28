# Control Center — P-2026-001-saudi-hotels

_Rebuilt by `/ba-status`. Do not edit by hand, except the Notes section at the bottom._

Last updated: 2026-09-28

## Right now

| | |
| --- | --- |
| Current phase | 3. Define (gate not started). Phase 1 and Phase 2 both ended PARTIAL on 2026-09-28 (GATE-001, GATE-002) |
| Next required action | Resolve the top findings from check 4. The high one, **C4-01** (Saudi tax, invoice and privacy rules), needs Ahmed: ask Yusuf for his contact details (DEP-012), then send him Q-049. Define also needs the roles settled (**C4-03**: Q-064 and Q-065) and the goal confirmed (**C4-02**: Q-061 and Q-062). Two quick fixes are yours: **C4-08** (which deadline counts: RULE-001 or RULE-010) and **C4-13** (RULE-009 states a guess as fact). The flag update from check 4 has not run yet, so `items.md` still shows check 3's flags: run `! python "C:/Users/absar/AppData/Local/Temp/claude/C--Projects-BA-OS/ebb70264-26d8-401f-9e4e-e3ba8e3d07be/scratchpad/apply_check4.py"`. After that, `03-define.md` has 11 empty sections that Gate 3 needs (Problem statement, Goals and success measures, Root causes, Desired future state, Non-goals, User roles and permissions, Key journeys, Future workflows, Business rules, Integrations, Exceptions and edge cases); ask me to draft them. Gate 3 also needs the problem statement and at least one goal with a success measure to be `REVIEWED` (GOAL-004 is still `AI-DRAFT`). |
| Blockers | No gate is `BLOCKED` and no dependency blocks Phase 3. One high finding from check 4 is open: **C4-01** (Saudi rules on VAT, ZATCA e-invoicing, privacy and card handling are unknown, and nobody has a date for the answers). It is the risk accepted in GATE-002. Three medium findings matter early in Define: the December scope (C4-05, Q-070), the role mapping (C4-03, Q-064) and the payment mechanics (C4-04). There are also 4 open `CONFLICT` items; each has a question (Q-036, Q-040, Q-041, Q-042). |
| Overall confidence | low — 114 of 200 open items are `KNOWN` (57%) and every quote was checked against `inputs/`, but no item is `REVIEWED` yet (only the profile and 4 Discover sections are), there are 4 open conflicts and 31 unanswered questions, 1 high finding is open, and 44 of 69 requirements have no priority. The December scope (Q-070) keeps growing (16 MVP requirements in about 13 weeks), and the 4-month and end-of-December deadlines are not yet reconciled (C4-08). |

## Project

| | |
| --- | --- |
| Project | saudi hotels |
| Client | Yusuf (owner; company name UNKNOWN). Makes the final decisions (RULE-002). His team: Fatima (head office manager: testing and approval 10 hours a week, day-to-day support after launch), Layla (translation and content, 5 hours a week), Yusuf (about 5 hours a week) (REQ-064, DEP-009, DEP-010, DEP-011) |
| Type / size | Booking website with online payment, customer accounts and admin dashboard / complex (suggested; profile approved 2026-09-28, DEC-001) |
| Business objective | GOAL-004: reach 50% of bookings direct, counted by money, by the end of the first year (year one runs from launch, "Dec 2026 to Dec 2027"). It replaces GOAL-002 (30%) and the conflict GOAL-003. Direct share today is about 10% by number of bookings, a client estimate (ASM-003); the share by money is UNKNOWN (Q-062). Booking sites take 15% commission (PRB-005). Status `AI-DRAFT` |
| Deadline | End of December is the "hard deadline" and the go-live date (RULE-010, about 13 weeks from 2026-09-28, calculated). "4 months maximum" (RULE-001) is still on file and is later; the two are not yet reconciled (C4-08). Features can follow in January |
| Budget signal | About 120,000 SAR (~$32,000), "flexible if it's worth it" (RULE-003). It includes hosting, payment fees, translation, running the platform and first-year support (RULE-019). How it splits is not known (Q-048, RISK-005) |

## Gates

| Phase | Depth | Gate result | Date |
| --- | --- | --- | --- |
| 1. Intake | standard | PARTIAL | 2026-09-28 |
| 2. Discover | standard | PARTIAL | 2026-09-28 |
| 3. Define | standard | not started | |
| 4. Shape | deep | not started | |
| 5. Commit | standard | not started | |
| 6. Deliver and learn | standard | not started | |

## Items by status

| Status | Count |
| --- | --- |
| AI-DRAFT | 107 |
| AI-CHECKED | 93 |
| REVIEWED | 0 |
| CONFIRMED | 0 |
| APPROVED | 0 |
| REJECTED | 0 |
| SUPERSEDED | 19 |

Total: 219 items. All 107 `AI-DRAFT` items went through checks 3 and 4 and carry finding flags.

## Items by label (open items only)

| Label | Count |
| --- | --- |
| KNOWN | 114 |
| ASSUMPTION | 10 |
| UNKNOWN | 72 |
| CONFLICT | 4 |

Open items: 200. All 72 `UNKNOWN` are Q items. 41 of them have an answer recorded, and 31 have none: Q-036, Q-040 to Q-042, Q-045 to Q-056, Q-058 to Q-060 and Q-061 to Q-072. The 4 `CONFLICT` items are REQ-059 (currencies), REQ-063 (domain), RULE-027 (date changes) and RULE-028 (data deletion).

## Top open questions

MVP-related first. The MVP items are REQ-001, REQ-002, REQ-003, REQ-009, REQ-013, REQ-019, REQ-028, REQ-030, REQ-048, REQ-053, REQ-064, REQ-065, REQ-066, REQ-072, REQ-073 and REQ-075 (all proposed, none confirmed).

| ID | Question | Ask |
| --- | --- | --- |
| Q-070 | Your December list is: online booking and payment confirmation, a staff booking list, Arabic pages, staff logins and roles, a screen to type in bookings, and the 7-day email reminder. Which of these are also needed in December: guest accounts and sign-in, guests viewing, cancelling or changing bookings online, SADAD and Apple Pay (or cards only), hotel managers editing hotel information, monthly reports? (sets the December scope) | Yusuf |
| Q-064 | In round 2 you wrote "Manager" for overriding a confirmation, cancelling, sending reminders, changing prices and seeing reports. Which of your five roles may do each? May head office also change a booking's dates? (blocks RULE-031; REQ-046) | Yusuf |
| Q-050 | Do managers need two-factor login, yes or no? Who creates the managers' own logins? (blocks REQ-048) | Yusuf |
| Q-065 | Do you and Fatima each have your own login that shows all six hotels, or do you share one login? (blocks REQ-066) | Yusuf |
| Q-071 | You said the admin dashboard can wait a month or two, but head office wants one login that shows all six hotels "in a dashboard". Is a bookings list covering all six hotels enough for December? (blocks REQ-066) | Yusuf |

Also important, but not MVP: Q-049 (ZATCA, invoices and data rules, for Ahmed the accountant), Q-048 (how the budget splits), Q-068 (which payment service is used today), Q-069 (bookings that exist at launch) and Q-060 (which of the client's requests are in scope; the BA decides first).

## Top risks

| ID | Risk | Impact |
| --- | --- | --- |
| RISK-001 | Rooms could be double-booked if the platform and the booking sites do not share availability | high |
| RISK-002 | The hard deadline (now end of December) and the fixed budget may not fit the full wanted scope | high |
| RISK-005 | The 120,000 SAR budget also has to cover running costs, so less is left for building | high |
| RISK-006 | VAT, ZATCA registration and invoicing rules may add scope, time or cost that is not yet known | high |
| RISK-008 | Card numbers are taken by phone and charged by hand, which may break card-payment security rules | high |

RISK-007 (automatic sync with Booking.com and Agoda may need extra time, cost or a third-party service) is also high.

## Recent decisions

| ID | Date | Decision |
| --- | --- | --- |
| GATE-002 | 2026-09-28 | Phase 2 Discover: PARTIAL. Open risk: C4-01 (Saudi rules unknown). Reason not stated |
| DEC-005 | 2026-09-28 | Reviewed `02-discover.md` section "Current systems, data and integrations" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-004 | 2026-09-28 | Reviewed `02-discover.md` section "Current workflows" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-003 | 2026-09-28 | Reviewed `02-discover.md` section "Current state" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-002 | 2026-09-28 | Reviewed `02-discover.md` section "Stakeholders" (AI-DRAFT → REVIEWED). Reason not stated |

## Input log

| File in `inputs/` | Received | Extracted on |
| --- | --- | --- |
| brief-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-round-2-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-round-3-2026-09-28.md | 2026-09-28 | 2026-09-28 |

## Last check

Run 4 · 2026-09-28 · Phase 2 (Discover) · 27 findings (high 1, medium 14, low 12) · 0 items became AI-CHECKED (no item changed since run 3) · Gate suggestion: PARTIAL is possible, with the Saudi tax and privacy rules, the December scope, the role mapping and the payment mechanics named as risks · Report: `checks/check-4-2026-09-28.md` (earlier: `checks/check-3-2026-09-28.md`, `checks/check-2-2026-09-28.md`, `checks/check-1-2026-09-28.md`). Gate 2 was recorded as PARTIAL (GATE-002). No check has been run for Phase 3 yet.

## Notes

(Your own notes. `/ba-status` keeps this section as it is.)
