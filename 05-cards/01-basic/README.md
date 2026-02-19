# Card Components — Basic Card 🟢

**Branch:** `cards-basic`

## Learning Objectives

- [ ] Build a reusable card component with semantic HTML
- [ ] Use `box-shadow` and `border-radius` for depth
- [ ] Create a smooth hover lift effect with `transform` and `transition`
- [ ] Make cards responsive with a grid layout
- [ ] Understand the `article` element and when to use it

## The Design

```
┌────────────────────────┐
│  [Image — 16:9 ratio]  │
│                        │
│  Tag label             │
│  Card Title (h3)       │
│  Short description...  │
│  text wraps nicely.    │
│                        │
│  [Read More →]         │
└────────────────────────┘
```

3 cards in a row on desktop, 2 on tablet, 1 on mobile. All cards in a row are equal height regardless of content length.

### Exercises

1. Build one card with semantic HTML: `<article>`, proper heading level, `<img>`, `<p>`, `<a>`
2. Style it: `border-radius`, `box-shadow`, `overflow: hidden` to clip the image
3. Hover: `translateY(-4px)` lift + deeper shadow — use `transition: transform 0.2s, box-shadow 0.2s`
4. Make the image maintain 16:9 ratio: `aspect-ratio: 16/9` + `object-fit: cover`
5. Build a card grid using CSS Grid: `repeat(auto-fill, minmax(280px, 1fr))`

## Acceptance Criteria

- [ ] Card uses semantic HTML (`article`, appropriate heading)
- [ ] Image maintains 16:9 ratio regardless of source dimensions
- [ ] Hover effect is smooth and subtle
- [ ] Grid layout is responsive without explicit media queries (`auto-fill`)
- [ ] Card link wraps the entire card OR is clearly labelled (not just "Read More")
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: article element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article)
- [MDN: CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)
- [MDN: aspect-ratio](https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio)
- [MDN: box-shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
