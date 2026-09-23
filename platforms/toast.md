# Toast photo requirements

Type: **point of sale with its own online ordering**
All figures verified live **2026-09-21**.

Toast is **not a delivery marketplace**. Photos surface on the restaurant's own ordering
site, on POS screens and on kiosks. There is no moderation queue and no rejection path, so
the rejection language that applies to DoorDash and Uber Eats does not transfer here.

## The contradiction, first

**Toast's own recommended size fails Toast's own requirement.**

| | |
|---|---|
| Menu Manager recommends | "a rectangle 750 px by 450 px" |
| Online Ordering Pro requires | "a minimum height or width of 1000 pixels", and one of 1:1, 4:3 or 16:9 |

750 x 450 fails on both counts:

- **Size.** 750 is its longest side, 250 px short of the 1000 px floor.
- **Shape.** 750 x 450 is 5:3 (1.667). That is none of 1:1 (1.0), 4:3 (1.333) or 16:9 (1.778).

A restaurant following Toast's recommendation exactly produces a file Toast's own Online
Ordering Pro requirement rejects.

**Resolution: export 1920 x 1080 (16:9) or 1200 x 1200 (1:1).** Either clears both
specifications.

## Menu item photos

| Field | Menu Manager | Online Ordering Pro |
|---|---|---|
| Size | 750 x 450 px recommended | Minimum 1000 px on the longest side |
| Aspect | 5:3 implied | 1:1, 4:3 or 16:9 |
| File types | .jpg, .png | **Not stated** |
| Max file size | 5 MB | **Not stated** |

Where Online Ordering Pro states nothing, fall back to the Menu Manager article.

## Cropping behaviour

Quoted from Toast: images "may be cropped or zoomed to fit certain POS displays because the
POS applies its own aspect-ratio framing. Center the key content of the image so it remains
visible after cropping."

Online Ordering Pro adds: "All images will fill the container within the menu layout
selected."

Both point the same way. Keep the dish centered with margin, because Toast will reframe it
for surfaces you cannot preview.

## Carry-over

Menu Manager images "will carry over to your Toast online ordering website." One upload
serves the POS and the ordering site.

## Brand images: logo, banner, eGift

A different asset class with different pages.

| Asset | Minimum | Max file size | Formats |
|---|---|---|---|
| Logo | 230 x 230 px | 5 MB | not stated on the customization page |
| Banner | 1400 x 788 px | **5 MB or 9 MB, see below** | .jpg, .jpeg, .png |
| eGift card image | 640 x 400 px | 5 MB | |

**The banner file size is stated two ways.** The site customization page says 5 MB. Two other
Toast pages say 9 MB. The two most recent were updated **one day apart** and disagree. Stay
under 5 MB.

Banner placement, quoted: it "appears in the Toast Local app, Online Ordering, loyalty
sign-up, email sign-up, and email campaigns."

Toast's own banner advice: high resolution, no filters, a single featured food item, and
**no alcohol, no servers, no diners**. That is stricter on people than DoorDash or Uber Eats
are for item photos.

## One file that satisfies Toast and DoorDash

A rare case where two platforms line up instead of conflicting.

| | Toast | DoorDash | One file for both |
|---|---|---|---|
| Logo minimum | 230 x 230 | 230 x 230, 1:1, under 2 MB | **230 x 230 square, under 2 MB** |
| Banner minimum | 1400 x 788 | 1400 x 800, under 2 MB | **1400 x 800, under 2 MB** |

Logo minimums are **identical**. Banner minimums differ by 12 px of height at the same width,
so DoorDash's 1400 x 800 clears Toast's 1400 x 788 automatically.

DoorDash figures re-read 2026-09-21 rather than carried over from the earlier pass.

## Review

**Toast publishes no photo review or approval process**, and none appears in the documented
upload flow.

That claim is scoped to the documentation on purpose. The product itself was not checked, and
a documented absence never establishes that something does not exist.

## Sources

- `support.toasttab.com/en/article/Adding-Images-to-Menu-Items-in-the-Menu`
- `support.toasttab.com/en/article/Online-Ordering-Pro-Menu-Image-Requirements`
- `support.toasttab.com/en/article/Customize-Your-Online-Ordering-Site`
- `doc.toasttab.com/doc/platformguide/adminAddingImagesToMenuItems.html`
