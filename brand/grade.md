# The grade

Every Build & Brew photo carries **one consistent grade** so the whole feed reads as a single brand. The grade is a light-touch cinematic treatment: warm, slightly darkened, gently desaturated. It is applied on the photo layer (in Paper, as the image layer's filter; in the design-source HTML, as a CSS `filter`). Never bake a heavy filter into the photo before it goes in, and never stack two grades.

## The standard grade (use this by default)
Applied as a filter on the photo layer:

| Archetype | Filter | Why this one |
|---|---|---|
| A (photo, contain) | `brightness(.96) contrast(1.05) saturate(.93)` | Whole photo on paper, no text over it, so it stays bright (same as D). |
| G (timestamp) | `brightness(.72) contrast(1.06) saturate(.86)` | Darkest, most mood; a centered time reads over it. |
| D (block + photo band) | `brightness(.96) contrast(1.05) saturate(.93)` | The photo is a clean band, not a scrim, so it stays brighter. |
| Build Master story | `brightness(.82) contrast(1.06) saturate(.88)` | Same feel as A. |

Common thread: a small desaturation (`saturate` .86–.93, roughly 7–14% down), a hair more contrast (1.05–1.06), and a brightness set by how much text sits on the photo. Subtle wins. The photo should still read as the moment, never mush.

## Strong colored lighting (party / RGB / magenta lights)
Build & Brew rooms often have coloured event lighting (magenta, purple, RGB). The standard grade's gentle desaturation is not enough: the cast stays and reads off-brand. For these photos:

- **Desaturate harder:** `saturate(.4) brightness(.9) contrast(1.08)`. Pulling saturation down roughly 60% neutralises most of the colour cast toward the brand's warm neutral.
- **Warm it back:** add a paper-toned overlay (`#f8f5f1` at ~12–18%, soft-light or overlay blend) on top of the photo, so the neutralised image leans warm rather than grey.
- **Sanity-check:** it should sit in the same family as the standard grade (warm, quiet), just recovered from bad lighting. If faces have gone grey or waxy, ease the desaturation back up (`saturate(.5)`).

## The rule
One grade per feed. Pick standard or the colored-lighting branch per photo, apply it on the photo layer, and leave it. The QA read-back checks the grade is applied and the photo still reads as the moment.
