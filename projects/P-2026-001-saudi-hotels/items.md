# Items — P-2026-001-saudi-hotels

The single register of every tracked item in this project.
Format and field rules: `method/labels-and-statuses.md`. Requirement rules: `method/requirement-standard.md`.

Items are grouped by type below. Add new items at the end of their group. Never delete an item; mark it `SUPERSEDED` or `REJECTED`.

## Goals (GOAL)

### GOAL-001 · The business goal for the new platform is not stated
- type: GOAL
- label: UNKNOWN
- status: SUPERSEDED
- source: inputs/brief-2026-09-28.md (whole brief)
- why: The brief lists wanted features and a deadline, but not why the client wants the new platform or how success will be measured.
- superseded-by: GOAL-002
- blocked-by: Q-001, Q-014
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 superseded by GOAL-002 after the client answered Q-001

### GOAL-002 · Increase direct bookings on the client's own platform to 30% of all bookings within the first year
- type: GOAL
- label: KNOWN
- status: SUPERSEDED
- source: client answer 2026-09-28 (Q-001)
- quote: "Success means 30% of bookings come direct within the first year."
- why: Purpose, in the client's words: "We want to increase direct bookings on our own platform instead of always going through booking sites like Booking.com." The current share of direct bookings, and what the 30% is counted on, are not stated.
- blocked-by: Q-035
- superseded-by: GOAL-004
- flags: C2-01, C2-18
- history:
  - 2026-09-28 created from client answer to Q-001 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 superseded by GOAL-004 after client answers, round 3

### GOAL-003 · The first-year target for direct bookings is unclear: 30% or 50% (two answers differ)
- type: GOAL
- label: CONFLICT
- status: SUPERSEDED
- sources:
  - inputs/client-answers-2026-09-28.md (answer 1, headed "[Q-001] Business goal"): "Success means 30% of bookings come direct within the first year."
  - inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-018"): "We want to push that 10% direct up to 50% in the first year, which means the platform has to be really easy."
- why: Both are the client's words. Round 1 says 30% of bookings direct within the first year; round 2 says push direct from about 10% to 50% in the first year. No winner is picked here.
- blocked-by: Q-035
- superseded-by: GOAL-004
- flags: C2-01
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 superseded by GOAL-004 after client answers, round 3

### GOAL-004 · Reach 50% of bookings direct, counted by money, by the end of the first year
- type: GOAL
- label: KNOWN
- status: AI-DRAFT
- source: inputs/client-answers-round-3-2026-09-28.md (Section A, answer headed "Q-035")
- quote: "50% is what we want to reach by end of year one, not by December."
- why: The client also said "Count it by money, not by number of bookings" and "Year one starts when we launch, so if we launch in December, year one runs Dec 2026 to Dec 2027." Direct is defined in RULE-029. The 10% direct share today is by number of bookings (about 60 of about 600, ASM-003), not by money, so the share by money is UNKNOWN (Q-062). Replaces GOAL-002 (30%) and GOAL-003 (the conflict): the client answered Q-035.
- blocked-by: Q-061, Q-062
- flags: C4-02, C4-19
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md. Replaces GOAL-002 and GOAL-003

## Problems (PRB)

### PRB-001 · The current website is outdated
- type: PRB
- label: KNOWN
- status: SUPERSEDED
- parent: GOAL-001
- source: inputs/brief-2026-09-28.md line 18
- quote: "We already have a website but it is outdated."
- why: The client names this as the situation today. "Outdated" is not defined, so the symptom is known but the cause is not.
- superseded-by: PRB-003
- blocked-by: Q-002
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 superseded by PRB-003 after the client answered Q-002

### PRB-002 · The client pays booking sites too much commission
- type: PRB
- label: KNOWN
- status: SUPERSEDED
- parent: GOAL-002
- source: client answer 2026-09-28 (Q-001)
- quote: "We're paying them too much commission."
- why: "Too much" is the client's judgement. No commission rate or yearly amount was given.
- blocked-by: Q-018
- superseded-by: PRB-005
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-001 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 superseded by PRB-005 after client answers, round 2

### PRB-003 · The current website is slow, looks outdated and is not mobile-friendly
- type: PRB
- label: KNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: client answer 2026-09-28 (Q-002); also inputs/brief-2026-09-28.md line 18
- quote: "It's slow, looks outdated, not mobile-friendly."
- why: The client also said "Guests complain." How many guests complain, and about what, is not stated.
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-002 (answers pasted by the BA). Replaces PRB-001
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### PRB-004 · Front desk staff track rooms in a manual spreadsheet
- type: PRB
- label: KNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: client answer 2026-09-28 (Q-013)
- quote: "front desk uses a spreadsheet to track rooms — very manual."
- why: The client says there is no booking system today. The link to GOAL-002 is indirect: the platform is meant to replace this (REQ-026). Round 3: "One shared spreadsheet for all six hotels (one sheet per hotel inside it)." "Fatima and the hotel managers can edit it." "It's stored on Google Drive." The client calls it "a mess because people sometimes forget to update it". Round 1 said "front desk uses a spreadsheet"; round 3 lists Fatima and the hotel managers as editors.
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-013 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section E, "Q-16"): why
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### PRB-005 · The client loses money because guests cannot book direct and booking sites take 15% commission
- type: PRB
- label: KNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-016")
- quote: "We're losing money right now because guests can't book direct — they go to Booking.com and pay 15% commission."
- why: Round 2 also gives the rates: "Booking.com charges 15%, Agoda charges 15%." and an example: "So if a guest pays 1000 SAR, we get 850." Replaces PRB-002.
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2. Replaces PRB-002
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### PRB-006 · Booking-site bookings arrive by email and are typed into a shared spreadsheet by hand
- type: PRB
- label: KNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: inputs/client-answers-round-3-2026-09-28.md (Section E, answer headed "Q-14")
- quote: "Today, I get an email from Booking.com and Agoda."
- why: The client: "I forward it to Fatima." and "She types it into a shared Excel spreadsheet and marks that room as "booked" for those dates." If two bookings come in for the same room and dates: "Check the email timestamps — first one wins", "Contact the second guest and offer them a different room or date", or "we offer them a nearby hotel". He calls it "messy and manual" ("It's messy and manual.") and wants the system "to prevent double-sells in the first place". See RISK-001.
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

## Needs (NEED)

### NEED-001 · Customers need to find, book and pay for a room at the client's hotels online
- type: NEED
- label: ASSUMPTION
- status: SUPERSEDED
- parent: GOAL-001
- source: BA reasoning
- why: Inferred from "Online room booking", "Online payment" and "Customer accounts" (lines 9–11). The brief lists these as solutions and does not say what problem they solve. GOAL-001 is used as parent because no other item fits yet.
- superseded-by: NEED-003
- blocked-by: Q-001
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 superseded by NEED-003 after the client answered Q-001

### NEED-002 · The client's team needs to manage bookings and see reports
- type: NEED
- label: KNOWN
- status: AI-DRAFT
- parent: GOAL-004
- source: client answer 2026-09-28 (Q-009, Q-010)
- quote: "We need to view all bookings, see guest details, confirm or cancel them, track which ones have paid the deposit, and send reminders before arrival."
- why: The reports part comes from Q-010: "We need to see per-hotel data and combined data." The users are head office, hotel managers and front desk staff (Q-004).
- flags: C4-19
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answers to Q-004, Q-009, Q-010: label ASSUMPTION → KNOWN, quote added, parent GOAL-001 → GOAL-002
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### NEED-003 · Guests need to book quickly and manage their reservations themselves instead of calling
- type: NEED
- label: KNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: client answer 2026-09-28 (Q-001)
- quote: "they should be able to book quickly and manage their reservations themselves, not call us."
- why: "Quickly" now has targets: no more than 5 steps to book (REQ-073) and no more than 3 clicks to cancel or change (REQ-074).
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-001 (answers pasted by the BA). Replaces NEED-001
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section D, "Q-019"): why
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3
  - 2026-09-28 blocked-by updated after client answers, round 3

## Requirements (REQ)

### REQ-001 · The platform includes a new website
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: PRB-003
- source: inputs/brief-2026-09-28.md line 8
- quote: "A modern website"
- why: The client's definition of modern: "Modern means fast, mobile-first, simple to use." That is still not measurable (Q-019). Round 3 gives targets: pages load in under 3 seconds on a phone on 4G (REQ-072) and a booking takes no more than 5 steps (REQ-073).
- priority: MVP (proposed from the client's first-version list in the answer to Q-007; to be confirmed)
- acceptance: not drafted. The targets are in REQ-072 and REQ-073.
- flags: C4-06
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answers to Q-002, Q-007: parent PRB-001 → PRB-003, priority set, blocked-by changed
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section D, "Q-019"): why and acceptance
  - 2026-09-28 blocked-by updated after client answers, round 3

### REQ-002 · Rooms can be booked online
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/brief-2026-09-28.md line 9
- quote: "Online room booking"
- why: In the first version, per the client (Q-007). How bookings from other channels get into the platform is not yet known.
- priority: MVP (proposed from the client's first-version list in the answer to Q-007; to be confirmed)
- acceptance:
  - Given a guest has chosen a hotel, dates and a room type, when they enter their details and pay the deposit, then the booking is created and the room is no longer offered for those dates.
  - Given two guests want the last room, when both try to pay, then the first to complete payment gets it and the other is told the room is gone.
- flags: C4-06
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answers to Q-003, Q-007, Q-013: parent NEED-001 → NEED-003, priority set, blocked-by changed
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3: acceptance drafted from RULE-018 and REQ-073

### REQ-003 · Payment can be made online
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/brief-2026-09-28.md line 10
- quote: "Online payment"
- why: In the first version, per the client (Q-007). Details are in RULE-012, RULE-033, RULE-034, RULE-035, RULE-016, REQ-013, REQ-036, REQ-015 and DEP-001.
- priority: MVP (proposed from the client's first-version list in the answer to Q-007; to be confirmed)
- acceptance:
  - Given a guest books 7 or more days before arrival, when they pay, then the deposit charged is 25% of the total and the rest is shown as due 2 days before arrival.
  - Given a guest books less than 7 days before arrival, when they pay, then the deposit charged is 50% of the total.
  - Given a payment fails, when the guest is told, then the booking is not confirmed and the room is held for 2 hours and then released.
- flags: C4-06
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answers to Q-005, Q-006, Q-007: parent NEED-001 → NEED-003, priority set, blocked-by changed
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3: why refreshed, acceptance drafted from RULE-012, RULE-033 and RULE-017
  - 2026-09-28 blocked-by updated after client answers, round 3

### REQ-004 · Customers can have accounts
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/brief-2026-09-28.md line 11
- quote: "Customer accounts"
- why: The client says accounts are optional for booking (REQ-016). What accounts are for is described in REQ-017. Whether accounts are in the first version is not stated.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Sign-up, sign-in and password steps are not described (see Q-024).
- flags: C4-05, C4-07, C4-21
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answer to Q-008: parent NEED-001 → NEED-003, blocked-by changed
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-005 · Admin users have a dashboard
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/brief-2026-09-28.md line 12
- quote: "Admin dashboard"
- why: Three roles will use it (REQ-023, REQ-024, REQ-025). Client on numbers: "We have 2 people at head office, and about 1-2 staff at each hotel." The client says it can come after the first version: "We can add the admin dashboard and reports later."
- priority: WONT (proposed: the client says it "can wait a month or two"; for the December release)
- acceptance: not drafted. What the dashboard shows is not described (see Q-015).
- flags: C4-03, C4-07
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answers to Q-004, Q-007: why, priority and blocked-by changed
  - 2026-09-28 priority set from client answer, round 2 (Section A, "Q-015")
  - 2026-09-28 blocked-by updated after client answers, round 2

### REQ-006 · Bookings can be managed
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/brief-2026-09-28.md line 13
- quote: "Booking management"
- why: Umbrella item. Detail is in REQ-019, REQ-020, REQ-021 and REQ-022. Hotel managers handle cancellations for their own hotel: "Hotel managers should handle cancellations for their own hotel."
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See the detail items for the actions.
- flags: C4-05, C4-12
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answer to Q-009: why and blocked-by changed
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-007 · Monthly reports show bookings, revenue, occupancy, cancellations and no-shows
- type: REQ
- label: KNOWN
- status: AI-CHECKED
- parent: NEED-002
- source: client answer 2026-09-28 (Q-010); also inputs/brief-2026-09-28.md line 14
- quote: "Monthly reports showing: total bookings, revenue (by hotel and all together), occupancy rate, cancellations, and no-shows."
- why: Read by head office, per hotel and combined. Format: "Nothing fancy — Excel is fine, or PDF." The client says reports can come after the first version. How revenue and occupancy are calculated is not stated.
- priority: WONT (proposed: the client says reports can be added later; for the December release)
- acceptance:
  - Given bookings exist for more than one hotel in a month, when head office opens the monthly report, then it shows total bookings, revenue, occupancy rate, cancellations and no-shows for each hotel and for all hotels together.
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answers to Q-007, Q-010: title, quote, why, acceptance and priority changed
  - 2026-09-28 priority set from client answers (round 1 Q-007, round 2 Section A "Q-015")
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### REQ-008 · Everything in the platform is available in Arabic and English
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-011); also inputs/brief-2026-09-28.md line 16
- quote: "Everything in both Arabic and English: the customer website, confirmation emails, payment pages, the admin dashboard, reports, everything."
- why: Round 2 gives the reason: "80% of guests are Saudi" (Arabic first) and English for "international and expat guests", so the parent is NEED-003 (guests). Scope is "everything": website, emails, payment pages, dashboard and reports. The English should be "clear and professional". See REQ-053 for the order.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Which text is written by whom is not yet known (see Q-030).
- flags: C4-05, C4-07, C4-12
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answer to Q-011: title, quote and blocked-by changed (scope is now "everything")
  - 2026-09-28 updated from client answer, round 2 (Section E, "Q-028 [NEW]"): parent none → NEED-003
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-009 · Guests can search for available rooms
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-007)
- quote: "room search"
- why: Named by the client as part of the first version. How guests search is not described. Round 2: guests pick a hotel (or see all six), dates, number of guests and room type; results show available rooms, price per night and total price for the stay.
- priority: MVP (proposed from the client's first-version list in the answer to Q-007; to be confirmed)
- acceptance:
  - Given a guest has chosen dates, number of guests and a room type, for one hotel or all six, when they search, then the results show available rooms with the price per night and the total price for the stay.
- flags: C4-06
- history:
  - 2026-09-28 created from client answer to Q-007 (answers pasted by the BA)
  - 2026-09-28 updated from client answer, round 2 (Section D, "Q-016"): why and acceptance
  - 2026-09-28 blocked-by updated after client answers, round 2

### REQ-010 · One platform serves all 6 hotels
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: GOAL-004
- source: client answer 2026-09-28 (Q-003)
- quote: "One platform for all 6 hotels."
- why: The client also said "We manage everything centrally from the head office here." This replaces ASM-001.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-028 for what differs between hotels.
- flags: C4-05, C4-07
- history:
  - 2026-09-28 created from client answer to Q-003 (answers pasted by the BA). Replaces ASM-001
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-011 · Each hotel has its own page
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-003)
- quote: "each hotel should have its own page"
- why: What each page contains is not described. Only two hotels are named so far: "Al Riyadh and Al Jeddah are our flagship hotels."
- blocked-by: Q-053
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Page content is not described (see Q-028).
- flags: C4-05, C4-07
- history:
  - 2026-09-28 created from client answer to Q-003 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-012 · The new platform replaces the old website and keeps the same domain name
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: PRB-003
- source: client answer 2026-09-28 (Q-012)
- quote: "We can keep the same domain name"
- why: The client gave the domain only as "something like saudhotels.com or similar", so the exact name is UNKNOWN. The current site is "hosted with a small Saudi hosting company". This replaces ASM-002.
- blocked-by: Q-042
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. The exact domain and hosting plan are not known (see Q-029).
- flags: C4-05, C4-07, C4-11, C4-14
- history:
  - 2026-09-28 created from client answer to Q-012 (answers pasted by the BA). Replaces ASM-002
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-013 · Visa and Mastercard credit cards are accepted
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-005)
- quote: "We need to accept credit cards (Visa, Mastercard)"
- why: Part of online payment (REQ-003). The payment provider is not chosen yet (DEP-001).
- priority: MVP (proposed because online payment is in the client's first-version list; to be confirmed)
- acceptance:
  - Given a guest is paying a deposit, when they pay with a valid Visa or Mastercard credit card, then the payment succeeds and the booking shows the deposit as paid.
- flags: C4-06
- history:
  - 2026-09-28 created from client answer to Q-005 (answers pasted by the BA)

### REQ-014 · Local Saudi payment methods are accepted
- type: REQ
- label: ASSUMPTION
- status: SUPERSEDED
- parent: NEED-003
- source: client answer 2026-09-28 (Q-005)
- why: The client said "some Saudi guests use local payment methods" right after listing the cards they need. That suggests these must be accepted too, but it was not stated as a requirement and no method was named.
- blocked-by: Q-020
- priority: unknown (see Q-015)
- acceptance: not drafted. The methods are not named (see Q-020).
- superseded-by: REQ-036
- flags: C1-05
- history:
  - 2026-09-28 created from client answer to Q-005 (answers pasted by the BA)
  - 2026-09-28 superseded by REQ-036 after client answers, round 2

### REQ-015 · Payments can be made in Saudi Riyal and in US dollars
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-005)
- quote: "Mostly Saudi Riyal, but some international guests pay in USD."
- why: How US dollar payments work (display, exchange rate, charge currency) is not stated.
- blocked-by: Q-036
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-022.
- flags: C4-05, C4-07, C4-14
- history:
  - 2026-09-28 created from client answer to Q-005 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-016 · Guests can book without creating an account
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-008)
- quote: "They can book without creating an account"
- why: Accounts are optional. What guests without an account can do afterwards is unclear (Q-024).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a guest who is not signed in has chosen a room, when they enter their details and pay, then the booking is created without creating an account.
- flags: C4-05
- history:
  - 2026-09-28 created from client answer to Q-008 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-017 · Guests can see their booking details and cancel or change dates
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-008)
- quote: "Guests should see their booking, check-in dates, room details, and be able to cancel or modify dates."
- why: The client also said "if they do, they can manage their reservations easily", which may mean only guests with an account (Q-024). Cancellation and date-change terms are in RULE-006 and RULE-007.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Unclear who can do this (see Q-024).
- flags: C4-05, C4-07, C4-11
- history:
  - 2026-09-28 created from client answer to Q-008 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-018 · Guests receive booking confirmations and reminders
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: client answer 2026-09-28 (Q-008, Q-009)
- quote: "We want to collect their email and phone so we can send confirmations and reminders."
- why: Q-009 adds "send reminders before arrival". Channels (email, SMS, WhatsApp) and timing are not stated.
- blocked-by: Q-051
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Channels and timing are not stated (see Q-025).
- flags: C4-05, C4-07
- history:
  - 2026-09-28 created from client answers to Q-008, Q-009 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-019 · Authorised staff can view all bookings and guest details
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: client answer 2026-09-28 (Q-009)
- quote: "view all bookings, see guest details"
- why: Who sees which bookings is set by the roles in REQ-064 and REQ-065: head office sees all six hotels (REQ-066); hotel managers and front desk staff see their own hotel.
- priority: MVP (proposed: the client lists "staff to see bookings in a simple list" for December; to be confirmed)
- acceptance:
  - Given bookings exist at several hotels, when a head office user opens the bookings list, then all bookings from all 6 hotels are shown with guest details.
