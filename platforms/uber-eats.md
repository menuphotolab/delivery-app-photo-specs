# Uber Eats photo requirements

Type: **delivery marketplace**
All figures verified **2026-08-30**.

Uber Eats is the best-documented platform in this repository. It is the only one that
publishes a **maximum** resolution and the only one that publishes a **review SLA**.

## Item photo specs

| Field | Value |
|---|---|
| Width | 550 to 10,000 px |
| Height | 440 to 10,000 px |
| Aspect ratio | Between 5:4 and 6:4, i.e. 1.25 to 1.5 |
| File types | jpg, png, gif |
| Max file size | 10 MB |

### The aspect ratio is a recommendation, and only that

Uber's wording is: *"Be between 5:4 and 6:4 aspect ratio **(recommended)**."*

That parenthetical is Uber's, and it is **the only line in the entire requirements list that
carries one**. Every other rule on the page is stated unqualified.

This matters if you are building validation. A 16:9 file is outside the band but is not
failing a stated requirement, so it warrants a warning rather than a rejection.

### The floor and the shape are the same rule twice

550 x 440 is exactly 1.25:1, which is 5:4. Uber's minimum size and its minimum shape are
the same constraint expressed two ways.

## Cover image

| Field | Value |
|---|---|
| Size | 2880 x 2304 px |
| Aspect ratio | 5:4 |
| Format | JPEG |

## Content rules

**Hands: allowed.** The prohibition reads "Depict people (except for hands)."

**One item only.** "Contain more than 1 single item" is prohibited. This is stricter than it
sounds for platters, combination plates and anything served with sides.

**Centered framing required.** Images must be "framed in the center (i.e. items should not
appear at the corners or off frame)." This rules out off-centre editorial composition.

**Also prohibited:** blurry or out-of-focus images; strong shadows or insufficient lighting;
unsanitary environments including dirty surfaces, plating, packaging or used cutlery; text
and watermarks, with an exception for text or branding genuinely present on the food or its
packaging; anything infringing someone's rights.

**Category bans:** smoke-related items (tobacco, vapes, cigars, CBD, e-cigars), infant
formula, prescription items. Alcohol images must be referential with no brand displayed.

## Review process

| | |
|---|---|
| SLA | **Up to 3 business days** |
| Statuses | Pending, Approved, Rejected |
| Rejection detail | A "See Reasons" link, also sent by email |
| Appeal | **None published.** The documented route is to edit and resubmit |

Upload path: Menu Maker in Uber Eats Manager. Open the item, use the Photo section, Save,
then Request Approval.

## Customers can put photos on your menu

Uber runs a customer photo programme. Customers "can now submit photos of their purchased
items for review." Accepted photos "may be featured on the restaurant's Uber Eats page,"
appear "within 1-5 business days," and "may also be featured on the restaurant's menu or for
other promotional purposes."

Uber instructs submitters not to send AI-generated or heavily edited images.

**No merchant opt-out is published on either customer-photo page.** This is the Uber
counterpart to DoorDash sourcing photos from Instagram or Yelp, and it is similarly
under-discussed.

## Free photoshoot and usage terms

Qualifying restaurants get one complimentary shoot during onboarding, with more available by
scheduling. It covers individual items plus one profile image. Files are emailed to the
merchant and to the Uber representative.

On usage, Uber's page says: *"Feel free to use the photos in your own marketing, too."* It
states **no** restriction regarding other delivery platforms anywhere on that page.

**Silence is not permission.** DoorDash publishes an explicit restriction; Uber publishes a
permission for "your own marketing" and says nothing about marketplaces. Those are different
things and neither page is a contract. Read your merchant agreement.

## A gap worth knowing about

Uber's own "how to photograph your food" advice page covers lighting, top-down versus
45-degree angles, cutting sandwiches in half, garnish and working fast. It **publishes no
specifications at all**. Every number above lives only in the help centre, on different
pages.

## Sources

- `help.uber.com/merchants-and-restaurants/article/merchant-submitted-menu-catalog-photo-guidelines`
- `help.uber.com/merchants-and-restaurants/article/store-submitted-menu-photo-guidelines`
- `help.uber.com/merchants-and-restaurants/article/adding-menu-photos---faq`
- `help.uber.com/ubereats/restaurants/article/user-submitted-photos-faq`
- `merchants.ubereats.com/us/en/restaurant-submitted-photos/`
