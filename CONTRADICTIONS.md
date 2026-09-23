# Where these platforms contradict themselves

Every entry below is a case where a single platform publishes two figures that cannot both
be followed, or where its documentation and its product disagree. None of these are
disagreements between us and a platform. They are disagreements inside the platform's own
material.

We record both values and state the conflict. We do not pick a winner, because picking one
would mean publishing a number the platform does not stand behind.

---

## 1. DoorDash states two file size caps on the same page

| | |
|---|---|
| **Values** | 2 MB and 16 MB |
| **Where** | Both appear on the same DoorDash requirements page |
| **Verified** | 2026-08-27 |

The page lists 2 MB earlier and 16 MB in the item photo run-down. A merchant reading top to
bottom gets one answer; a merchant reading the item section gets another.

**Practical effect:** stay under 2 MB and you satisfy both readings.

---

## 2. Grubhub publishes two complete item specs that disagree on every field

The largest contradiction in this repository. Neither page acknowledges the other.

| Field | Help centre | Developer portal |
|---|---|---|
| Minimum size | 200 x 200 px | **1600 x 1200 px** |
| Aspect ratio | 1:1 | **4:3** |
| File formats | .png only | .png, .jpeg, .jpg |

Verified 2026-08-27 on both pages.

These are not different levels of detail. They are different requirements. An image that
satisfies the help centre (200 x 200, square, png) is **8 times too small** and the wrong
shape for the developer portal.

**Which one binds appears to depend on how the menu arrives:** manual upload through Grubhub
for Restaurants, versus a POS or integration partner feed. Grubhub does not say this
anywhere. It is inference from which audience each page addresses.

**One observation worth recording.** Grubhub's help-centre figure of 200 x 200 square is
*identical* to the developer portal's **logo** specification. The number the wider industry
repeats as Grubhub's photo requirement is the same number Grubhub gives for logos. We state
this as a coincidence we noticed, not as a claim about what Grubhub intended.

**A note for anyone re-checking this:** the developer portal is a JavaScript single-page app.
It returns `Grubhub is loading...` to curl and to simple fetchers, so a naive fetch looks
like it succeeded and tells you nothing. It has to be rendered in a headless browser.

---

## 3. Toast's recommended size fails Toast's own requirement

| | |
|---|---|
| **Toast Menu Manager recommends** | "a rectangle 750 px by 450 px" |
| **Toast Online Ordering Pro requires** | "a minimum height or width of 1000 pixels" and one of 1:1, 4:3 or 16:9 |
| **Verified** | 2026-09-21, both pages |

750 x 450 fails on two counts at once:

- **Size.** 750 is its longest side, 250 px short of the 1000 px floor.
- **Shape.** 750 x 450 is 5:3 (1.667), which is none of 1:1 (1.0), 4:3 (1.333) or 16:9 (1.778).

A restaurant that follows Toast's recommendation exactly produces a file Toast's own Online
Ordering Pro rejects on both dimensions.

**Resolution:** export **1920 x 1080** (16:9) or **1200 x 1200** (1:1). Either clears both
specifications with room to spare.

---

## 4. Toast states two banner file size caps

| | |
|---|---|
| **Values** | 5 MB and 9 MB |
| **Where** | The site customization page says 5 MB. Two other Toast pages say 9 MB. |
| **Verified** | 2026-09-21 |

The two most recent of those pages were updated **one day apart** and disagree.

**Practical effect:** stay under 5 MB.

---

## 5. Square: an open question, not yet a contradiction

We are deliberately not calling this one a contradiction, because we cannot yet show the two
rules govern the same file.

| | |
|---|---|
| **Item images** | "at least 2000 x 2000 pixels", 1:1 |
| **Site non-background images** | "no more than 1,000 pixels on its longest side" |
| **And** | "Images uploaded to your item catalog will sync across your point of sale app and devices, and Square Online" |
| **And** | "You cannot have different images for the same item across your point of sale app and Square Online" |
| **Verified** | 2026-09-21 |

If the 1000 px ceiling applies to item photos once they render on the Square Online site,
then the same file is required to be **at least 2000 px** and **at most 1000 px**, and the
one-image-per-item rule removes the obvious workaround.

**Why we are not publishing that as a conflict:** the 1000 px article is about pictures you
place into page sections, and it may not govern catalog item photos at all. Square does not
state which rule applies to an item photo on the online store.

If you know the answer, [please open an issue](../../issues).

---

## 6. DoorDash's documentation and DoorDash's product disagree about appeals

Not a numbers conflict. A more useful kind.

| | |
|---|---|
| **DoorDash's help centre** | Publishes no photo appeal process |
| **DoorDash's merchant portal** | Puts a **Request review** control on the rejection notice, worded "If you think this was a mistake, you can request another review" |
| **Verified** | 2026-08-30, in-product |

No time limit or turnaround is published anywhere.

This one is included as a caution about method. Reading a platform's documentation and
finding nothing only ever supports the claim **"they do not publish this."** It never
supports **"this does not exist."** We learned that by publishing the stronger claim and
being wrong.

---

## 7. Two DoorDash pages disagree on whether photoshoot images may be reused

DoorDash offers free photoshoots. Two of its own pages describe the resulting usage rights
differently.

| Source | Wording |
|---|---|
| Merchant blog | "You cannot use the photos on any other third-party delivery platforms." |
| Help centre | "These images are yours to keep, we only ask that you don't use the photos on any other third-party delivery platforms." |

Verified 2026-09-14, both live, quoted verbatim.

One states a prohibition. The other states a request. **Neither page is the merchant
agreement**, so neither settles the legal position. Anyone relying on this should read their
own contract rather than either page.

Uber Eats, by contrast, says of its photoshoot images: "Feel free to use the photos in your
own marketing, too," and states no marketplace restriction anywhere on that page. **Silence
is not permission.** We record what each platform published and nothing more.

---

*Maintained by [MenuPhotoLab](https://menuphotolab.com). Corrections welcome via
[issues](../../issues).*