- flags: C4-03, C4-06
- history:
  - 2026-09-28 created from client answer to Q-009 (answers pasted by the BA)
  - 2026-09-28 priority set from client answer, round 2 (Section A, "Q-015")
  - 2026-09-28 updated by /ba-extract from client answers, round 3: why

### REQ-020 · Authorised staff can confirm or cancel bookings
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: client answer 2026-09-28 (Q-009)
- quote: "confirm or cancel them"
- why: Round 2: bookings are confirmed automatically once payment clears (REQ-028) and "Manager can override" (REQ-046). Round 3: front desk staff may record phone cancellations, and only hotel managers change dates (REQ-069, RULE-031). Which roles may cancel is still open (Q-064).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-025.
- flags: C4-03, C4-05, C4-07
- history:
  - 2026-09-28 created from client answer to Q-009 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3: why
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-021 · Authorised staff can see which bookings have paid the deposit
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: client answer 2026-09-28 (Q-009)
- quote: "track which ones have paid the deposit"
- why: Deposit rule is in RULE-005.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a booking, when an authorised user opens it, then it shows whether the deposit has been paid.
- flags: C4-03, C4-05, C4-07
- history:
  - 2026-09-28 created from client answer to Q-009 (answers pasted by the BA)
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-022 · A cancellation made by phone can be recorded in the system quickly
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: client answer 2026-09-28 (Q-009)
- quote: "If a guest calls to cancel, someone needs to mark it in the system quickly."
- why: "Someone" and "quickly" are not defined. Front desk staff cannot change bookings (REQ-025), and hotel managers may not always be available. Round 2 gives a target: "Within 5 minutes if possible, or before the shift ends." Round 3: front desk staff may record it: "Record phone cancellation: YES".
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Who does this and how fast is not stated (see Q-026).
- flags: C4-03, C4-05, C4-07, C4-12
- history:
  - 2026-09-28 created from client answer to Q-009 (answers pasted by the BA)
  - 2026-09-28 why updated from client answer, round 2 (Section D, "Q-021")
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section B, "Q-039"): why
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-023 · Head office users can see all hotels, manage all bookings, change prices and availability, and view reports
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: client answer 2026-09-28 (Q-004)
- quote: "Head office — can see all 6 hotels, manage all bookings, change prices and availability, view reports."
- why: Client: "We have 2 people at head office". This role covers several permissions in one line, so it may need splitting later. Round 3: head office is Yusuf (owner) and Fatima (head office manager), with the same access (REQ-064).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a head office user, when they open the bookings list, then they see bookings from all 6 hotels and can change prices and availability.
- flags: C4-03, C4-05, C4-11, C4-12, C4-15
- history:
  - 2026-09-28 created from client answer to Q-004 (answers pasted by the BA)
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section B, "Q-037"): why
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-024 · Hotel managers see and manage only their own hotel's bookings
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: client answer 2026-09-28 (Q-004)
- quote: "Hotel manager — only sees their own hotel's bookings and can manage them."
- why: "Manage" is taken to include the cancellations described in Q-009. Whether hotel managers can change prices is not stated; the client gave price changes to head office only.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a manager of one hotel, when they open the bookings list, then they see only that hotel's bookings and can manage them.
- flags: C4-03, C4-05, C4-11, C4-12
- history:
  - 2026-09-28 created from client answer to Q-004 (answers pasted by the BA)
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-025 · Front desk staff can view bookings but cannot change anything
- type: REQ
- label: KNOWN
- status: SUPERSEDED
- parent: NEED-002
- source: client answer 2026-09-28 (Q-004)
- quote: "Front desk staff — can only view bookings, not change anything."
- why: Client: "about 1-2 staff at each hotel". This conflicts in practice with recording no-shows and phone cancellations (Q-026), so it is a question, not a conflict item.
- blocked-by: Q-039
- priority: unknown (see Q-015)
- acceptance:
  - Given a front desk user, when they open a booking, then they can see it and cannot change or cancel it.
- superseded-by: REQ-068
- flags: C2-02, C2-05, C2-07
- history:
  - 2026-09-28 created from client answer to Q-004 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 superseded by REQ-068 after client answers, round 3

### REQ-026 · The new platform is the client's single source of truth for rooms and bookings
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: client answer 2026-09-28 (Q-013)
- quote: "The new platform should be our single source of truth."
- why: Client on today's channels: "Most bookings come through Booking.com or Agoda." and "We also have a WhatsApp number where guests message us directly." How those bookings reach the platform is not stated.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-017.
- flags: C4-05, C4-07
- history:
  - 2026-09-28 created from client answer to Q-013 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-027 · Which content from the current website moves to the new platform is unclear (two answers differ)
- type: REQ
- label: CONFLICT
- status: SUPERSEDED
- parent: PRB-003
- sources:
  - client answer 2026-09-28 (Q-002): "What should be kept: the hotel photos are good, the location information is useful, and the contact details. Everything else needs to be new."
  - client answer 2026-09-28 (Q-012): "Content (descriptions, photos, some guest reviews) should move over."
- why: Both are the client's words. The first keeps only photos, location information and contact details. The second also moves descriptions and some guest reviews. No winner is picked here.
- blocked-by: Q-027
- superseded-by: REQ-052
- flags: C1-05, C1-20
- history:
  - 2026-09-28 created from client answers to Q-002 and Q-012 (answers pasted by the BA)
  - 2026-09-28 superseded by REQ-052 after client answers, round 2

### REQ-028 · A booking is confirmed automatically once payment clears, and the guest gets a confirmation email
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-019")
- quote: "Automatic. As soon as payment clears, it's confirmed. Guest gets an email confirmation."
- why: "Staff can see it immediately in the system." Managers can override (REQ-046).
- priority: MVP (proposed: "payment confirmation" is in the client's December list; to be confirmed)
- acceptance: Given a guest has paid the deposit, when the payment clears, then the booking shows Confirmed and the guest receives a confirmation email.
- flags: C4-06, C4-11
- history:
  - 2026-09-28 created from client answers, round 2

### REQ-029 · Bookings from Booking.com and Agoda are synchronised automatically
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-026
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-017")
- quote: "Ideally, automatic sync from the booking sites."
- why: The client accepts typing them in by hand for the first month if this is too complex (REQ-031). How sync would work has not been researched (RISK-007).
- priority: SHOULD (proposed: the client says "Ideally" and accepts a manual fallback)
- acceptance: not drafted. The method and sites are not yet known (see RISK-007).
- flags: C4-19
- history:
  - 2026-09-28 created from client answers, round 2

### REQ-030 · Front desk staff type in phone and walk-in bookings
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-026
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-017")
- quote: "Walk-ins and phone bookings — our front desk staff will type those in when the guest calls or arrives."
- why: Round 3 confirms it: "Type in phone bookings: YES" and "Screen to type bookings: YES, front desk needs this for phone bookings." It needs a staff screen for typing bookings in (REQ-075). The first answers said front desk staff were view-only (REQ-025, superseded by REQ-068).
- priority: MVP (proposed: the client says "Screen to type bookings: YES, front desk needs this for phone bookings." for December; to be confirmed)
- acceptance: not drafted. The front desk permissions are in conflict (see REQ-062).
- flags: C4-06, C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Sections B and D): why and priority
  - 2026-09-28 blocked-by updated after client answers, round 3

### REQ-031 · Staff can type in booking-site bookings by hand during the first month
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-026
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-017")
- quote: "we can manually type them in for the first month"
- why: A fallback if automatic sync (REQ-029) is too complex. Who types them in is not stated.
- blocked-by: Q-063
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Who does this is not stated (see Q-039).
- flags: C4-05, C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-032 · A loyalty discount gives 10% off the fourth booking after three
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-018b [NEW]")
- quote: "if a guest books 3 times, give them 10% off the fourth"
- why: For a later release: "Not in December." (REQ-035).
- priority: WONT (proposed: the client says loyalty is for later; for the December release)
- acceptance: not drafted. Later release.
- flags: C4-24
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### REQ-033 · A mobile app
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-018b [NEW]")
- quote: "Mobile app is nice-to-have for year two."
- why: Not for December.
- priority: WONT (proposed: "nice-to-have for year two"; for the December release)
- acceptance: not drafted. Later release.
- flags: C4-24
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### REQ-034 · Breakfast and other extras can be added to a booking
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-018b [NEW]")
- quote: "Breakfast and extras — maybe later, not now."
- why: Not for December.
- priority: WONT (proposed: "maybe later, not now"; for the December release)
- acceptance: not drafted. Later release.
- flags: C4-24
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### REQ-035 · Promotions and discount codes
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-018b [NEW]")
- quote: "Not in December. Just bookings and payment."
- why: "Just bookings and payment" is narrower than what other answers need in December (see Q-034).
- priority: WONT (proposed: "Not in December"; for the December release)
- acceptance: not drafted. Later release.
- flags: C4-24
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### REQ-036 · SADAD and Apple Pay payments are accepted
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-008")
- quote: "SADAD (bank transfer), credit card (Visa/Mastercard), and Apple Pay."
- why: Replaces REQ-014. Cards are REQ-013. The client also said "WhatsApp payments from guests is common too, but that's manual." and "We don't use cash online."
- blocked-by: Q-046
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Timing of SADAD confirmations is not known (see Q-046).
- flags: C4-04, C4-05, C4-11
- history:
  - 2026-09-28 created from client answers, round 2. Replaces REQ-014
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-037 · VAT is charged on room prices
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section C, answer headed "Q-014 [NEW]")
- quote: "charge VAT on room prices"
- why: The rate is not confirmed: the client said "I think it's 15%" and "We need to ask our accountant." (DEP-006). Round 3: "VAT is 15% on room prices." (RULE-032). Registration and reporting details are still with the accountant (Q-049).
- blocked-by: Q-049
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. The rate and rules are not confirmed (see Q-049).
- flags: C4-01, C4-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section C, "Q-049"): why
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-038 · The system is registered with ZATCA
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section C, answer headed "Q-014 [NEW]")
- quote: "we need to register the system with ZATCA (the tax authority)"
- why: What registration involves for this platform is not known (RISK-006).
- blocked-by: Q-049
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-049.
- flags: C4-01, C4-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-039 · Guests receive an invoice after they book
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section C, answer headed "Q-014 [NEW]")
- quote: "guests need invoices after they book"
- why: Format and legal content depend on the accountant's answer (Q-049). Round 3: "VAT invoices: Not critical. We can do it manually after launch if needed." Today "No receipt is issued yet — we just keep a note." Whether invoices are legally needed from the first booking is not known (Q-049).
- blocked-by: Q-049
- priority: WONT (proposed: the client says "Not critical. We can do it manually after launch if needed."; for the December release)
- acceptance: not drafted. See Q-049.
- flags: C4-01
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Sections D and E): why and priority

