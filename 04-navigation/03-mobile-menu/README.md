# Navigation — Animated Mobile Menu 🟠

**Branch:** `navigation-mobile-menu`  
**Prerequisite:** Complete `navigation-mega-menu` (Branch 2) first.

## Learning Objectives

- [ ] Build a CSS-only hamburger menu animation
- [ ] Implement slide-in navigation panel
- [ ] Create an overlay/backdrop behind an open menu
- [ ] Use CSS to animate the hamburger icon into an X
- [ ] Handle the mobile/desktop switch cleanly with media queries

## The Design

**Closed (mobile):**
```
┌──────────────────────┐
│  [Logo]          [≡] │  ← hamburger icon
└──────────────────────┘
```

**Open (mobile):**
```
┌──────────────────────┐
│  [Logo]          [✕] │  ← transforms to X
│  ─────────────────── │
│  Home                │  ← slides in from right
│  About               │
│  Work                │
│  Blog                │
│  Contact             │
│  [Get in touch]      │
└──────────────────────┘
█████ dark overlay ████
```

### Exercises

1. Use `<input type="checkbox" id="nav-toggle">` + `<label for="nav-toggle">` for the hamburger
2. Animate 3 `<span>` elements inside the label to form the hamburger and transform into X on check
3. Slide the nav panel in from the right using `transform: translateX(100%)` → `translateX(0)`
4. Create the dark overlay with a full-screen `::before` pseudo-element on `body` or the nav toggle — clicking it closes the menu
5. On desktop (≥768px): show standard horizontal navigation, hide hamburger

## Acceptance Criteria

- [ ] Hamburger animates into X when menu opens
- [ ] Nav panel slides in with a smooth transition
- [ ] Overlay appears behind the panel and closes menu when clicked
- [ ] Desktop shows standard navbar with no hamburger icon
- [ ] Toggle is keyboard accessible (can be triggered with Enter/Space)
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: CSS Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_transitions)
- [MDN: transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)
- [MDN: :checked](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked)
- [CSS-only hamburger menu](https://css-tricks.com/the-checkbox-hack/)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
