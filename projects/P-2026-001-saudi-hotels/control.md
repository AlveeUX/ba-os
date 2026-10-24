# Control Center — P-2026-001-saudi-hotels

_Rebuilt by `/ba-status`. Do not edit by hand, except the Notes section at the bottom._

Last updated: 2026-09-29

## Right now

| | |
| --- | --- |
| Current phase | 4. Shape (gate not started). Phases 1, 2 and 3 all ended PARTIAL (GATE-001, GATE-002, GATE-003) |
| Next required action | `04-shape.md` is entirely empty — every section still says `status: empty`. Start with **Solution options** (compare 2-3 directions) and **Chosen direction** (a recorded decision with alternatives considered — Gate 4 needs this). Before or alongside that, close the gap Gate 4 will check for: **10 of the 24 MVP requirements still have no acceptance criteria** (check 8, C8-03: REQ-001, REQ-004, REQ-017, REQ-030, REQ-041, REQ-042, REQ-048, REQ-064, REQ-076, REQ-079) — Gate 4 requires every MVP REQ to have them. |
| Blockers | No gate is `BLOCKED`. One high finding carries forward as an accepted risk from GATE-003: **C8-01** (Saudi tax, e-invoicing, privacy and card rules — still waiting on Ahmed's contact after three rounds). It does not block Shape directly, but it should be resolved before Commit, where the commercial terms and estimate get fixed. No open `CONFLICT` items. |
| Overall confidence | medium — 119 of 202 open items are `KNOWN` (59%), zero conflicts, and Define closed with all 11 sections reviewed and a recorded PARTIAL gate. Shape itself has no data yet (`04-shape.md` is empty), so this reflects the strength of the foundation it will build on, not Shape's own progress. What would raise it to `high`: acceptance criteria on the remaining MVP requirements, a chosen solution direction recorded as a decision, and C8-01 resolved. |

## Project

| | |
| --- | --- |
| Project | saudi hotels |
| Client | Yusuf (owner; company name UNKNOWN). Makes the final decisions (RULE-002). His team: Fatima (head office manager: testing and approval 10 hours a week, day-to-day support after launch), Layla (translation and content, 5 hours a week), Yusuf (about 5 hours a week) (REQ-064, DEP-009, DEP-010, DEP-011) |
| Type / size | Booking website with online payment, customer accounts and admin dashboard / complex (suggested; profile approved 2026-09-28, DEC-001; profile itself is now stale, C8-13) |
| Business objective | GOAL-004: reach 50% of bookings direct, counted by money, by the end of the first year ("Dec 2026 to Dec 2027"), with milestones of 15-20% by end of December 2026 and 30% by end of Q1 2027 (Q-061). Direct share today is about 10% by number of bookings (ASM-003) and about 8-10% by money (Q-062). Section reviewed (DEC-014) |
| Deadline | End of December is the "hard deadline" and go-live date (RULE-010). "4 months maximum" (RULE-001) is still on file and later; the two are not yet reconciled (C8-06) |
| Budget signal | About 120,000 SAR (~$32,000), split roughly 80,000 SAR building / 40,000 SAR running and first-year support (Q-048) |

## Gates

| Phase | Depth | Gate result | Date |
| --- | --- | --- | --- |
| 1. Intake | standard | PARTIAL | 2026-09-28 |
| 2. Discover | standard | PARTIAL | 2026-09-28 |
| 3. Define | standard | PARTIAL | 2026-09-29 |
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

Total: 230 items. Unchanged since check 8.

## Items by label (open items only)

| Label | Count |
| --- | --- |
| KNOWN | 119 |
| ASSUMPTION | 10 |
| UNKNOWN | 73 |
| CONFLICT | 0 |

Open items: 202. All 73 `UNKNOWN` are Q items. 55 have an answer recorded, and 18 have none: Q-045, Q-046, Q-047, Q-049, Q-051 to Q-056, Q-058, Q-059, Q-060, Q-063, Q-066, Q-067, Q-072 and Q-073. No `CONFLICT` items remain.

## Top open questions

MVP-related first. The MVP requirements are 24: REQ-001 to REQ-004, REQ-009, REQ-013, REQ-017, REQ-019, REQ-028, REQ-030, REQ-040 to REQ-042, REQ-048, REQ-053, REQ-064 to REQ-066, REQ-072, REQ-073, REQ-075, REQ-076, REQ-078 and REQ-079 (all proposed, none confirmed — confirming them is Shape/Commit work).

| ID | Question | Ask |
| --- | --- | --- |
| Q-046 | Should Saudi debit cards (for example mada) or other wallets also be supported? Does the 2-hour room hold apply to SADAD/bank transfers? (SADAD is MVP, REQ-076) | Yusuf |
| Q-066 | What privacy and consent text must show at sign-up and at booking, and who writes it? Is that inside the 120,000 SAR? (guest accounts and sign-in are MVP) | Yusuf |
| Q-063 | Who types in Booking.com/Agoda bookings during the first month, and who enters the 20-30 bookings that already exist before launch (REQ-079)? | Yusuf |
| Q-047 | What happens if a guest abandons a booking before paying, or leaves halfway? | Yusuf |
| Q-049 | Ask Ahmed: ZATCA registration, e-invoicing, Makkah/Medina rules, data residency? Still waiting on Ahmed's contact details (DEP-012), promised in rounds 3, 4 and 5 | Ahmed, via Yusuf |

Also open, not MVP: Q-051 to Q-056, Q-058 to Q-060, Q-067, Q-072 (payment/pricing/support detail) and Q-073 (who manages DNS day to day).

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
| GATE-003 | 2026-09-29 | Phase 3 Define: PARTIAL. Reason: "Saudi tax rules still pending". Open risk: C8-01 |
| DEC-016 | 2026-09-29 | Reviewed `03-define.md` section "Exceptions and edge cases" (AI-DRAFT → REVIEWED). All 11 Define sections now reviewed |
| DEC-015 | 2026-09-29 | Reviewed `03-define.md` section "User roles and permissions" (AI-DRAFT → REVIEWED) |
| DEC-014 | 2026-09-29 | Reviewed `03-define.md` section "Goals and success measures" (AI-DRAFT → REVIEWED) |
| DEC-013 | 2026-09-28 | Reviewed `03-define.md` section "Key journeys" (AI-DRAFT → REVIEWED). Reason not stated |

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

Run 8 · 2026-09-29 · Phase 3 (Define) · 24 findings (high 1, medium 11, low 12) · Gate suggestion: PARTIAL is possible (a PASS was equally defensible on the criteria alone) · **Recorded as GATE-003, PARTIAL**, with C8-01 as the named risk · Report: `checks/check-8-2026-09-29.md` (earlier: `checks/check-7-2026-09-29.md`, `checks/check-6-2026-09-29.md`, `checks/check-5-2026-09-29.md`, `checks/check-4-2026-09-28.md`, `checks/check-3-2026-09-28.md`, `checks/check-2-2026-09-28.md`, `checks/check-1-2026-09-28.md`). No check has been run for Phase 4 yet; `04-shape.md` is empty.

## Notes

(Your own notes. `/ba-status` keeps this section as it is.)
