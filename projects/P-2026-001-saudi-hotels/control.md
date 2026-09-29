# Control Center — P-2026-001-saudi-hotels

_Rebuilt by `/ba-status`. Do not edit by hand, except the Notes section at the bottom._

Last updated: 2026-09-29

## Right now

| | |
| --- | --- |
| Current phase | 3. Define (gate not started). Phase 1 and Phase 2 both ended PARTIAL on 2026-09-28 (GATE-001, GATE-002) |
| Next required action | Two sections of `03-define.md` are content-complete and fully unblocked — "Goals and success measures" and "User roles and permissions" — and are ready for you to run `/ba-approve section` on each. Beyond that, resolve the open findings from check 7 (`checks/check-7-2026-09-29.md`): the one high finding, **C7-01** (Saudi tax, e-invoicing, privacy and card rules — Ahmed's contact details still haven't arrived after three rounds of promises), and the medium findings that matter most for what comes next: **C7-03** (10 of 24 MVP requirements still lack acceptance criteria, needed before Gate 4) and **C7-05** (35 of 70 requirements have no priority). |
| Blockers | No gate is `BLOCKED`. One high finding is open: **C7-01** (Saudi rules), which depends on Ahmed, outside the project team. There are **no open `CONFLICT` items** — all 4 were resolved in round 5. |
| Overall confidence | low, but improving steadily — 119 of 202 open items are `KNOWN` (59%), up from 57% three rounds ago. Every open conflict is gone and all three quote-quality findings from check 6 were fixed and re-verified. What is holding this back from `medium`: no item itself is `REVIEWED` yet (only stage-file sections and the profile are), the MVP list has grown twice (16 → 24 requirements) against the same ~13-week deadline, 10 of those MVP requirements still lack acceptance criteria, and the one open high finding depends on a third party who has not delivered in three rounds. |

## Project

| | |
| --- | --- |
| Project | saudi hotels |
| Client | Yusuf (owner; company name UNKNOWN). Makes the final decisions (RULE-002). His team: Fatima (head office manager: testing and approval 10 hours a week, day-to-day support after launch), Layla (translation and content, 5 hours a week), Yusuf (about 5 hours a week) (REQ-064, DEP-009, DEP-010, DEP-011) |
| Type / size | Booking website with online payment, customer accounts and admin dashboard / complex (suggested; profile approved 2026-09-28, DEC-001; profile itself is now stale, C7-13) |
| Business objective | GOAL-004: reach 50% of bookings direct, counted by money, by the end of the first year (year one runs from launch, "Dec 2026 to Dec 2027"), with interim milestones of 15-20% by end of December 2026 and 30% by end of Q1 2027 (round 5, Q-061). Direct share today is about 10% by number of bookings (ASM-003) and about 8-10% by money (Q-062). Booking sites take 15% commission (PRB-005). Status `AI-DRAFT`, content-complete, ready for `/ba-approve section` |
| Deadline | End of December is the "hard deadline" and go-live date (RULE-010). "4 months maximum" (RULE-001) is still on file and later; the two are not yet reconciled (C7-06) |
| Budget signal | About 120,000 SAR (~$32,000), split roughly 80,000 SAR building / 40,000 SAR running and first-year support (Q-048) |

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
| AI-DRAFT | 104 |
| AI-CHECKED | 98 |
| REVIEWED | 0 |
| CONFIRMED | 0 |
| APPROVED | 0 |
| REJECTED | 0 |
| SUPERSEDED | 28 |

Total: 230 items. Check 7 (2026-09-29) promoted RULE-036 and RULE-037 to `AI-CHECKED` after their quote formatting was fixed; REQ-078 was also fixed but keeps one flag (C7-03) as part of the MVP-acceptance-criteria set.

## Items by label (open items only)

| Label | Count |
| --- | --- |
| KNOWN | 119 |
| ASSUMPTION | 10 |
| UNKNOWN | 73 |
| CONFLICT | 0 |

Open items: 202. All 73 `UNKNOWN` are Q items. 55 of them have an answer recorded, and 18 have none: Q-045, Q-046, Q-047, Q-049, Q-051 to Q-056, Q-058, Q-059, Q-060, Q-063, Q-066, Q-067, Q-072 and Q-073. **No `CONFLICT` items remain** — the four that existed (currencies, domain, date changes, data deletion) were all resolved by the client's round-5 answers.

## Top open questions

