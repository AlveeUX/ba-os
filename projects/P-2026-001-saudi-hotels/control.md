# Control Center — P-2026-001-saudi-hotels

_Rebuilt by `/ba-status`. Do not edit by hand, except the Notes section at the bottom._

Last updated: 2026-09-29

## Right now

| | |
| --- | --- |
| Current phase | 3. Define (gate not started, but **all 11 required `03-define.md` sections are now `REVIEWED`**, DEC-006 to DEC-016). Phase 1 and Phase 2 both ended PARTIAL on 2026-09-28 (GATE-001, GATE-002) |
| Next required action | Run `/ba-check` again — this would be the first check since every Define section was reviewed, and could support a stronger gate suggestion than check 7's. Then record the gate with `/ba-approve gate 3 <result>`. The one thing likely to keep it at PARTIAL rather than a clean PASS: **C7-01** (Saudi tax, e-invoicing, privacy and card rules — Ahmed's contact still hasn't arrived after three rounds). Worth resolving first if you want a stronger result: the 10 MVP requirements still missing acceptance criteria (C7-03) and the register's 35 unprioritised requirements (C7-05) matter more for Gate 4 than Gate 3, so they don't have to block this gate. |
| Blockers | No gate is `BLOCKED`. One high finding is open: **C7-01**, which depends on Ahmed, outside the project team. **No open `CONFLICT` items.** |
| Overall confidence | medium, up from low — 119 of 202 open items are `KNOWN` (59%), every open conflict is resolved, all quote-quality findings are fixed, and now every Define section has been read and reviewed by the BA (not just AI-drafted), which is what Gate 3 actually asks for. Still holding it below `high`: no item itself is `REVIEWED` yet (only the sections that reference them), the MVP list has grown twice (16 → 24) against the same ~13-week deadline, 10 of those MVP requirements still lack acceptance criteria, and the one open high finding depends on a third party who has not delivered in three rounds. |

## Project

| | |
| --- | --- |
| Project | saudi hotels |
| Client | Yusuf (owner; company name UNKNOWN). Makes the final decisions (RULE-002). His team: Fatima (head office manager: testing and approval 10 hours a week, day-to-day support after launch), Layla (translation and content, 5 hours a week), Yusuf (about 5 hours a week) (REQ-064, DEP-009, DEP-010, DEP-011) |
| Type / size | Booking website with online payment, customer accounts and admin dashboard / complex (suggested; profile approved 2026-09-28, DEC-001; profile itself is now stale, C7-13) |
| Business objective | GOAL-004: reach 50% of bookings direct, counted by money, by the end of the first year ("Dec 2026 to Dec 2027"), with milestones of 15-20% by end of December 2026 and 30% by end of Q1 2027 (Q-061). Direct share today is about 10% by number of bookings (ASM-003) and about 8-10% by money (Q-062). Booking sites take 15% commission (PRB-005). Section reviewed (DEC-014); item itself still `AI-DRAFT` |
| Deadline | End of December is the "hard deadline" and go-live date (RULE-010). "4 months maximum" (RULE-001) is still on file and later; the two are not yet reconciled (C7-06) |
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

Total: 230 items. Unchanged since check 7 — no items were added or edited recording the three section approvals (DEC-014, DEC-015, DEC-016); those changed `03-define.md` and `decisions.md`, not `items.md`.

## Items by label (open items only)

| Label | Count |
| --- | --- |
| KNOWN | 119 |
| ASSUMPTION | 10 |
| UNKNOWN | 73 |
| CONFLICT | 0 |

Open items: 202. All 73 `UNKNOWN` are Q items. 55 have an answer recorded, and 18 have none: Q-045, Q-046, Q-047, Q-049, Q-051 to Q-056, Q-058, Q-059, Q-060, Q-063, Q-066, Q-067, Q-072 and Q-073. No `CONFLICT` items remain.

## Top open questions

MVP-related first. The MVP requirements are 24: REQ-001 to REQ-004, REQ-009, REQ-013, REQ-017, REQ-019, REQ-028, REQ-030, REQ-040 to REQ-042, REQ-048, REQ-053, REQ-064 to REQ-066, REQ-072, REQ-073, REQ-075, REQ-076, REQ-078 and REQ-079 (all proposed, none confirmed).

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
| DEC-016 | 2026-09-29 | Reviewed `03-define.md` section "Exceptions and edge cases" (AI-DRAFT → REVIEWED), refreshed first to match RULE-036, RULE-037, REQ-080, REQ-079. All 11 Define sections now reviewed |
| DEC-015 | 2026-09-29 | Reviewed `03-define.md` section "User roles and permissions" (AI-DRAFT → REVIEWED), refreshed first with the round-4 permission matrix |
| DEC-014 | 2026-09-29 | Reviewed `03-define.md` section "Goals and success measures" (AI-DRAFT → REVIEWED), refreshed first with the round-4/5 baseline and milestones |
| DEC-013 | 2026-09-28 | Reviewed `03-define.md` section "Key journeys" (AI-DRAFT → REVIEWED). Reason not stated |
| DEC-012 | 2026-09-28 | Reviewed `03-define.md` section "Future workflows" (AI-DRAFT → REVIEWED). Reason not stated |

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

Run 8 · 2026-09-29 · Phase 3 (Define) · 24 findings (high 1, medium 11, low 12), same substance as check 7, renumbered — no item changed · **All five Gate 3 criteria are now formally `met`** (the last two closed by DEC-014 and DEC-015) · Gate suggestion: PARTIAL is possible (carrying C8-01 as a named risk, same shape as GATE-001/002), though a PASS is equally defensible on the criteria alone if C8-01 is accepted as a risk carried into Shape — the BA's call via `/ba-approve gate 3 <result>` · Report: `checks/check-8-2026-09-29.md` (earlier: `checks/check-7-2026-09-29.md`, `checks/check-6-2026-09-29.md`, `checks/check-5-2026-09-29.md`, `checks/check-4-2026-09-28.md`, `checks/check-3-2026-09-28.md`, `checks/check-2-2026-09-28.md`, `checks/check-1-2026-09-28.md`).

## Notes

(Your own notes. `/ba-status` keeps this section as it is.)
