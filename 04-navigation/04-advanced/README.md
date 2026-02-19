# Navigation — Complex Navigation System 🔴

**Branch:** `navigation-advanced`  
**Prerequisite:** Complete `navigation-mobile-menu` (Branch 3) first.

## Learning Objectives

- [ ] Combine mega menu, mobile menu, and advanced features into one system
- [ ] Add a functional site search bar with expand/collapse animation
- [ ] Build a multi-level sidebar navigation (for a docs-style site)
- [ ] Implement breadcrumb, pagination, and in-page anchor navigation
- [ ] Apply full keyboard and screen reader support across all nav components

## The Design

Build a complete documentation site navigation system including:

**Top navigation:**
```
┌──────────────────────────────────────────────────────────────┐
│ [Logo] Docs ▾  Guide ▾  API ▾  Blog    [🔍] [v2.0 ▾] [☰]  │
└──────────────────────────────────────────────────────────────┘
```

**Sidebar (docs-style):**
```
┌─────────────────┐
│ Getting Started │ ← section header
│   ├ Introduction│ ← active
│   ├ Installation│
│   └ Quick Start │
│ Core Concepts   │ ← collapsed section (click to expand)
│   ▶ ...         │
│ API Reference   │
│   ▶ ...         │
└─────────────────┘
```

**In-page navigation:**
```
On the right side:
  On this page:
  • Introduction
  • Installation
  • Configuration
  • Examples         ← current position highlighted
  • FAQ
```

### Exercises

1. **Search bar:** Hidden by default, expands on click (CSS `:focus-within` on wrapper). Animate width from `0` to `300px`
2. **Sidebar accordion:** Multi-level collapsible sections using `<details>`/`<summary>` — nested up to 2 levels
3. **Sidebar active state:** Current page link highlighted, parent section automatically expanded
4. **In-page nav:** Fixed to the right, links to `<h2>` anchors on the page, active section highlighted as user scrolls (CSS only approximation using `:target`)
5. **Breadcrumb + pagination:** Complete navigation ecosystem at the bottom of the content area

## Acceptance Criteria

- [ ] All navigation components work together as a cohesive system
- [ ] Search bar expands and collapses with smooth animation
- [ ] Sidebar accordion works with nested levels — CSS/HTML only
- [ ] Active states are clear at every level of navigation
- [ ] Keyboard navigation works across all components
- [ ] All ARIA attributes are correct (aria-expanded, aria-current, aria-label)
- [ ] Lighthouse Accessibility score is 100
- [ ] Lighthouse Best Practices score is 100

## Resources

- [MDN: details element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details)
- [MDN: :focus-within](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus-within)
- [ARIA: aria-expanded](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-expanded)
- [MDN: :target](https://developer.mozilla.org/en-US/docs/Web/CSS/:target)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
