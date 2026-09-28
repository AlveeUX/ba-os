# 3. Define — P-2026-001-saudi-hotels

Stages inside this phase: **Frame** (turn information into a clear problem) and **Model** (describe the system before designing it).
Gate question: *Are the problem, users, flows and rules agreed?* (criteria: `method/phases.md`)

Principle: do not solve a symptom before understanding the root problem.

Section markers: **[light]** always done · **[standard]** at standard depth or deeper · **[deep]** at deep depth only.

Drafted by AI on 2026-09-28 from items in `items.md` and the client's answers in `inputs/`. Item IDs show where each fact comes from. Anything the client has not said is marked `UNKNOWN`. Depth for this phase is standard, so the deep-depth Data model section is left empty.

## Problem statement [light]
status: REVIEWED

Yusuf's company runs six hotels in Saudi Arabia (380 rooms in total, REQ-058). About 90% of its bookings come through Booking.com and Agoda, which each keep 15%: "if a guest pays 1000 SAR, we get 850" (PRB-005, ASM-003). Guests cannot book direct on the current website, which is slow, outdated and not mobile-friendly (PRB-003, PRB-005). Direct bookings by phone, WhatsApp and email are handled by hand: booking-site emails are forwarded to Fatima, who types them into a shared spreadsheet that is "a mess because people sometimes forget to update it" (PRB-004, PRB-006). The cost the client names is the commission and the lost direct business ("We're losing money right now"). The yearly amount is UNKNOWN. A good outcome is that guests book and pay online quickly and manage their own reservations (NEED-003), staff see every booking in one place (REQ-026), and 50% of booking money comes direct by the end of the first year (GOAL-004).

## Goals and success measures [light]
status: AI-DRAFT

