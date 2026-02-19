# Animation & Transitions — Advanced Animations 🔴

**Branch:** `animations-advanced`  
**Prerequisite:** Complete `animations-complex` (Branch 3) first.

## Learning Objectives

- [ ] Master 3D transforms and `perspective`
- [ ] Animate SVG properties with CSS
- [ ] Create custom `cubic-bezier()` easing curves
- [ ] Build a complete animated UI component library
- [ ] Understand performance: composite layers vs layout thrashing

## Task

Build a **Premium UI Animation Component Library** — a page that demonstrates animations that feel like they belong in a polished production app.

### Exercise 1: Custom Easing Deep Dive

Create a comparison visualiser of easing functions:
- Display 8 boxes, each animating with a different `cubic-bezier()`:
  - `linear` — mechanical
  - `ease` — browser default
  - `ease-in-out` — smooth symmetric
  - `cubic-bezier(0.68, -0.55, 0.265, 1.55)` — overshoot/spring
  - `cubic-bezier(0.23, 1, 0.32, 1)` — expo out (snappy deceleration)
  - `cubic-bezier(0.755, 0.05, 0.855, 0.06)` — expo in (slow then fast)
  - `steps(5, end)` — mechanical steps
  - `steps(1, end)` — instant toggle
- All triggered simultaneously on hover of a "Play" area
- Labels show the easing name below each box

### Exercise 2: 3D Card Flip Interaction

A grid of "flashcard" components with 3D flip. Look into `perspective`, `transform-style: preserve-3d`, `rotateY()`, and `backface-visibility: hidden` to build the flip effect. Use a smooth `cubic-bezier` easing.

Front: question with decorative icon. Back: answer + "Got it ✓" button.

### Exercise 3: SVG Icon Animation System

Create 6 animated icon states — all CSS-driven:
1. **Hamburger → X**: 3 lines morph into an X
2. **Play → Pause**: triangle morphs to two bars
3. **Heart**: fills with colour + scale bounce on click (`:active`)
4. **Loading circle**: `stroke-dasharray` + `stroke-dashoffset` spinning arc
5. **Checkmark**: draws itself with `stroke-dashoffset: 0`
6. **Bell**: rings with `rotate(-15deg)` ↔ `rotate(15deg)` oscillation

Use `<svg>` with inline CSS transitions on SVG attributes.

### Exercise 4: Performance Audit

Research and document in a `PERFORMANCE.md` file:
- What is "composite layer promotion" and why does it matter?
- Which CSS properties trigger layout, paint, and composite?
- Fill in this table for 10 CSS properties:

| Property | Triggers Layout | Triggers Paint | Composite Only |
|---|---|---|---|
| `transform` | No | No | ✅ Yes |
| `opacity` | No | No | ✅ Yes |
| `width` | ... | ... | ... |
| `top` | ... | ... | ... |
| `background-color` | ... | ... | ... |
| `border-radius` | ... | ... | ... |
| `box-shadow` | ... | ... | ... |
| `font-size` | ... | ... | ... |
| `color` | ... | ... | ... |
| `visibility` | ... | ... | ... |

- How do you use Chrome DevTools Performance tab to spot janky animations?
- What is `will-change: transform` and when should you use it (and NOT use it)?

## Acceptance Criteria

- [ ] 8 easing comparison boxes with correct cubic-bezier values
- [ ] 3D card flip works smoothly with `preserve-3d`
- [ ] All 6 SVG icon animations complete with CSS only
- [ ] PERFORMANCE.md table is fully filled in with correct values
- [ ] PERFORMANCE.md explains `will-change` with real examples
- [ ] `@media (prefers-reduced-motion: reduce)` disables all animations
- [ ] Chrome DevTools shows no layout thrashing in Performance trace
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: cubic-bezier()](https://developer.mozilla.org/en-US/docs/Web/CSS/easing-function#cubic_b%C3%A9zier_easing_function)
- [MDN: perspective](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective)
- [MDN: SVG stroke-dashoffset](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/stroke-dashoffset)
- [CSS Triggers — layout/paint/composite reference](https://csstriggers.com/)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