### REQ-040 · Guests without an account can view, cancel or change a booking with the booking number and email
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-017")
- quote: "They can use that booking number + email to log back in without a full account."
- why: The client also said "They should get a booking number and confirmation email." and "If they lose the booking number, they can search by email."
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: Given a guest booked without an account, when they enter their booking number and email, then they see their booking and can cancel or change it within the rules.
- flags: C4-05, C4-11
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-041 · Guests can sign up with email, password and phone number
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-018 [NEW]")
- quote: "Sign up: email, password, phone number."
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Validation and error cases are not described.
- flags: C4-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-042 · Guests can sign in with email and password, or with Google or Apple
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-018 [NEW]")
- quote: "Sign in: email + password or Google/Apple login."
- why: Google and Apple sign-in were not mentioned in round 1.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. Error cases are not described.
- flags: C4-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-043 · Guests can reset their password with an email link
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-018 [NEW]")
- quote: "Reset password: email link."
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. How long the link works is not stated.
- flags: C4-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-044 · Guests can close their account after confirming by email
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-018 [NEW]")
- quote: "Close account: just delete their data after they confirm (email confirmation)."
- why: This conflicts with keeping guest data for 3 years (RULE-028).
- blocked-by: Q-041
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-041.
- flags: C4-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-045 · Guests get reminders by email 7 days and 1 day before arrival, and by SMS 2 days before
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-023 [NEW]")
- quote: "Reminders should go out 7 days before arrival (email), 2 days before (SMS), 1 day before (email)."
- why: Also: "Email is primary. SMS too, if possible. WhatsApp only if guest asks for it." SMS is "if possible", so it is not firm. Refines REQ-018.
- blocked-by: Q-051
- priority: SHOULD (proposed: the client says the 7-day email reminder "is nice" and the 2-day and 1-day reminders are "nice-to-have, not essential"; for December)
- acceptance: not drafted. Whether SMS is required is not clear (see Q-051).
- flags: C4-11
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority set from client answer, round 3 (Section D, "Q-034")

### REQ-046 · Managers can override an automatic booking confirmation
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-020 [NEW]")
- quote: "Confirm: Automatic, but Manager can override"
- why: Which "manager" may override is not clear after round 3, which has five roles (Q-064).
- blocked-by: Q-064
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-037.
- flags: C4-03, C4-05, C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3: why
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-047 · Front desk staff record check-ins and no-shows when the guest arrives
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-021")
- quote: "Front desk records check-ins and no-shows when guest arrives."
- why: Round 3 confirms it: "Record check-in: YES" and "Record no-show: YES". Reports need no-shows (REQ-007). Hotel managers may also mark no-shows (REQ-069).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-039.
- flags: C4-05, C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section B, "Q-039"): why
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-048 · Managers create staff logins with an email and a temporary password
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-022 [NEW]")
- quote: "Manager creates staff logins in the system."
- why: The client adds: "Each staff member gets email + temporary password." Who creates the managers' own logins is not stated.
- blocked-by: Q-050
- priority: MVP (proposed: the client says "Staff logins and roles: YES, essential." for December; to be confirmed)
- acceptance: not drafted. See Q-050.
- flags: C4-03, C4-06
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority set from client answer, round 3 (Section D, "Q-034")

### REQ-049 · Staff must change their temporary password at first login
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-022 [NEW]")
- quote: "Staff need to change password on first login."
- why: On extra security the client is unsure: "maybe two-factor authentication for managers, but not front desk staff" (Q-050).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: Given a staff member logs in for the first time with a temporary password, when they sign in, then they must set a new password before continuing.
- flags: C4-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-050 · Hotel managers can update their own hotel's information after launch
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-025 [NEW]")
- quote: "the manager at each hotel can update their own hotel's info"
- why: Changes need approval before going live (RULE-024). This sits oddly with "Manager (all six hotels)" (REQ-061).
- blocked-by: Q-052
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-052.
- flags: C4-05, C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-051 · Only 4-star and 5-star guest reviews (about 50, chosen by Yusuf) move to the new site
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-054
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-027")
- quote: "Reviews: only 4-star and 5-star reviews, maybe 50 of them total. I'll pick which ones."
- why: The client also said "No 1-star or 2-star reviews going up." 3-star reviews are not mentioned (Q-056).
- blocked-by: Q-056
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-056.
- flags: C4-05, C4-25
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-052 · All photos, the location and contact details, and refreshed descriptions move to the new site
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-054
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-027")
- quote: "Photos: yes, all of them. Location and contact: yes. Descriptions: yes, but some are outdated — we'll refresh them."
- why: This answers the conflict in REQ-027: descriptions and reviews also move over. Replaces REQ-027. Who refreshes the descriptions is not stated (Q-056).
- blocked-by: Q-056
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-056.
- flags: C4-05, C4-11
- history:
  - 2026-09-28 created from client answers, round 2. Replaces REQ-027
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-053 · Arabic is shown first and English second
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-028 [NEW]")
- quote: "Arabic first — 80% of guests are Saudi. English second for international and expat guests."
- why: REQ-008 says everything is bilingual; this sets the order.
- priority: MVP (proposed: the client says "Arabic pages: YES, must have." for December; to be confirmed)
- acceptance: Given a guest opens the site with no language chosen, when the page loads, then it is shown in Arabic and English can be chosen.
- flags: C4-06
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority set from client answer, round 3 (Section D, "Q-034")

### REQ-054 · The old website is turned off and the new platform replaces it on launch day
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: PRB-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-032")
- quote: "Replace it completely on launch day."
- why: The client adds: "Turn off the old site, point everything to the new one. Clean break. No running both at the same time."
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. The domain is in conflict (see REQ-063).
- flags: C4-05, C4-09
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-055 · The platform supports about 200 bookings a month in the first year
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-033 [NEW]")
- quote: "We want to grow to 200 per month in year one."
- why: Today: "Right now: 50 bookings per month across all hotels (that's our current total)." Busy seasons: "Hajj (Sept-Oct), holidays (Dec-Jan, June-July), weekends always." These numbers look low next to the room counts (Q-057). Round 3 answers Q-057: "It's the real total across all six hotels, right now." Per hotel: "Jeddah and Riyadh do maybe 20 bookings a month each." "Dammam, Medina, Abha are slower — 5 each." "Makkah is seasonal (only Hajj time, so maybe 30 bookings in one month, zero the rest of the year)." These add up to about 690 bookings a year (calculated), against "~600 bookings a year" (ASM-003), so all the figures are rough.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-057.
- flags: C4-02, C4-05, C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section A, "Q-057"): why
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-056 · The site works on older phones and slow internet connections
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-033 [NEW]")
- quote: "the site should work on older phones and slow internet"
- why: The client also said "Phones: probably 40% of visitors use phones, 60% desktop." and "No specific accessibility needs". "Older" and "slow" have no measurable target (Q-058, Q-019). Round 3: "Page load time: under 3 seconds on phone on 4G (not 5G, because some guests have older connections)" (REQ-072). Which older phones and browsers is still open (Q-058).
- blocked-by: Q-058
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. No target yet (see Q-058).
- flags: C4-05, C4-12
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section D, "Q-019"): why
  - 2026-09-28 blocked-by updated after client answers, round 3
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-057 · Someone is reachable if the site or payment stops working outside business hours
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-034 [NEW]")
- quote: "We need someone reachable if the site crashes at 3 AM during Hajj."
- why: The client asks: "maybe you have an on-call plan?" Whether this is in the project scope is not decided (Q-059, RISK-004).
- blocked-by: Q-059
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-059.
- flags: C4-05, C4-09, C4-12
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-058 · The platform holds the client's six hotels with their room types and room counts
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-010
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-024")
- quote: "Jeddah Grand: Jeddah, 80 rooms (20 single, 40 double, 15 suite, 5 presidential)"
- why: The client's list: "Riyadh Palace: Riyadh, 120 rooms (30 single, 60 double, 20 suite, 10 presidential)"; "Dammam Beach: Dammam, 60 rooms (15 single, 30 double, 10 suite, 5 deluxe)"; "Makkah Comfort: Makkah, 40 rooms (20 single, 20 double) — only during Hajj season"; "Medina Rest: Medina, 50 rooms (15 single, 25 double, 10 suite)"; "Abha Heights: Abha, 30 rooms (10 single, 15 double, 5 suite)". The room counts add up to 380 (calculated). Round 1 named "Al Riyadh and Al Jeddah" (Q-053).
- blocked-by: Q-053
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See Q-053.
- flags: C4-05, C4-11, C4-19
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 priority note updated after client answers, round 3 (still unknown)

### REQ-059 · Which currencies guests see and pay in is unclear (answers differ)
- type: REQ
- label: CONFLICT
- status: AI-DRAFT
- parent: REQ-015
- sources:
  - inputs/client-answers-2026-09-28.md (answer 8, headed "[Q-005] Payment and currencies"): "Mostly Saudi Riyal, but some international guests pay in USD."
  - inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-009"): "Show both SAR and USD, but charge in SAR."
  - inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-028 [NEW]"): "Currency always in SAR."
- why: Round 1 says some guests pay in USD. Round 2 says charge in SAR only, show USD for reference, and also "Currency always in SAR." No winner is picked here. REQ-015 stays as written.
- blocked-by: Q-036
- priority: unknown (open conflict)
- acceptance: not drafted. Open conflict.
- flags: C4-05, C4-14
- history:
  - 2026-09-28 created from client answers, round 2

### REQ-060 · Which staff roles exist is unclear (two lists differ)
- type: REQ
- label: CONFLICT
- status: SUPERSEDED
- parent: NEED-002
- sources:
  - inputs/client-answers-2026-09-28.md (answer 11, headed "[Q-004] Admin roles"): "Three roles: (1) Head office — can see all 6 hotels, manage all bookings, change prices and availability, view reports. (2) Hotel manager — only sees their own hotel's bookings and can manage them. (3) Front desk staff — can only view bookings, not change anything."
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-020 [NEW]"): "Three roles: Guest, Front Desk Staff, Hotel Manager."
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-020 [NEW]"): "Change prices: Only Manager"
- why: Round 1 has head office, hotel manager and front desk. Round 2 has guest, front desk and manager, with no head office role, and gives price changes and reports to "Manager". The client also asked whether Fatima logs in once for all six hotels (Q-033). No winner is picked here. REQ-023, REQ-024 and REQ-025 stay as written.
- blocked-by: Q-037, Q-033
- priority: unknown (open conflict)
- acceptance: not drafted. Open conflict.
- superseded-by: REQ-064
- flags: C2-02, C2-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 superseded by REQ-064 after client answers, round 3

### REQ-061 · Whether hotel managers see only their own hotel or all six is unclear (answers differ)
- type: REQ
- label: CONFLICT
- status: SUPERSEDED
- parent: REQ-024
- sources:
  - inputs/client-answers-2026-09-28.md (answer 11, headed "[Q-004] Admin roles"): "Hotel manager — only sees their own hotel's bookings and can manage them."
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-020 [NEW]"): "View bookings: Guest (own), Front Desk (all at their hotel), Manager (all six hotels)"
- why: Round 2 also says "the manager at each hotel can update their own hotel's info" (REQ-050), and the client asks "can all staff see all hotels, or only their own?" No winner is picked here.
- blocked-by: Q-038
- priority: unknown (open conflict)
- acceptance: not drafted. Open conflict.
- superseded-by: REQ-065
- flags: C2-02, C2-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 superseded by REQ-065 after client answers, round 3

### REQ-062 · What front desk staff may do is unclear (view-only versus recording bookings)
- type: REQ
- label: CONFLICT
- status: SUPERSEDED
- parent: REQ-025
- sources:
  - inputs/client-answers-2026-09-28.md (answer 11, headed "[Q-004] Admin roles"): "Front desk staff — can only view bookings, not change anything."
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-021"): "Front desk records check-ins and no-shows when guest arrives."
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-020 [NEW]"): "Mark deposit paid: Front Desk (for phone bookings), automatic for online"
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-021"): "Phone cancellations — whoever takes the call (front desk or manager) records it immediately."
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-020 [NEW]"): "Cancel: Guest (if within cancellation window), Manager"
- why: Front desk is view-only in round 1, but in round 2 it records check-ins and no-shows, marks payments, types in phone bookings (REQ-030) and records phone cancellations, while the cancel permission list leaves front desk out. No winner is picked here.
- blocked-by: Q-039
- priority: unknown (open conflict)
- acceptance: not drafted. Open conflict.
- superseded-by: REQ-068
- flags: C2-02, C2-05
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 superseded by REQ-068 after client answers, round 3

### REQ-063 · Which domain name the new platform uses, and who sets it up, is unclear (answers differ)
- type: REQ
- label: CONFLICT
- status: AI-DRAFT
- parent: REQ-012
- sources:
  - inputs/client-answers-2026-09-28.md (answer 5, headed "[Q-012] Migration from old site"): "We can keep the same domain name (something like saudhotels.com or similar). My IT person can handle that."
  - inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-031"): "Domain: saudiarabbookings.com (not finalized yet, maybe). I haven't registered it. Can you register it and handle the DNS?"
  - inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-031"): "Our current site is on a different domain — oldsite.sa — but we're not using it anymore."
- why: Round 1 keeps the current domain and has the client's IT person handle it. Round 2 gives a new, unregistered domain and asks the project team to register it and handle DNS. No winner is picked here. REQ-012 and DEP-004 stay as written.
- blocked-by: Q-042
- priority: unknown (open conflict)
- acceptance: not drafted. Open conflict.
- flags: C4-05, C4-14
- history:
  - 2026-09-28 created from client answers, round 2

### REQ-064 · The platform has five roles: Owner, Head office manager, Hotel manager, Front desk staff and Guest
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: NEED-002
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-037")
- quote: "So really, it's 5 roles: Owner (me), Head office manager (Fatima), Hotel manager (6 of them), Front desk staff (many), Guest."
- why: Yusuf is the owner and Fatima the head office manager: "Fatima (my manager): Also head office. She runs day-to-day operations across all six hotels. Same access as me." Replaces REQ-060. REQ-023 (head office) and REQ-024 (hotel managers) still stand.
- priority: MVP (proposed: the client says "Staff logins and roles: YES, essential." for December; to be confirmed)
- acceptance: not drafted. What each role may do is in REQ-065 to REQ-069, RULE-030 and RULE-031.
- flags: C4-06, C4-11
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md. Replaces REQ-060

