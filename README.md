# Delivery app photo specs

Photo requirements for restaurant menu items, read off each platform's own documentation,
with the date each figure was verified and the URL it came from.

Covers the three delivery marketplaces (**DoorDash, Uber Eats, Grubhub**) and the two
restaurant POS platforms that run their own online ordering (**Toast, Square**). The POS
platforms are included because the same photo usually has to work on both.

Machine-readable version: [`specs.json`](./specs.json)

## The short answer

No single image file satisfies every platform.

| Platform | Item photo aspect | As a decimal | Binding? |
|---|---|---|---|
| DoorDash | 16:9 landscape | 1.778 | Landscape only |
| Uber Eats | 5:4 to 6:4 | 1.25 to 1.5 | Marked "(recommended)" |
| Grubhub (help centre) | 1:1 | 1.0 | Conflicts with the line below |
| Grubhub (developer portal) | 4:3 | 1.333 | Conflicts with the line above |
| Toast (Online Ordering Pro) | 1:1, 4:3 or 16:9 | 1.0 / 1.333 / 1.778 | Three accepted |
| Square | 1:1 | 1.0 | Recommended |

DoorDash's 16:9 falls outside Uber Eats' accepted band. Grubhub's two contradicting
specifications land on **opposite sides** of that band: 4:3 sits inside it, 1:1 sits below it.

### The harder version of the same problem

The conflict is not only *between* platforms. It exists *inside* one.

DoorDash renders menu **thumbnails at 1:1** and **detail headers at 16:9**, from the same
uploaded file. Grubhub's ordering app displays **square cards**. Uber Eats runs **landscape**.

So one framing has to survive a square crop and a landscape crop at the same time. That is a
decision made when the photo is taken, not an export setting applied afterwards.

## Item photo requirements

| Platform | Minimum / recommended | Aspect | Formats | Max size | Verified |
|---|---|---|---|---|---|
| DoorDash | 1400 x 800 px | 16:9, landscape only | | 16 MB (see note) | 2026-09-22 |
| Uber Eats | 550 to 10,000 px wide, 440 to 10,000 px high | 5:4 to 6:4 (recommended) | jpg, png, gif | 10 MB | 2026-09-22 |
| Grubhub (help centre) | 200 x 200 px | 1:1 | png only | not stated | 2026-09-22 |
| Grubhub (developer portal) | 1600 x 1200 px | 4:3 | png, jpeg, jpg | not stated | 2026-09-22 |
| Toast (Menu Manager) | 750 x 450 px | 5:3 | jpg, png | 5 MB | 2026-09-22 |
| Toast (Online Ordering Pro) | 1000 px on the longest side | 1:1, 4:3 or 16:9 | not stated | not stated | 2026-09-22 |
| Square | 2000 x 2000 px | 1:1 | jpg, jpeg, png, gif | 15 MB | 2026-09-22 |

Uber Eats is the only platform here that publishes a **maximum** resolution.

