# Card Components — Card Variations 🟡

**Branch:** `cards-variations`  
**Prerequisite:** Complete `cards-basic` (Branch 1) first.

## Learning Objectives

- [ ] Build multiple card layout variations for different content types
- [ ] Use CSS Grid internally within cards for complex layouts
- [ ] Create overlay effects with `position: absolute` and gradients
- [ ] Style pricing cards with visual hierarchy
- [ ] Build testimonial cards with quotation styling

## Task

Build a complete card system with 4 different card types, all sharing a design language (same colours, fonts, radius, shadows) but with unique layouts.

### Card Type 1: Horizontal Media Card
```
┌────────────────────────────────────────────────┐
│  [Image]  │  Tag                               │
│  square   │  Title of the article here         │
│           │  Short description text...         │
│           │  By Author  ·  5 min read          │
└────────────────────────────────────────────────┘
```

### Card Type 2: Overlay Card
```
┌──────────────────────┐
│                      │
│  [Background Image]  │
│                      │
│  Category Tag        │
│  ▓▓ Title (on image) │
│  ▓▓ gradient overlay │
└──────────────────────┘
```
Text sits on top of the image with a gradient overlay for readability.

### Card Type 3: Pricing Card
```
┌──────────────────────┐
│  Most Popular ★       │ ← highlighted card
│  Pro Plan            │
│  €29 / month         │
│  ─────────────────   │
│  ✓ Feature one       │
│  ✓ Feature two       │
│  ✓ Feature three     │
│  ✗ Enterprise only   │
│  ─────────────────   │
│  [Get Started]       │
└──────────────────────┘
```

### Card Type 4: Testimonial Card
```
┌──────────────────────┐
│  " This is the best  │
│    course I have     │
│    ever taken! "     │
│                      │
│  [Avatar] Name       │
│           @username  │
│  ⭐⭐⭐⭐⭐           │
└──────────────────────┘
```

### Exercises

1. Build each card type on a page showing all 4 variations
2. Overlay card: `position: relative` on card, `position: absolute` for text, gradient `::after` on image
3. Pricing card: the "Most Popular" card should be visually elevated — try `transform: scale(1.05)` or an accent border
4. Testimonial: use `::before` to add a large decorative quotation mark
5. All cards share the same CSS custom properties for colours, radius, and shadow

## Acceptance Criteria

- [ ] All 4 card types are present on the page
- [ ] Overlay card text is readable on any image (gradient ensures contrast)
- [ ] Pricing card "popular" variant is clearly distinguished
- [ ] Testimonial uses proper `<blockquote>` and `<cite>` elements
- [ ] All cards share a consistent design language via CSS custom properties
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: position](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- [MDN: CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [MDN: blockquote element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote)
- [MDN: ::before pseudo-element](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
