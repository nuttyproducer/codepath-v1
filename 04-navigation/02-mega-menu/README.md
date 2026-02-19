# Navigation — Mega Menu 🟡

**Branch:** `navigation-mega-menu`  
**Prerequisite:** Complete `navigation-navbar` (Branch 1) first.

## Learning Objectives

- [ ] Build a multi-level dropdown menu
- [ ] Use CSS Grid inside a mega menu
- [ ] Position dropdowns correctly with `position: absolute/relative`
- [ ] Implement hover-triggered dropdowns with accessible focus management
- [ ] Create visual groupings within a dropdown

## The Design

```
┌──────────────────────────────────────────────────────────┐
│  [Logo]   Home   Products ▾   Resources ▾   Contact     │
└──────────────────────────────────────────────────────────┘
                    │
         ┌──────────▼──────────────────────────────────┐
         │  PRODUCTS MEGA MENU (Grid: 3 columns)        │
         │  ┌────────────┐ ┌────────────┐ ┌──────────┐ │
         │  │ 🖥 Software │ │ 📱 Mobile  │ │ 🎓 Learn │ │
         │  │ App 1      │ │ iOS App    │ │ Docs     │ │
         │  │ App 2      │ │ Android    │ │ Tutorials│ │
         │  │ App 3      │ │ PWA Guide  │ │ Blog     │ │
         │  └────────────┘ └────────────┘ └──────────┘ │
         │  ──────────────────────────────────────────  │
         │  Featured: [Banner image + CTA button]       │
         └─────────────────────────────────────────────┘
```

### Exercises

1. Build the dropdown using `position: relative` on the nav item and `position: absolute` on the dropdown panel
2. Show/hide with CSS `visibility: hidden / opacity: 0` + transition (NOT `display: none` — why?)
3. Use CSS Grid with 3 columns inside the mega menu
4. Add a featured banner at the bottom of the dropdown
5. Make it keyboard accessible: dropdown opens on `:focus-within`, not just `:hover`

## Acceptance Criteria

- [ ] Dropdowns open on hover AND on keyboard focus
- [ ] Dropdown uses CSS Grid layout
- [ ] Transition is smooth (opacity + visibility trick)
- [ ] Dropdown closes when focus leaves it
- [ ] ARIA attributes: `aria-haspopup="true"`, `aria-expanded` (CSS-driven with `:focus-within`)
- [ ] Lighthouse Accessibility score is 100

## Resources

- [CSS dropdown menus](https://css-tricks.com/solved-with-css-dropdown-menus/)
- [visibility vs display none](https://css-tricks.com/css-tricks-almanac/properties/v/visibility/)
- [accessible dropdown navigation](https://www.w3.org/WAI/tutorials/menus/flyout/)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
