# Typography & Content — Advanced Typography 🟠

**Branch:** `typography-advanced`  
**Prerequisite:** Complete `typography-rich` (Branch 2) first.

## Learning Objectives

- [ ] Use `clamp()` for fluid, responsive type sizes
- [ ] Create a multi-column text layout
- [ ] Implement OpenType font features (`font-variant-*`, `font-feature-settings`)
- [ ] Use `text-wrap: balance` and `text-wrap: pretty` (modern CSS)
- [ ] Understand vertical rhythm and baseline grids

## Background

**Fluid typography** with `clamp()` allows font sizes to scale smoothly between a minimum and maximum value based on the viewport width. The `clamp(min, preferred, max)` function takes three arguments: the smallest size, a fluid middle value (often expressed with `vw` units), and the largest size. Research the formula for calculating the preferred value from your min/max sizes and viewport range.

## Task

Build an advanced **typography laboratory** page — a place to test and demonstrate cutting-edge CSS typography.

### Exercise 1: Fluid Type Scale

Create a complete fluid type scale using `clamp()` for every heading level. Define each step as a CSS custom property in `:root` with a descriptive name (e.g., `--text-xs` through `--text-4xl`). Show a "resize to see fluid type" demo area on the page.

### Exercise 2: Multi-Column Magazine Layout

A long-form article styled like a magazine:
```
┌──────────────────────────────────────────────────────────┐
│          DROP CAP FIRST LETTER — Full-width headline     │
├──────────────────────────┬───────────────────────────────┤
│  Main text column        │  Sidebar:                     │
│  (spans most width)      │  Pull quote, related links,   │
│  Uses column-count or    │  or advertisement placeholder │
│  CSS Grid                │                               │
├──────────────────────────┴───────────────────────────────┤
│  Full-width image with caption                           │
├────────────┬──────────────────┬──────────────────────────┤
│  Column 1  │    Column 2      │       Column 3           │
│  cont...   │    cont...       │       cont...            │
└────────────┴──────────────────┴──────────────────────────┘
```
Use `column-count: 3`, `column-gap`, `column-rule` for the 3-column section. Use `column-span: all` to let the image break across all columns.

### Exercise 3: OpenType Features

Explore advanced font features on a font that supports them (try: Source Serif 4, Recursive, or Fira Code):
- `font-variant-numeric: oldstyle-nums` — numbers that align with lowercase text
- `font-variant-numeric: tabular-nums` — fixed-width numbers for tables
- `font-variant-ligatures: common-ligatures` — fi, fl, ffi ligatures
- `font-variant-caps: small-caps` — uppercase styled as small caps
- `font-feature-settings: "zero" 1` — slashed zero for clarity

Show a before/after comparison for each feature.

### Exercise 4: Modern Text Wrapping

Demonstrate the new `text-wrap` CSS values:
- `text-wrap: balance` — balances line lengths in headings (no widows)
- `text-wrap: pretty` — avoids orphaned words on last line of body text
- `text-wrap: nowrap` — classic single-line, combined with `overflow: hidden`

Show side-by-side examples of each with and without the property.

Also apply `hyphens: auto` to long-form body text in narrow columns.

## Acceptance Criteria

- [ ] All 8 fluid type scale variables are defined and used
- [ ] Fluid type visibly scales when browser is resized (demonstrate with a resize note)
- [ ] Magazine multi-column layout is present with `column-count` 3-column section
- [ ] `column-span: all` is used for a full-width element inside the multi-column layout
- [ ] At least 3 OpenType font-variant features are demonstrated with before/after
- [ ] `text-wrap: balance` is applied to all headings
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp)
- [MDN: column-count](https://developer.mozilla.org/en-US/docs/Web/CSS/column-count)
- [MDN: font-variant](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant)
- [MDN: text-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/text-wrap)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
