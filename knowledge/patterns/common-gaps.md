# Common Gaps Checklist

Questions that are missed on most digital projects. `/ba-check` asks each one that applies and raises a `Q` item when the answer is not in the project yet.

## Users and roles
- Are "users", "staff" or "admin" split into real roles with different permissions?
- Who creates, edits, approves and deletes each kind of record?
- What happens when someone leaves or changes role?

## Accounts and access
- How do people sign up, sign in, reset a password and close an account?
- Is there single sign-on, social login or two-factor authentication?

## Content and data
- Who enters the initial data, and is there data to migrate from an old system?
- What must be kept for audit, and for how long?
- What personal data is collected, and what consent is needed?
- Does everyone define the key numbers the same way (formula, unit, counted by number or by money)? Who owns each definition? (L-001)

## Regulation and reporting
- Which tax, e-invoicing or data-protection rules apply, and who on the client side can confirm them?
- Must anything be reported to a government or industry authority, how often, and in what format?

## Money
- Which payment methods, currencies and taxes apply?
- What are the refund, cancellation and partial-payment rules?
- Who reconciles payments, and with which accounting tool?

## Notifications
- Which events send an email, SMS, WhatsApp or in-app message, and to whom?
- Who writes and approves the message text, and in which languages?

## Operations
- Who runs the system day to day, and what reports do they need?
- What happens outside business hours?
- What does support look like after launch?

## Launch and cut-over
- Does the new system replace something (a website, a spreadsheet, a manual process)? (L-002)
- Will old and new run side by side, and for how long?
- Is there a pilot (one location, one team, one month) before full rollout?
- What is the fallback if launch fails, and who decides to use it?

## Multiple locations
- Which differences between locations, branches or teams are legitimate and must be kept, and which should be standardised? Who decides?
- What does head office see compared with each location?

## Edge cases
- Empty states: what does a new user or an empty list look like?
- Failures: what happens when a payment, an integration or an upload fails?
- Duplicates, cancellations halfway through, and two people editing the same thing.

## Non-functional
- Expected number of users, records and peak times.
- Devices and browsers; mobile vs desktop share.
- Accessibility level required.
- Languages, date and number formats, right-to-left text.
- Hosting, backups and who owns the domain and accounts.

## Commercial and delivery
- Who signs off each phase, and how fast can they respond?
- What content, logins or third-party accounts must the client provide, and by when?
- What is explicitly out of scope?
- Are we writing an RFP for the client, or responding to one? If responding: what sections, format and deadline does it require, and how will it be evaluated? (L-003)
- Build, buy or configure: who decides, and by when? (L-004)
- Is any answer or contact still missing after it was promised twice? Treat it as a risk, not a question. (L-005)
