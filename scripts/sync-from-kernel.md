# Regenerating brand/ from the kernel

`brand/colors.json` and the token values in `brand/typography.md` are a **snapshot** of the internal NextWork kernel. Do not hand-edit them. When the kernel changes, regenerate here so this public kit stays true and never drifts.

## Source of truth
The internal `nextwork-kernel` repo, `agent/visual/tokens/brand.json`.

## What to pull (public-safe subset only)
- `tokens.color.core` to `brand/colors.json` core (paper, leather)
- `tokens.color.diagramAccents` to `brand/colors.json` accents (the six)
- `tokens.typography` heading + body families to `brand/typography.md`

## What NOT to pull (keep this repo public-safe)
- The internal chunk system, voice taboos / anti-tells, retrieval rules, soul.md
- The brandScale ramp, enforcement scoring, thresholds
- Any internal names, tickets, analytics, or private repo paths
- Real team member photos or the host library

## Process
1. Read the current kernel `brand.json`.
2. Update the values in `brand/colors.json` (keep the generated header) and the font families in `brand/typography.md`.
3. Bump the kernel version in the header.
4. Open a PR. The PR is the brand-review gate.