### REQ-065 · Hotel managers and front desk staff see only their own hotel's bookings
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-064
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-038")
- quote: "Hotel manager: only their own hotel. Front desk: only their own hotel."
- why: Round 3 also says "Fatima and me: all six hotels." (REQ-066). This matches round 1 (REQ-024). "Manager (all six hotels)" in round 2 is taken to mean the head office manager (Q-064). Replaces REQ-061.
- priority: MVP (proposed: the client says "Staff logins and roles: YES, essential." for December; to be confirmed)
- acceptance:
  - Given a hotel manager or a front desk user of one hotel, when they open the bookings list, then they see only that hotel's bookings.
- flags: C4-06
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md. Replaces REQ-061

### REQ-066 · Head office users log in once and see all six hotels
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-064
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-033")
- quote: "One login that shows all six hotels in a dashboard is much better."
- why: The client also said "One login for me and Fatima. Six separate logins is too much hassle." Whether that means each has one login or they share one is not clear (Q-065). He also said the admin dashboard can wait (REQ-005), so whether "dashboard" means more than a bookings list in December is open (Q-071).
- blocked-by: Q-065, Q-071
- priority: MVP (proposed: staff roles are essential for December and head office needs to see all six hotels (REQ-019); to be confirmed)
- acceptance:
  - Given a head office user has signed in, when they open the bookings list, then they see the bookings of all six hotels without signing in again.
- flags: C4-03, C4-06
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-067 · Guests see only their own bookings
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-064
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-038")
- quote: "Guests: only their own booking."
- why: Round 3 also says guests "Can book, view their own bookings, cancel/change within rules." (REQ-017, REQ-040).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a guest is signed in, or has entered a booking number and email, when they open their bookings, then they see only their own booking.
- flags: C4-05
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-068 · Front desk staff can mark a payment as received for phone and card bookings
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-064
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-039")
- quote: "Mark payment received: YES (for phone/card bookings)"
- why: Replaces REQ-062 and REQ-025. The round-3 answers on what front desk staff may do: "Type in phone bookings: YES" (REQ-030), "Record check-in: YES" and "Record no-show: YES" (REQ-047), "Record phone cancellation: YES" (REQ-022), "Change booking dates: NO — only hotel manager can do that" (RULE-031), "Change prices: NO" (RULE-030).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a front desk user has taken a phone booking and charged the card, when they mark the payment as received, then the booking shows the deposit as paid.
- flags: C4-05
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md. Replaces REQ-062 and REQ-025

### REQ-069 · Hotel managers can mark payments and no-shows for their hotel
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-064
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-037")
- quote: "can mark payments and no-shows"
- why: The round-3 description of the hotel manager: "They see only their own hotel's bookings, can mark payments and no-shows, but can't change prices or policies — I approve that." Only hotel managers change a booking's dates (RULE-031).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a hotel manager opens a booking of their hotel, when they mark it as a no-show, then the booking shows No-show.
- flags: C4-05, C4-11
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-070 · The rest of the payment can be paid by card, SADAD or a payment link emailed 3 days before arrival
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: RULE-033
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-043")
- quote: "we can email a payment link 3 days before"
- why: The client: "How: same method as deposit (card, SADAD, or we can email a payment link 3 days before". Applies to online bookings (RULE-033). Whether the system sends the link is not stated; today the client sends links by hand (Q-068).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance: not drafted. See RULE-033 and Q-072.
- flags: C4-04, C4-05, C4-11, C4-19
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-071 · Staff can mark in the system that the rest of the payment was paid at the desk
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: RULE-033
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-043")
- quote: "we need a way to mark it in the system"
- why: A guest who has not paid the rest before arrival "can still check in and pay at the desk". Which role marks it is not stated; front desk staff may mark payments received for phone and card bookings (REQ-068).
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a guest has not paid the rest before arrival, when they pay at the desk, then a staff member can mark the rest of the payment as paid and the booking shows paid in full.
- flags: C4-05
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-072 · Pages load in under 3 seconds on a phone on a 4G connection
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-001
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-019")
- quote: "Page load time: under 3 seconds on phone on 4G"
- why: The client adds "(not 5G, because some guests have older connections)". This is the target for "fast" (Q-019). See REQ-056.
- priority: MVP (proposed: "fast" is part of REQ-001, which is in the first version; to be confirmed)
- acceptance:
  - Given a guest opens a page on a phone on a 4G connection, when the page loads, then it has loaded in under 3 seconds.
- flags: C4-06
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-073 · A guest can book in no more than 5 steps: hotel, dates, room type, guest information and payment
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-002
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-019")
- quote: "To book: no more than 5 steps (hotel → dates → room type → guest info → payment)"
- why: This is the target for "simple to use" when booking (Q-019).
- priority: MVP (proposed: booking is in the first version; to be confirmed)
- acceptance:
  - Given a guest wants to book a room, when they go from choosing a hotel to paying, then they need no more than 5 steps: hotel, dates, room type, guest information and payment.
- flags: C4-06, C4-12
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-074 · A guest can cancel or change a booking in no more than 3 clicks
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-017
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-019")
- quote: "To cancel or change: no more than 3 clicks"
- why: Where the 3 clicks start (from the booking, or from the site) is not stated.
- priority: unknown (not in the client's December answers; see Q-070)
- acceptance:
  - Given a guest has opened their booking, when they cancel it or change its dates, then they need no more than 3 clicks.
- flags: C4-05, C4-12
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### REQ-075 · Staff can type in a booking in no more than 2 minutes
- type: REQ
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-030
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-019")
- quote: "Staff to type in a booking: no more than 2 minutes total"
- priority: MVP (proposed: the client says a screen to type in bookings is a December must-have (REQ-030); to be confirmed)
- acceptance:
  - Given a front desk user has a guest on the phone, when they type in the booking, then it takes no more than 2 minutes in total.
- flags: C4-06
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

## Business rules (RULE)

### RULE-001 · The new platform is wanted within 4 months
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: none
- source: inputs/brief-2026-09-28.md line 20
- quote: "We want the new platform within 4 months."
- why: Parent is none because the deadline applies to the whole project. The client now says: "The deadline is hard: 4 months maximum." and "The 4 months starts now (late September)." That points to about late January. See also RULE-004 for the end-of-December date.
- flags: C4-07, C4-08
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answers to Q-007, Q-014: why and blocked-by changed
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 blocked-by updated after client answers, round 2

### RULE-002 · The client, Yusuf, makes the final decisions
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: none
- source: client answer 2026-09-28 (Q-014)
- quote: "I make the final decisions."
- why: An approval rule for the whole project. Yusuf's job title is not stated.
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-014 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1

### RULE-003 · The budget for the platform is about 120,000 Saudi Riyals
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: none
- source: client answer 2026-09-28 (Q-014)
- quote: "I have about 120,000 Saudi Riyals (~$32,000 USD) for the platform"
- why: The client also said "I'm flexible if it's worth it", which has no limit. What the budget includes is not stated (Q-031).
- blocked-by: Q-048
- flags: C4-07, C4-20
- history:
  - 2026-09-28 created from client answer to Q-014 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2

### RULE-004 · Guests must be able to book online by the end of December
- type: RULE
- label: KNOWN
- status: SUPERSEDED
- parent: none
- source: client answer 2026-09-28 (Q-007)
- quote: "What matters is guests can book online by end of December."
- why: This is earlier than the 4-month deadline in RULE-001. The two may be two milestones; it is not stated (Q-016).
- blocked-by: Q-016
- superseded-by: RULE-010
- flags: C1-20
- history:
  - 2026-09-28 created from client answer to Q-007 (answers pasted by the BA)
  - 2026-09-28 superseded by RULE-010 after client answers, round 2

### RULE-005 · A deposit is paid when booking, usually 25-50% of the total
- type: RULE
- label: KNOWN
- status: SUPERSEDED
- parent: REQ-003
- source: client answer 2026-09-28 (Q-005)
- quote: "Guests should pay a deposit up front — usually 25-50% of the total."
- why: "Usually" means the percentage varies. What decides it, and how the rest is paid, is not stated.
- blocked-by: Q-021
- superseded-by: RULE-012
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-005 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 superseded by RULE-012 after client answers, round 2

### RULE-006 · Free cancellation up to 7 days before arrival; after that the deposit is kept, with no partial refunds
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: client answer 2026-09-28 (Q-006)
- quote: "Free cancellation up to 7 days before arrival. After that, we keep the deposit. No partial refunds — it's all or nothing."
- why: "Free" is taken to mean the deposit is refunded in full. Edge cases (late bookings, no-shows) are not stated (Q-023).
- blocked-by: Q-040
- flags: C4-07, C4-14
- history:
  - 2026-09-28 created from client answer to Q-006 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 blocked-by updated after client answers, round 2

### RULE-007 · Changing dates instead of cancelling is free at any time
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: client answer 2026-09-28 (Q-006)
- quote: "If a guest needs to change dates instead of cancel, that's free anytime."
- why: "Anytime" could include the arrival day, and could let a guest avoid losing the deposit under RULE-006 (Q-023).
- blocked-by: Q-040
- flags: C4-07, C4-14
- history:
  - 2026-09-28 created from client answer to Q-006 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 blocked-by updated after client answers, round 2

### RULE-008 · Room types and prices differ slightly between hotels
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-011
- source: client answer 2026-09-28 (Q-003)
- quote: "different room types and slightly different pricing"
- why: The client also said the hotels are "all 3-star". How prices are set is not stated (Q-028).
- blocked-by: Q-054
- flags: C4-07
- history:
  - 2026-09-28 created from client answer to Q-003 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 blocked-by updated after client answers, round 2

### RULE-009 · No booking data is moved from the old website
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-012
- source: client answer 2026-09-28 (Q-012)
- quote: "We don't have old booking data"
- why: The client said guests "called or booked through third-party sites", so there are no old customer accounts to move either.
- flags: C4-13
- history:
  - 2026-09-28 created from client answer to Q-012 (answers pasted by the BA)

### RULE-010 · End of December is the hard deadline, and the platform goes live then
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: none
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-016")
- quote: "End of December is our hard deadline."
- why: Parent is none because it applies to the whole project. The client adds: "After December, we'll add features in January if needed, but December is when we go live." About 13 weeks from 2026-09-28 (calculated). Earlier than the 4-month limit in RULE-001. Replaces RULE-004.
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2. Replaces RULE-004
  - 2026-09-28 checked by /ba-check run 2

### RULE-011 · All payments go to one central head-office account first
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-006 [NEW]")
- quote: "everything goes to head office first"
- why: The client said "One central account for now." and that money is split between hotels in the accounting system. Who processes refunds and which accounting tool is used are not stated (Q-045).
- blocked-by: Q-045
- flags: C4-04
- history:
  - 2026-09-28 created from client answers, round 2

### RULE-012 · The deposit is 25% for bookings 7 or more days before arrival and 50% for bookings less than 7 days before
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-007")
- quote: "25% for bookings 7+ days before arrival. 50% for bookings less than 7 days."
- why: Replaces RULE-005. When and how the rest is paid: see RULE-033.
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2. Replaces RULE-005
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3: why
  - 2026-09-28 blocked-by updated after client answers, round 3

### RULE-013 · Walk-ins and phone bookings are paid in full
- type: RULE
- label: KNOWN
- status: SUPERSEDED
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-007")
- quote: "Full payment for walk-ins and phone bookings — they pay when they arrive or reserve by phone."
- why: It is not clear whether phone guests pay when they reserve or on arrival (Q-044).
- blocked-by: Q-044
- superseded-by: RULE-034
- flags: C2-04
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 superseded by RULE-034 after client answers, round 3

### RULE-014 · A no-show loses the deposit
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-010")
- quote: "No-show: We keep the deposit, they lose it."
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-015 · A guest who changes to a costlier period pays the difference before arrival
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-017
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-010")
- quote: "Changes to costlier period: They pay the difference before arrival."
- why: Changing to a cheaper period is not mentioned.
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-016 · Refunds go back to the same payment method within 48 hours
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-010")
- quote: "Refunds: Go back to the same payment method within 48 hours."
- why: How refunds work for SADAD is not stated (Q-045, Q-046).
- blocked-by: Q-045
- flags: C4-04
- history:
  - 2026-09-28 created from client answers, round 2

### RULE-017 · A failed payment leaves the booking unconfirmed, and the room is held for 2 hours and then released
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-011 [NEW]")
- quote: "If payment fails, the booking is not confirmed. Room is held for 2 hours, then released."
- why: SADAD and bank transfers may take longer than 2 hours to confirm (Q-046). The answer to "leaves halfway" is unclear (Q-047).
- blocked-by: Q-046, Q-047
- flags: C4-04
- history:
  - 2026-09-28 created from client answers, round 2

### RULE-018 · If two guests want the last room, the first to complete payment gets it
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-002
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-011 [NEW]")
- quote: "If two guests want the last room, first one to complete payment gets it."
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-019 · The 120,000 SAR budget includes hosting, payment gateway fees, translation, running the platform and first-year support
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: RULE-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-013")
- quote: "Yes, all of it. Hosting, payment gateway fees, translation of descriptions, running the platform, support for the first year."
- why: The client adds: "After year one, we pay separately." The split is not stated (Q-048, RISK-005).
- blocked-by: Q-048
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-020 · Guest data is kept for 3 years for accounting
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section C, answer headed "Q-015 [NEW]")
- quote: "Keep guest data for 3 years for accounting."
- why: This conflicts with deleting data when an account is closed (RULE-028). Privacy text: "I trust you to handle that." (RISK-004).
- flags: C4-01
- history:
  - 2026-09-28 created from client answers, round 2

### RULE-021 · Prices are set by room type and date; high season is 2x normal price and low season is the same or discounted
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-011
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-024")
- quote: "Prices are set by room type and date. High season (Hajj, holidays): 2x normal price. Low season: same or discounted."
- why: The season dates are not given, and "discounted" has no amount (Q-054).
- blocked-by: Q-054
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-022 · Makkah Comfort sells rooms only during Hajj season
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-058
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-024")
- quote: "Makkah Comfort: Makkah, 40 rooms (20 single, 20 double) — only during Hajj season"
- why: Hajj dates are not given. The client wrote "Hajj (Sept-Oct)" for busy seasons, which needs checking (Q-054).
- blocked-by: Q-054
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-023 · Shown prices include VAT and any booking fee
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-024")
- quote: "Yes, show the total the guest will pay, including VAT and any booking fee."
- why: It is not known what the "booking fee" is (Q-055).
- blocked-by: Q-055
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 3

