# Square photo requirements

Type: **point of sale with its own online ordering**
All figures verified live **2026-09-21**.

Like Toast, Square is a point of sale with an online store attached, not a delivery
marketplace.

## Item images

| Field | Value |
|---|---|
| Recommended size | "at least 2000 x 2000 pixels with a 1:1 aspect ratio" |
| Hard minimum | **Not stated** |
| File types | JPG, JPEG, PNG, GIF |
| Max file size | "Images can be up to 15MB" |

15 MB is the most generous file size cap of any platform in this repository.

## Site images (a different rule set)

| Field | Value |
|---|---|
| Non-background images | "no more than 1,000 pixels on its longest side" |
| Background images | "at least 2,000 x 1,000 pixels" |
| File types | JPG, PNG, GIF |

### Unique filenames are required

Square states that duplicate filenames cause images to swap places or fail to load
altogether.

This is a genuine trap and nobody writes about it. If you export a set of dish photos from a
camera or a tool that names everything `image.jpg` or `export-1.jpg`, uploading them will
produce results that look random. Rename before uploading.

## One image per item, and it syncs everywhere

Two quoted rules that matter together:

> "Images uploaded to your item catalog will sync across your point of sale app and devices,
> and Square Online."

> "You cannot have different images for the same item across your point of sale app and
> Square Online."

So a single file has to work on the POS screen and on the web store, and there is no
per-surface override.

## An open question we are not calling a contradiction

Square publishes a **2000 px floor** for item images and a **1000 px ceiling** for site
non-background images. Item images sync automatically into Square Online. The
one-image-per-item rule removes the obvious workaround.

If the ceiling governs item photos once they render on the site, the same file is required to
be at least 2000 px and at most 1000 px.

**We are not publishing that as a contradiction**, because the 1000 px article is about
pictures you place into page sections and it may not govern catalog item photos at all.
Square does not state which rule applies to an item photo on the Square Online site.

If you can point at a Square page that settles it, [please open an issue](../../issues).

## Not yet checked

- Square for Restaurants and Square for Franchises menu images, which have their own
  documentation
- Whether Square operates any photo review process

## Sources

- `squareup.com/help/us/en/article/6894-product-images-on-square-online-store`
- `squareup.com/help/us/en/article/6887-adding-pictures-to-your-square-online-store`
