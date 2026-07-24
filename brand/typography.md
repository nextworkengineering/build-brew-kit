# Typography

Two fonts, three rules. That's the whole system.

- **Headline:** Instrument Serif. This is the only place a display font appears.
- **Everything else:** Inter. Body, captions, labels, the CTA.

## Rules
1. Never mix the two fonts inside one element.
2. Caption and UI text use `letter-spacing: 0`, even when uppercase. Only large display headlines carry tracking.
3. Keep one line of text per photo. If you need a paragraph, it's a different post.

## Free fonts, loaded for you
Instrument Serif and Inter are both free, open-licensed fonts, so the kit can ship them. The templates load them from Google Fonts, so the post looks right on any machine with no font install. If a render context blocks web fonts they fall back to `system-ui` / a system serif and the post still works. The photos carry the brand far more than the exact typeface does.

```css
--font-heading: 'Instrument Serif', Georgia, serif;
--font-body: 'Inter', system-ui, sans-serif;
```
