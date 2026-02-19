# Card Components — Interactive Cards 🟠

**Branch:** `cards-interactive`  
**Prerequisite:** Complete `cards-variations` (Branch 2) first.

## Learning Objectives

- [ ] Build a CSS-only flip card (front and back)
- [ ] Create expandable/collapsible card content using `<details>`
- [ ] Add status badges with `position: absolute`
- [ ] Implement complex hover animations combining multiple properties
- [ ] Use `:has()` to style a card based on its internal state

## Task

### Card Type 1: Flip Card

```
FRONT:                    BACK (on hover):
┌────────────────────┐    ┌────────────────────┐
│  [Product Image]   │    │  Quick Details     │
│  Product Name      │    │  ───────────     │
│  €49.99            │    │  ★ 4.8 rating      │
│                    │ ↔  │  ✓ In stock        │
│  [Hover to flip]   │    │  ✓ Free shipping   │
│                    │    │  [Add to Cart]     │
└────────────────────┘    └────────────────────┘
```

Use 3D CSS transforms: look into `perspective`, `transform-style: preserve-3d`, and `rotateY()`.

### Card Type 2: Expandable Card

Use `<details>` and `<summary>` natively. Style it to look like a card:
- Summary shows: image, title, one-line teaser
- When expanded: full description, stats, and action button slide in with smooth animation
- Arrow indicator rotates on expand

### Card Type 3: Card with Status Badge

Combine with the basic card from Branch 1:
- `NEW`, `SALE`, `SOLD OUT` badges — `position: absolute` top-left of card image
- Badge colour based on class (`.badge--new`, `.badge--sale`, `.badge--sold-out`)
- Sold out card: image grayscale filter, text muted, button disabled style
- Use `:has(.badge--sold-out)` to style the whole card when sold out badge is present

### Card Type 4: Multi-stage Hover Animation

Create a card where hovering triggers a choreographed sequence:
- 0ms: card lifts (`translateY(-8px)`) and shadow deepens
- 100ms delay: a "Quick View" button fades in at the bottom of the image
- 150ms delay: a wishlist heart icon slides in from the top-right corner
- Use `animation-delay` and `@keyframes` OR `transition-delay` for the sequence

## Acceptance Criteria

- [ ] Flip card rotates correctly in 3D — front hides, back reveals
- [ ] `<details>` card expands smoothly with CSS animation
- [ ] Badges are positioned correctly and don't overflow the card boundary
- [ ] Sold-out cards are visually distinct and `:has()` is used for card-level styling
- [ ] Multi-stage hover animation runs in sequence, not all at once
- [ ] All animations respect `prefers-reduced-motion`
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: perspective](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective)
- [MDN: details element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details)
- [MDN: :has()](https://developer.mozilla.org/en-US/docs/Web/CSS/:has)
- [MDN: animation-delay](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-delay)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
