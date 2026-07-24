# Archetypes — the kit of parts

These HTML files are the **design source** for the Paper boards, not something you run. The agent builds every post on the **Build & Brew Kit** Paper canvas (see `AGENT.md`); the files here define each board's layout, grade, and `{{SLOTS}}` so the boards stay consistent. Each is a 1080×1350 (4:5) slide.

## Slots
Pick a board by the moment and fill its photo + copy from the slot list below.

**Theming (ground + accent).** Each board carries a default look; ground and accent are adjustable on the board via tokens (`--ground`, `--accent`).
- Ground: light (paper + ink) or dark (leather + cream), on the block / text archetypes (D, build-master).
- Accent: the default is none (fully tonal), so the photos are the hero. If one is wanted: pumpkin, cornflower, plum, canary, sand, or emerald. In A it colours the big word; `none` = fully tonal. A sits on a paper ground (contain, text below the photo); G stays photo-with-scrim, so ground mostly moves the block / text archetypes.

## The templates

| File | Use it for | Slots |
|---|---|---|
| `A-photo-contain.html` | **Single post / carousel cover.** One photo shown whole on paper (never cropped), line + big word below. Group- and landscape-safe. | `PHOTO META LINE1 ACCENT DESC` |
| `D-block-photo.html` | **Poster / landscape.** Clean photo up top, bold grotesk claim on a paper block below. The go-to for a landscape / wide photo (single post or carousel slide): the text lives in the block, so it works every time. | `PHOTO KICKER H1 H2 BODY CTA` |
| `G-timestamp.html` | **Carousel moment.** Photo + centered time + one line. Order them to tell the night. | `PHOTO META TIME LINE` |
| `individual-build-master.html` | **Build Master story.** Names you + your event, first person, two-tone. | `PHOTO ROLE CLAIM CONTEXT NAME EVENT CTA` |

## Group shots (keep the whole crew)
A wide group photo loses its edge people if you cover-crop it into 4:5. A (contain) and D already show the whole photo. Keep everyone:
- **Square 1:1** (1080×1080) — more width than 4:5, good for small-to-medium groups.
- **D (block + photo)** or a **contain/letterbox on the ground** — shows the whole photo, best for wide groups.
- **Focal + tag** — if a crop is unavoidable, keep the clear subject and tag everyone in the caption.
Never drop a learner silently. See the GROUP SHOTS rule in `AGENT.md`.

## A carousel, in order
Build the boards in swipe order and keep the same look on every slide:
1. **Cover** — A (photo) or D (block).
2. **A few moments** — G (timestamp), one beat each (6:00 doors → 9:00 demos). A landscape moment? Use D (block + photo) instead of G, so the wide shot isn't force-cropped.
3. **Invite** — A or D (come build the next one).

Then export from Paper (see the EXPORT rules in `AGENT.md`): Instagram = the 1080×1350 boards in order; LinkedIn = one PDF, a board per page.