MVP-related first. The MVP requirements are 24: REQ-001 to REQ-004, REQ-009, REQ-013, REQ-017, REQ-019, REQ-028, REQ-030, REQ-040 to REQ-042, REQ-048, REQ-053, REQ-064 to REQ-066, REQ-072, REQ-073, REQ-075, REQ-076, REQ-078 and REQ-079 (all proposed, none confirmed).

| ID | Question | Ask |
| --- | --- | --- |
| Q-046 | Should Saudi debit cards (for example mada) or other wallets also be supported? Does the 2-hour room hold apply to SADAD/bank transfers? (SADAD is MVP, REQ-076) | Yusuf |
| Q-066 | What privacy and consent text must show at sign-up and at booking, and who writes it? Is that inside the 120,000 SAR? (guest accounts and sign-in are MVP) | Yusuf |
| Q-063 | Who types in Booking.com/Agoda bookings during the first month, and who enters the 20-30 bookings that already exist before launch (REQ-079)? | Yusuf |
| Q-047 | What happens if a guest abandons a booking before paying, or leaves halfway? | Yusuf |
| Q-049 | Ask Ahmed: ZATCA registration, e-invoicing, Makkah/Medina rules, data residency? Still waiting on Ahmed's contact details (DEP-012), promised in rounds 3, 4 and 5 | Ahmed, via Yusuf |

Also open, not MVP: Q-051 to Q-056, Q-058 to Q-060, Q-067, Q-072 (payment/pricing/support detail) and Q-073 (who manages DNS day to day — new this round, from the domain answer).

## Top risks

| ID | Risk | Impact |
| --- | --- | --- |
| RISK-001 | Rooms could be double-booked if the platform and the booking sites do not share availability | high |
| RISK-002 | The hard deadline and the fixed budget may not fit the full wanted scope — the MVP list has grown from 16 to 24 requirements | high |
| RISK-005 | The 120,000 SAR budget also has to cover running costs; the split is known (80,000/40,000), but whether 80,000 SAR is enough for the now-larger MVP is not yet estimated | high |
| RISK-006 | VAT, ZATCA registration and invoicing rules may add scope, time or cost that is not yet known | high |
| RISK-008 | Card numbers are taken by phone and charged by hand, which may break card-payment security rules | high |

RISK-007 (automatic sync with Booking.com and Agoda may need extra time, cost or a third-party service) is also high. RISK-003 (goal may not be measurable) now has a tracking method (Q-061) but it depends on a report not due until January (REQ-007).

## Recent decisions

| ID | Date | Decision |
| --- | --- | --- |
| DEC-013 | 2026-09-28 | Reviewed `03-define.md` section "Key journeys" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-012 | 2026-09-28 | Reviewed `03-define.md` section "Future workflows" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-011 | 2026-09-28 | Reviewed `03-define.md` section "Integrations" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-010 | 2026-09-28 | Reviewed `03-define.md` section "Business rules" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-009 | 2026-09-28 | Reviewed `03-define.md` section "Non-goals" (AI-DRAFT → REVIEWED). Reason not stated |

No new `DEC`, `CHG` or `GATE` entry since these; `/ba-extract` and `/ba-check` only add and update items, they do not decide anything. "Goals and success measures" and "User roles and permissions" are ready for a `DEC` entry via `/ba-approve section` whenever you choose.

## Input log

| File in `inputs/` | Received | Extracted on |
| --- | --- | --- |
| brief-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-round-2-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-round-3-2026-09-28.md | 2026-09-28 | 2026-09-28 |
| client-answers-round-4-2026-09-29.md | 2026-09-29 | 2026-09-29 |
| client-answers-round-5-2026-09-29.md | 2026-09-29 | 2026-09-29 |

## Last check

Run 7 · 2026-09-29 · Phase 3 (Define) · 24 findings (high 1, medium 11, low 12) · 2 items became AI-CHECKED (RULE-036, RULE-037) · All three quote-formatting findings from check 6 closed (C6-02 REQ-078, C6-03 RULE-036, C6-04 RULE-037) · Only one high finding remains open: C7-01 (Saudi tax/privacy) · Gate suggestion: PARTIAL is possible — register data quality is clean (no open conflicts, no bad quotes); what's left is procedural (two sections ready for `/ba-approve section`) and the one third-party-dependent finding · Report: `checks/check-7-2026-09-29.md` (earlier: `checks/check-6-2026-09-29.md`, `checks/check-5-2026-09-29.md`, `checks/check-4-2026-09-28.md`, `checks/check-3-2026-09-28.md`, `checks/check-2-2026-09-28.md`, `checks/check-1-2026-09-28.md`).

## Notes

(Your own notes. `/ba-status` keeps this section as it is.)
