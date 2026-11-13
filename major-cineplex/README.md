# Major Cineplex × CleverTap × Reshape | Interactive Journey Lab

**Client concept demo**, not a production Major Cineplex app or a CleverTap campaign deployment.

Open major-cineplex/index.html from a static server. Use the EN / ไทย toggle. The interactive gallery preserves four of the original five CleverTap gallery adaptations, replaces the streaming-derived checkout recovery with a cinema-specific flow, and adds **six app-engagement gamification journeys**, four **M PASS / M GEN membership demos**, three **Priority 3.1 concession cross-selling** concepts, and one **Priority 3.2 at-home popcorn delivery** vision demo.

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
| 8 | Checkout recovery | Booking conversion | Rebuilt `Major_Booking_Recovery_Clicked` |
| 9 | Cinema passport (6 verified visits) | Repeat cinema attendance | Major_Passport_Visit_Simulated |
| 10 | Badge wall | Loyal member recognition | Existing badge scaffold |
| 11 | Cinema year recap | Retention / sharing | Existing recap scaffold |

The six new games live in standalone engagement.html with query parameters: mode=checkin, quests, quiz, scratch, wheel, passport; lang=th or en.

## Bilingual scope

The showcase shell and all six new gamification demos have full English and Thai copy. Four retained upstream-derived HTML experiences preserve their original rendering and event scaffolds; assets/legacy-th.js supplies key Thai translations for those four. The checkout recovery was rewritten with native Thai and English content. **Full production editorial localisation of all upstream experiences remains required.**

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

For the six games, track(name, properties) dispatches CustomEvent("major:demo-event") and sends a same-origin message to the parent gallery. It is **event preview only**, not actual CleverTap telemetry. Four upstream adaptations retain their event scaffolds. The checkout recovery has new synthetic booking and concession cross-sell events.

Production work requires:
- Real CleverTap SDK bridge, event data design, user identity/consent and profile integration.
- Backend-authoritative once-per-day entitlement, streak histories, idempotency and anti-fraud. Browser localStorage is not an entitlement store.
- Approved reward catalog, points and expiry rules, terms, eligibility, and legal review of chance-based promotions. Outcomes and fulfilment must be server-side; the demo's stars are not tickets, coupons, money or real loyalty points.
- Ticket/POS verification for cinema passport stamps. Do not award based only on frontend clicks.
- Approved production deep links and actual seat-hold rules for booking rescue.
- Frequency limits, accessibility, PDPA assessment, Thai/English legal copy, native Android/iOS webview QA.

## Attribution

The initial five templates were adapted from [SJ Neo's CleverTap Custom HTML Template Gallery](https://github.com/shijunneo-bot/ct-template-gallery): carousel, genre poll, payment recovery, badges, year recap. The checkout screen is now a new cinema-native rebuild. The six game designs reuse generic gamification ideas, with independent demo logic.

## New: Membership, concession commerce and delivery (13 November 2026)

### M PASS / M GEN (4 bilingual concepts)

- **M PASS: value reminder**. Sample Standard package, upcoming movies, and official member concession positioning. Never implies an unlimited number of redemptions for one film. Source: user-provided current-app M PASS screens and [Major M PASS terms](https://www.majorcineplex.com/mpass/usempass.php?lang=en).
- **M PASS: cinema upgrade**. Explore standard, IMAX or premium-seat options with explicit caveats on possible upgrade fees, package limits and participating branches. Source: supplied app screen and [Major M PASS package branches](https://www.majorcineplex.com/mpass/application.php).
- **M GEN: membership benefit overview**. Illustrative 6/20 member-priced seats used, 14 remaining. M GEN is **not classified as a student-only programme**. Source: user-provided M GENERATION NEXT screen and [Major M GEN overview](https://web.majorcineplex.com/m-pass-m-gen).
- **M GEN: birthday-week entitlement preview**. Simulate eligibility for a complimentary movie ticket during birthday week. This is not a real ticket and the official terms apply. Source: current-app screen and [Major member information](https://www.majorcineplex.com/member/login/home/).

### Priority 3.1: Concession cross-sell (3 bilingual concepts)

- **During ticket checkout**: optional popcorn, drinks and nachos with illustrative basket math; consistent with cinema ticket conversion.
- **Post-booking, pre-show pickup**: invite ticket holders to add snacks and choose a pickup window. No real collection reference is generated.
- **Personalised concession prompt**: the member's fictional usual order triggers a relevant add-on suggestion.
- **Checkout recovery fixed**: original CATCHPLAY subscription copy replaced entirely. Movie, branch, showtime, seats and member context only. Removes downloads, simultaneous screens and any streaming benefits. Illustrative eight-minute timer and optional snacks; actual seat-hold window must come from ticketing.

### Priority 3.2: At-home popcorn commerce (1 bilingual future-state vision)

- Major app offers standalone snacks without a cinema ticket; user selects products and conceptual delivery / collection.
- The in-app direct-order model is proposed, **not asserted as an existing Major app feature**.
- Delivery partners such as Grab or LINE MAN are illustrative fulfilment options. This deliberately avoids API, integration, contractual and inventory implementation claims.
- Official Major information confirms existing third-party popcorn delivery distribution; see [Major delivery announcement](https://www.majorcineplex.com/news/major-popcorn-delivery/) and [2026 promotions](https://majorcineplex.com/promotion/nano-gauntlet-popcorn-bucket-set/). No promise of active partner coverage in the proposed in-app experience.

### Demo routes

- membership.html?mode=mpass-value, mpass-upgrade, mgen-benefits, mgen-birthday
- concessions.html?mode=booking, pickup, recommend, delivery
- templates/03-checkout-recovery.html (cinema-specific rebuild)
- Every new route accepts lang=th or lang=en. A showcase category selector separates Membership, 3.1 Concessions and 3.2 Delivery Vision, increasing the gallery to 19 interactive examples.

### Commercial and product safeguards

- Prices, M PASS package and M GEN seat balances are sample data. No real entitlement data is queried or updated.
- No tickets, gift privileges, snack orders, delivery dispatches, payments, notifications or real loyalty rewards occur.
- Buttons preview user journeys and emit only synthetic local events; real CleverTap app SDK and Major server integrations require a separate project.
- Before sales use, verify branding approval, current membership programme validity, concession catalogue, promotion terms, eligibility, expected partner availability, booking time holds and Thai legal copy.

## Verification

- [x] Brand logo sourced from original Reshape asset, grounded public Major and CleverTap logo URLs.
- [x] Isolated branch; no DHL files or repository-root changes.
- [x] Bilingual shell and six newly built games.
- [x] Repeat-day and daily-limit logic implemented for synthetic local data.
- [x] Syntax checks passed for the new membership, concessions, checkout and gallery scripts.
- [x] Mock interactions in Thai and English covered M PASS discovery/upgrade, M GEN member-price/birthday, and cinema checkout plus optional concession toggle.
- [ ] Full real-browser screenshot QA and verified hosted GitHub Pages serving.
- [ ] Live CleverTap SDK, ticketing, POS and fulfilment backend QA.
- [ ] Major / CleverTap logo and campaign approval.

Expected path when hosted with GitHub Pages main/root: /clevertap/major-cineplex/. Do not claim publicly live until verified.
