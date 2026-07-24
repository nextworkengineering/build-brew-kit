# NextWork Community Kit

A ready-made kit for **Build Masters & Brew Masters**: point your AI agent at it and turn your event photos into clean, on-brand social posts in minutes. No design-tool wrangling, no blank page.

Running a Build & Brew is leadership. This helps you show it.

## Why post your events

You ran a room where people built real things. That's leadership, and this is your personal brand: proof, on the record, that you ship and bring people together.

- **It reads as leadership.** Running events and posting about them signals initiative, community, and active self-improvement beyond your day job. That is what people skim CVs and LinkedIn for.
- **It's a build session.** You upskill on the AI-agent workflow while you make the asset. The post is the byproduct of learning a real skill, the same skill NextWork teaches.
- **It compounds.** Tag the people in your photos. Their feeds see it, their friends see it, and your next event fills itself.
- **It passes the torch.** Someone who sees your post thinks "I could do that too," starts their own first project, and runs their own night. You're the start of that in your city.

## What's in the kit

- `AGENT.md` — **the one file you hand to your AI agent.** It carries the brand rules, the kit of parts, the copy rules, and how to render and export, so your posts look right by default.
- `templates/archetypes/` — the **kit of parts**: six post archetypes (the design source for the Paper boards). See its `README.md` for the archetype list and slots.
- `brand/` — the colours, fonts, and voice that make a post feel like NextWork.
- `templates/caption-and-tags.md` — the post's text field, who to tag, and how to credit NextWork and open the door for the next person (the growth loop, in your voice).
- `start-your-own-build-and-brew.md` — never run one? The whole format on one page. The on-ramp for the next host.
- `free-paper-path/` — running the kit on a free Paper account, and where the free-tier limits are.
- `EXAMPLES/` — sample event photos and rendered demos.

## Quickstart

Your AI agent does the design. You talk, you approve, it builds. There is a one-time Paper setup, then you run it. No design skills, no tech skills needed.

### Step 1 — set up Paper (once, about 2 minutes)
Do all four, in order. Skipping any one of them is the usual reason a run stalls.
1. **Open the Paper desktop app** (the Mac app, not the website) and leave it open. Your agent works through this app, so it has to be running.
2. **Make a new blank Paper file** for your post, and remember what you named it. Your agent builds there.
3. **Give Paper Full Disk Access:** System Settings > Privacy & Security > Full Disk Access > switch on **Paper** > quit and reopen Paper. This is the step that lets the agent use your photos. Skip it and photo import just hangs with no error.
4. **Make a folder on your Desktop** and drop your event photos into it.

### Step 2 — run it
1. **Clone this repo** (or download the ZIP) and open it in your AI agent (Claude Code or Cursor, with the **Paper MCP connected**).
2. **Paste this**, filling in your photo folder and the file you named:
   > "Read AGENT.md and follow it. My Build & Brew photos are in `./photos`, and I opened a blank Paper file called '<name>'. Make me a single post about the event."
3. It asks about the night, shows you a plan to approve (Gate 1), builds it on the **Paper canvas** for you to react to (Gate 2), then exports it. You never touch a design tool.

**No photos (virtual event)?** Use the text-only archetype (F), or a screenshot of what a member built as the photo in D. See `AGENT.md`.

## The ask (optional, but it's the flywheel)

- Tag attendees and @NextWork so the post travels.
- Credit what got you here and leave a door open for the next person (see `templates/caption-and-tags.md`). That's how a viewer becomes the next builder.
- Haven't run one yet? `start-your-own-build-and-brew.md` is the whole format on one page. Your first event fills the next room.
- Found a layout you like, or built a new archetype? PR it back (see `CONTRIBUTING.md`) so the whole community gets it.

---

*Brand values here are a snapshot of the internal NextWork kernel. See `scripts/sync-from-kernel.md`.*
