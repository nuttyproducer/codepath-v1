# Animation & Transitions — CSS Keyframe Animations 🟡

**Branch:** `animations-keyframes`  
**Prerequisite:** Complete `animations-transitions` (Branch 1) first.

## Learning Objectives

- [ ] Write `@keyframes` rules with multiple steps
- [ ] Understand all `animation-*` properties
- [ ] Build loading spinners and skeleton screens
- [ ] Create looping animations (pulse, bounce, ping)
- [ ] Use `animation-fill-mode` to control before/after state

## Background

Where **transitions** react to state changes, **keyframe animations** run independently on a schedule. They repeat, delay, and play forwards or backwards.

`@keyframes` rules let you define multiple steps (using percentages like `0%`, `50%`, `100%` or keywords like `from` / `to`) for an animation. The `animation` property then applies the keyframe by name, along with duration, easing, and fill-mode settings.

## Task

Build a **Loading States & Animations Library** page — a showcase of all the components web apps use for loading and feedback states.

### Exercise 1: Loading Spinners

Create 4 spinner variants using only CSS:
1. **Classic circle**: `border-radius: 50%`, one coloured border segment, `animation: spin 1s linear infinite`
2. **Dots**: 3 circles that bounce in sequence using `animation-delay`
3. **Bars**: 5 vertical bars that grow/shrink in a wave with staggered delay
4. **Ping**: a solid circle that pulses outward like a radar ping

```
  ◐   •••   ▁▃▅▇▅   ◎
  spinner dots bars  ping
```

### Exercise 2: Skeleton Loading Screens

Build skeleton screens for:
1. A blog post card (image placeholder, title line, 3 text lines, button)
2. A user profile header (avatar circle, name line, two stat boxes)

The shimmer effect uses an animated `background-position` on a `linear-gradient` to create a sweeping highlight across the placeholder. Research how to combine `background-size` and `animation` to achieve this.

```
  [====shimmer====] ← sweeping highlight across placeholder
```

### Exercise 3: Entrance Animations

An "Articles" section where 6 cards animate in when the page loads:
- Cards use `@keyframes fadeSlideUp` (opacity 0→1 + translateY 20px→0)
- Each card delays 100ms more than the last (stagger using `:nth-child()` selectors)
- Cards only animate ONCE using `animation-fill-mode: forwards`
- Add `animation-play-state: paused` by default, only play on `:hover` of the container (fun bonus challenge)

### Exercise 4: Notification / Alert Badges

Animated badges and indicators:
1. **New message badge**: number badge that pulses with a `ping` animation when count > 0
2. **Live indicator**: green dot + ripple effect indicating "live" / "online"
3. **Processing bar**: horizontal indeterminate progress bar (unknown duration — travels side to side)
4. **Success checkmark**: checkmark that draws itself using `stroke-dashoffset` animation on an SVG `<path>`

## Acceptance Criteria

- [ ] 4 distinct spinner variants using only CSS
- [ ] 2 skeleton screen components with shimmer
- [ ] 6 staggered entrance animation cards
- [ ] All 4 notification badge/indicator styles present
- [ ] `@media (prefers-reduced-motion: reduce)` disables all animations
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: @keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes)
- [MDN: animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)
- [MDN: animation-delay](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-delay)
- [MDN: animation-fill-mode](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-fill-mode)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
