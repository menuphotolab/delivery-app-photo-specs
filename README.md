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
| DoorDash | 1400 x 800 px | 16:9, landscape only | | 16 MB (see note) | 2026-08-27 |
| Uber Eats | 550 to 10,000 px wide, 440 to 10,000 px high | 5:4 to 6:4 (recommended) | jpg, png, gif | 10 MB | 2026-08-30 |
| Grubhub (help centre) | 200 x 200 px | 1:1 | png only | not stated | 2026-08-27 |
| Grubhub (developer portal) | 1600 x 1200 px | 4:3 | png, jpeg, jpg | not stated | 2026-08-27 |
| Toast (Menu Manager) | 750 x 450 px | 5:3 | jpg, png | 5 MB | 2026-09-21 |
| Toast (Online Ordering Pro) | 1000 px on the longest side | 1:1, 4:3 or 16:9 | not stated | not stated | 2026-09-21 |
| Square | 2000 x 2000 px | 1:1 | jpg, jpeg, png, gif | 15 MB | 2026-09-21 |

Uber Eats is the only platform here that publishes a **maximum** resolution.

## Where platforms contradict themselves

These are the parts no one else writes down, so they get their own section:
[`CONTRADICTIONS.md`](./CONTRADICTIONS.md).

1. **DoorDash states two file size caps on the same page**, 2 MB and 16 MB.
2. **Grubhub publishes two complete item specs that disagree on every field**, and neither
   page acknowledges the other.
3. **Toast's recommended 750 x 450 fails Toast's own Online Ordering Pro requirement.** It is
   250 px short of the 1000 px floor and its 5:3 shape is none of the three permitted ratios.
4. **Toast states two different banner file size caps** on pages updated one day apart.
5. **Square** publishes a 2000 px floor for item images and a 1000 px ceiling for site
   images, and item images sync automatically into the online store. Recorded as an open
   question rather than a contradiction, because it is not clear the ceiling governs item
   photos at all.

## Rules that differ by platform

| | DoorDash | Uber Eats | Grubhub |
|---|---|---|---|
| **Hands in frame** | Allowed, if they do not obscure the item | Allowed | **Prohibited** |
| **Review SLA published** | No | Yes, up to 3 business days | No |
| **Appeal published** | No | No | No |
| **Platform adds its own photos** | Yes, from a connected Instagram account or Yelp | Customer-submitted photos, no published merchant opt-out | Not published |

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

## Corrections

If a platform has changed a spec, or one of these is wrong, please
[open an issue](../../issues). A dated source URL is the most useful thing you can include.
See [CONTRIBUTING.md](./CONTRIBUTING.md).

## License

[CC BY 4.0](./LICENSE). Use it, quote it, build on it. Attribution appreciated.

Maintained by [MenuPhotoLab](https://menuphotolab.com).
