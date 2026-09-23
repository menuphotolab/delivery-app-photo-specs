# Grubhub photo requirements

Type: **delivery marketplace**
Both specifications verified live **2026-08-27**.

**Grubhub publishes two complete item-photo specifications that contradict each other on
every field.** Neither page acknowledges the other. This page documents both.

## The two specifications

| Field | Help centre | Developer portal |
|---|---|---|
| Minimum size | 200 x 200 px | **1600 x 1200 px** |
| Aspect ratio | 1:1 | **4:3** |
| File formats | .png only | .png, .jpeg, .jpg |

These are not different levels of detail for the same rule. They are different rules. A file
that satisfies the help centre is **8 times too small** in each dimension for the developer
portal, and the wrong shape.

### Which one applies to you

Grubhub does not say. The most likely explanation, inferred from which audience each page
addresses rather than from anything Grubhub states:

- **Help centre** addresses restaurants uploading manually through Grubhub for Restaurants.
- **Developer portal** addresses POS and integration partners submitting menus by feed.

If you are unsure, the developer portal spec is the safer target: **1600 x 1200 at 4:3
satisfies the minimum on both pages**, though not the help centre's 1:1 shape or its png-only
rule.

### One observation

Grubhub's help-centre figure of **200 x 200 square is identical to the developer portal's
logo specification**. The number the wider industry repeats as Grubhub's photo requirement is
the same number Grubhub publishes for logos.

We state that as a coincidence we noticed. We are not claiming to know what Grubhub intended.

## Other assets (developer portal)

| Asset | Size | Aspect | Note |
|---|---|---|---|
| Header | 2400 x 1800 px | 4:3 | Desktop web crops it to 4:1 |
| Profile / search | 2400 x 1200 px | 2:1 | |
| Logo | 200 x 200 px | Square artboard | .png, .jpeg, .jpg |

The help centre adds that a logo requires a background colour, and that white is acceptable.

## Content rules

**Hands: prohibited.** The developer portal states no body parts, giving "hands holding food"
and "people eating" as examples.

Of the three marketplaces in this repository, Grubhub is the only one that bans hands
outright. DoorDash permits them conditionally, Uber Eats permits them.

**No copyrighted or stock imagery**, with an exception for corporate photos belonging to the
corresponding chain.

**Framing advice**, quoted: "Cropping works best on all platforms when the focal point is
centered, and the image is captured from a distance."

## Rendering

Grubhub's ordering app displays **square cards**. A 4:3 file submitted to the developer spec
will therefore be cropped toward square in the surface customers browse.

## Review process

**Neither page publishes a review time or an appeal process.**

Upload path: Grubhub for Restaurants, Menu tab, Add Photo icon, accept the terms. The photo
enters a review status.

## Re-verifying the developer portal

**The developer portal is a JavaScript single-page app.** It returns `Grubhub is loading...`
to curl and to simple fetchers, so a naive fetch returns HTTP 200 with no content and looks
like it worked.

It has to be rendered in a headless browser. Wait for network idle, then read the DOM. A
verification pass that skips this step will silently miss the entire developer specification,
which is how this contradiction went unnoticed for a day on our own first attempt.

## Sources

- [Grubhub menu overview, help centre](https://get.grubhub.com/help-center/grubhub-menu-overview/)
- [Menu imagery specifications, developer portal](https://developer.grubhub.com/docs/3zSHFME4nnntcOeqwbOTYl/menu-imagery-specifications)
