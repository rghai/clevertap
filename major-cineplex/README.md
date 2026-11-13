# Major Cineplex × CleverTap × Reshape | Interactive Journey Lab

**Client concept demo**, not a production Major Cineplex app or a CleverTap campaign deployment.

Open major-cineplex/index.html from a static server. Use the EN / ไทย toggle. The interactive gallery preserves the original five concept templates and adds **six app-engagement gamification journeys**.

## Branding

- **Major Cineplex** official logo via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Major_Cineplex_Logo.svg), attributed to Major Cineplex Group (trademark still applies).
- **CleverTap** authentic company logo via [official CleverTap SDK repository](https://github.com/CleverTap/clevertap-ios-sdk/blob/master/docs/images/clevertap-logo.png). Demo hotlinks official SDK image; confirm up-to-date customer-facing brand approval.
- **Reshape Consulting** first-party original logo from designated Google Drive Reshape brand folder, committed to assets/reshape-logo.svg; viewBox cropped to display authentic mark cleanly.

## Journeys

| # | Journey | Primary driver | Example event |
|---|---|---|---|
| 1 | Daily check-in and 7-day streak | Repeated app opens | Major_Daily_Checkin |
| 2 | Daily movie missions | Habit / feature discovery | Major_Daily_Quest_Completed |
| 3 | Daily cinema trivia | Return visits / interaction | Major_Daily_Trivia_Answered |
| 4 | Scratch-and-reveal | Daily habit loop | Major_Scratch_Revealed |
| 5 | Daily spin wheel | Return visits | Major_Daily_Wheel_Spun |
| 6 | Film carousel | Discovery | Existing carousel tracking scaffold |
| 7 | Genre poll | Preference enrichment | Existing poll tracking scaffold |
| 8 | Checkout recovery | Booking conversion | Existing recovery tracking scaffold |
| 9 | Cinema passport (6 verified visits) | Repeat cinema attendance | Major_Passport_Visit_Simulated |
| 10 | Badge wall | Loyal member recognition | Existing badge scaffold |
| 11 | Cinema year recap | Retention / sharing | Existing recap scaffold |

The six new games live in standalone engagement.html with query parameters: mode=checkin, quests, quiz, scratch, wheel, passport; lang=th or en.

## Bilingual scope

The showcase shell and all six new gamification demos have full English and Thai copy. The five retained upstream-derived HTML experiences preserve their own rendering and events; assets/legacy-th.js provides Thai translation for key displayed copy. **Full production editorial localisation of all upstream experiences remains required.**

## Demonstrating repeat usage

1. Choose Daily Check-in, then claim today's +10 demo stars.
2. Reload or revisit; duplicate same-day claims are blocked.
3. Choose Simulate next day +1 and check in again. Streak increments for consecutive simulated Bangkok-local dates.
4. Repeat to day seven for a bonus +30. Skipping a day resets streak on the next check-in.
5. Daily App Missions grants a bonus once upon finishing three synthetic events.
6. Trivia, Scratch and Spin are each limited to one claim per simulated date.
7. Cinema Passport begins at a fictional 3/6 stamps and demonstrates a six-visit milestone.
8. Reset clears demo state. Everything is stored locally in browser localStorage, not in CleverTap or a backend.

## Event and production contract

For the six games, track(name, properties) dispatches CustomEvent("major:demo-event") and sends a same-origin message to the parent gallery. It is **event preview only**, not actual CleverTap telemetry. The original five templates retain their existing scaffold.

Production work requires:
- Real CleverTap SDK bridge, event data design, user identity/consent and profile integration.
- Backend-authoritative once-per-day entitlement, streak histories, idempotency and anti-fraud. Browser localStorage is not an entitlement store.
- Approved reward catalog, points and expiry rules, terms, eligibility, and legal review of chance-based promotions. Outcomes and fulfilment must be server-side; the demo's stars are not tickets, coupons, money or real loyalty points.
- Ticket/POS verification for cinema passport stamps. Do not award based only on frontend clicks.
- Approved production deep links and actual seat-hold rules for booking rescue.
- Frequency limits, accessibility, PDPA assessment, Thai/English legal copy, native Android/iOS webview QA.

## Attribution

Original five templates are adapted from [SJ Neo's CleverTap Custom HTML Template Gallery](https://github.com/shijunneo-bot/ct-template-gallery): carousel, genre poll, payment recovery, badges, year recap. The six new game designs reuse generic gamification ideas, with independent demo logic.

## Verification

- [x] Brand logo sourced from original Reshape asset, grounded public Major and CleverTap logo URLs.
- [x] Isolated branch; no DHL files or repository-root changes.
- [x] Bilingual shell and six newly built games.
- [x] Repeat-day and daily-limit logic implemented for synthetic local data.
- [ ] Live GitHub Pages verification and browser/mobile screenshot QA.
- [ ] Actual CleverTap SDK and backend QA.
- [ ] Major / CleverTap logo and campaign approval.

Expected path when hosted with GitHub Pages main/root: /clevertap/major-cineplex/. Do not claim publicly live until verified.
