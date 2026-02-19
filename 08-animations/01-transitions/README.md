# Animation & Transitions — CSS Transitions 🟢

**Branch:** `animations-transitions`

## Learning Objectives

- [ ] Understand what CSS `transition` property does and when to use it
- [ ] Know the four parts of a transition: `property`, `duration`, `easing`, `delay`
- [ ] Apply transitions to hover, focus, and active states
- [ ] Choose correct easing functions for different types of movement
- [ ] Know which CSS properties can and cannot be transitioned

## Background

A **transition** smoothly animates a CSS property from one value to another when the value changes (on hover, on focus, via class change). It is perfect for small UI state changes.

The `transition` property accepts four parts: the property to animate, the duration, the easing function, and an optional delay. Not all CSS properties can be transitioned — properties like `display` cannot, while `opacity`, `transform`, `color`, and `box-shadow` can. Research which properties animate smoothly for the best results.

## Task

Build a **UI Transitions Showcase** page demonstrating transitions on real UI elements.

### Exercise 1: Button States
Create 5 button variants, each with a distinct transition:
- Primary button: `background-color` change `0.2s ease`
- Ghost button: `border-color` + `color` change
- Icon button: `transform: rotate(90deg)` on hover
- Danger button: `box-shadow` glow on hover (`0 0 0 3px rgba(220,38,38,0.4)`)
- Success button: `background-color` from blue to green on `:active`

### Exercise 2: Card Hover Effects

Four cards in a grid, each with a different hover effect:
1. **Lift**: `transform: translateY(-4px)` + larger `box-shadow`
2. **Glow**: `box-shadow: 0 0 0 2px` accent colour
3. **Zoom image**: image inside zooms `transform: scale(1.05)` — wrap in `overflow: hidden`
4. **Reveal**: initially grey overlay covers card, hover fades it out

### Exercise 3: Navigation Link Underlines

A horizontal nav bar where each link has an animated underline:
- Underline using `::after` pseudo-element with `width: 0` → `width: 100%` on hover
- Two variants: slide from left, slide from centre outward
- Must work with `transition: width 0.3s ease`

### Exercise 4: Form Focus Transitions

An input/form where focus state transitions are smooth:
- `border-color` transition from grey → blue on focus
- `box-shadow` expands on focus (ring effect)
- Label slides up out of the input with `transform: translateY()` (floating label effect)
- Error state: border transitions to red with `background-color` tint

## Acceptance Criteria

- [ ] 5 button variants with distinct transitions
- [ ] 4 card hover effects demonstrating different properties
- [ ] Nav underline animation (both left and centre variants)
- [ ] Form with floating label and focus ring transitions
- [ ] NO animation on users who prefer reduced motion: `@media (prefers-reduced-motion: reduce)`
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: transition](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)
- [MDN: easing functions](https://developer.mozilla.org/en-US/docs/Web/CSS/easing-function)
- [MDN: transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)
- [MDN: prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