### RULE-024 · Changes to hotel information need Yusuf's approval before they go live
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-050
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-025 [NEW]")
- quote: "But changes need my approval before they go live"
- why: The client adds: "I don't want wrong prices or descriptions showing." Round 2 also says "Change prices: Only Manager" with no approval step (Q-052).
- blocked-by: Q-052
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-025 · Yusuf reviews and approves the room and price data before launch
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-058
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-026 [NEW]")
- quote: "Then I'll review and approve before launch."
- why: With DEP-007. The client also said "You or your team enters it." (RISK-004).
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-026 · Dates are shown as DD/MM/YYYY in both languages
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-053
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-028 [NEW]")
- quote: "Dates should show as DD/MM/YYYY in both languages."
- why: The client also said "Currency always in SAR." (see REQ-059).
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### RULE-027 · Whether changing dates is free at any time or only more than 7 days before arrival is unclear (answers differ)
- type: RULE
- label: CONFLICT
- status: AI-DRAFT
- parent: RULE-007
- sources:
  - inputs/client-answers-2026-09-28.md (answer 9, headed "[Q-006] Cancellation rules"): "If a guest needs to change dates instead of cancel, that's free anytime."
  - inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-010"): "Free date change: Only if changed more than 7 days before. After that, it costs."
- why: Round 1 says free anytime. Round 2 says free only more than 7 days before. No winner is picked here. RULE-007 stays as written.
- blocked-by: Q-040
- flags: C4-14
- history:
  - 2026-09-28 created from client answers, round 2

### RULE-028 · What happens to guest data when an account is closed is unclear (delete versus keep 3 years)
- type: RULE
- label: CONFLICT
- status: AI-DRAFT
- parent: REQ-044
- sources:
  - inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-018 [NEW]"): "Close account: just delete their data after they confirm (email confirmation)."
  - inputs/client-answers-round-2-2026-09-28.md (Section C, answer headed "Q-015 [NEW]"): "Keep guest data for 3 years for accounting."
- why: Deleting data on closure and keeping it for 3 years cannot both apply to the same data. No winner is picked here.
- blocked-by: Q-041
- flags: C4-14
- history:
  - 2026-09-28 created from client answers, round 2

### RULE-029 · A booking counts as direct when it does not come through Booking.com or Agoda
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: inputs/client-answers-round-3-2026-09-28.md (Section A, answer headed "New Q-3")
- quote: "Yes, phone and walk-in count as direct — they're not going through Booking.com or Agoda."
- why: The client lists direct as "10% direct (phone, email, walk-in)". Bookings that staff type in for phone and walk-in guests count as direct. The goal is counted by money (GOAL-004).
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### RULE-030 · Hotel managers cannot change prices or policies; the owner approves those changes
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-064
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-037")
- quote: "can't change prices or policies — I approve that"
- why: The owner has the "ability to change prices and policies" and Fatima has the "Same access as me." Front desk staff: "Change prices: NO". Round 2 said "Change prices: Only Manager"; which manager is meant is open (Q-064).
- flags: C4-15
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### RULE-031 · Only a hotel manager can change a booking's dates; front desk staff cannot
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-064
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-039")
- quote: "Change booking dates: NO — only hotel manager can do that"
- why: This is in the answer on what front desk staff may do. Guests can change dates within the rules (RULE-007, RULE-027, Q-040). Whether head office can also change dates is not stated (Q-064).
- blocked-by: Q-064
- flags: C4-19
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### RULE-032 · VAT is 15% on room prices
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-037
- source: inputs/client-answers-round-3-2026-09-28.md (Section C, answer headed "Q-049")
- quote: "VAT is 15% on room prices."
- why: A client statement, not checked against an official source. In round 2 he said "I think it's 15%". His accountant Ahmed handles the details (DEP-006). Shown prices include VAT (RULE-023).
- flags: C4-01
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### RULE-033 · The rest of the payment is due 2 days before arrival; a guest who has not paid can still check in and pay at the desk
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: RULE-012
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-043")
- quote: "If they don't pay the rest before arrival, they can still check in and pay at the desk."
- why: The client also said "Deposit: paid at booking time (online, card or SADAD)" and "Rest of payment: due 2 days before arrival, or at check-in". What "or at check-in" means is not clear (Q-072).
- blocked-by: Q-072
- flags: C4-04, C4-19
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

### RULE-034 · Phone bookings pay the deposit by card over the phone, and the rest at check-in
- type: RULE
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-044")
- quote: "Phone booking: I take their card number over the phone and charge the deposit (25% or 50%). The rest is due at check-in."
- why: Replaces RULE-013 for phone bookings (RULE-013 said phone bookings pay in full). In the system: "Mark phone bookings as "deposit paid" (because the rest is due later)." Taking card numbers by phone is a risk (RISK-008).
- flags: C4-04
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md. Replaces RULE-013

### RULE-035 · Walk-in guests pay in full at the desk, in cash or by card
- type: RULE
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-044")
- quote: "Walk-in: They pay in full at the desk, cash or card."
- why: In the system: "Walk-ins: mark as "paid in full" once they hand over the money." This keeps the walk-in part of RULE-013 (superseded).
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

## Features (FEAT)

## Assumptions (ASM)

### ASM-001 · One platform serves all 6 hotels
- type: ASM
- label: ASSUMPTION
- status: SUPERSEDED
- parent: REQ-002
- source: BA reasoning
- why: The brief says "We operate 6 hotels in Saudi Arabia" (line 5) and asks for "the new platform" (line 20) in the singular, which suggests one shared platform. It does not say so.
- risk-if-wrong: Scope, cost and design change a lot if each hotel needs its own site or its own rules.
- validate-by: Ask Yusuf (Q-003).
- superseded-by: REQ-010
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 superseded by REQ-010 after the client answered Q-003

### ASM-002 · The new platform replaces the current website
- type: ASM
- label: ASSUMPTION
- status: SUPERSEDED
- parent: PRB-001
- source: BA reasoning
- why: The brief says "We already have a website but it is outdated." (line 18) and asks for "the new platform" (line 20). Replacing the old site is inferred, not stated.
- risk-if-wrong: The old site may need to stay live alongside the new one, or content, the web address and old bookings may need to move across.
- validate-by: Ask Yusuf (Q-012).
- superseded-by: REQ-012
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 superseded by REQ-012 after the client answered Q-012

### ASM-003 · About 10% of bookings are direct today
- type: ASM
- label: ASSUMPTION
- status: AI-DRAFT
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-018")
- why: A client estimate, not a measurement: "Right now, maybe 10% come direct (email, phone, walk-in), 90% from Booking.com and Agoda." Round 3 gives the last 12 months: "roughly 60% Booking.com, 30% Agoda, 10% direct (phone, email, walk-in)" and "out of ~600 bookings a year, 360 from Booking.com, 180 from Agoda, 60 direct." Still rough ("roughly"), and by number of bookings, not by money (Q-062).
- risk-if-wrong: The first-year target (30% or 50%) and how success is measured depend on this starting point.
- validate-by: Ask Yusuf for booking counts by channel for the last 12 months.
- flags: C4-02
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section A, "New Q-3"): why
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### ASM-004 · Guest data stays in Saudi Arabia
- type: ASM
- label: ASSUMPTION
- status: AI-DRAFT
- parent: REQ-004
- source: inputs/client-answers-round-3-2026-09-28.md (Section C, answer headed "New Q-9")
- why: The client's own assumption: "I assume it stays in Saudi Arabia since the guests are Saudi, but again, ask Ahmed." He does not know the rules.
- risk-if-wrong: Hosting choice, cost and personal-data rules may change if guest data must stay in Saudi Arabia, or may go abroad.
- validate-by: Ask Ahmed (Q-049).
- flags: C4-01
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

## Open questions (Q)

### Q-001 · What business goal should the new platform achieve, and how will success be measured?
- type: Q
- label: UNKNOWN
- status: AI-DRAFT
- parent: GOAL-001
- source: inputs/brief-2026-09-28.md lines 7–14
- why: The brief lists solutions (website, booking, payment, accounts, dashboard, reports) but not the problem they should solve or what success looks like.
- ask: Yusuf
- answer: "We want to increase direct bookings on our own platform instead of always going through booking sites like Booking.com. We're paying them too much commission. Success means 30% of bookings come direct within the first year. Also, guests expect a modern experience — they should be able to book quickly and manage their reservations themselves, not call us."
- answered-on: 2026-09-28
- flags: C4-17
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to GOAL-002, PRB-002, NEED-003, Q-018

### Q-002 · What is outdated on the current website, and what would "modern" look like in a way we can check?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-001
- source: inputs/brief-2026-09-28.md lines 8 and 18
- why: "Modern" and "outdated" are vague words with no measurable target. We do not know which parts of the current site are the problem, or what works today and must be kept.
- ask: Yusuf
- answer: "It's slow, looks outdated, not mobile-friendly. Guests complain. What should be kept: the hotel photos are good, the location information is useful, and the contact details. Everything else needs to be new. Modern means fast, mobile-first, simple to use."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to PRB-003, REQ-027, Q-019, Q-027
  - 2026-09-28 checked by /ba-check run 2

### Q-003 · Should one platform serve all 6 hotels or one site per hotel, and how do the hotels differ?
- type: Q
- label: UNKNOWN
- status: AI-DRAFT
- parent: ASM-001
- source: inputs/brief-2026-09-28.md line 5
- why: The brief mentions 6 hotels but does not say whether they share rooms, prices, policies, languages, branding or staff.
- ask: Yusuf
- answer: "One platform for all 6 hotels. But each hotel should have its own page. The hotels are similar — all 3-star, but different room types and slightly different pricing. Al Riyadh and Al Jeddah are our flagship hotels. We manage everything centrally from the head office here."
- answered-on: 2026-09-28
- flags: C4-17
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to REQ-010, REQ-011, RULE-008, Q-028

### Q-004 · Who are the "admin" users, which real roles exist, and what may each role do?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-005
- source: inputs/brief-2026-09-28.md line 12
- why: "Admin" is a vague role. With 6 hotels there may be hotel-level and group-level roles with different permissions, but the brief does not say.
- ask: Yusuf
- answer: "Three roles: (1) Head office — can see all 6 hotels, manage all bookings, change prices and availability, view reports. (2) Hotel manager — only sees their own hotel's bookings and can manage them. (3) Front desk staff — can only view bookings, not change anything. We have 2 people at head office, and about 1-2 staff at each hotel."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to REQ-023, REQ-024, REQ-025, Q-026
  - 2026-09-28 checked by /ba-check run 2

### Q-005 · For online payment: what is paid for, which methods and currencies, which payment provider, and who receives the money?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: inputs/brief-2026-09-28.md line 10
- why: "Online payment" does not say whether guests pay the full amount, a deposit or nothing up front, or how money reaches each hotel.
- ask: Yusuf
- answer: "Guests should pay a deposit up front — usually 25-50% of the total. We need to accept credit cards (Visa, Mastercard), and some Saudi guests use local payment methods. Mostly Saudi Riyal, but some international guests pay in USD. We don't have a payment provider yet — you'll recommend one."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to RULE-005, REQ-013, REQ-014, REQ-015, DEP-001, Q-020, Q-021, Q-022. The part about who receives the money was not answered
  - 2026-09-28 checked by /ba-check run 2

### Q-006 · What are the cancellation, refund and partial-payment rules?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-003
- source: inputs/brief-2026-09-28.md line 10
- why: Online payment and booking management both need these rules, and the brief states none. They should become RULE items once answered.
- ask: Yusuf
- answer: "Free cancellation up to 7 days before arrival. After that, we keep the deposit. No partial refunds — it's all or nothing. If a guest needs to change dates instead of cancel, that's free anytime."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to RULE-006, RULE-007, Q-023
  - 2026-09-28 checked by /ba-check run 2

### Q-007 · When do the 4 months start, and what must be live by then?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-001
- source: inputs/brief-2026-09-28.md line 20
- why: The brief does not say whether the deadline is for everything listed or for a first version. Without this, no requirement can be given a priority (MVP, SHOULD, COULD, WONT).
- ask: Yusuf
- answer: "The 4 months starts now (late September). But we don't need everything on day one. A first version with the basics — a nice website, room search, booking, and payment — is fine. We can add the admin dashboard and reports later. What matters is guests can book online by end of December."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to RULE-004, REQ-009, priorities on REQ-001/002/003, Q-015, Q-016
  - 2026-09-28 checked by /ba-check run 2

### Q-008 · What should a customer account be used for, and can someone book without one?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-004
- source: inputs/brief-2026-09-28.md line 11
- why: "Customer accounts" does not say what customers can do in an account or whether an account is required to book.
- ask: Yusuf
- answer: "Guests should see their booking, check-in dates, room details, and be able to cancel or modify dates. They can book without creating an account, but if they do, they can manage their reservations easily. We want to collect their email and phone so we can send confirmations and reminders."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to REQ-016, REQ-017, REQ-018, Q-024
  - 2026-09-28 checked by /ba-check run 2

### Q-009 · What does "booking management" cover: who manages bookings, and which actions (view, change, cancel, refund)?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-006
- source: inputs/brief-2026-09-28.md line 13
- why: The brief does not say whether customers, the client's team or both manage bookings, or which actions are included.
- ask: Yusuf
- answer: "We need to view all bookings, see guest details, confirm or cancel them, track which ones have paid the deposit, and send reminders before arrival. Hotel managers should handle cancellations for their own hotel. If a guest calls to cancel, someone needs to mark it in the system quickly."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to REQ-019, REQ-020, REQ-021, REQ-022, Q-025, Q-026. Refunds were not answered separately
  - 2026-09-28 checked by /ba-check run 2

### Q-010 · Which reports are needed, for whom, how often, and per hotel or for all hotels together?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-007
- source: inputs/brief-2026-09-28.md line 14
- why: "Reports" names no report, reader, frequency or level of detail.
- ask: Yusuf
- answer: "Monthly reports showing: total bookings, revenue (by hotel and all together), occupancy rate, cancellations, and no-shows. Head office reads these. We need to see per-hotel data and combined data. Nothing fancy — Excel is fine, or PDF."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Updated REQ-007
  - 2026-09-28 checked by /ba-check run 2

### Q-011 · Which parts must be in both Arabic and English, and who writes and approves the text?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-008
- source: inputs/brief-2026-09-28.md line 16
- why: The brief does not say whether the customer website, emails and messages, payment pages, admin dashboard and reports must all be bilingual, or who provides the translations.
- ask: Yusuf
- answer: "Everything in both Arabic and English: the customer website, confirmation emails, payment pages, the admin dashboard, reports, everything. My head office team writes and approves the Arabic — I'll get them involved. The English should be clear and professional."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Updated REQ-008. Led to DEP-002, Q-030
  - 2026-09-28 checked by /ba-check run 2

