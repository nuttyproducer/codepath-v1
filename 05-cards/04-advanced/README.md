# Card Components — Advanced Card System 🔴

**Branch:** `cards-advanced`  
**Prerequisite:** Complete `cards-interactive` (Branch 3) first.

## Learning Objectives

- [ ] Build a masonry-style grid layout
- [ ] Create skeleton loading states for all card types
- [ ] Implement a CSS-only filter/sort system using radio buttons
- [ ] Use `@container` queries for truly component-level responsive design
- [ ] Build a card with embedded tab interface

## Task

### Exercise 1) Masonry layout

Create a Pinterest-style masonry grid where cards have varying heights:
- Use CSS Grid with `grid-template-rows: masonry` (experimental) OR the `grid-row: span N` technique
- Cards span different numbers of rows based on their content (short = 1 row, tall = 2 rows)
- Add `@container` query on individual cards so a card adapts its internal layout based on its own width (not the viewport)

### Exercise 2) Skeleton loading system

Create skeleton states for every card type from branches 1-3:
- A `loading` class on the card shows animated shimmer placeholders
- Placeholders mimic the exact layout of the real content (same heights, same positions)
- When `loading` class is removed (CSS class toggle in DevTools for demo), real content appears with a fade-in
- Shimmers use the same gradient animation technique from the Bikes for Refugees branch

### Exercise 3) CSS-only filter interface

Build a category filter using radio buttons:
- Categories: All, Design, Development, Marketing, Business
- Clicking a category hides cards that don't belong to it (using `:not(:checked)` + sibling selectors + `data-category` attributes)
- Active filter button is highlighted
- Cards transition out with `opacity` + `transform` (they don't reflow, just become invisible — explain this limitation in a comment and document how JavaScript would solve it)

### Exercise 4) Card with internal tabs

A "profile card" that contains its own mini tab interface:
```
┌─────────────────────┐
│  [Avatar]  Name     │
│  Title · Company    │
│  ───────────────    │
│  [Posts][About][🔗] │  ← mini tabs inside card
│  ─────────────────  │
│  Tab content here   │
└─────────────────────┘
```
Uses `:checked` radios entirely inside the card component.

## Acceptance Criteria

- [ ] Masonry layout uses `grid-row: span` or CSS masonry
- [ ] `@container` queries adapt card internals based on card's own width
- [ ] Skeleton states match real card layouts precisely
- [ ] Filter system hides/shows cards by category using CSS only
- [ ] Filtering limitation is documented in a code comment
- [ ] Profile card tabs work independently within the card
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)
- [MDN: @container](https://developer.mozilla.org/en-US/docs/Web/CSS/@container)
- [MDN: animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)
- [MDN: :has()](https://developer.mozilla.org/en-US/docs/Web/CSS/:has)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
