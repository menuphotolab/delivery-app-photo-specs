# Uber Eats photo requirements

Type: **delivery marketplace**
All figures verified live **2026-09-22**.

Uber Eats is the best-documented platform in this repository. It is the only one that
publishes a **maximum** resolution and the only one that publishes a **review SLA**.

## Item photo specs

| Field | Value |
|---|---|
| Width | 550 to 10,000 px |
| Height | 440 to 10,000 px |
| Aspect ratio | Between 5:4 and 6:4, i.e. 1.25 to 1.5 |
| File types | jpg, png, gif |
| Max file size | 10 MB (5 MB for Creative Hub in Uber Marketing Manager) |

### The aspect ratio is marked as a recommendation

Uber's wording is: *"Be between 5:4 and 6:4 aspect ratio **(recommended)**."*

In a list where every other line is stated as a flat requirement ("Accurately represent a
single item", "Be framed in the center"), this is **the only one softened to a
recommendation**.

That matters if you are building validation. A 16:9 file is outside the band but is not
failing a stated requirement, so it warrants a warning rather than a rejection.

### The floor and the shape are the same rule twice

550 x 440 is exactly 1.25:1, which is 5:4. Uber's minimum size and its minimum shape are
the same constraint expressed two ways.

## Cover image

| Field | Value |
|---|---|
| Size | 2880 x 2304 px ("Margins must fill the expected dimension") |
| Aspect ratio | 5:4 |
| Format | JPEG |
| Framing | "centered, leveled, and properly cropped" |

Uber also discourages people in cover images, because it "would require their image
authorization," and bans storefront exteriors, interiors, animals, black and white, collages,
and anything showing only a single product.

## Content rules for item photos

**Hands: allowed.** The prohibition reads "Depict people (except for hands)."

**One item only.** "Contain more than 1 single item" is prohibited, with Uber's own example:
"photos for pizza should display only pizza; not pizza and hamburgers." This is stricter than
it sounds for platters, combination plates and anything served with sides.

**Centered framing required.** "Be framed in the center (items should not appear at the
corners or off frame)." This rules out off-centre editorial composition.

**Also prohibited:** blurry or out-of-focus images; strong shadows or insufficient lighting;
unsanitary environments including dirty surfaces, plating, packaging or used cutlery; logos
or watermarks; any text or words; anything infringing someone's rights. There is an exception
for logos and text genuinely on the food or its packaging, with no profanities.

**Category bans:** smoke-related items (tobacco, vapes, cigars, CBD, e-cigars), infant
formula, prescription items. Alcohol images must be referential with no particular brand
displayed, otherwise a health warning is required.

## Review process

| | |
|---|---|
| SLA | **Up to 3 business days**, stated for **cover images** |
| Statuses | Pending, Approved, Rejected |
| Rejection detail | A "See Reasons" link |
| Appeal | **None published.** The documented route is to edit and resubmit |
| Withdraw | **Yes.** A pending photo can be pulled back before review completes |

**A scoping note, because we got this slightly wrong at first.** Uber states "The review
process can take up to 3 business days" in the section about **cover images**. It does not
publish an equivalent SLA for item photos. It remains the only published review timeframe of
any platform here, but it is narrower than a general "Uber reviews photos in 3 days."

Upload path for item photos: Menu Maker, click the item, Photo section, drag and drop or
browse, Save, then Request Approval.

To withdraw a pending photo: Menu Maker, click the item, **Cancel photo update**, then
**Withdraw**. Nobody else documents this, and it is useful if you spot a problem after
submitting.

## Uber may edit your photo after approving it

Two statements, both quoted verbatim, that are not written about anywhere else:

> "Once approved, we may edit the size, orientation, lighting, and/or color of your photos"

And under the heading "Why was the photo I submitted edited?":

> "The photo you submitted may have been edited to fit our photo guidelines."

So the image a customer sees is not guaranteed to be the file you uploaded. If colour
accuracy matters to you, that is worth knowing before you spend money on photography.

## The rights you grant by uploading

Quoted verbatim, and it appears on two separate Uber pages:

> "By uploading photos, you (1) represent and warrant that you have usage rights and don't
> violate any third party rights; (2) **sub-license the right to such photos to Uber,
> including the right to modify photos without permission**; and (3) release Uber from
> liability relating to such photos."

Read alongside the editing behaviour above, the second clause is what makes it possible.

## Customers can put photos on your menu

Uber runs a customer photo programme. Customers "can now submit photos of their purchased
items for review." Accepted photos "may be featured on the restaurant's Uber Eats page,"
appear "within 1-5 business days," and "may also be featured on the restaurant's menu or for
other promotional purposes."

Uber instructs submitters not to send AI-generated or heavily edited images.

**No merchant opt-out is published on either customer-photo page.** This is the Uber
counterpart to DoorDash sourcing photos from Instagram or Yelp, and it is similarly
under-discussed. *(Verified 2026-08-30, not re-checked 2026-09-22.)*

## Free photoshoot and usage terms

Qualifying restaurants get one complimentary shoot during onboarding, with more available by
scheduling. It covers individual items plus one profile image. Files are emailed to the
merchant and to the Uber representative.

On usage, Uber's page says: *"Feel free to use the photos in your own marketing, too."* It
states **no** restriction regarding other delivery platforms anywhere on that page.

**Silence is not permission.** DoorDash publishes an explicit restriction; Uber publishes a
permission for "your own marketing" and says nothing about marketplaces. Those are different
things and neither page is a contract. Read your merchant agreement.
*(Verified 2026-08-30, not re-checked 2026-09-22.)*

## A gap worth knowing about

Uber's own "how to photograph your food" advice page covers lighting, top-down versus
45-degree angles, cutting sandwiches in half, garnish and working fast. It **publishes no
specifications at all**. Every number above lives only in the help centre, on different
pages.

## Sources

- [Merchant submitted menu catalog photo guidelines](https://help.uber.com/en/merchants-and-restaurants/article/merchant-submitted-menu-catalog-photo-guidelines?nodeId=6985355b-0426-4523-94f2-89bb9b0566e9)
- [Adding cover images and menu catalog photos](https://help.uber.com/en/merchants-and-restaurants/article/adding-cover-images-and-menu-catalog-photos?nodeId=b2dfa2b7-20f2-4f5f-81a3-32fa4c2aea89)
- [Store submitted menu photo guidelines](https://help.uber.com/en/merchants-and-restaurants/article/store-submitted-menu-photo-guidelines?nodeId=0ad2da19-95e9-47d0-9db4-d7ddb346c357)
- [User-submitted photos FAQ](https://help.uber.com/en/ubereats/restaurants/article/user-submitted-photos-faq?nodeId=eb8e9ce2-82dc-456b-9d0b-9feb545e6294)
- [Restaurant menu photography guidelines](https://merchants.ubereats.com/us/en/restaurant-submitted-photos/)

Uber's help URLs need their `nodeId` parameter. The slug on its own returns a 404, and Uber
serves 404 to non-browser requests even for valid URLs, so an automated link checker will
report false failures here.

The `adding-menu-photos---faq` slug now **redirects** to
`adding-cover-images-and-menu-catalog-photos`. The link above points at the destination.