### Q-012 · What must carry over from the current website (content, customer data, old bookings, web address, hosting), and who owns those accounts?
- type: Q
- label: UNKNOWN
- status: AI-DRAFT
- parent: ASM-002
- source: inputs/brief-2026-09-28.md line 18
- why: The brief says a website exists but not what it holds, who runs it, or what should move to the new platform.
- ask: Yusuf
- answer: "Our current website is hosted with a small Saudi hosting company. Content (descriptions, photos, some guest reviews) should move over. We don't have old booking data — guests called or booked through third-party sites. We can keep the same domain name (something like saudhotels.com or similar). My IT person can handle that."
- answered-on: 2026-09-28
- flags: C4-17
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to REQ-012, REQ-027, RULE-009, DEP-004, Q-027, Q-029

### Q-013 · How are rooms, prices and availability managed today, and must the new platform connect to any existing system?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-002
- source: inputs/brief-2026-09-28.md line 9
- why: The brief does not say how bookings are taken today or whether other systems (for example hotel software or third-party booking sites) must stay in sync.
- ask: Yusuf
- answer: "Most bookings come through Booking.com or Agoda. We also have a WhatsApp number where guests message us directly. Inside the hotels, front desk uses a spreadsheet to track rooms — very manual. No system. The new platform should be our single source of truth."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to PRB-004, REQ-026, RISK-001, Q-017
  - 2026-09-28 checked by /ba-check run 2

### Q-014 · Who decides scope, budget and the deadline, and is there a budget range?
- type: Q
- label: UNKNOWN
- status: AI-DRAFT
- parent: GOAL-001
- source: inputs/brief-2026-09-28.md (whole brief)
- why: The brief names no decision maker and gives no budget. Yusuf's role is not stated.
- ask: Yusuf
- answer: "I make the final decisions. I have about 120,000 Saudi Riyals (~$32,000 USD) for the platform, but I'm flexible if it's worth it. The deadline is hard: 4 months maximum. My team will help with content and testing."
- answered-on: 2026-09-28
- flags: C4-17
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 answer recorded (pasted by the BA). Led to RULE-002, RULE-003, DEP-003, RISK-002, Q-031. Updated RULE-001

### Q-015 · Which features must be in the first version, and how will head office and the hotels see and handle bookings on day one if the admin dashboard comes later?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-005
- source: client answer 2026-09-28 (Q-007)
- why: The client listed the first version as "a nice website, room search, booking, and payment" and said the admin dashboard and reports come later. Accounts, guest self-service, booking management, confirmation messages and Arabic/English are in neither list. Staff also need to see bookings and deposits from the first booking.
- ask: Yusuf
- answer: "End of December, we need guests to book online, staff to see bookings in a simple list, and payment confirmation. Admin dashboard can wait a month or two. But I have six hotels — does Fatima log in once and see all six, or six separate logins? And can all staff see all hotels, or only their own?"
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-007 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-015" in the client file; line breaks joined with spaces)

### Q-016 · Is "end of December" a first release with the full platform due in late January, or is end of December the real deadline? What must be live on each date?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-004
- source: client answer 2026-09-28 (Q-007, Q-014)
- why: The client gave two dates: "What matters is guests can book online by end of December." and "The deadline is hard: 4 months maximum." from late September, which is about late January. They may be two milestones, but this is not stated.
- ask: Yusuf
- answer: "End of December is our hard deadline. We're losing money right now because guests can't book direct — they go to Booking.com and pay 15% commission. After December, we'll add features in January if needed, but December is when we go live."
- answered-on: 2026-09-28
- flags: C4-17, C4-22
- history:
  - 2026-09-28 created from client answers to Q-007 and Q-014 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-016" in the client file; line breaks joined with spaces)

### Q-017 · How should bookings from Booking.com, Agoda, WhatsApp, phone and walk-ins get into the platform, by staff typing them in or by automatic sync? Will the hotels stay on those booking sites?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-026
- source: client answer 2026-09-28 (Q-013)
- why: The platform is meant to be the single source of truth, but most bookings come from other channels. Without a link, room availability could differ between systems (see RISK-001).
- ask: Yusuf
- answer: "Ideally, automatic sync from the booking sites. But if that's too complex, we can manually type them in for the first month. Walk-ins and phone bookings — our front desk staff will type those in when the guest calls or arrives."
- answered-on: 2026-09-28
- flags: C4-22
- history:
  - 2026-09-28 created from client answer to Q-013 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-017" in the client file; line breaks joined with spaces)

### Q-018 · What share of bookings are direct today, what commission do the booking sites charge, and is the 30% counted by number of bookings or by revenue? When does the first year start?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: client answer 2026-09-28 (Q-001)
- why: The success measure has no starting figure, no definition and no start date, so it cannot be checked yet. See RISK-003.
- ask: Yusuf
- answer: "Right now, maybe 10% come direct (email, phone, walk-in), 90% from Booking.com and Agoda. Booking.com charges 15%, Agoda charges 15%. So if a guest pays 1000 SAR, we get 850. We want to push that 10% direct up to 50% in the first year, which means the platform has to be really easy."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-001 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-018" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### Q-019 · How fast is "fast" and how simple is "simple to use", for example a page load time or a maximum number of steps to book?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-001
- source: client answer 2026-09-28 (Q-002)
- why: The client defined modern as "fast, mobile-first, simple to use". These are still vague words with no measurable target.
- ask: Yusuf
- answer: "Page load time: under 3 seconds on phone on 4G (not 5G, because some guests have older connections) To book: no more than 5 steps (hotel → dates → room type → guest info → payment) To cancel or change: no more than 3 clicks Staff to type in a booking: no more than 2 minutes total"
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-002 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 not answered in round 2; still open
  - 2026-09-28 answer recorded from round 3 (headed "Q-019" in the client file; line breaks joined with spaces)

### Q-020 · Which local Saudi payment methods must be supported?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-014
- source: client answer 2026-09-28 (Q-005)
- why: The client said "some Saudi guests use local payment methods" but named none.
- ask: Yusuf
- answer: "Most are Saudi nationals, so SADAD (bank transfer), credit card (Visa/Mastercard), and Apple Pay. Some international guests use card. WhatsApp payments from guests is common too, but that's manual. We don't use cash online."
- answered-on: 2026-09-28
- flags: C4-17
- history:
  - 2026-09-28 created from client answer to Q-005 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-008" in the client file; line breaks joined with spaces)

### Q-021 · What decides whether the deposit is 25% or 50%, and how and when is the rest paid?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-005
- source: client answer 2026-09-28 (Q-005)
- why: "Usually 25-50%" is a range. The system needs a rule (for example by hotel, room type, dates or guest), and the payment of the remaining balance is not described.
- ask: Yusuf
- answer: "25% for bookings 7+ days before arrival. 50% for bookings less than 7 days. Full payment for walk-ins and phone bookings — they pay when they arrive or reserve by phone."
- answered-on: 2026-09-28
- flags: C4-17
- history:
  - 2026-09-28 created from client answer to Q-005 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-007" in the client file; line breaks joined with spaces)

### Q-022 · How should US dollar payments work: are prices shown in both currencies, who sets the exchange rate, and which currency is the guest charged in?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-015
- source: client answer 2026-09-28 (Q-005)
- why: The client said some international guests pay in USD but not how prices and conversion should work.
- ask: Yusuf
- answer: "Some international guests ask about USD. Show both SAR and USD, but charge in SAR. We use today's exchange rate (1 USD = 3.75 SAR roughly). We don't want to manage two currencies, so USD is just for reference."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-005 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-009" in the client file; line breaks joined with spaces)

### Q-023 · Cancellation details: what if a guest books less than 7 days before arrival, does not show up, or changes dates to a more expensive period or when the hotel is full? Is "free anytime" also true on the arrival day, and how is a refund paid back?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-006
- source: client answer 2026-09-28 (Q-006)
- why: The rules cover the normal case only. Changing dates "anytime" for free could let a guest avoid losing the deposit under the 7-day rule.
- ask: Yusuf
- answer: "Less than 7 days: They pay 50% deposit. If they don't show up, we keep it. No-show: We keep the deposit, they lose it. Changes to costlier period: They pay the difference before arrival. Free cancellation: Only if cancelled more than 7 days before. Free date change: Only if changed more than 7 days before. After that, it costs. Refunds: Go back to the same payment method within 48 hours."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-006 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-010" in the client file; line breaks joined with spaces)

### Q-024 · Can guests who booked without an account still view, cancel or change their booking (for example with a booking number)?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-017
- source: client answer 2026-09-28 (Q-008)
- why: The goal is that guests manage reservations themselves and do not call, but the client said only guests with an account "can manage their reservations easily".
- ask: Yusuf
- answer: "Yes. They should get a booking number and confirmation email. They can use that booking number + email to log back in without a full account. If they lose the booking number, they can search by email."
- answered-on: 2026-09-28
- flags: C4-22
- history:
  - 2026-09-28 created from client answer to Q-008 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-017" in the client file; line breaks joined with spaces)

### Q-025 · Is a booking confirmed automatically once the deposit is paid, or does staff confirm it? Which channels (email, SMS, WhatsApp) and how many days before arrival are confirmations and reminders sent?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-018
- source: client answer 2026-09-28 (Q-008, Q-009)
- why: The client said staff "confirm or cancel" bookings and that guests get confirmations and reminders, but not what triggers a confirmation, which channels are used or when reminders go out.
- ask: Yusuf
- answer: "Automatic. As soon as payment clears, it's confirmed. Guest gets an email confirmation. Staff can see it immediately in the system. (Channels and timing were answered under the client's 'Q-023 [NEW]'; see REQ-045.)"
- answered-on: 2026-09-28
- flags: C4-22
- history:
  - 2026-09-28 created from client answers to Q-008 and Q-009 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-019" in the client file; line breaks joined with spaces)

### Q-026 · Front desk staff can only view bookings. Who records check-ins, no-shows and cancellations made by phone at each hotel, and is a hotel manager always available?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-068
- source: client answer 2026-09-28 (Q-004, Q-009, Q-010)
- why: Reports need no-shows, and a phone cancellation must be "mark[ed] in the system quickly", but front desk staff cannot change anything and hotel managers handle cancellations.
- ask: Yusuf
- answer: "Front desk records check-ins and no-shows when guest arrives. Phone cancellations — whoever takes the call (front desk or manager) records it immediately. How fast? Within 5 minutes if possible, or before the shift ends."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers to Q-004, Q-009 and Q-010 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-021" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent REQ-025 → REQ-068 after client answers, round 3

### Q-027 · Which content from the old website moves over: only photos, location information and contact details, or also descriptions and some guest reviews? Which reviews, and who decides?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-027
- source: client answer 2026-09-28 (Q-002, Q-012)
- why: The two answers differ (see REQ-027). Guest reviews were also mentioned without saying where they come from.
- ask: Yusuf
- answer: "Photos: yes, all of them. Location and contact: yes. Descriptions: yes, but some are outdated — we'll refresh them. Reviews: only 4-star and 5-star reviews, maybe 50 of them total. I'll pick which ones. No 1-star or 2-star reviews going up."
- answered-on: 2026-09-28
- flags: C4-17
- history:
  - 2026-09-28 created from client answers to Q-002 and Q-012 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-027" in the client file; line breaks joined with spaces)

### Q-028 · For each of the 6 hotels: what is the name, city and room types, and how are prices set (by room type, date or season)? What does "flagship" mean for this project? Do displayed prices include taxes and fees?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-008
- source: client answer 2026-09-28 (Q-003)
- why: Only "Al Riyadh and Al Jeddah" were named, as "our flagship hotels". The other four hotels, the room types and the pricing method are not described.
- ask: Yusuf
- answer: "Jeddah Grand: Jeddah, 80 rooms (20 single, 40 double, 15 suite, 5 presidential) Riyadh Palace: Riyadh, 120 rooms (30 single, 60 double, 20 suite, 10 presidential) Dammam Beach: Dammam, 60 rooms (15 single, 30 double, 10 suite, 5 deluxe) Makkah Comfort: Makkah, 40 rooms (20 single, 20 double) — only during Hajj season Medina Rest: Medina, 50 rooms (15 single, 25 double, 10 suite) Abha Heights: Abha, 30 rooms (10 single, 15 double, 5 suite) Prices are set by room type and date. High season (Hajj, holidays): 2x normal price. Low season: same or discounted. Flagship? Jeddah Grand is our oldest and most prestigious — it should look premium on the site. Do shown prices include tax and fees? Yes, show the total the guest will pay, including VAT and any booking fee."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-003 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-024" in the client file; line breaks joined with spaces)

### Q-029 · What is the exact domain name, who registered it and holds the login, and should the new platform stay with the current hosting company or move? Who is the IT person and how much time can they give?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-012
- source: client answer 2026-09-28 (Q-012)
- why: The domain was given as "something like saudhotels.com or similar", and the IT person was not named.
- ask: Yusuf
- answer: "Domain: saudiarabbookings.com (not finalized yet, maybe). I haven't registered it. Can you register it and handle the DNS? We need it to point to the new platform. Our current site is on a different domain — oldsite.sa — but we're not using it anymore."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-012 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-031" in the client file; line breaks joined with spaces)

### Q-030 · Who writes and checks the English text and the translation of hotel descriptions? Who in the head office team approves the Arabic, and how fast can they respond?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-008
- source: client answer 2026-09-28 (Q-011)
- why: The client said the head office team writes and approves the Arabic and that the English "should be clear and professional", but did not say who writes the English or who the Arabic contact is.
- ask: Yusuf
- answer: "You write English. I'll review it. For Arabic, I have a colleague Layla who speaks both — she'll translate and check. How fast? She can turn around translations in 3-5 days."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-011 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-029" in the client file; line breaks joined with spaces)

### Q-031 · Does the 120,000 SAR include hosting, payment fees, content and translation, and running and support costs for the first year? What does "flexible if it's worth it" mean in practice?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-003
- source: client answer 2026-09-28 (Q-014)
- why: "For the platform" does not say what is inside the budget, and "flexible" has no limit.
- ask: Yusuf
- answer: "Yes, all of it. Hosting, payment gateway fees, translation of descriptions, running the platform, support for the first year. After year one, we pay separately."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answer to Q-014 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-013" in the client file; line breaks joined with spaces)

### Q-032 · How should guests search for rooms: by hotel, dates, number of guests, room type? What do they see in the results?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-009
- source: client answer 2026-09-28 (Q-007)
- why: "Room search" is in the first version but the search inputs and results are not described.
- ask: Yusuf
- answer: "Yes to all four. Guest picks hotel (or sees all six), dates, number of guests, room type (single, double, suite, etc.). Results should show available rooms, price per night, total price for the stay."
- answered-on: 2026-09-28
- flags: C4-22
- history:
  - 2026-09-28 created from client answer to Q-007 (answers pasted by the BA)
  - 2026-09-28 checked by /ba-check run 1
  - 2026-09-28 answer recorded from round 2 (headed "Q-016" in the client file; line breaks joined with spaces)

