# Major Cineplex | CleverTap interactive concepts

Five executable HTML examples adapted from the [SJ Neo CleverTap Custom HTML In-App Gallery](https://github.com/shijunneo-bot/ct-template-gallery) for a **synthetic, non-production** client workshop.

Open `index.html` using a static server to navigate the phone mockups. Each self-contained file in `templates/` can also be opened independently.

| Journey moment | Source template | Demo |
| --- | --- | --- |
| Discovery | `a14-horizontal-snap-carousel.html` | `01-now-showing-carousel.html` |
| Preference capture | `catchplay-poll.html` | `02-genre-poll.html` |
| Checkout rescue | `catchplay-payment-recovery.html` | `03-checkout-recovery.html` |
| Loyalty | `catchplay-badges.html` | `04-major-rewards-badges.html` |
| Retention | `catchplay-wrapped.html` | `05-cinema-year-recap.html` |

## Intent and limitations

- Five interactive custom HTML prototypes, **not** live CleverTap campaigns or a live Major app.
- Movie names, preferences, points, purchase events and metrics are fictitious. No real film posters or licensed assets are embedded.
- Templates retain their original interaction and analytics scaffolding, with brand names and sample content adapted.
- **Integration work remains**: review each template's JS bridge calls and event names, define Major event/property mapping, replace placeholder app URL schemes with the approved production deep links, localise and test Thai/English, and validate app webview compatibility.
- The payment recovery base template originally targets streaming subscriptions, so confirm every remaining display string and countdown assumption against actual cinema booking holds before production use.
- Do not use this showcase for a real booking or payment. No production customer data should be injected.
- To serve as a GitHub Pages project site without disturbing the repository's existing DHL example, configure Pages source for this branch and path, or publish the `major-cineplex/` directory via a dedicated hosting workflow. No Pages setting has been modified.

## Suggested CleverTap journey

1. Movie Discovery: show personalised film card selection based on previous genre and visit signals.
2. Preference Collection: poll captures explicit first-party genre preference.
3. Conversion Recovery: on an abandoned booking, target a short-lived recovery campaign subject to real seat-hold rules.
4. Loyalty: recognise cinema milestones, contingent on backend-verified booking events.
5. Recap: present a playful annual retention moment with customer-approved profile/event data.

## Attribution

Derived from files in [shijunneo-bot/ct-template-gallery](https://github.com/shijunneo-bot/ct-template-gallery). Original gallery curated by SJ Neo. Check upstream licence and permissions before commercial distribution.

## QA checklist

- [x] Source templates identified and adapted as standalone HTML.
- [x] Entry-point showcase with five selectable iframe previews.
- [ ] Browser visual / mobile interaction QA on actual hosted page.
- [ ] Verified functional CleverTap SDK tracking on device.
- [ ] Verified Major marketing approval and production URLs.
- [ ] Thai/English editorial and legal review.
