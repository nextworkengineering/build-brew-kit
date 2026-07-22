# The Build Master run — how the kit actually works

> The canonical workflow. `AGENT.md` is what the agent follows; this is the human-readable
> version of the same journey, so you can teach it, test it, and see where it should improve.

**One principle: story-first, never output-first.** The agent's first move is to *ask*, not to
render. A Build Master should be walked through making their post — hearing the night back in
their own words, seeing it before it publishes, and iterating — not handed finished files.

**Why a Build Master posts.** The point is their empowerment, not our marketing. Running a room
where people build real things is leadership, and posting it builds their personal brand as
someone who ships and brings people together. Making the post also *is* the skill: driving an
agent to produce something clean and on-brand is exactly what NextWork teaches. NextWork's win is
downstream and honest: a viewer sees a peer building in public, thinks "I could do that too," and
starts their own first project or runs their own night. The kit is built to make that hero the
Build Master and to leave the door open, never to turn their post into an ad.

---

## The journey

### Phase 0 · Setup (once)
The Build Master makes a folder on their Desktop and drops the night's photos in:
```
~/Desktop/build-brew-<city>/        e.g. ~/Desktop/build-brew-austin/
```
They point the agent at it. The agent looks at the photos before choosing anything — archetype
picks are a lighting decision (warm/dim → cinematic A/G; bright/celebratory → D invite).

### Phase 1 · Intake → draft  · **Gate 1**
A short conversation *before any image is made*. The agent asks:
1. Single post or carousel? (Unsure → tell me about the night, I'll recommend.)
2. **What happened?** The arc — doors, pairing up, building, demos, who shipped what, the one
   human moment. *These words become the copy.*
3. Who are you (Build Master name), event name, city.
4. The numbers — headcount, projects shipped, any "first ever."
5. Where are you posting — Instagram, LinkedIn, or both.
6. The look — ground **light (paper)** or **dark (leather)**? Accent — pumpkin, cornflower,
   plum, canary, sand, or **none**? *Asked every run; no default.*

The agent drafts the archetype pick(s) + the line(s) in the Build Master's voice and **shows
them**. → **Gate 1: yes on the copy + plan before anything renders.**

### Phase 2 · Preview → iterate  · **Gate 2**
- **With Paper (canonical):** the agent builds the chosen archetypes as boards on the Paper
  canvas ("Build & Brew Kit" file), fills photo + copy, applies the chosen ground + accent, and
  puts the **caption + tags as a text board beside the slides** so the whole post is in one
  place. The Build Master iterates live — swap a photo, change a line, try another accent.
- **Without Paper (fallback):** the agent renders the slides with `render.sh` and shows the PNGs
  in chat. Same purpose — see it, tweak it, re-render.

**The magic trick (before Gate 2).** Correct-and-clean is the floor. The agent asks for the one
human thing it can't invent: the candid laughing photo over the posed one, the line only the
Build Master would write, the real people to tag. That is what makes the post theirs and what
fills the next room. See `magic_trick.md`.

→ **Gate 2: yes on the visuals before export.**

### Phase 3 · Export (only after Gate 2)
- Instagram single → PNG 1080×1350.
- Instagram carousel → numbered PNGs (01, 02, …).
- LinkedIn carousel → one PDF, a slide per page (a swipeable document).

### Phase 4 · Post (and close the loop)
The agent surfaces the caption + tags and the tag-the-faces checklist. Tagging the people in the
photos is the single biggest reach lever. Then it closes the loop, in the Build Master's voice:
- **Credit** NextWork the way you credit anything that helped you get here. Honest, not an ad.
- **On-ramp** a viewer two ways: start their own first project, or run their own Build & Brew
  (see `start-your-own-build-and-brew.md`). A viewer becoming the next builder, then the next
  host, is the whole loop.
- **Trackable link** so the loop is measurable (see the link convention in
  `templates/caption-and-tags.md`).

---

## Preview surface — Paper-first, scripts as fallback
Paper is the canonical preview/iterate surface (richest control, licensed fonts, live tweaks).
The HTML templates + `render.sh` are the **portable fallback** so a Build Master with no Paper
can still see and approve before exporting. Both honor the same two gates.

> **Ground + accent are wired both ways.** On Paper you apply them directly. In the scripts, pass
> `MODE=light|dark` (ground on the block/text archetypes D, numbers, build-master, F) and
> `TINT=<accent|none>` (the accent colour; `none` = fully tonal). Photo slides (A, G) stay
> photo-with-scrim, so MODE mainly moves the block/text archetypes.

---

## How to test this workflow (dry-run)
1. Put a few event photos in `~/Desktop/build-brew-<city>/` (or reuse `EXAMPLES/_test-photos/`).
2. Start a fresh session in the repo, hand the agent `AGENT.md`.
3. Watch that it **asks Phase 1 before rendering** (Gate 1), **previews before exporting**
   (Gate 2), asks ground + accent (no default), and surfaces the caption on the canvas.
4. Anything it skips or trips on is the next fix.
