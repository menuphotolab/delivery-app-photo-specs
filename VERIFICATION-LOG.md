# Verification log

What was checked, when, where, and what came of it. A figure without a row here should not be
trusted.

**Next scheduled re-verification: 2026-11-24.**

| Date | Platform | What was checked | Source | Result |
|---|---|---|---|---|
| 2026-08-27 | Grubhub | Both item-photo specifications, read in full | Developer portal (rendered in headless Chromium) and the help centre | **They contradict each other on minimum size, aspect ratio and file format.** Developer portal: 1600 x 1200 at 4:3, png/jpeg/jpg. Help centre: 200 x 200 at 1:1, png only. Also captured: header 2400 x 1800 (4:3), profile 2400 x 1200 (2:1), logo 200 x 200 |
| 2026-08-27 | DoorDash | Full spec set, rejection flow, platform-added photos | DoorDash merchant learning centre and help centre | Four photo types with four different specs, not one. The 2 MB vs 16 MB contradiction confirmed on a single page. **Hands are allowed with conditions.** DoorDash may add photos from a connected Instagram account or Yelp, with an opt-out |
| 2026-08-30 | DoorDash | Rejection UI and appeal path | Merchant Portal, Menu Manager (in-product) | **A Request review control exists on the rejection notice and appears in no DoorDash documentation.** Also captured: a rejected item stays in stock and keeps selling with a broken image, and the rejection reason is shown in the item drawer rather than only emailed |
| 2026-08-30 | Uber Eats | Full spec set, rejection rules, review flow, customer photos, photoshoot terms | Uber help centre (four articles) and the Uber Eats merchant site | Every figure confirmed. The aspect-ratio line is **the only requirement on the page marked "(recommended)"**. Uber runs a customer-photo programme with no published merchant opt-out. Uber's photoshoot page permits use "in your own marketing" and states no marketplace restriction |
| 2026-08-30 | Cross-platform | Aspect ranges compared as decimals | Arithmetic on the verified figures | Uber Eats accepts 1.25 to 1.5. DoorDash's 16:9 is 1.778 and falls outside. Grubhub's developer 4:3 is 1.333 and falls **inside**; its help-centre 1:1 is 1.0 and falls below. **Grubhub's two specs land on opposite sides of Uber's band** |
| 2026-09-14 | DoorDash | Photoshoot usage terms, both sources | Merchant blog and help centre | Both still live, quoted verbatim. **The two pages disagree**: the blog states a prohibition on other delivery platforms, the help centre states it as a request |
| 2026-09-21 | Toast | Item photo specs, brand image specs, review process | Three Toast support articles | **Toast's recommended 750 x 450 fails Toast's own Online Ordering Pro requirement** on both size and shape. Banner file size cap stated as 5 MB on one page and 9 MB on two others, updated one day apart |
| 2026-09-21 | Square | Item image and site image specs, sync behaviour | Two Square support articles | 2000 x 2000 recommended for items, 15 MB cap. Site non-background images capped at 1000 px on the longest side. **Recorded as an open question, not a contradiction**, because it is unclear the site ceiling governs catalog item photos |
| 2026-09-21 | DoorDash | Source URL check | Merchant learning centre | The learning-centre photo-rejection URL now **301s** to the help-centre article. Links updated to the destination |
| 2026-09-22 | - | Repository published | - | First public release. All figures above carried over with their original verification dates, unchanged |

## Known gaps

These are recorded so nobody mistakes silence for coverage.

| Gap | Status |
|---|---|
| Google Business Profile | Figures held but never verified against the platform. **Not published.** |
| Instagram | Same. **Not published.** |
| ChowNow, Slice, Caviar | Not researched. |
| Square: does the 1000 px site ceiling govern catalog item photos? | Open. See [CONTRADICTIONS.md](./CONTRADICTIONS.md) section 5 |
| Square for Restaurants / Franchises menu images | Not checked |
| Whether Square runs any photo review | Not checked |
| Toast: does the product enforce a review step the docs omit? | Not checked. The absence claim is scoped to the documentation on purpose |

## How to re-verify

Two things make this pass cheap or expensive:

1. **Grubhub's developer portal is a JavaScript single-page app.** It returns
   `Grubhub is loading...` to curl and to simple fetchers, so a naive fetch looks successful
   and tells you nothing. Render it in a headless browser and read the DOM. Skipping this is
   how the Grubhub contradiction went unnoticed for a day.
2. **DoorDash moves its URLs.** The learning-centre path already 301'd once. Follow redirects
   and record the destination, not the link you started from.