### Q-033 · Should head-office users log in once and see all six hotels, or use six separate logins?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-064
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-015")
- why: The client asked this himself ("does Fatima log in once and see all six, or six separate logins?"). It is a design question for the BA to answer with a recommendation.
- ask: BA to recommend, then Yusuf decides
- answer: "One login for me and Fatima. Six separate logins is too much hassle. One login that shows all six hotels in a dashboard is much better."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-033" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent REQ-060 → REQ-064 after client answers, round 3

### Q-034 · For December, do you also need Arabic pages, VAT invoices, staff logins and roles, a screen for staff to type in bookings, and guest reminders, or only "guests book online, staff see bookings in a simple list, and payment confirmation"?
- type: Q
- label: UNKNOWN
- status: AI-DRAFT
- parent: RULE-010
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-015")
- why: The client's December list is short, but other answers depend on more: Arabic first for 80% of guests, invoices, staff logins for the booking list, typing in phone and booking-site bookings, and reminders.
- ask: Yusuf
- answer: "For December MVP: Arabic pages: YES, must have. 80% of guests are Saudi. VAT invoices: Not critical. We can do it manually after launch if needed. Staff logins and roles: YES, essential. I need to control who sees what. Screen to type bookings: YES, front desk needs this for phone bookings. Guest reminders: Email reminder 7 days before is nice. 2 days and 1 day are nice-to-have, not essential. So: Arabic, staff roles, booking entry — yes. Invoices and multiple reminders — can be after December."
- answered-on: 2026-09-28
- flags: C4-22
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-034" in the client file; line breaks joined with spaces)

### Q-035 · Which first-year target is right, 30% or 50% of bookings direct? Is it counted by number of bookings or by money, and when does the first year start?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-018")
- why: The two answers differ (GOAL-003). The rest of the original question, how it is counted and when the year starts, was not answered.
- ask: Yusuf
- answer: "50% is what we want to reach by end of year one, not by December. Right now it's 10% direct. By December, maybe 20%. By end of next year, 50%. Count it by money, not by number of bookings — a high-value booking matters more than a walk-in. Year one starts when we launch, so if we launch in December, year one runs Dec 2026 to Dec 2027."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-035" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent GOAL-003 → GOAL-004 after client answers, round 3

### Q-036 · Which currencies do guests see and pay in? Is USD shown for reference only, and is the rate fixed at 3.75 or live?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-059
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-009")
- why: The answers differ (REQ-059). The client said "today's exchange rate (1 USD = 3.75 SAR roughly)", which is not exact.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-037 · Which staff roles exist: head office, hotel manager and front desk (first answer), or guest, front desk and manager (second answer)? Where do you, Fatima and head office fit?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-064
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-020 [NEW]")
- why: The two role lists differ (REQ-060).
- ask: Yusuf
- answer: "Three roles: Me (Yusuf): Head office, owner. I should see everything — all hotels, all reports, ability to change prices and policies. Fatima (my manager): Also head office. She runs day-to-day operations across all six hotels. Same access as me. Hotel manager (one per hotel): Each hotel has a manager (like the manager in Jeddah). They see only their own hotel's bookings, can mark payments and no-shows, but can't change prices or policies — I approve that. Front desk staff (multiple per hotel): View bookings, type in phone bookings, mark check-ins. No access to other hotels. Guests: Can book, view their own bookings, cancel/change within rules. So really, it's 5 roles: Owner (me), Head office manager (Fatima), Hotel manager (6 of them), Front desk staff (many), Guest."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-037" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent REQ-060 → REQ-064 after client answers, round 3

### Q-038 · Does a hotel manager see only their own hotel or all six? Can all staff see all hotels, or only their own?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-065
- source: inputs/client-answers-round-2-2026-09-28.md (Section A, answer headed "Q-015")
- why: The answers differ (REQ-061), and the client asked the second part himself.
- ask: Yusuf
- answer: "Hotel manager: only their own hotel. Front desk: only their own hotel. Fatima and me: all six hotels. Guests: only their own booking."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-038" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent REQ-061 → REQ-065 after client answers, round 3

### Q-039 · May front desk staff change bookings (type in phone bookings, mark payments, record no-shows and phone cancellations), or only view?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-068
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-021")
- why: The answers differ (REQ-062). Who types in booking-site bookings during the first month is also not stated (REQ-031).
- ask: Yusuf
- answer: "They may change some things: Type in phone bookings: YES Mark payment received: YES (for phone/card bookings) Record check-in: YES Record no-show: YES Record phone cancellation: YES Change booking dates: NO — only hotel manager can do that Change prices: NO"
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-039" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent REQ-062 → REQ-068 after client answers, round 3

### Q-040 · Is changing dates free at any time, or only more than 7 days before arrival? What happens exactly 7 days before, for cancellations and for date changes?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-027
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-010")
- why: The answers differ (RULE-027). Round 1 says "up to 7 days before", round 2 says "more than 7 days before", and deposits use "7+ days".
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-041 · When a guest closes their account, is their data deleted, or kept for 3 years for accounting (for example bookings and invoices)?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-028
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-018 [NEW]")
- why: The answers cannot both apply (RULE-028).
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-042 · Which domain will the new platform use (saudiarabbookings.com or another), and who registers it and sets up DNS: your IT person or the project team? Where will the platform be hosted?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-063
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-031")
- why: The answers differ (REQ-063). Where to host, and who owns hosting and backups, were not answered.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-043 · For online bookings, when and how is the rest of the payment (after the 25% or 50% deposit) paid?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-012
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-007")
- why: The original question asked this. The answer covered only walk-ins and phone bookings.
- ask: Yusuf
- answer: "Deposit: paid at booking time (online, card or SADAD) Rest of payment: due 2 days before arrival, or at check-in How: same method as deposit (card, SADAD, or we can email a payment link 3 days before If they don't pay the rest before arrival, they can still check in and pay at the desk. But we need a way to mark it in the system."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-043" in the client file; line breaks joined with spaces)

### Q-044 · How do phone-booking and walk-in guests pay (card over the phone, a payment link, at the desk)? Is that recorded as "deposit paid" or "paid in full"?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-034
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-007")
- why: The answer says "they pay when they arrive or reserve by phone", but round 2 also says front desk marks the "deposit" paid for phone bookings.
- ask: Yusuf
- answer: "Phone booking: I take their card number over the phone and charge the deposit (25% or 50%). The rest is due at check-in. Walk-in: They pay in full at the desk, cash or card. In the system: Mark phone bookings as "deposit paid" (because the rest is due later). Walk-ins: mark as "paid in full" once they hand over the money."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-044" in the client file; line breaks joined with spaces)
  - 2026-09-28 parent RULE-013 → RULE-034 after client answers, round 3

### Q-045 · Who processes refunds, and which accounting system splits the money between hotels?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-016
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-006 [NEW]")
- why: The answer said the money is split "in the accounting system" but named no tool or person. Who processes refunds (paid back within 48 hours) is not stated.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-046 · Should Saudi debit cards (for example mada) or other wallets also be supported? SADAD and bank transfers may confirm more slowly than cards: does the 2-hour room hold apply to them?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-036
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-008")
- why: The client named only credit cards, SADAD and Apple Pay. Confirmation time of each method has not been checked (to be checked with the payment provider).
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-047 · The answer says "If a guest leaves halfway, they've already paid the deposit or full amount, so no refund". Did that mean a guest leaving their stay early? What happens if a guest abandons a booking before paying?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-017
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-011 [NEW]")
- why: The answer reads as if the guest had already paid, which does not fit "leaves halfway" through booking.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-048 · How is the 120,000 SAR split between building, hosting, payment fees, translation, running and first-year support? Does "translation" mean paying the project team or using Layla's time?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-019
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-013")
- why: The budget covers running costs as well as building (RISK-005), and translation is also done by Layla (DEP-009).
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-049 · Ask Ahmed (Yusuf's accountant): what do ZATCA registration and e-invoicing require, do invoices go to guests or only to your records, are there special rules for Makkah and Medina, and must guest data stay in Saudi Arabia?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-038
- source: inputs/client-answers-round-2-2026-09-28.md (Section C, answer headed "Q-014 [NEW]")
- why: Round 3 answers part of it: "VAT is 15% on room prices." (RULE-032). The client does not know the rest: "I honestly don't know the details." Ahmed handles it, and Yusuf will send his contact details (DEP-012). Research only if the BA asks.
- ask: Ahmed (Yusuf's accountant), contact details from Yusuf (DEP-012)
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 partly answered in round 3 (Section C, "Q-049"): VAT rate recorded as RULE-032; the rest goes to the accountant, so the question stays open and is narrower

### Q-050 · Do managers need two-factor login, yes or no? Who creates the managers' own logins?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-048
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-022 [NEW]")
- why: The client said "maybe" to two-factor for managers. He said managers create staff logins but not who creates managers'.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-051 · Are reminders sent automatically, by a manager, or both? Is SMS required, or only "if possible"?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-045
- source: inputs/client-answers-round-2-2026-09-28.md (Section D, answer headed "Q-023 [NEW]")
- why: Round 2 lists reminders as an automatic schedule, and also lists "Send reminders: Manager" as a permission.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-052 · Do all changes (prices, availability, descriptions) need your approval before they go live, and who approves when you are away?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-024
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-025 [NEW]")
- why: The client wants to approve changes before they go live, but the permission list says "Change prices: Only Manager" with no approval step.
- ask: Yusuf
- flags: C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-053 · Are "Al Riyadh" and "Al Jeddah" (first answer) the same hotels as Riyadh Palace and Jeddah Grand? Is Riyadh Palace also a flagship? What does "premium" look mean for the Jeddah Grand page?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-058
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-024")
- why: Round 1 said "Al Riyadh and Al Jeddah are our flagship hotels". Round 2 names only Jeddah Grand as flagship and says it "should look premium on the site".
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-054 · What are the exact Hajj dates this year and next, and the other high-season and low-season date ranges? When does Makkah Comfort open and close?
- type: Q
- label: UNKNOWN
- status: AI-DRAFT
- parent: RULE-021
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-024")
- why: No season dates were given. The client wrote "Hajj (Sept-Oct)" (Section F, "Q-033 [NEW]"). My understanding is that Hajj dates move earlier each year, so this needs checking (not researched).
- ask: Yusuf
- flags: C4-23
- history:
  - 2026-09-28 created from client answers, round 2

### Q-055 · What is the "booking fee" in the shown price, and how much is it?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-023
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-024")
- why: The client said prices include "any booking fee" but no such fee was described before.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-056 · Who refreshes the outdated descriptions, and by when? May 3-star reviews be used?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-052
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-027")
- why: The client said "we'll refresh them" without saying who, and only 4-star and 5-star reviews were named.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-057 · 50 bookings a month looks low for the 380 rooms listed (calculated from the six lists). Is the 50 per hotel, per week, or the real total?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-055
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-033 [NEW]")
- why: The direct-booking numbers depend on it: 10% of 50 is about 5 direct bookings a month today, and the targets are 200 a month and 30% or 50% direct.
- ask: Yusuf
- answer: "It's the real total across all six hotels, right now. We're not at full capacity. Jeddah and Riyadh do maybe 20 bookings a month each. Dammam, Medina, Abha are slower — 5 each. Makkah is seasonal (only Hajj time, so maybe 30 bookings in one month, zero the rest of the year). So yeah, 50 total is realistic for now. But with the new platform and direct bookings, we expect to grow to 200 a month by year end."
- answered-on: 2026-09-28
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 answer recorded from round 3 (headed "Q-057" in the client file; line breaks joined with spaces)

### Q-058 · Which older phones and browsers, and what internet speed, must the site work on? Are the phone and desktop shares (40% and 60%) measured or a guess?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-056
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-033 [NEW]")
- why: The client said "probably 40% ... use phones" but also wants "mobile-first". "Older" and "slow" have no target.
- ask: Yusuf
- flags: C4-07
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-059 · Who is reachable outside business hours if the site or payment fails, and is on-call support part of what the project team provides?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-057
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-034 [NEW]")
- why: The client said "I don't know yet" and asked "maybe you have an on-call plan?".
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-060 · Which of these client requests are in project scope and priced: recommend a payment provider, write the English text, register the domain and set up DNS, enter the first room and price data, write the privacy text, provide on-call support?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RISK-004
- source: inputs/client-answers-round-2-2026-09-28.md (several answers; see RISK-004)
- why: The client assumes the project team will do these. This is a decision for the BA first, and then to confirm with Yusuf.
- ask: BA to decide, then Yusuf
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### Q-061 · You said "By December, maybe 20%" of bookings direct. The platform goes live in December, so which December do you mean, and should we track 20% as a milestone?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: inputs/client-answers-round-3-2026-09-28.md (Section A, answer headed "Q-035")
- why: The answer to Q-035 gives 10% today, "By December, maybe 20%. By end of next year, 50%." The platform is not live until the end of December (RULE-010), so what would lift direct bookings from 10% to 20% before launch is unclear.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-062 · What share of your booking money (in SAR) came direct in the last 12 months?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: GOAL-004
- source: inputs/client-answers-round-3-2026-09-28.md (Section A, answer headed "New Q-3")
- why: The client wants the goal counted by money (GOAL-004). The 10% direct share he gave is by number of bookings: about 60 of about 600 a year (ASM-003). The share by money is not known.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-063 · Who types in Booking.com and Agoda bookings during the first month: Fatima, the hotel managers or front desk staff?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-031
- source: inputs/client-answers-round-3-2026-09-28.md (Section E, answer headed "Q-14")
- why: Today Fatima types them in: "I forward it to Fatima." The first-month fallback (REQ-031) does not say who does it, and only some roles may type in bookings.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-064 · In round 2 you wrote "Manager" for overriding a confirmation, cancelling, sending reminders, changing prices and seeing reports. Which of your five roles (Owner, Head office manager, Hotel manager, Front desk staff, Guest) may do each? May head office also change a booking's dates?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-046
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-037")
- why: Round 3 has five roles, and hotel managers cannot change prices (RULE-030), so it is not clear who "Manager" meant in the round-2 permission list (REQ-046, RULE-031, Q-051).
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-065 · Do you and Fatima each have your own login that shows all six hotels, or do you share one login?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-066
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-033")
- why: The answer says "One login for me and Fatima." Two people sharing one login would hide who did what.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-066 · What privacy and consent text must show at sign-up and at booking, and who writes it: the project team with Ahmed, or a lawyer? Is that inside the 120,000 SAR?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RISK-004
- source: inputs/client-answers-round-3-2026-09-28.md (Section C, answer headed "New Q-9")
- why: The client does not know the wording: "Privacy text — I don't know what the exact wording should be." He says "That's something you need to put together with Ahmed, our accountant, or a lawyer."
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-067 · Must the English pages also be ready in December, or only Arabic?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-053
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-034")
- why: The client said "Arabic pages: YES, must have. 80% of guests are Saudi." and did not mention English for December. Round 2 says English second, for international and expat guests (REQ-053).
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-068 · Which payment service or card machine do you use today to charge cards by phone and to send payment links on WhatsApp and email? Is it from your bank?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: DEP-001
- source: inputs/client-answers-round-3-2026-09-28.md (Section E, answer headed "Q-15")
- why: The client says "we reply with a payment link (via a payment service)" and "I take their card number over the phone and charge the deposit". Earlier he said he has no payment provider yet (DEP-001).
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-069 · At launch, must bookings that already exist (in the spreadsheet, on Booking.com and on Agoda) be entered into the new platform, and who enters them?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-054
- source: inputs/client-answers-round-3-2026-09-28.md (Section E, answer headed "Q-16")
- why: The client says the shared spreadsheet is "our single source of truth right now" and that the old site is turned off on launch day (REQ-054). RULE-009 covers only old website data.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-070 · Your December list is: online booking and payment confirmation, a staff booking list, Arabic pages, staff logins and roles, a screen to type in bookings, and the 7-day email reminder. Which of these are also needed in December: guest accounts and sign-in, guests viewing, cancelling or changing bookings online, SADAD and Apple Pay (or cards only), hotel managers editing hotel information, monthly reports?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-010
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-034")
- why: The answer to Q-034 says nothing on guest accounts and sign-in, guest self-service, SADAD and Apple Pay, hotel information editing or reports. Many requirements still have no priority.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-071 · You said the admin dashboard can wait a month or two, but head office wants one login that shows all six hotels "in a dashboard". Is a bookings list covering all six hotels enough for December?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: REQ-066
- source: inputs/client-answers-round-3-2026-09-28.md (Section B, answer headed "Q-033")
- why: REQ-005 (admin dashboard) is proposed as not for December, while REQ-066 asks for a view of all six hotels.
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

### Q-072 · Is the rest of the payment due 2 days before arrival with the desk as a fallback, or may guests choose to pay it at check-in from the start?
- type: Q
- label: UNKNOWN
- status: AI-CHECKED
- parent: RULE-033
- source: inputs/client-answers-round-3-2026-09-28.md (Section D, answer headed "Q-043")
- why: The client wrote "Rest of payment: due 2 days before arrival, or at check-in".
- ask: Yusuf
- flags: none
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
  - 2026-09-28 checked by /ba-check run 3

## Risks (RISK)

### RISK-001 · Rooms could be double-booked if the platform and the booking sites do not share availability
- type: RISK
- label: ASSUMPTION
- status: AI-DRAFT
- parent: REQ-026
- source: BA reasoning
- why: The client says "Most bookings come through Booking.com or Agoda" and wants the platform as the single source of truth. If a room is sold on a booking site and on the platform at the same time, availability differs. How availability is kept in sync is not stated (Q-017). In round 2 the client accepts typing booking-site bookings in by hand for the first month if sync is too complex (REQ-031), which raises this risk. Round 3: today double bookings are settled by hand: "Check the email timestamps — first one wins" (PRB-006).
- probability: unknown (depends on Q-017)
- impact: high
- mitigation: Decide in Q-017 how availability is kept in sync before design starts.
- flags: C4-07, C4-18
- history:
  - 2026-09-28 created from client answer to Q-013 (answers pasted by the BA)
  - 2026-09-28 why updated from client answer, round 2 (Section A, "Q-017")
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section E, "Q-14"): why

### RISK-002 · The hard 4-month deadline and the fixed budget may not fit the full wanted scope
- type: RISK
- label: ASSUMPTION
- status: AI-DRAFT
- parent: RULE-001
- source: BA reasoning
- why: The wanted scope includes two languages, 6 hotels, online payment, three staff roles, reports and a single source of truth. The client calls the deadline hard (RULE-001) and the budget about 120,000 SAR (RULE-003). No estimate exists yet, so this is a concern, not a finding. In round 2 the client says end of December is the hard deadline (RULE-010), about 13 weeks from 2026-09-28 (calculated), and that the budget also covers running costs (RULE-019).
- probability: unknown (no estimate yet)
- impact: high
- mitigation: Agree the first-version scope (Q-015), and give estimates as ranges with confidence and assumptions in the Commit phase.
- flags: C4-05, C4-08, C4-18
- history:
  - 2026-09-28 created from client answer to Q-014 (answers pasted by the BA)
  - 2026-09-28 why updated from client answers, round 2

### RISK-003 · The first-year direct-booking goal may not be measurable in the first version
- type: RISK
- label: ASSUMPTION
- status: AI-DRAFT
- parent: GOAL-004
- source: BA reasoning
- why: The client wants the goal counted by money (GOAL-004). Without a record of where each booking came from and how much it was worth, success cannot be checked. Direct means "not going through Booking.com or Agoda" (RULE-029). The client says reports can come later (REQ-007).
- probability: unknown (depends on Q-062)
- impact: medium
- mitigation: Decide in the Shape phase whether the booking source and the amount are recorded from the first booking.
- flags: C4-02, C4-18
- history:
  - 2026-09-28 created from client answer to Q-001 (answers pasted by the BA)
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section A, "Q-035"): title, why, probability and mitigation (30% goal replaced by GOAL-004)
  - 2026-09-28 parent GOAL-002 → GOAL-004 after client answers, round 3

