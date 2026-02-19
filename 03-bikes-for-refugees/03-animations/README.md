# Bikes for Refugees — Animations 🟠

**Branch:** `bikes-for-refugees-animations`  
**Prerequisite:** Complete `bikes-for-refugees-responsive` (Branch 2) first.

## Learning Objectives

- [ ] Write `@keyframes` animations from scratch
- [ ] Control animation with `timing-function`, `duration`, `delay`, `iteration-count`
- [ ] Use `transition` for interactive hover and focus effects
- [ ] Apply `transform` (translate, scale, rotate) for smooth movement
- [ ] Use CSS custom properties inside animations
- [ ] Respect user preferences with `prefers-reduced-motion`

## Task

The website is now responsive. It's time to bring it to life with **animations and transitions**. Every animation must serve a purpose — it should guide the user's attention, provide feedback, or communicate something meaningful. Avoid animations just for decoration.

### Exercise 1) Button transitions

Add smooth transitions to all buttons on the page:
- Smoothly transition `background-color`, `color`, `transform`, and `box-shadow` on hover and focus
- On hover: the button should lift slightly (`translateY(-2px)`) and deepen its shadow
- On click (`:active`): the button should press down slightly (`translateY(1px)`)
- Timing: `0.2s ease` feels natural — experiment and explain your choice

### Exercise 2) Navigation link underline animation

Replace the static hover style on nav links with an **animated underline**:
- Use `::after` pseudo-element as the underline
- On hover, animate it from `width: 0` to `width: 100%`
- The underline should slide in from left to right
- Use `transition` — no `@keyframes` needed here

### Exercise 3) Card entrance animation

When the page loads, the article cards should animate into view:
- Start: `opacity: 0` and `translateY(20px)` (below their final position)
- End: `opacity: 1` and `translateY(0)` (normal position)
- Stagger each card with `animation-delay` (0s, 0.1s, 0.2s, 0.3s...)
- Use `@keyframes fadeInUp` for this

### Exercise 4) Statistics counter animation

In the alert bar there is a number (`72`). Make it count up from `0` to `72` on page load using only CSS:
- Use `@keyframes` with CSS counters
- This is a hard CSS-only challenge — research `counter-increment` in animations
- The number should animate over `2s` with `steps()` timing

### Exercise 5) Skeleton loading state

Create a **skeleton loading placeholder** for the sidebar articles using CSS only:
- Create a pulsing grey block effect that mimics text and image placeholders
- Use `@keyframes` to animate a shimmer gradient from left to right
- Apply to a class `skeleton` that can be toggled (leave the real content in place, add skeleton divs above it and hide real content with CSS for demo purposes)

### Bonus: Respect reduced motion

Wrap all your animations in a `@media (prefers-reduced-motion: no-preference)` query. This ensures animations don’t cause discomfort for users who have requested reduced motion in their OS settings.

## Acceptance Criteria

- [ ] All buttons have smooth hover and active transitions
- [ ] Nav links have an animated underline on hover
- [ ] Article cards animate in on page load with staggered delays
- [ ] The statistics number in the alert has a CSS count-up animation
- [ ] A skeleton loading state is created using CSS animations
- [ ] All animations are wrapped in `prefers-reduced-motion` query
- [ ] No animation lasts longer than 0.5s (except count-up) — keeps UX snappy
- [ ] Lighthouse Accessibility score is still 100

## Resources

- [MDN: @keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes)
- [MDN: CSS Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_transitions/Using_CSS_transitions)
- [MDN: transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)
- [CSS Skeleton Loading](https://css-tricks.com/building-skeleton-screens-css-custom-properties/)
- [prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)
- [CSS animation-delay for stagger](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-delay)

💡 **Stuck?** Ask an AI assistant — describe what you’re trying to achieve and let it explain the concept.