| GOAL | Success measure | Baseline today | Target |
| --- | --- | --- | --- |
| GOAL-004 | The share of booking money (SAR) that comes direct. A booking is direct when it does not come through Booking.com or Agoda, so phone, email and walk-in count (RULE-029) | About 10% of bookings by number, roughly 60 of about 600 a year (ASM-003, the client's estimate). The share by money is UNKNOWN (Q-062). About 50 bookings a month in total (REQ-055) | 50% by the end of the first year, which runs from launch, "Dec 2026 to Dec 2027" (GOAL-004). The client also said "By December, maybe 20%", which does not fit a December launch (Q-061) |

Supporting targets the client gave, which are requirements, not goals: 200 bookings a month by year end (REQ-055); pages load in under 3 seconds on a phone on 4G (REQ-072); a booking in no more than 5 steps (REQ-073); cancelling or changing in no more than 3 clicks (REQ-074); typing in a booking in no more than 2 minutes (REQ-075).

GOAL-004 is `AI-DRAFT`. It replaces GOAL-002 (30%) and GOAL-003 (the 30% or 50% conflict), which were superseded on the strength of the answer to Q-035. Gate 3 needs a goal with a success measure to be `REVIEWED`; confirm the 50% with Yusuf first (check 4, C4-02).

## Root causes [standard]
status: REVIEWED

The client links the commission cost to guests not booking direct. Why guests choose the booking sites over the client's own site is not stated and was not researched.

| Symptom | Root cause (PRB) | Evidence |
| --- | --- | --- |
| About 90% of bookings come through Booking.com and Agoda, which keep 15% each | Guests cannot book direct on the client's site (PRB-005). Whether that is only because the site has no booking function, or also because it is slow and outdated (PRB-003), is UNKNOWN | PRB-005: "guests can't book direct — they go to Booking.com and pay 15% commission". ASM-003 |
| The website looks outdated and guests complain | The site is slow, outdated and not mobile-friendly (PRB-003) | PRB-003: "It's slow, looks outdated, not mobile-friendly." The number of complaints is not stated |
| Bookings are typed in by hand and the spreadsheet is unreliable | There is no booking system; booking-site bookings arrive by email and are copied by hand (PRB-006). Room tracking is one shared spreadsheet that people forget to update (PRB-004) | PRB-004 and PRB-006 quotes. RISK-001 (double booking) |
| Double bookings have to be sorted out by hand | Availability is not shared between the booking sites and the spreadsheet (inferred from PRB-006 and RISK-001) | PRB-006: "Check the email timestamps — first one wins". How often it happens is UNKNOWN |

## Desired future state [light]
status: REVIEWED

- Guests search all six hotels or one, book and pay a deposit online, and manage their booking themselves, in Arabic first and English second (REQ-009, REQ-002, REQ-003, REQ-017, REQ-053, NEED-003).
- Bookings are confirmed automatically once payment clears, and the guest gets an email (REQ-028).
- The platform is the single source of truth for rooms and bookings (REQ-026). Booking-site bookings are typed in by hand for the first month, with automatic sync wanted "ideally" (REQ-031, REQ-029).
- Front desk staff type in phone and walk-in bookings and record payments, check-ins and no-shows (REQ-030, REQ-068, REQ-047). Head office sees all six hotels; hotel managers and front desk see only their own (REQ-065, REQ-066).
- 50% of booking money comes direct by the end of the first year (GOAL-004).
- **December release** (proposed, Q-070 still open): online booking and payment confirmation, a staff booking list, Arabic pages, staff logins and roles, a screen to type in bookings, and the 7-day email reminder (REQ-002, REQ-003, REQ-019, REQ-028, REQ-053, REQ-048, REQ-064, REQ-030, REQ-045).
- **Later** (proposed): admin dashboard, monthly reports, loyalty discount, mobile app, extras, promotions, and probably invoices (REQ-005, REQ-007, REQ-032 to REQ-035, REQ-039).

## Non-goals [light]
status: REVIEWED

The client has not stated any non-goals in so many words. What follows comes from his "not now" and "no" answers.

- **Not in the December release** (proposed as `WONT` for December; these are later, not rejected): the admin dashboard (REQ-005), monthly reports (REQ-007), the loyalty discount (REQ-032), a mobile app (REQ-033), breakfast and extras (REQ-034), promotions and discount codes (REQ-035). VAT invoices are proposed for after December too (REQ-039).
- **No old and new site side by side:** the old site is turned off on launch day (REQ-054).
- **No old booking data moves over** (RULE-009).
- **USD is for reference only, not a payment currency:** round 2 says "charge in SAR", but round 1 said some guests pay in USD, so this is still a conflict (REQ-059, Q-036).
- **UNKNOWN:** whether the client rules anything else out. Q-060 (which of his requests are in scope and priced) and Q-070 decide more of this.

## User roles and permissions [light]
status: AI-DRAFT

Five roles, from the client's answer (REQ-064). Which role may do each action in round 2's permission list is still open (Q-064).

| Role | Goals | Can do | Cannot do |
| --- | --- | --- | --- |
| Owner (Yusuf) | More direct bookings (GOAL-004); control of prices and policies | See everything: all hotels and all reports. Change prices and policies. Approve changes to hotel information and the room and price data (REQ-064, RULE-030, RULE-024, RULE-025) | Nothing is stated as forbidden (UNKNOWN) |
| Head office manager (Fatima) | Runs day-to-day operations across all six hotels | "Same access as me": the same as the owner (REQ-064). One login shows all six hotels (REQ-066). Whether she and Yusuf share a login is open (Q-065) | Nothing is stated as forbidden (UNKNOWN) |
| Hotel manager (one per hotel, 6 in all) | Run their own hotel's bookings | See only their own hotel's bookings. Mark payments and no-shows. Change a booking's dates. Update their own hotel's information, with the owner's approval (REQ-065, REQ-069, RULE-031, REQ-050, RULE-024) | See other hotels (REQ-065). Change prices or policies (RULE-030) |
| Front desk staff (multiple per hotel) | Handle phone bookings, arrivals and payments at the desk | See only their own hotel's bookings. Type in phone bookings. Mark payments received for phone and card bookings. Record check-ins, no-shows and phone cancellations (REQ-065, REQ-030, REQ-068, REQ-047, REQ-022) | See other hotels (REQ-065). Change booking dates (RULE-031). Change prices (RULE-030) |
| Guest | Book quickly and manage the reservation without calling (NEED-003) | Search rooms, book with or without an account, pay, view their own booking, cancel or change dates within the rules, sign up, sign in, reset a password and close an account (REQ-009, REQ-016, REQ-040, REQ-017, REQ-041 to REQ-044) | See anyone else's booking (REQ-067) |

Open on roles: which round-2 actions each role may do (Q-064); two-factor login for managers and who creates the managers' own logins (Q-050); who may send reminders (Q-051); how many staff logins there will be (round 1 said about 1 to 2 staff per hotel, round 3 says "many"). Managers create staff logins with a temporary password, and staff must change it at first login (REQ-048, REQ-049).

## Key journeys [standard]
status: REVIEWED

Each journey: entry point → steps → decisions → end states. Steps the client has not described are `UNKNOWN`.

**J1. A guest books a room online** (REQ-009, REQ-073, REQ-002, REQ-003, REQ-013, REQ-036, REQ-028)
- Entry: the guest opens the site, in Arabic first (REQ-053).
- Steps: choose a hotel or all six, dates, number of guests and room type → see available rooms with the price per night and the total, including VAT (RULE-023) → enter details, an account is optional (REQ-016) → pay the deposit → the booking is confirmed and an email is sent (REQ-028).
- Decision: the deposit is 25% if arrival is 7 or more days away, 50% if less (RULE-012). The guest pays by card, and by SADAD or Apple Pay if these are in December (REQ-013, REQ-036, Q-070).
- End states: Confirmed (reminders follow, REQ-045; the rest is due 2 days before arrival or paid at the desk, RULE-033); Cancelled; No-show; Checked in.
- **Failure paths:** payment fails, so the booking is not confirmed and the room is held 2 hours, then released (RULE-017). Two guests want the last room, so the first to complete payment gets it (RULE-018). SADAD may confirm slower than the 2-hour hold (Q-046). A guest who leaves halfway: UNKNOWN (Q-047).

**J2. A guest cancels or changes a booking** (REQ-017, REQ-040, REQ-074, RULE-006, RULE-007, RULE-027)
- Entry: the guest opens the booking, signed in or with the booking number and email (REQ-040).
- Steps: choose cancel or change dates → the system applies the rules → confirmation.
- Decisions: cancelling more than 7 days before arrival is free, later the deposit is kept (RULE-006). Changing dates is free "anytime" or only more than 7 days before: in conflict (RULE-007, RULE-027, Q-040). A change to a costlier period means paying the difference before arrival (RULE-015). Refunds go back to the same payment method within 48 hours (RULE-016).
- End states: Cancelled and refunded; Cancelled, deposit kept; Dates changed.
- **Failure paths:** a no-show loses the deposit (RULE-014). A refund to a SADAD payment: UNKNOWN (Q-045, Q-046). A guest who lost the booking number can search by email (REQ-040).

**J3. Front desk types in a phone booking** (REQ-030, REQ-075, RULE-034, REQ-068)
- Entry: a guest phones. Today Yusuf or Fatima take these calls; who takes them after launch is UNKNOWN (check 4, C4-04).
- Steps: open the booking screen and type in the booking, in no more than 2 minutes (REQ-075) → charge the deposit (25% or 50%) by card over the phone (RULE-034) → mark the payment as received (REQ-068) → the booking shows "deposit paid" → a confirmation goes out by SMS or WhatsApp (today's practice).
- End states: Deposit paid, the rest due at check-in (RULE-034).
- **Failure paths:** the card is declined: UNKNOWN. The room is gone by the time of the call: UNKNOWN (RULE-018 covers online only). Card numbers taken by phone are a security risk (RISK-008).

**J4. A walk-in guest** (REQ-030, RULE-035)
- Entry: the guest arrives at the desk.
- Steps: staff type in the booking → the guest pays in full, in cash or by card → staff mark it as "paid in full".
- End states: Paid in full; Checked in.
- **Failure paths:** no room is free: UNKNOWN.

**J5. Head office looks at all bookings** (REQ-019, REQ-066, REQ-064)
- Entry: the owner or the head office manager signs in once (REQ-066).
- Steps: open the bookings list for all six hotels (a dashboard or a list, Q-071) → open a booking to see guest details.
- End states: The booking is seen.
- **Failure paths:** a hotel manager or front desk user tries to see another hotel's bookings and is refused (REQ-065). Staff password reset: UNKNOWN.

**J6. A booking-site booking is typed in during the first month** (REQ-031, REQ-029, PRB-006)
- Entry: Booking.com or Agoda emails the booking.
- Steps: someone types it into the platform (who: Q-063) → the room is blocked for those dates.
- End states: The room is unavailable on the platform.
- **Failure paths:** the same room is already booked on the platform. Today "first email wins" and the second guest is offered another room or hotel (PRB-006); what applies on the platform is UNKNOWN (RISK-001).

**J7. A manager creates a staff login** (REQ-048, REQ-049)
- Entry: a manager opens the staff screen. Which manager creates which logins is UNKNOWN (Q-050).
- Steps: enter the staff member's email → a temporary password is issued → the staff member signs in and must set a new password (REQ-049).
- End states: The staff member can sign in.
- **Failure paths:** a forgotten password and two-factor login for managers: UNKNOWN (Q-050).

**J8. A hotel manager updates their hotel's information** (REQ-050, RULE-024)
- Entry: a hotel manager edits their own hotel's description, photos or offers.
- Steps: save the change → it waits for Yusuf's approval → it goes live (RULE-024).
- End states: Live; Not approved.
- **Failure paths:** Yusuf is away: UNKNOWN (Q-052). Whether this is in December is open (Q-070).

Guest sign-up, sign-in, password reset and closing an account (REQ-041 to REQ-044) are not drafted as journeys; they are not in the client's December answers (Q-070).

## Future workflows [standard]
status: REVIEWED

| Workflow | Today | After launch | Items |
| --- | --- | --- | --- |
| Booking-site bookings | Emails to Yusuf, forwarded to Fatima, typed into a shared spreadsheet (PRB-006) | Typed into the platform by hand for the first month, then automatic sync "ideally" (who: Q-063) | REQ-031, REQ-029, REQ-026, RISK-007 |
| Direct bookings online | Not possible (PRB-005) | Guests book and pay a deposit on the site; confirmed automatically | REQ-002, REQ-003, REQ-028 |
| Phone and walk-in bookings | Yusuf or Fatima take calls and charge cards; walk-ins pay at the desk | Front desk types them in (who takes the calls is UNKNOWN) | REQ-030, RULE-034, RULE-035 |
| Payments | Card details taken by phone; payment links by WhatsApp or email "via a payment service" | Card, SADAD and Apple Pay; the deposit goes to one central head-office account (which payment provider: DEP-001, Q-068) | RULE-011, RULE-012, REQ-036, RISK-008 |
| The rest of the payment | Not stated | Due 2 days before arrival, or paid at the desk and marked in the system | RULE-033, REQ-071, Q-072 |
| Refunds | Not stated | Back to the same payment method within 48 hours (who processes: Q-045) | RULE-016 |
| Room tracking | One shared Google Drive spreadsheet | The platform is the single source of truth (existing bookings at launch: Q-069) | REQ-026, PRB-004 |
| Reminders | Not stated | 7-day email; 2-day SMS and 1-day email after December | REQ-045 |
| Invoices and receipts | No receipt is issued; a note is kept | Manual after launch if needed; rules depend on Ahmed | REQ-039, Q-049 |
| Hotel information | Not stated | Hotel managers edit their own hotel; Yusuf approves before it goes live | REQ-050, RULE-024 |
| Reports | Not stated | Monthly, after December | REQ-007 |
| Support | Not stated | Fatima day to day; out-of-hours cover undecided | DEP-011, REQ-057, Q-059 |
| The old website | Live, slow and outdated | Turned off on launch day, the domain is in conflict | REQ-054, REQ-063 |

## Business rules [standard]
status: REVIEWED

All 32 active RULE items, each listed once. Open points are noted.

- **Pricing:** RULE-021 (prices by room type and date; high season 2x, season dates open, Q-054), RULE-023 (shown prices include VAT and any booking fee, Q-055), RULE-032 (VAT is 15%, the client's statement, not checked), RULE-008 (room types and prices differ between hotels).
- **Approval:** RULE-002 (Yusuf makes the final decisions), RULE-024 (changes to hotel information need his approval), RULE-025 (he approves the room and price data before launch).
- **Permission:** RULE-030 (hotel managers cannot change prices or policies), RULE-031 (front desk staff cannot change booking dates).
- **Cancellation and changes:** RULE-006 (free cancellation more than 7 days before, "up to" or "more than" is open), RULE-007 and RULE-027 (date changes, in conflict, Q-040), RULE-014 (a no-show loses the deposit), RULE-015 (a costlier period is paid before arrival), RULE-016 (refunds to the same method within 48 hours).
- **Payment:** RULE-011 (one central head-office account), RULE-012 (deposit 25% or 50%), RULE-017 (a failed payment leaves the room held for 2 hours), RULE-033 (the rest due 2 days before arrival, or at the desk, Q-072), RULE-034 (phone bookings pay the deposit by phone), RULE-035 (walk-ins pay in full at the desk).
- **Inventory:** RULE-018 (two guests for the last room: the first to pay gets it), RULE-022 (Makkah Comfort sells only during Hajj season).
- **Commission:** the booking sites take 15% each (PRB-005). There is no commission rule of the client's own.
- **Other:** RULE-001 and RULE-010 (the deadlines, not yet reconciled), RULE-003 and RULE-019 (the budget and what it includes), RULE-009 (no old booking data moves), RULE-020 and RULE-028 (guest data kept 3 years, in conflict with deleting it on closure, Q-041), RULE-026 (dates as DD/MM/YYYY), RULE-029 (what counts as a direct booking).

Rules that still sit inside requirement text: the reminder timing in REQ-045, and the order of the languages in REQ-053. Consider splitting them into RULE items.

## Data model [deep]
status: empty

| Entity | Key attributes | Relationships | States | Owner |
| --- | --- | --- | --- | --- |
| | | | | |

## Integrations [standard]
status: REVIEWED

| System | Direction (in/out) | Data | Failure behaviour | DEP / REQ |
| --- | --- | --- | --- | --- |
| Payment provider (not chosen) | Out: charge and refund. In: the result | Card, SADAD and Apple Pay payments, deposits, refunds | A failed payment leaves the booking unconfirmed and the room held 2 hours (RULE-017). SADAD timing: UNKNOWN | DEP-001, REQ-013, REQ-036, Q-068 |
| Booking.com | In: bookings. Out: availability, if synchronised | Bookings, room availability | Fall back to typing bookings in by hand (REQ-031). Double booking is the risk | REQ-029, RISK-001, RISK-007 |
| Agoda | In: bookings. Out: availability, if synchronised | Bookings, room availability | As for Booking.com | REQ-029, RISK-001, RISK-007 |
| Email | Out | Confirmations, reminders, password-reset links | UNKNOWN | REQ-028, REQ-045, REQ-043 |
| SMS | Out | The 2-day reminder, "if possible" | UNKNOWN | REQ-045, Q-051 |
| WhatsApp | Out, only if the guest asks | Confirmations and reminders | UNKNOWN | REQ-045 |
| Google and Apple sign-in | In | Guest identity | UNKNOWN | REQ-042 |
| Accounting system (name UNKNOWN) | Out | Money split between hotels | UNKNOWN | RULE-011, Q-045 |
| ZATCA (the tax authority) | UNKNOWN | Registration and e-invoicing, if required | UNKNOWN | REQ-038, REQ-039, Q-049, DEP-006 |
| Domain, DNS and hosting | Not applicable | The new site's address and home | Domain is in conflict | REQ-063, DEP-004, Q-042 |
| Google Drive spreadsheet | In, once at launch, if needed | Existing bookings and room use | UNKNOWN | Q-069, PRB-004 |
| Old website content | In, once | Photos, location, contact, descriptions, about 50 reviews | UNKNOWN | REQ-052, REQ-051 |

## Exceptions and edge cases [standard]
status: AI-DRAFT

- **Payments:** a payment fails (RULE-017). SADAD or a bank transfer confirms after the 2-hour hold (Q-046). A refund to a SADAD payment (Q-045). The rest of the payment is not paid before arrival, so the guest pays at the desk and staff mark it in the system (RULE-033, REQ-071). A card is declined on a phone booking: UNKNOWN. Cash is paid at the desk (RULE-035).
- **Availability:** two guests want the last room (RULE-018). A booking-site booking arrives for a room already booked on the platform (PRB-006, RISK-001). A walk-in arrives and no room is free: UNKNOWN. Makkah Comfort outside Hajj season: what a guest sees is UNKNOWN (RULE-022, Q-054).
- **Cancellation and changes:** cancelling exactly 7 days before, the arrival day, and changing to a cheaper period are not stated (RULE-006, Q-040, RULE-015). A guest leaves halfway (Q-047). A no-show (RULE-014). A guest lost the booking number (REQ-040).
- **Booking made late:** less than 7 days before arrival needs a 50% deposit (RULE-012).
- **Permissions:** a hotel manager or front desk user tries to see another hotel (REQ-065). Front desk tries to change dates or prices (RULE-031, RULE-030). A staff password is forgotten, or two-factor login fails (Q-050). Yusuf is away when an approval is needed (Q-052).
- **Empty states:** a new guest with no bookings, a search with no available rooms, a hotel with no rooms listed yet: UNKNOWN.
- **Integrations:** the booking-site sync fails (RISK-007), the payment provider is down, an email or SMS does not send: all UNKNOWN.
- **Data:** a guest closes an account while the data must be kept for 3 years (RULE-028, Q-041). A guest sees prices in SAR only or also in USD (REQ-059, Q-036).
- **Devices and speed:** an older phone or a slow connection (REQ-056, REQ-072).
- **Launch:** bookings that already exist on launch day (Q-069). The site fails at launch or out of hours (REQ-057, Q-059).
