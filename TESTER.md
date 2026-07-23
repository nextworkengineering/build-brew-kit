# Try the Build & Brew Kit (thanks, Maya!)

You're one of the first to test this. The kit turns your event photos into clean, on-brand posts, and
your AI agent does the design for you on the Paper canvas. You don't design anything yourself: you talk,
you approve, it builds. No photos of your own yet? Use the samples in `EXAMPLES/_test-photos/` to run the
whole thing.

## What you need
- The kit: `git clone https://github.com/nextworkengineering/build-brew-kit.git` (or unzip, if Jon sent a zip).
- An AI agent (Claude Code or Cursor) with the **Paper MCP connected**. That's the one requirement, because
  the agent builds everything on the Paper canvas. There is nothing else to install.

## Run it
1. Open the kit in Claude Code or Cursor.
2. Paste this:

   > Read AGENT.md and follow it. My Build & Brew photos are in `EXAMPLES/_test-photos` (or point it
   > at your own folder). Make me a single post and a short carousel about the night.

3. It will ask you a few things about the night, show you a plan (Gate 1), then build the post on the
   Paper canvas for you to react to (Gate 2), and export it.

**One thing you do by hand: the photos.** Paper runs in the cloud, so the agent can't pull images off
your Mac. When it's ready to place a photo it'll ask you to **drag the JPGs onto the Paper file** — do
that once and it takes over. (Phone photos are HEIC; the agent converts them to JPG first.)

**On a free Paper account?** There's a weekly limit on how much the agent can do in Paper, so a full
carousel may not fit — start with a single post.

**If a preview looks blank,** it's probably Paper's screenshot hiccup, not your post — just look at the
canvas yourself and tell the agent what you see. You can also leave a comment right on a board and it'll read it.

If you tweak the canvas yourself, paste this so it re-checks the board before exporting:
> Run the brand-QA read-back on the board: fonts, grade, one accent as a small highlight, no face cropped,
> one line per photo, sentence case, and it reads at feed size. If the screenshot is blank, verify with
> computed styles and ask me to eyeball it. Fix any fail; don't export on a fail.

## What we'd love your feedback on
- Was it clear what to do, from start to finish?
- Did it make something you'd actually post?
- Did it feel like **your** brand and your voice, or generic?
- Where did you get stuck, confused, or annoyed?

This is early and we're iterating fast, so be blunt. Tell us what's clunky. That's the most useful thing
you can give us.
