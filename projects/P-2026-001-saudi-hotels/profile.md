# Project Profile — P-2026-001-saudi-hotels

status: APPROVED

This file tells every `/ba-` command how to treat this project. `/ba-start` drafts it; you review it and record your approval with `/ba-approve profile`.

Updated 2026-09-28 with the client's answers from rounds 1 and 2 (check 2, finding C2-11). Item IDs show where each fact comes from. It stays `AI-DRAFT` until you have read it and run `/ba-approve profile`.

## Basics

| Field | Value |
| --- | --- |
| Project ID | P-2026-001-saudi-hotels |
| Project name | saudi hotels |
| Client | Yusuf (name given by the BA on 2026-09-28; company name UNKNOWN). He makes the final decisions: "I make the final decisions." (RULE-002) |
| Industry | Hospitality: hotels. Source: brief, "We operate 6 hotels in Saudi Arabia." |
| Project type | Booking website with online payment, customer accounts and admin dashboard (replaces an existing website). Source: `inputs/brief-2026-09-28.md` |
| Project owner (BA) | |
| Started | 2026-09-28 |
| Deadline (if given) | "End of December is our hard deadline." The platform goes live then (RULE-010, about 13 weeks from 2026-09-28, calculated). Round 1 also said "The deadline is hard: 4 months maximum." (RULE-001, about late January). The two are not yet reconciled (check 2, C2-08). Features can follow in January |
| Budget signal (if given) | About 120,000 Saudi Riyals, "flexible if it's worth it" (RULE-003). It includes hosting, payment gateway fees, translation, running the platform and first-year support (RULE-019). How it splits between building and running is UNKNOWN (Q-048) |
| Language of outputs | English |
| privacy | internal |

`privacy` is one of: `public`, `internal`, `confidential`. Confidential projects live in `projects/_confidential/`.

Privacy note: the BA asked for everything to be backed up, so this is not `confidential`. The BA did not say `public` or `internal`, so `internal` (the template default) is used until told otherwise.

## Size

size: complex (suggested, not decided)

Signals that drive this size (see `method/depth-by-size.md`). They come from the brief and the client's answers.

- **Payments**: online payment with a deposit (RULE-012), cards, SADAD and Apple Pay (REQ-013, REQ-036), refunds (RULE-016), VAT and ZATCA registration (REQ-037, REQ-038). Complex row for security / regulation.
- **Locations**: 6 hotels in 6 cities, 380 rooms in total (calculated from REQ-058), one platform with head-office control (REQ-010).
- **Modules**: the brief lists 7 wants (website, room booking, payment, customer accounts, admin dashboard, booking management, reports). For December the client names a smaller list: guests book online, staff see bookings in a simple list, and payment confirmation (Q-015, Q-034 still open).
- **Languages**: Arabic first, English second, one of them right-to-left (REQ-053). This is not a row in the sizing table, but it adds design and testing work.
- **Integrations**: automatic sync with Booking.com and Agoda is wanted "ideally", with manual entry as a fallback for the first month (REQ-029, REQ-031, RISK-007). The payment provider is not chosen (DEP-001).
- **Decision makers**: one, Yusuf (RULE-002).

Signals still `UNKNOWN`:

- User roles: two lists that differ (REQ-060 to REQ-062, Q-037 to Q-039).
- Business rules: many are now recorded (RULE-010 to RULE-028), but VAT, ZATCA, invoicing and privacy rules are not known (Q-049).
- Technical unknowns: hosting, domain and backups (Q-042), how booking-site sync would work (RISK-007).

If the December scope turns out small, size may drop to `moderate`. Record any change in `decisions.md`.

## Depth per phase

Suggested depth for `complex` in `method/depth-by-size.md`.

| Phase | Depth |
| --- | --- |
| 1. Intake | standard |
| 2. Discover | standard |
| 3. Define | standard |
| 4. Shape | deep |
| 5. Commit | standard |
| 6. Deliver and learn | standard |

