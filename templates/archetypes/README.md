# Archetypes — the kit of parts

Ready-to-render post templates. Pick one by the moment, fill its `{{SLOTS}}`, render to a 1080×1350 PNG.

## Render

```
cd templates/archetypes
./render.sh <template.html> <out.png> KEY=VALUE [KEY=VALUE ...]
```
First-time setup: `npx playwright install chromium`. `PHOTO` takes any path (auto-resolved) or a URL.
Carousel dots: `DOTS=2/6` (active/total). 2× export: add `W=2160 H=2700`.

**Theming (ground + accent).** Pass neither and every template renders its default look.
- `MODE=light|dark` — the ground on the block / text archetypes (D, numbers, build-master, F). light = paper + ink, dark = leather + cream.
- `TINT=pumpkin|cornflower|plum|canary|sand|emerald|none|#hex` — the accent colour. In A it colours the accent word; in F it colours the claim; `none` = cream (fully tonal). Photo slides (A, G) are photo-with-scrim, so MODE mainly moves the block/text archetypes.

## The templates

| File | Use it for | Slots |
|---|---|---|
| `A-photo-serif.html` | **Single post / carousel cover.** One photo, serif line + big accent word, bottom-anchored. | `PHOTO META LINE1 ACCENT DESC` |
| `D-block-photo.html` | **Poster.** Clean photo up top, bold grotesk claim on a paper block below. | `PHOTO KICKER H1 H2 BODY CTA` |
| `F-narrative-text.html` | **Story beat / hot take.** No photo. Two-tone statement. | `CLAIM CONTEXT HANDLE SERIES` |
| `G-timestamp.html` | **Carousel moment.** Photo + centered time + one line. Order them to tell the night. | `PHOTO META TIME LINE DOTS` |
| `numbers.html` | **Proof slide.** Big stats on leather. | `META N1 L1 N2 L2 N3 L3 DOTS` |
| `individual-build-master.html` | **Build Master story.** Names you + your event, first person, two-tone. | `PHOTO ROLE CLAIM CONTEXT NAME EVENT CTA` |

B (top-left title) and E (card over photo) also exist as boards in the Paper file (the pro option); script templates for them can be added the same way.

## A carousel in one sitting

```
# cover
./render.sh A-photo-serif.html 01.png PHOTO=../../photos/group.jpg META="Build & Brew · Austin" \
  LINE1="One night in Austin." ACCENT="Six real things," DESC="shipped."
# moments
./render.sh G-timestamp.html 02.png PHOTO=../../photos/coffee.jpg META="Build & Brew · Austin" \
  TIME="6:00 PM" LINE="Doors open. Coffee's on." DOTS=2/6
./render.sh G-timestamp.html 03.png PHOTO=../../photos/build.jpg META="Build & Brew · Austin" \
  TIME="9:00 PM" LINE="First demos. Real code, real nerves." DOTS=3/6
# proof
./render.sh numbers.html 04.png META="Build & Brew · Austin" \
  N1="45" L1="builders in the room" N2="6" L2="real projects shipped" N3="1" L3="night in Austin" DOTS=4/6
# invite
./render.sh D-block-photo.html 05.png PHOTO=../../photos/crowd.jpg KICKER="Build & Brew · Austin" \
  H1="Come build" H2="the next one." BODY="Free build nights across Texas. Bring a friend." CTA="RSVP"
```

Then export (see the EXPORT rules in `AGENT.md`): Instagram → the numbered PNGs; LinkedIn → combine them into one PDF.
