# Typography

One font, three rules. That's the whole system.

- **Everything is Inter.** Headlines, body, captions, labels, the CTA. No serif, no second family.
- **Hierarchy comes from size and weight, not a second typeface.** Display moments (a headline, the big word in A, the timestamp in G, a cover title) are Inter Medium 500 at a large size, elegant not heavy. Body and labels are Inter 400 / 500.

## Rules
1. One family only. Inter everywhere.
2. Caption and UI text use `letter-spacing: 0`, even when uppercase. Only large display headlines carry a little negative tracking.
3. Keep one line of text per photo. If you need a paragraph, it's a different post.

## Free font, loaded for you
Inter is a free, open-licensed font, so the kit can ship it and every learner can reproduce a post exactly. The templates load it from Google Fonts, so the post looks right on any machine with no font install. If a render context blocks web fonts it falls back to `system-ui` and the post still works. The photos carry the brand far more than the exact typeface does. (We deliberately don't use a paid display face like Suisse here: we can't share the licence with learners, and a free serif substitute looks too different to stay on brand.)

```css
--font-display: 'Inter', system-ui, sans-serif;
--font-body: 'Inter', system-ui, sans-serif;
```