If you want to test a file against the table above rather than read it off by hand,
there is a free browser-based checker at
[menuphotolab.com/tools/rejection-checker](https://menuphotolab.com/tools/rejection-checker).
No signup, and the file is never uploaded: it is measured in the page. It checks size,
shape, format and file size only, not the content rules further down this page.

## Where platforms contradict themselves

These are the parts no one else writes down, so they get their own section:
[`CONTRADICTIONS.md`](./CONTRADICTIONS.md).

1. **DoorDash states two file size caps on the same page**, 2 MB and 16 MB.
2. **Grubhub publishes two complete item specs that disagree on every field**, and neither
   page acknowledges the other.
3. **Toast's recommended 750 x 450 collides with Toast's own Online Ordering Pro guidance.**
   It is 250 px short of the 1000 px Toast recommends elsewhere, and its 5:3 shape is none of
   the three ratios Online Ordering Pro says its templates support.
4. **Toast states two different banner file size caps** on pages updated one day apart.
5. **Square** publishes a 2000 px floor for item images and a 1000 px ceiling for site
   images, and item images sync automatically into the online store. Recorded as an open
   question rather than a contradiction, because it is not clear the ceiling governs item
   photos at all.

## Rules that differ by platform

| | DoorDash | Uber Eats | Grubhub |
|---|---|---|---|
| **Hands in frame** | Allowed, if they do not obscure the item | Allowed | **Prohibited** |
| **Review SLA published** | No | Yes, up to 3 business days (stated for cover images) | No |
| **Appeal published** | No | No | No |
| **Platform adds its own photos** | Yes, from a connected Instagram account or Yelp | Customer-submitted photos, no published merchant opt-out | Not published |
| **Platform edits your photo** | Not published | **Yes**, size, orientation, lighting and colour, after approval | Not published |

Three platforms, three different answers on hands alone.

## Method

- **Only figures read directly off a platform's own documentation appear here.** Figures
  repeated by third parties, including by us, are excluded.
- Every figure carries a verification date. Treat anything older than a quarter as needing a
  re-check.
- Where a platform's own sources disagree, **both values are recorded** and the disagreement
  is stated. We do not pick a winner.
- **"Not published" is not the same as "does not exist."** Platform products sometimes
  contain behaviour the documentation omits. DoorDash's photo appeal is a live example: it
  exists in the merchant portal and appears nowhere in the help centre.

See [`VERIFICATION-LOG.md`](./VERIFICATION-LOG.md) for what was checked when, and
[`platforms/`](./platforms) for the full per-platform detail.

## Not covered

Google Business Profile and Instagram are deliberately absent. We hold figures for both, but
they have not been verified against the platforms, and unverified numbers do not belong in a
reference. ChowNow, Slice and Caviar have not been researched at all.

## Official sources

Every figure in this repository comes from one of these pages. They are linked so you can
check any claim yourself, which is the point of a reference.

**DoorDash**
- [Common photo issues explained](https://help.doordash.com/en-us/merchants/article/common-photo-issues-explained) (the merchant learning-centre photo-rejection URL now redirects here)
- [Photos terms glossary](https://help.doordash.com/en-us/merchants/article/photos-terms-glossary)
- [Menu photography (merchant blog)](https://merchants.doordash.com/en-us/blog/menu-photography)
- [Free DoorDash photoshoots](https://help.doordash.com/en-us/merchants/article/free-doordash-photoshoots)

**Uber Eats**
- [Merchant submitted menu catalog photo guidelines](https://help.uber.com/en/merchants-and-restaurants/article/merchant-submitted-menu-catalog-photo-guidelines?nodeId=6985355b-0426-4523-94f2-89bb9b0566e9)
- [Store submitted menu photo guidelines](https://help.uber.com/en/merchants-and-restaurants/article/store-submitted-menu-photo-guidelines?nodeId=0ad2da19-95e9-47d0-9db4-d7ddb346c357)
- [Adding cover images and menu catalog photos](https://help.uber.com/en/merchants-and-restaurants/article/adding-menu-photos---faq?nodeId=b2dfa2b7-20f2-4f5f-81a3-32fa4c2aea89)
- [User-submitted photos FAQ](https://help.uber.com/en/ubereats/restaurants/article/user-submitted-photos-faq?nodeId=eb8e9ce2-82dc-456b-9d0b-9feb545e6294)
- [Restaurant menu photography guidelines](https://merchants.ubereats.com/us/en/restaurant-submitted-photos/)

**Grubhub**
- [Grubhub menu overview (help centre)](https://get.grubhub.com/help-center/grubhub-menu-overview/)
- [Menu imagery specifications (developer portal)](https://developer.grubhub.com/docs/3zSHFME4nnntcOeqwbOTYl/menu-imagery-specifications)

**Toast**
- [Adding images to menu items](https://support.toasttab.com/en/article/Adding-Images-to-Menu-Items-in-the-Menu)
- [Online Ordering Pro menu image requirements](https://support.toasttab.com/en/article/Online-Ordering-Pro-Menu-Image-Requirements)
- [Customize your online ordering site](https://support.toasttab.com/en/article/Customize-Your-Online-Ordering-Site)

**Square**
- [Product images on Square Online](https://squareup.com/help/us/en/article/6894-product-images-on-square-online-store)
- [Adding pictures to your Square Online store](https://squareup.com/help/us/en/article/6887-adding-pictures-to-your-square-online-store)

Two notes on these links, learned by checking them. **DoorDash moves its URLs**: the
learning-centre path already redirected once. **Uber Eats help URLs require their `nodeId`
parameter**; the slug alone returns a 404, and Uber serves 404 to non-browser requests even
for valid URLs, so an automated link checker will report false failures on that domain.

## Corrections

If a platform has changed a spec, or one of these is wrong, please
[open an issue](../../issues). A dated source URL is the most useful thing you can include.
See [CONTRIBUTING.md](./CONTRIBUTING.md).

## License

[CC BY 4.0](./LICENSE).

**The figures themselves are facts and are free to use without attribution.** They describe
how someone else's product behaves and are not ours to license. What CC BY covers is the
written analysis, the compilation, and the structured representation in `specs.json`. See
[NOTICE.md](./NOTICE.md) for the full breakdown, including the quoted platform wording,
which belongs to the platforms.

Maintained by [MenuPhotoLab](https://menuphotolab.com).
