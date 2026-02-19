# Navigation — Simple Navbar 🟢

**Branch:** `navigation-navbar`

## Learning Objectives

- [ ] Build a semantic `<nav>` element
- [ ] Style horizontal navigation with Flexbox
- [ ] Implement hover and active link states
- [ ] Integrate a logo alongside navigation
- [ ] Create accessible keyboard-navigable links

## Task

Build a standalone navigation bar component that could be dropped into any website. It must look polished and work on both desktop and mobile.

### The Design

```
┌────────────────────────────────────────────────────┐
│  [Logo]    Home    About    Work    Blog   Contact  │
└────────────────────────────────────────────────────┘
```

- Logo on the left, links on the right
- Active link (current page): visually distinct (bold, accent colour, underline)
- Hover: smooth colour transition
- Full-width with `max-width` container

### Exercises

1. Write semantic HTML: `<header>` > `<nav>` > `<ul>` > `<li>` > `<a>`
2. Use Flexbox to place logo left, links right with `justify-content: space-between`
3. Add `aria-current="page"` to the active link and style it with CSS
4. Create hover underline effect using `::after` pseudo-element (grows from centre)
5. Add a skip link: `<a href="#main" class="skip-link">Skip to main content</a>` — visible only on focus

## Acceptance Criteria

- [ ] Correct semantic HTML structure
- [ ] Logo and links are horizontally aligned
- [ ] Hover transition is smooth (0.2s)
- [ ] Active state is clearly distinct from hover
- [ ] Skip link is present and visible on focus
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: nav element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)
- [aria-current](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-current)
- [Skip navigation links](https://webaim.org/techniques/skipnav/)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
