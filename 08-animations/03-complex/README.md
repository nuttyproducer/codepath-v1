# Animation & Transitions — Complex Animations 🟠

**Branch:** `animations-complex`  
**Prerequisite:** Complete `animations-keyframes` (Branch 2) first.

## Learning Objectives

- [ ] Chain multiple animations on a single element
- [ ] Animate along a path using `offset-path` / `motion-path`
- [ ] Create parallax scroll effects with CSS only
- [ ] Use `@scroll-timeline` / `animation-timeline: scroll()` (modern CSS)
- [ ] Build sequential multi-element choreographed animations

## Task

Build an **interactive animation showcase** — a landing page hero section with rich animated content.

### Exercise 1: Hero Section Choreography

A hero section where elements animate in as a sequence:
```
t=0.0s → background gradient fades in
t=0.2s → headline slides up
t=0.4s → subheadline slides up  
t=0.6s → CTA button pops in with bounce
t=0.8s → decorative circles appear with ping
t=1.0s → scroll indicator bounces
```
Each element has its own `@keyframes` and uses `animation-delay` to create the chain.

### Exercise 2: Animated Statistics Counter

```
  0 → 1,247        0 → 98%         0 → 4.9★
  Students          Satisfaction     Rating
```
Use `@keyframes` with CSS custom properties to count numbers up. Research the `@property` (Houdini) API which allows animating custom properties — this lets you animate an integer value and display it with `counter()`. Note: document browser support in a code comment.

### Exercise 3: Parallax Hero with CSS

A hero with layered background elements that move at different speeds using CSS `perspective` and `translateZ`:
- Background mountains: `translateZ(-2px) scale(3)` — moves slowest
- Midground trees: `translateZ(-1px) scale(2)` — moves medium
- Foreground text: no transform — moves at scroll speed

Use the `perspective` on the scroll container and `transform-style: preserve-3d` on children.

### Exercise 4: CSS Scroll-Driven Animation (Modern CSS)

Use the modern `animation-timeline: scroll()` or `animation-timeline: view()` to animate elements as the user scrolls. Research the `animation-range` property for controlling when in the scroll the animation runs. Document browser support and provide a `@supports` fallback that makes elements fully visible.

## Acceptance Criteria

- [ ] Hero choreography plays in correct sequence with correct timing
- [ ] Stats counter animates from 0 to final value on page load
- [ ] CSS parallax is present with at least 3 depth layers
- [ ] Scroll-driven animation works in supported browsers
- [ ] `@supports` fallback ensures full visibility in unsupported browsers
- [ ] `@media (prefers-reduced-motion: reduce)` disables all motion
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: animation-delay](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-delay)
- [MDN: @property](https://developer.mozilla.org/en-US/docs/Web/CSS/@property)
- [MDN: animation-timeline](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-timeline)
- [MDN: @supports](https://developer.mozilla.org/en-US/docs/Web/CSS/@supports)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
