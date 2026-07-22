# Examples

Rendered reference posts, plus the exact command that made each — copy the command and swap in your own photos.

## Demo renders
`demo-single.png` and `demo-slide-1..3.png` were produced by the kit from the real sample photos in `_test-photos/`, so they show what the archetypes actually look like.

```bash
cd templates/archetypes
# single post (archetype A)
./render.sh A-photo-serif.html ../../EXAMPLES/demo-single.png \
  PHOTO=../../EXAMPLES/_test-photos/cafe-lounge.jpg \
  META="Build & Brew · Austin" LINE1="One night in Austin," ACCENT="we built" DESC="and shipped six real things."

# a 3-slide carousel: A cover -> G moment -> numbers
./render.sh A-photo-serif.html s1.png PHOTO=../../EXAMPLES/_test-photos/group-dusk.jpg \
  META="Build & Brew · Austin" LINE1="One night in Austin." ACCENT="Six real things," DESC="shipped."
./render.sh G-timestamp.html s2.png PHOTO=../../EXAMPLES/_test-photos/build-table.jpg \
  META="Build & Brew · Austin" TIME="7:30 PM" LINE="Paired up and building." DOTS=2/3
./render.sh numbers.html s3.png META="Build & Brew · Austin" \
  N1=45 L1="builders in the room" N2=6 L2="real projects shipped" N3=1 L3="night in Austin" DOTS=3/3
```

`_test-photos/` are real Build & Brew photos you can practice on.

## A real worked example
`austin-build-brew/` is a full event run through the story-first workflow: single post + a 5-slide
carousel (tonal, no accent), the Instagram PNGs and the LinkedIn PDF, and `caption.md` with the growth
loop closed in the host's voice. Its `README.md` shows the story-first trail and the exact commands.

Want to add yours? See `../CONTRIBUTING.md`.
