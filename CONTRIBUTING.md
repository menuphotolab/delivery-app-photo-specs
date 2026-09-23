# Contributing

The most valuable contribution here is **a spec that changed**. These platforms update their
documentation without announcing it, and a stale number in a reference is worse than no
reference at all.

## Reporting a changed or wrong spec

[Open an issue](../../issues) with:

1. **The platform and the field.** For example: "Uber Eats, item photo maximum file size."
2. **The value you are seeing**, quoted exactly as the platform words it.
3. **The URL** you read it on.
4. **The date** you read it.

Item 3 is the one that matters most. A correction without a source URL cannot be verified,
and an unverifiable figure does not go in.

## What gets accepted

**Yes:**

- A figure read directly off a platform's own documentation, with a URL and a date.
- A screenshot of platform behaviour that its documentation does not describe. First-party
  product evidence counts, and it is how the DoorDash appeal path in
  [CONTRADICTIONS.md](./CONTRADICTIONS.md) was established.
- A new contradiction inside a platform's own material.
- A platform we do not cover yet, if you have verified figures for it.

**No:**

- Figures from third-party blog posts, roundups or tool marketing, including ours. These
  contradict each other constantly, which is the whole reason this repository exists.
- "I heard" or "someone told me," without a source.
- A best guess at which of two contradicting official figures is the real one. If a platform
  disagrees with itself, that disagreement is the finding. We record both.

## The standard applied to every entry

Three rules, and they are not negotiable because the repository's only value is being right:

1. **Only what the platform itself published.** If we cannot point at their page, it does not
   go in.
2. **A date on every figure.** No undated numbers.
3. **Absence is scoped carefully.** Finding nothing in a platform's documentation supports
   "they do not publish this." It never supports "this does not exist."

## Re-verification

Everything here is re-checked on a quarterly cycle. If you are reading a figure whose date is
more than a quarter old and it matters to a decision you are making, check it against the
platform yourself and please open an issue either way. Confirmations are as useful as
corrections, and both let us move the date forward.
