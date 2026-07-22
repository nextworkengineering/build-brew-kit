# Typography

Two fonts, three rules. That's the whole system.

- **Headline:** Suisse Neue. This is the only place a display font appears.
- **Everything else:** FK Grotesk Neue. Body, captions, labels, the CTA.

## Rules
1. Never mix the two fonts inside one element.
2. Caption and UI text use `letter-spacing: 0`, even when uppercase. Only large display headlines carry tracking.
3. Keep one line of text per photo. If you need a paragraph, it's a different post.

## Fonts you don't have (that's fine)
Most Build Masters won't have the licensed NextWork fonts, and that's okay. Fall back to `system-ui` and the post still works. The photos carry the brand far more than the exact typeface does.

```css
--font-heading: 'Suisse Neue', system-ui, sans-serif;
--font-body: 'FK Grotesk Neue', system-ui, sans-serif;
```
