# DoorDash photo requirements

Type: **delivery marketplace**
Figures verified **2026-08-27**, usage terms re-read **2026-09-14**, source URL re-checked
**2026-09-21**.

## Specs, by asset type

DoorDash publishes **four photo types with four different specifications**, not one.

| Asset | Size | Aspect | Max file size |
|---|---|---|---|
| **Menu item photo** | 1400 x 800 px | 16:9, **landscape only** | 16 MB (but see below) |
| Logo | 230 x 230 px | 1:1 square recommended | 2 MB |
| Header / carousel | 1400 x 800 px | 4:1 on web, 16:9 in the app | 2 MB |

"Landscape only" is DoorDash's own framing for item photos. It is the strictest orientation
rule of any platform in this repository.

### The file size contradiction

**2 MB and 16 MB both appear on the same DoorDash page.** The 2 MB figure appears earlier;
16 MB appears in the item photo run-down. We record both. Staying under 2 MB satisfies either
reading.

## How one file gets displayed at two shapes

DoorDash renders **menu thumbnails at 1:1** and **detail headers at 16:9**, from the same
uploaded image.

This means a 16:9 file that looks correct in the detail view loses roughly the left and right
quarter of its frame in the thumbnail. Anything important near a horizontal edge disappears in
the surface a customer sees first.

Practically: keep the dish centered, and keep it away from the left and right edges.

## Hands

**Allowed, conditionally.** DoorDash's wording is that hands are acceptable "only if they
don't distract from or obscure the item."

Keep them out of focus, off to the side, secondary to the dish. Utensils in action are fine
where the hand itself is not visible.

This is worth stating clearly because the opposite is widely repeated. Of the three
marketplaces here, DoorDash permits with conditions, Uber Eats permits outright, and Grubhub
prohibits.

## Review and appeals

| | |
|---|---|
| Review SLA published | **No** |
| Appeal process published | **No** |
| Appeal process exists in the product | **Yes** |

The merchant portal places a **Request review** control on the rejection notice, worded "If
you think this was a mistake, you can request another review." Nothing in DoorDash's help
centre mentions it. No time limit or turnaround is published anywhere.

Two further behaviours captured in-product on 2026-08-30:

- A rejected item **stays in stock and keeps selling** with a broken image.
- The rejection reason is shown in the Menu Manager item drawer in plain language, not only
  by email.

## DoorDash may add photos you did not upload

If an item has no photo, DoorDash may supply one from **a connected Instagram business
account or from Yelp**.

- Your own upload always replaces it.
- You can opt out through Merchant Support.
- Yelp-sourced photos can be removed from Menu Manager via Request Menu Help.

This is rarely written about and it surprises merchants who find images on their menu they
never provided.

## Free photoshoot and what you may do with the results

DoorDash offers qualifying merchants a free photoshoot. **Two DoorDash pages describe the
resulting usage rights differently:**

| Source | Wording |
|---|---|
| Merchant blog | "You cannot use the photos on any other third-party delivery platforms." |
| Help centre | "These images are yours to keep, we only ask that you don't use the photos on any other third-party delivery platforms." |

One states a prohibition, the other a request. **Neither page is the merchant agreement**, so
neither settles the legal position. Read your own contract.

## Sources

- `help.doordash.com/en-us/merchants/article/common-photo-issues-explained` (the
  merchant learning-centre photo-rejection URL now 301s here)
- `help.doordash.com/en-us/merchants/article/photos-terms-glossary`
- `merchants.doordash.com/en-us/blog/menu-photography`
- `help.doordash.com/en-us/merchants/article/free-doordash-photoshoots`
- DoorDash Merchant Portal, Menu Manager (in-product, 2026-08-30)
