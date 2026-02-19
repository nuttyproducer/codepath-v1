# Wireframe — E-Commerce Product Page 🔴

**Branch:** `wireframe-ecommerce`  
**Prerequisite:** Complete `wireframe-dashboard` (Branch 3) first.

## The Wireframe

```
┌─────────────────────────────────────────────────────────────┐
│  HEADER: Logo  |  Search [______]  |  🛒 Cart (2) | 👤     │
├─────────────────────────────────────────────────────────────┤
│  Home > Men > Running > Nike Air Zoom Pegasus 40            │
├───────────────────────┬─────────────────────────────────────┤
│  ┌─────────────────┐  │  Nike Air Zoom Pegasus 40           │
│  │                 │  │  ⭐⭐⭐⭐⭐  4.8  (1,247 reviews)     │
│  │  MAIN IMAGE     │  │                                     │
│  │  (big square)   │  │  ~~€129.99~~  €99.99  Save 23%     │
│  │                 │  │  ✅ In Stock — Ships in 2-3 days    │
│  └─────────────────┘  │                                     │
│  [🖼][🖼][🖼][🖼][🖼]  │  Colour: Black ← selected           │
│  thumbnails           │  ⬛  ⬜  🟥  🔵  (swatches)         │
│                       │                                     │
│                       │  Size (EU):                         │
│                       │  [39][40][41][42][43][44][45]       │
│                       │       ↑ selected=42                 │
│                       │                                     │
│                       │  Qty: [−] 1 [+]                    │
│                       │                                     │
│                       │  [🛒 Add to Cart — €99.99]          │
│                       │  [❤️ Save to Wishlist]              │
│                       │                                     │
│                       │  🚚 Free shipping over €75          │
│                       │  🔄 30-day returns                  │
├───────────────────────┴─────────────────────────────────────┤
│  [Description]  [Reviews (47)]  [Shipping]  [Size Guide]   │
├─────────────────────────────────────────────────────────────┤
│  Tab content area changes based on active tab              │
├─────────────────────────────────────────────────────────────┤
│  You May Also Like                                          │
│  [Card ←]  [Card]  [Card]  [Card]  [→ Card]               │
├─────────────────────────────────────────────────────────────┤
│  FOOTER                                                     │
└─────────────────────────────────────────────────────────────┘
```

## Learning Objectives

- [ ] Build a CSS-only image gallery with thumbnail selection
- [ ] Create custom radio button swatches (colour and size selectors)
- [ ] Implement CSS-only tab interface with smooth transitions
- [ ] Use `position: sticky` for the purchase panel on large screens
- [ ] Create a strikethrough pricing display with sale badge
- [ ] Handle out-of-stock states visually with CSS

## Task

This is the mastery challenge. An e-commerce product page is one of the most interaction-dense pages on the web. Every selector must feel professional. Plan your full HTML structure before writing a single line of CSS.

### Exercise 1) Image gallery with thumbnail selection

Build a gallery that swaps the main image when a thumbnail is clicked — CSS only:
- 5 thumbnail images (use coloured placeholder `<div>` elements)
- Use `<input type="radio" name="gallery">` hidden behind each thumbnail
- When a radio is checked, the corresponding large image becomes visible
- Main image area: square, `object-fit: cover`
- Active thumbnail: border highlight
- Smooth fade between images using `opacity` transition
- Keyboard accessible: thumbnails are labelled

### Exercise 2) Colour and size selectors

Both use radio buttons styled as visual selectors:

**Colour swatches:**
- 4 options: Black, White, Red, Navy
- Display as 32px circles with the actual colour as `background-color`
- Selected: 3px offset ring using `outline` + `outline-offset`
- Hover: slight scale up
- Add `aria-label="Colour: Black"` to each label

**Size buttons:**
- 7 sizes (39–45)
- Display as pill buttons
- Selected: filled background, white text
- Out of stock (e.g., 41): grey, line through, `cursor: not-allowed`, `aria-disabled="true"`
- Use `disabled` on the radio input for out-of-stock

### Exercise 3) Sticky purchase panel

On desktop (≥1024px), the right-side purchase panel should stick while the left image scrolls:
- Use `position: sticky` with `top: 80px` (below fixed header)
- The panel should have `max-height: calc(100vh - 100px)` and `overflow-y: auto`
- On mobile: stack vertically, no sticky

### Exercise 4) Tab interface with content

Four tabs: Description, Reviews, Shipping, Size Guide:
- CSS-only using radio inputs
- Active tab: bottom border accent, slightly bolder text
- Tab content: only the active panel is visible (`display: none` / `display: block`)
- Smooth `opacity` + `transform` transition when switching tabs
- Reviews tab shows a star breakdown (5 bars showing % of each star rating — CSS only)

### Exercise 5) Product cards carousel layout

Create a "You May Also Like" section:
- 5 product cards in a horizontally scrollable container
- Uses `display: flex`, `overflow-x: auto`, `scroll-snap-type: x mandatory`
- Each card `scroll-snap-align: start`
- Scrollbar hidden but still functional (`::-webkit-scrollbar { display: none }`)
- Cards have: image, name, price (with optional sale price), rating stars, "Add to Cart" button
- Hide scrollbar but add visual arrow hints (`◀ ▶`) using CSS pseudo-elements on the wrapper

## Acceptance Criteria

- [ ] Gallery switches main image on thumbnail click/keyboard — CSS only
- [ ] Colour swatches show real colours and selected state clearly
- [ ] Out-of-stock sizes are visually distinct and have `disabled` + `aria-disabled`
- [ ] Purchase panel is sticky on desktop, stacked on mobile
- [ ] All 4 tabs work and transition smoothly — CSS only
- [ ] Reviews tab shows star breakdown bars
- [ ] Product cards scroll horizontally with snap behaviour
- [ ] Pricing display shows original (struck through), sale price, and discount badge
- [ ] All form controls are keyboard navigable
- [ ] Lighthouse Accessibility score is 100
- [ ] No JavaScript is used anywhere

## Resources

- [CSS :target for galleries](https://css-tricks.com/css-only-carousel/)
- [Scroll snap](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scroll_snap)
- [Custom radio as image swatches](https://css-tricks.com/custom-styling-form-inputs-with-modern-css-features/)
- [CSS-only tabs (revisited)](https://css-tricks.com/a-css-approach-to-trap-focus-within-an-element/)
- [outline vs border for focus rings](https://developer.mozilla.org/en-US/docs/Web/CSS/outline)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
