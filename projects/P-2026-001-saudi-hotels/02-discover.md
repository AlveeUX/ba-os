# 2. Discover — P-2026-001-saudi-hotels

Stages inside this phase: **Understand** (build the current-state picture) and **Research** (answer questions that affect decisions).
Gate question: *Is the current state known and are the unknowns listed?* (criteria: `method/phases.md`)

Section markers: **[light]** always done · **[standard]** at standard depth or deeper · **[deep]** at deep depth only.

Drafted by AI on 2026-09-28 and refreshed the same day after round 3, from items in `items.md` and the client's answers in `inputs/`. Item IDs show where each fact comes from. Anything the client has not said is marked `UNKNOWN`.

## Stakeholders [light]
status: REVIEWED

| Name or role | Type (decision maker, owner, operator, admin, customer, partner, internal team, external system) | Interest | Influence | Source |
| --- | --- | --- | --- | --- |
| Yusuf (client; "Head office, owner") | decision maker, owner | More direct bookings and less commission (GOAL-004, PRB-005). Sees everything and can change prices and policies (REQ-064, RULE-030) | Makes the final decisions; approves changes to hotel information and the room and price data (RULE-002, RULE-024, RULE-025). Gives about 5 hours a week (DEP-010) | RULE-002, REQ-064 |
| Fatima (Yusuf's manager; head office manager) | admin, internal team | "Runs day-to-day operations across all six hotels. Same access as me." (REQ-064). Tests and approves about 10 hours a week (DEP-010), handles support after launch (DEP-011). Today she types booking-site bookings into the spreadsheet (PRB-006) | Same access as the owner. Tests and approves. Many roles fall on her, and no backup is named (check 3, C3-10) | REQ-064, DEP-010, DEP-011, PRB-006 |
| Layla (Yusuf's colleague) | internal team | Translates and checks the Arabic text, about 5 hours a week, 3 to 5 days per batch (DEP-009) | Checks the Arabic. Whether she approves it is UNKNOWN | DEP-009 |
| Hotel managers (one per hotel, 6 in all) | admin, operator | See only their own hotel's bookings; mark payments and no-shows; change a booking's dates (REQ-065, REQ-069, RULE-031). Edit the shared spreadsheet today (PRB-004) | Cannot change prices or policies; the owner approves those (RULE-030). Update their hotel's information with Yusuf's approval (REQ-050, RULE-024) | REQ-065, REQ-069, RULE-030 |
| Front desk staff (multiple per hotel; round 1 said about 1 to 2 per hotel) | operator | See only their own hotel; type in phone bookings, mark payments received, record check-ins, no-shows and phone cancellations (REQ-030, REQ-047, REQ-068, REQ-022) | Cannot change booking dates or prices (RULE-031, RULE-030). The total number of logins is UNKNOWN | REQ-030, REQ-068, RULE-031 |
| Guests: about 80% Saudi, plus international and expat guests | customer | Book quickly and manage reservations without calling (NEED-003). Arabic first (REQ-053). See only their own bookings (REQ-067) | Their bookings decide the goal (GOAL-004). No direct say | NEED-003, REQ-053, REQ-067 |
| The client's IT person (name UNKNOWN) | internal team | The domain and hosting (DEP-004). Round 2 asks the project team to do this instead (REQ-063) | UNKNOWN | DEP-004, REQ-063 |
| Ahmed (Yusuf's accountant) | partner | ZATCA e-invoicing, VAT calculation and reporting, invoices, and privacy text with a lawyer (DEP-006, Q-049, Q-066). Yusuf will send his contact details (DEP-012) | His answers set tax scope (RISK-006) | DEP-006, DEP-012 |
| Current hosting company (small, Saudi, name UNKNOWN) | external system | Hosts the current website | UNKNOWN | REQ-012 |
| Booking.com and Agoda | partner | Source of most bookings; each charges 15% commission (PRB-005). Automatic sync is wanted "ideally" (REQ-029) | They set the rules for any sync (RISK-007) | PRB-005, REQ-029 |
| The payment service used today (name UNKNOWN) and the future payment provider | partner | Payment links and card charges today (Q-068). A provider recommendation is expected from the project team (DEP-001) | UNKNOWN | DEP-001, Q-068 |

## Current state [light]
status: REVIEWED

- **Six hotels in six cities, 380 rooms in total** (calculated from REQ-058): Jeddah Grand, Riyadh Palace, Dammam Beach, Makkah Comfort (only during Hajj season, RULE-022), Medina Rest and Abha Heights. Round 1 called them "all 3-star" and named "Al Riyadh and Al Jeddah" as flagship; round 2 names Jeddah Grand as the flagship. Whether these are the same hotels is open (Q-053).
- **Website:** an existing site, "slow, looks outdated, not mobile-friendly" (PRB-003). It is hosted with a small Saudi hosting company. Guests cannot book direct on it (PRB-005). What should be kept: photos, location and contact details. Descriptions move over and are refreshed, and about 50 four- and five-star reviews move over (REQ-052, REQ-051). Its domain is unclear (REQ-063).
- **Bookings, last 12 months:** about 600, roughly 60% from Booking.com, 30% from Agoda and 10% direct (phone, email, walk-in), which is about 360, 180 and 60 (ASM-003, the client's rough figures). That is about 50 a month in total: Jeddah and Riyadh about 20 each, Dammam, Medina and Abha about 5 each, Makkah about 30 in one Hajj month (REQ-055). The per-hotel figures add up to about 690 a year (calculated), so all the numbers are rough. Each booking site takes 15% (PRB-005). Phone and walk-in bookings count as direct (RULE-029).
- **Booking-site bookings:** Booking.com and Agoda email the bookings to Yusuf; he forwards them to Fatima, who types them into a shared spreadsheet (PRB-006).
- **Direct bookings:** by phone, the client takes the card details and charges the deposit on the spot, then sends a confirmation by SMS or WhatsApp. By WhatsApp or email, the client replies with a payment link "via a payment service". Walk-ins pay in full at the desk (RULE-034, RULE-035, Q-068). "No receipt is issued yet — we just keep a note." (REQ-039).
- **The spreadsheet:** one shared file for all six hotels, one sheet per hotel, on Google Drive. Fatima and the hotel managers can edit it. It is "our single source of truth right now", and "a mess because people sometimes forget to update it" (PRB-004, Q-069).
- **Double bookings:** if two bookings come in for the same room and dates, the first email wins, the second guest is offered another room or date, or a nearby hotel (PRB-006, RISK-001).
- **People:** 2 at head office (Yusuf and Fatima, REQ-064), 6 hotel managers, front desk staff at each hotel: round 1 said about 1 to 2 per hotel, round 3 says "multiple" (REQ-005, REQ-064).
- **Old data:** no old booking data exists to move from the website (RULE-009).
- **Money:** a Saudi business bank account and the business documents are ready (DEP-005). Money is split between the hotels "in the accounting system" (RULE-011), tool UNKNOWN (Q-045).
- **UNKNOWN today:** which payment service and card machine are used (Q-068), whether existing future bookings must be entered into the new platform (Q-069), how a phone booking is checked against availability, who updates the current website, and what reports exist.

## Current workflows [standard]
status: REVIEWED

Only what the client has said is written. Steps the client has not described are `UNKNOWN`.

1. **Booking through Booking.com or Agoda** (about 90% of bookings, ASM-003)
   1. The guest books and pays on the booking site.
   2. The hotel receives the payment less 15%: "if a guest pays 1000 SAR, we get 850" (PRB-005). **Pain point:** the commission.
   3. The booking site emails Yusuf. He forwards the email to Fatima.
   4. Fatima types it into the shared spreadsheet and marks that room as booked for those dates (PRB-006). **Pain point:** "messy and manual".
   5. If two bookings arrive for the same room and dates: check the email times, the first one wins; contact the second guest and offer a different room or date, or a nearby hotel (PRB-006, RISK-001).
2. **Booking by phone** (about 10% direct, ASM-003)
   1. Yusuf or Fatima takes the call and gets the card details.
   2. They charge the deposit (25% or 50%) on the spot. The rest is due at check-in (RULE-034).
   3. They send a confirmation by SMS or WhatsApp.
   4. In the system, a phone booking is marked "deposit paid" (RULE-034). How availability is checked before confirming: UNKNOWN. **Risk:** card numbers are taken by phone (RISK-008).
3. **Booking by WhatsApp or email**
   1. The guest messages or emails a booking request.
   2. The client replies with a payment link "via a payment service" (Q-068).
   3. The guest pays and the client confirms.
4. **Walk-in guest:** the guest pays in full at the desk, in cash or by card, and it is marked "paid in full" (RULE-035).
5. **Room tracking:** one shared spreadsheet on Google Drive, edited by Fatima and the hotel managers (PRB-004). **Pain point:** people forget to update it. Round 1 said front desk staff use it; who at the desk edits it today is UNKNOWN.
6. **Receipts:** none is issued; the hotel "just keeps a note" (REQ-039).
7. **Guest cancels or changes dates:** how it is handled today is UNKNOWN. The client gave cancellation rules (RULE-006, RULE-007) without saying whether they are today's practice, and the date-change rule is in conflict (RULE-027).
8. **Reports:** how head office gets numbers today is UNKNOWN.
9. **Website content changes:** who edits the current site and how is UNKNOWN.

## Current systems, data and integrations [standard]
status: REVIEWED

| System / tool | Used for | Data it holds | Connects to | Source |
| --- | --- | --- | --- | --- |
| Current website (small Saudi hosting company; domain in conflict) | Shows hotel information. Guests cannot book direct | Descriptions, photos, some guest reviews. No booking data | UNKNOWN | REQ-012, REQ-063, RULE-009, PRB-005 |
| Booking.com | Most bookings (about 60%); 15% commission | Bookings and guest details (UNKNOWN which) | Emails Yusuf. Automatic sync is wanted (REQ-029) | PRB-005, PRB-006, ASM-003 |
| Agoda | About 30% of bookings; 15% commission | Bookings and guest details (UNKNOWN which) | Emails Yusuf. Automatic sync is wanted (REQ-029) | PRB-005, PRB-006, ASM-003 |
| Yusuf's email | Receives booking notices and booking requests, and forwards them to Fatima | Booking details | Booking.com, Agoda, Fatima | PRB-006 |
| WhatsApp number | Guests message the hotels; payment links and confirmations are sent here; some payments are manual | Guest messages | A payment service (Q-068) | REQ-026, REQ-036, Q-068 |
| Shared spreadsheet on Google Drive (one sheet per hotel) | Tracking rooms and bookings; "our single source of truth right now" | Room use and booked dates (UNKNOWN which other fields) | Nothing stated; edited by hand | PRB-004, Q-069 |
| Payment service or card machine (name UNKNOWN) | Charging cards by phone and sending payment links | Card payments | UNKNOWN | Q-068, RULE-034 |
| Accounting system (name UNKNOWN) | Splitting money between hotels | UNKNOWN | UNKNOWN | RULE-011, Q-045 |
| Business bank account | Receiving payments | Money | Payment service (UNKNOWN) | DEP-005 |

## Constraints [light]
status: AI-DRAFT

- **Budget:** about 120,000 SAR, "flexible if it's worth it" (RULE-003). It also covers hosting, payment fees, translation, running the platform and first-year support (RULE-019). The split is UNKNOWN (Q-048, RISK-005).
- **Deadline:** end of December is the hard go-live date, about 13 weeks from 2026-09-28 (RULE-010). "4 months maximum" (RULE-001) is later and not yet reconciled (C3-08). Year one for the goal runs from launch, "Dec 2026 to Dec 2027" (GOAL-004). December to January includes holidays the client calls busy (REQ-055).
- **Technology:** pages load in under 3 seconds on a phone on 4G, and the site works on older phones and slow internet (REQ-072, REQ-056). Booking takes no more than 5 steps (REQ-073). Hosting, domain and backups are open (Q-042). No payment provider is chosen, though the client uses "a payment service" today (DEP-001, Q-068). Sync with booking sites is unresearched (RISK-007).
- **Roles and access:** five roles (Owner, Head office manager, Hotel manager, Front desk staff, Guest). Each hotel sees only its own bookings, except head office (REQ-064, REQ-065, REQ-066). Which role may do what in round 2's list is open (Q-064).
- **Legal:** VAT is stated as 15% by the client, not checked (RULE-032). ZATCA registration, e-invoicing and other rules are unknown and go to Ahmed (REQ-038, REQ-039, Q-049, DEP-012). Guest data is kept 3 years (RULE-020), which conflicts with deleting it on account closure (RULE-028). The client assumes guest data stays in Saudi Arabia (ASM-004). Privacy and consent text is open (Q-066). Card numbers are taken by phone (RISK-008).
- **Brand:** the Jeddah Grand page "should look premium" (Q-053). Other brand rules: UNKNOWN.
- **Team:** Layla 5 hours a week, Fatima 10, Yusuf about 5 (DEP-010). Arabic translation takes 3 to 5 days per batch (DEP-009). All key roles lean on Fatima (C3-10).
- **Language:** Arabic first, English second, right-to-left for Arabic (REQ-053, REQ-008). Dates as DD/MM/YYYY in both (RULE-026). Whether English is needed in December is open (Q-067).
- **Region:** Saudi Arabia only. Makkah Comfort sells rooms only during Hajj season (RULE-022).
- **Currency:** prices in SAR. Whether USD is shown or paid is in conflict (REQ-059).
- **Accessibility:** "No specific accessibility needs" (REQ-056).

## Known vs unknown summary [light]
status: AI-DRAFT

Counts are for open items on 2026-09-28 (not `SUPERSEDED`), after check 3.

| | Count | Most important |
| --- | --- | --- |
| KNOWN | 114 | GOAL-004, PRB-005, PRB-006, RULE-002, RULE-003, RULE-010, RULE-012, RULE-033, REQ-064 |
| ASSUMPTION | 10 | ASM-003 (10% direct today), ASM-004 (guest data stays in Saudi Arabia), RISK-001 (double booking), RISK-005 (budget covers running costs), RISK-008 (card numbers by phone) |
| UNKNOWN | 72 | All are questions. 41 have an answer recorded; 31 do not. Most important: Q-070 (which other features are needed in December), Q-064 (which role "Manager" meant), Q-049 (for Ahmed), Q-048 (budget split), Q-068 (payment service today), Q-069 (bookings that exist at launch) |
| CONFLICT | 4 | REQ-059 (currencies), REQ-063 (domain), RULE-027 (date changes), RULE-028 (data deletion). Each has a question (Q-036, Q-042, Q-040, Q-041) |

## Research plan [standard]
status: AI-DRAFT

Only research that changes a decision. **None has been started.** Research starts only when you ask for it.

| Research question | Why it matters (item ID) | Method | Findings file |
| --- | --- | --- | --- |
| What do VAT, ZATCA registration and e-invoicing, and personal-data rules require for a hotel booking site in Saudi Arabia? | REQ-037, REQ-038, REQ-039, RISK-006, Q-049. Sets tax scope, cost, and whether invoices can wait until after December | Official sources, then confirm with Ahmed | `research/saudi-tax-and-data-rules.md` (not started) |
| How can availability be synchronised with Booking.com and Agoda, and at what cost? | REQ-029, REQ-031, RISK-001, RISK-007. Decides whether sync fits the budget and December | Official partner documentation of both sites | `research/booking-site-sync.md` (not started) |
| Which payment providers in Saudi Arabia support cards, SADAD and Apple Pay, refunds and payment links, and what are their fees and approval times? | DEP-001, REQ-036, REQ-070, RULE-016, RULE-017, RISK-005. The client expects a recommendation, and already uses a payment service (Q-068) | Provider documentation for 2 to 3 providers | `research/payment-providers.md` (not started) |
| What rules apply to taking card numbers by phone and charging them by hand? | RISK-008, RULE-034, Q-068. Decides whether phone bookings can stay as they are | Official card-payment security guidance | `research/card-handling-rules.md` (not started) |
| What are the Hajj and holiday season dates for 2026 to 2027? | RULE-021, RULE-022, Q-054. Sets seasonal prices, when Makkah Comfort sells, and launch timing | Official calendars; could also be answered by the client | `research/season-dates.md` (not started) |

## Research summary [standard]
status: AI-DRAFT

No research has been done, so there are no findings and no `F-` IDs. The five questions above stay `UNKNOWN` until you ask for research or the client answers them.

## Localization and regional context [deep]
status: empty

Currency, language, RTL/LTR, date/time and address formats, local payment methods, regulations.
