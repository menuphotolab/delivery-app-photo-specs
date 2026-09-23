# Verification log

What was checked, when, where, and what came of it. A figure without a row here should not be
trusted.

**Next scheduled re-verification: 2026-12-22.** Most figures were re-confirmed against the live pages on 2026-09-22; see the rows for that date, including what was NOT re-checked.

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
| 2026-09-22 | Uber Eats | Cover image spec, spot-check | [Merchant submitted menu catalog photo guidelines](https://help.uber.com/en/merchants-and-restaurants/article/merchant-submitted-menu-catalog-photo-guidelines?nodeId=6985355b-0426-4523-94f2-89bb9b0566e9) | **Confirmed unchanged.** The page states "2880 pixel width and 2304 pixel height" and "a JPEG format with a 5:4 aspect ratio", matching the 2026-08-30 reading. The centered-framing rule is also still present |
| 2026-09-22 | All | Every source URL checked for reachability | The linked pages themselves | All resolve. **Two findings.** Uber's help URLs require their `nodeId` query parameter; the slug alone 404s. Uber also serves 404 to non-browser requests even for valid URLs, so an automated link checker reports false failures on that domain and the links had to be confirmed in a real browser |
| 2026-09-22 | - | Repository published | - | First public release |
| 2026-09-22 | DoorDash | Full item, logo and header spec set re-read | [Common photo issues explained](https://help.doordash.com/en-us/merchants/article/common-photo-issues-explained) | **All figures confirmed unchanged.** Item 1400 x 800 landscape 16:9, logo 230 x 230 1:1 under 2 MB, header 1400 x 800 at 4:1 web and 16:9 app under 2 MB. Hands wording verbatim. Instagram and Yelp sourcing still described. **The 2 MB vs 16 MB contradiction is real and still live**: the page states "Maximum file size: 2 MB" for item photos in one section and "Under 16 MB" for item photos in another. Checked twice because a first, looser read suggested the 2 MB applied only to logos and headers |
| 2026-09-22 | Toast | Both item-photo pages re-read | [Menu Manager](https://support.toasttab.com/en/article/Adding-Images-to-Menu-Items-in-the-Menu) and [Online Ordering Pro](https://support.toasttab.com/en/article/Online-Ordering-Pro-Menu-Image-Requirements) | **Contradiction confirmed unchanged.** Menu Manager still recommends 750 x 450, jpg or png, no larger than 5 MB. Online Ordering Pro still requires 1:1, 4:3 or 16:9 and "a minimum height or width of 1000 pixels", and still states neither file type nor size cap |
| 2026-09-22 | Grubhub | Both specs re-read, developer portal rendered in a browser | [Help centre](https://get.grubhub.com/help-center/grubhub-menu-overview/) and [developer portal](https://developer.grubhub.com/docs/3zSHFME4nnntcOeqwbOTYl/menu-imagery-specifications) | **Contradiction confirmed unchanged.** Help centre: at least 200 x 200, 1:1, "Must be saved as a .png file". Developer portal: at least 1600 x 1200, 4:3, png/jpeg/jpg. **New detail added**: the developer portal states mobile web menus use roughly 4:3 while desktop web uses 4:1. The JS-app warning in this file was also re-validated, a plain fetch again returned only "Grubhub is loading..." |
| 2026-09-22 | Square | Item image page re-read | [Product images on Square Online](https://squareup.com/help/us/en/article/6894-product-images-on-square-online-store) | **Confirmed unchanged.** "at least 2000 x 2000 pixels with a 1:1 aspect ratio", "Images can be up to 15MB", JPG/JPEG/PNG/GIF, and both sync sentences verbatim |
| 2026-09-22 | Uber Eats | **Full re-check completed**, both spec pages rendered in a browser | [Photo guidelines](https://help.uber.com/en/merchants-and-restaurants/article/merchant-submitted-menu-catalog-photo-guidelines?nodeId=6985355b-0426-4523-94f2-89bb9b0566e9) and [Adding cover images and menu catalog photos](https://help.uber.com/en/merchants-and-restaurants/article/adding-cover-images-and-menu-catalog-photos?nodeId=b2dfa2b7-20f2-4f5f-81a3-32fa4c2aea89) | **Every figure confirmed**: width 550-10,000, height 440-10,000, the "(recommended)" qualifier on the 5:4 to 6:4 band, jpg/png/gif, 10 MB (5 MB for Creative Hub), cover 2880 x 2304 at 5:4 JPEG, hands permitted, one-item rule, centered framing. **One correction made**: the "up to 3 business days" SLA is stated for COVER IMAGES, not item photos, and had been published here as a general figure. **Four new findings**: Uber may edit size, orientation, lighting and colour after approving a photo; the upload terms sub-license photos to Uber "including the right to modify photos without permission"; a pending photo can be withdrawn via Cancel photo update; and the `adding-menu-photos---faq` slug now redirects to `adding-cover-images-and-menu-catalog-photos` |

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