### RISK-004 · The client expects the project team to take on tasks that may not be in scope or budget
- type: RISK
- label: ASSUMPTION
- status: AI-CHECKED
- parent: RULE-003
- source: BA reasoning
- why: In round 2 the client says: "you'll recommend one" (payment provider), "You write English.", "Can you register it and handle the DNS?", "You or your team enters it." (room data), "I trust you to handle that." (privacy text) and "maybe you have an on-call plan?". Whether these are in scope and priced is not decided. In round 3 he again expects the project team to write the privacy text: "That's something you need to put together with Ahmed, our accountant, or a lawyer." (Q-066).
- probability: high
- impact: medium
- mitigation: Decide with Yusuf which of these are in scope and priced (Q-060), and record the decision.
- flags: none
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section C, "New Q-9"): why

### RISK-005 · The 120,000 SAR budget also has to cover running costs, so less is left for building
- type: RISK
- label: ASSUMPTION
- status: AI-DRAFT
- parent: RULE-019
- source: BA reasoning
- why: The client says the budget includes hosting, payment gateway fees, translation, running the platform and first-year support (RULE-019). Payment fees depend on how many bookings are paid online. How much is left for building is not known (Q-048).
- probability: unknown (depends on Q-048)
- impact: high
- mitigation: Get the split (Q-048), and give estimates as ranges with confidence in the Commit phase.
- flags: C4-18
- history:
  - 2026-09-28 created from client answers, round 2

### RISK-006 · VAT, ZATCA registration and invoicing rules may add scope, time or cost that is not yet known
- type: RISK
- label: ASSUMPTION
- status: AI-DRAFT
- parent: REQ-038
- source: BA reasoning
- why: The client says the system must be registered with ZATCA and guests need invoices, but does not know the details (DEP-006). Nothing has been researched.
- probability: unknown (accountant not yet asked)
- impact: high
- mitigation: Get the accountant's answer (Q-049). Research only if the BA asks.
- flags: C4-01, C4-18
- history:
  - 2026-09-28 created from client answers, round 2

### RISK-007 · Automatic sync with Booking.com and Agoda may need extra time, cost or a third-party service
- type: RISK
- label: ASSUMPTION
- status: AI-DRAFT
- parent: REQ-029
- source: BA reasoning
- why: The client says automatic sync is ideal (REQ-029). How sync would work has not been researched, and it may depend on requirements set by the booking sites.
- probability: unknown (not researched)
- impact: high
- mitigation: Plan for manual entry in the first month (REQ-031). Research only if the BA asks.
- flags: C4-18
- history:
  - 2026-09-28 created from client answers, round 2

### RISK-008 · Card numbers are taken by phone and charged by hand, which may break card-payment security rules
- type: RISK
- label: ASSUMPTION
- status: AI-DRAFT
- parent: RULE-034
- source: BA reasoning
- why: The client says "I take their card number over the phone and charge the deposit". Card details handled this way may be covered by card-payment security rules and put guests' card details at risk. Nothing has been researched.
- probability: unknown (not researched)
- impact: high
- mitigation: Ask which payment service is used today (Q-068). Prefer payment links over card numbers by phone. Research only if the BA asks.
- flags: C4-01, C4-18
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md

## Dependencies (DEP)

### DEP-001 · A payment provider must be chosen; the client expects a recommendation
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: client answer 2026-09-28 (Q-005)
- quote: "We don't have a payment provider yet — you'll recommend one."
- why: A recommendation needs research, which starts only when the BA asks. The final decision is Yusuf's (RULE-002). Round 3: the client already charges cards by phone and sends payment links "via a payment service" (Q-068).
- owner: BA (recommendation); Yusuf (final decision)
- needed-by: UNKNOWN
- flags: C4-04, C4-10
- history:
  - 2026-09-28 created by /ba-extract from inputs/brief-2026-09-28.md
  - 2026-09-28 updated from client answer to Q-005: title, label ASSUMPTION → KNOWN, quote and owner changed
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Sections D and E): why

### DEP-002 · The Arabic text is written and approved by the client's head office team
- type: DEP
- label: KNOWN
- status: SUPERSEDED
- parent: REQ-008
- source: client answer 2026-09-28 (Q-011)
- quote: "My head office team writes and approves the Arabic"
- why: The team members and their availability are not named (Q-030).
- owner: Client's head office team
- needed-by: UNKNOWN
- blocked-by: Q-030
- superseded-by: DEP-009
- flags: C1-16
- history:
  - 2026-09-28 created from client answer to Q-011 (answers pasted by the BA)
  - 2026-09-28 superseded by DEP-009 after client answers, round 2

### DEP-003 · The client's team helps with content and testing
- type: DEP
- label: KNOWN
- status: SUPERSEDED
- parent: RULE-001
- source: client answer 2026-09-28 (Q-014)
- quote: "My team will help with content and testing."
- why: Who is in the team and how much time they have is not stated. With a hard deadline, late content or testing feedback would delay the launch.
- owner: Client's team
- needed-by: UNKNOWN
- superseded-by: DEP-010
- flags: C1-16
- history:
  - 2026-09-28 created from client answer to Q-014 (answers pasted by the BA)
  - 2026-09-28 superseded by DEP-010 after client answers, round 2

### DEP-004 · The client's IT person handles the domain name and hosting move
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-012
- source: client answer 2026-09-28 (Q-012)
- quote: "My IT person can handle that."
- why: The IT person is not named, and the current hosting company holds the site today.
- owner: Client's IT person (name UNKNOWN)
- needed-by: UNKNOWN
- blocked-by: Q-042
- flags: C4-10, C4-19
- history:
  - 2026-09-28 created from client answer to Q-012 (answers pasted by the BA)
  - 2026-09-28 blocked-by updated after client answers, round 2

### DEP-005 · Business documents and a Saudi business bank account are ready for an online payment account
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-003
- source: inputs/client-answers-round-2-2026-09-28.md (Section B, answer headed "Q-012 [NEW]")
- quote: "We have all business documents."
- why: The client adds: "We're set up with a Saudi business bank account." No payment provider has been contacted yet (DEP-001).
- owner: Yusuf
- needed-by: UNKNOWN
- flags: C4-10
- history:
  - 2026-09-28 created from client answers, round 2

### DEP-006 · The client's accountant confirms VAT, ZATCA and invoice rules
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-038
- source: inputs/client-answers-round-2-2026-09-28.md (Section C, answer headed "Q-014 [NEW]")
- quote: "We need to ask our accountant."
- why: The client does not know the details of Saudi rules on payments, data, invoices and tax. Round 3 names the accountant: "My accountant (let's call him Ahmed) handles that."
- owner: Ahmed (Yusuf's accountant)
- needed-by: UNKNOWN
- blocked-by: Q-049
- flags: C4-01, C4-10
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 updated by /ba-extract from client answers, round 3 (Section C, "Q-049"): owner and why

### DEP-007 · Yusuf sends the original photos and descriptions, and a spreadsheet of room types and base prices
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-058
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-025 [NEW]")
- quote: "I'll send you original photos and descriptions."
- why: The client also said "I'll give you a spreadsheet with all room types and base prices." (Section E, "Q-026 [NEW]").
- owner: Yusuf
- needed-by: UNKNOWN
- flags: C4-10
- history:
  - 2026-09-28 created from client answers, round 2

### DEP-008 · Yusuf reviews the English text
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-008
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-029")
- quote: "You write English. I'll review it."
- why: The project team writing the English text may not be in scope (RISK-004, Q-060).
- owner: Yusuf (review)
- needed-by: UNKNOWN
- flags: C4-10
- history:
  - 2026-09-28 created from client answers, round 2

### DEP-009 · Layla translates and checks the Arabic text, with a 3 to 5 day turnaround
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: REQ-008
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-029")
- quote: "For Arabic, I have a colleague Layla who speaks both — she'll translate and check."
- why: The client adds: "She can turn around translations in 3-5 days." Replaces DEP-002.
- owner: Layla (colleague of Yusuf)
- needed-by: UNKNOWN
- flags: C4-10
- history:
  - 2026-09-28 created from client answers, round 2. Replaces DEP-002

### DEP-010 · The client's team gives fixed weekly hours for content, translation and testing
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: RULE-010
- source: inputs/client-answers-round-2-2026-09-28.md (Section E, answer headed "Q-030 [NEW]")
- quote: "Layla: 5 hours a week for translation and content review."
- why: Also: "Fatima (my manager): 10 hours a week for testing and approval." and "Me: I'll be available for big decisions, maybe 5 hours a week." Replaces DEP-003.
- owner: Layla, Fatima and Yusuf
- needed-by: UNKNOWN
- flags: C4-10
- history:
  - 2026-09-28 created from client answers, round 2. Replaces DEP-003

### DEP-011 · Fatima handles day-to-day support after launch
- type: DEP
- label: KNOWN
- status: AI-CHECKED
- parent: REQ-057
- source: inputs/client-answers-round-2-2026-09-28.md (Section F, answer headed "Q-034 [NEW]")
- quote: "Fatima handles day-to-day support."
- why: For tech issues: "she calls me or our IT person." Out-of-hours cover is not decided (Q-059).
- owner: Fatima
- needed-by: After launch
- blocked-by: Q-059
- flags: C4-10
- history:
  - 2026-09-28 created from client answers, round 2
  - 2026-09-28 checked by /ba-check run 2

### DEP-012 · Yusuf sends the contact details of his accountant, Ahmed
- type: DEP
- label: KNOWN
- status: AI-DRAFT
- parent: DEP-006
- source: inputs/client-answers-round-3-2026-09-28.md (Section C, answer headed "Q-049")
- quote: "I'll send you his contact info."
- why: Ahmed handles ZATCA e-invoicing, VAT calculation and reporting, and invoices (DEP-006, Q-049).
- owner: Yusuf
- needed-by: UNKNOWN
- flags: C4-01, C4-10
- history:
  - 2026-09-28 created by /ba-extract from inputs/client-answers-round-3-2026-09-28.md