## Domain notes

Checklists to use from `knowledge/patterns/` and anything specific to this domain that every command should keep in mind.

- Checklists: `knowledge/patterns/common-gaps.md`
- There is no hotel-specific checklist in `knowledge/patterns/` yet, and `knowledge/lessons.md` has no lessons yet, so none are listed.
- The brief says both "A modern website" and "the new platform". Do not assume they mean the same scope; ask. The client now separates a December release from later features (RULE-010, REQ-005, REQ-032 to REQ-035).
- Use "guest" for the client's users of the booking site; the brief says "customer" (check 2, C2-20).

## Extra checks for this project

Areas that need extra attention (for example payments, multi-language, multi-location, personal data, offline use).

- **Payments**: one central head-office account (RULE-011), deposit 25% or 50% (RULE-012), refunds within 48 hours to the same payment method (RULE-016). Open: which currencies (REQ-059), how SADAD and bank transfers fit the 2-hour room hold (RULE-017, Q-046), who processes refunds and which accounting tool splits the money (Q-045), how the rest of the payment is paid (Q-043, Q-044). The payment provider is not chosen (DEP-001).
- **Personal data**: guest accounts hold personal data. The client wants data kept 3 years for accounting (RULE-020) and also deleted when an account is closed (RULE-028, in conflict, Q-041). Privacy and consent text: "I trust you to handle that." (RISK-004).
- **Multi-location**: 6 hotels. Whether hotel managers see one hotel or all six is in conflict (REQ-061, Q-038). Prices depend on room type and date, high season is 2x (RULE-021). Makkah Comfort sells only during Hajj season (RULE-022).
- **Two languages, right-to-left**: Layla translates and checks the Arabic, 3 to 5 days per batch (DEP-009). Yusuf reviews the English (DEP-008). Who writes the English is not decided (RISK-004, Q-060).
- **Existing website**: it is replaced completely on launch day, with no running both (REQ-054). Photos, location, contact and refreshed descriptions move over (REQ-052). The domain is in conflict (REQ-063, Q-042). No booking data moves (RULE-009).
- **Regulation**: the client says the system must be registered with ZATCA, VAT applies and guests need invoices, but he does not know the details. "I think it's 15%." He will ask his accountant (REQ-037 to REQ-039, DEP-006, Q-049). Research only when the BA asks.
- **Reports**: monthly reports are wanted (REQ-007) but the client says they can come after the first version.
- **Timeline**: hard end-of-December go-live (RULE-010), in a period the client names as busy ("holidays (Dec-Jan, June-July)"). Client team hours: Layla 5, Fatima 10, Yusuf about 5 a week (DEP-010). No fallback for launch day is planned (check 2, C2-09).

## Stakeholders to confirm with

| Name or role | What they decide |
| --- | --- |
| Yusuf (client contact) | Makes the final decisions (RULE-002). Reviews the English text (DEP-008), approves changes to hotel information (RULE-024) and the room and price data before launch (RULE-025). His job title is UNKNOWN |
| Fatima (Yusuf's manager) | Tests and approves, about 10 hours a week (DEP-010). Handles day-to-day support after launch (DEP-011). What she decides beyond that is UNKNOWN |
| Layla (Yusuf's colleague) | Translates and checks the Arabic, about 5 hours a week, 3 to 5 days per batch (DEP-009) |
| The client's IT person (name UNKNOWN) | The domain and hosting (DEP-004). Round 2 asks the project team to do this instead (REQ-063, Q-042) |
| The client's accountant (name UNKNOWN) | VAT, ZATCA and invoice rules (DEP-006, Q-049) |
| UNKNOWN | Who owns the current website, its domain and its hosting account (Q-042). The client said only "hosted with a small Saudi hosting company" |
| UNKNOWN | Who sets payment, refund and pricing rules day to day (Yusuf decides finally, RULE-002) |
