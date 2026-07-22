# Worked example: Build & Brew, Austin

A real event run end-to-end through the story-first workflow (`WORKFLOW.md`). Photos are the cleared
event selects from `../_test-photos/`. The whole set is **tonal, no accent** (paper / leather / cream),
which is one valid answer to the "ground + accent?" intake question.

## What's here
- `single.png` — the single post (Build Master story archetype).
- `carousel/01–05.png` — the 5 slides, in swipe order.
- `carousel/instagram/` — the same slides numbered for Instagram.
- `carousel/linkedin/austin-build-brew.pdf` — one swipeable PDF for LinkedIn (5 pages, 1080×1350).
- `caption.md` — the captions + tags, with the growth loop closed in the host's voice.

## The story-first trail (how it was made)

**Phase 1 · Intake → draft (Gate 1).** Single post + a short carousel. The night: 45 builders, paired
off, six real projects shipped in one evening in Austin. Look: tonal, no accent. Archetype picks by
photo, leading with the candid shots (the magic trick) over posed ones.

**Phase 2 · Preview → iterate (Gate 2).** Rendered with the scripts (the no-Paper fallback) and eyeballed
before export. The magic trick: the cover and invite lead with the candid, arms-up, actually-laughing
photos, not the posed line-up.

**Phase 3 · Export.** Instagram PNGs + one LinkedIn PDF.

**Phase 4 · Post (loop closed).** Captions credit NextWork in the host's voice and open one door
(come learn / come host); slide 05 carries the on-ramp on the image itself.

## The exact commands
```bash
cd templates/archetypes
P=../../EXAMPLES/_test-photos
O=../../EXAMPLES/austin-build-brew

# single post — Build Master story
./render.sh individual-build-master.html $O/single.png PHOTO=$P/talk-warm.jpg \
  ROLE="Build Master · Build & Brew Austin" \
  CLAIM="Nobody watched a demo." CONTEXT="45 people built one." \
  NAME="Jon Neylon" EVENT="Build & Brew · Austin, TX" CTA="come build"

# carousel: D cover -> 2x G moments -> numbers -> D invite
./render.sh D-block-photo.html $O/carousel/01.png PHOTO=$P/group-dusk.jpg \
  KICKER="Build & Brew · Austin" H1="One night." H2="Six ships." \
  BODY="45 builders paired off over coffee and shipped six real, working projects. Here's how the night went." CTA="swipe"
./render.sh G-timestamp.html $O/carousel/02.png PHOTO=$P/build-table.jpg \
  META="Build & Brew · Austin" TIME="7:30" LINE="Paired up. Heads down." DOTS=2/5
./render.sh G-timestamp.html $O/carousel/03.png PHOTO=$P/coding-screen.jpg \
  META="Build & Brew · Austin" TIME="9:00" LINE="First demos. Real code, real nerves." DOTS=3/5
./render.sh numbers.html $O/carousel/04.png META="Build & Brew · Austin" \
  N1="45" L1="builders in the room" N2="6" L2="projects shipped in one night" N3="1" L3="Build & Brew, Austin" DOTS=4/5
./render.sh D-block-photo.html $O/carousel/05.png PHOTO=$P/cafe-lounge.jpg \
  KICKER="Build & Brew · Austin" H1="Come build" H2="the next one." \
  BODY="Free build nights in Austin. Bring a friend and ship something real. New to it? Start at nextwork.ai." CTA="come build"

# package
./export.sh instagram $O/carousel
./export.sh linkedin  $O/carousel austin-build-brew
```

## Note on the look
This set is fully tonal on purpose. It used D for the cover, but archetype **A** can now go tonal too:
pass `TINT=none` to render A's serif word in cream instead of an accent colour (and `MODE=light|dark`
sets the ground on the block/text archetypes). See `templates/archetypes/README.md`.
