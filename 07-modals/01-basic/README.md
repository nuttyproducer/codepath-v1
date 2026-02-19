# Modals & Overlays — Simple Modal 🟢

**Branch:** `modals-basic`

## Learning Objectives

- [ ] Understand the `<dialog>` HTML element
- [ ] Build a modal with proper overlay backdrop
- [ ] Centre content using CSS Grid or Flexbox
- [ ] Create a close button with correct accessibility
- [ ] Use `::backdrop` pseudo-element for the overlay

## Task

Build a modal that opens when a button is clicked — using the native `<dialog>` element (HTML-only, no JavaScript required for the basic open/close with `autofocus`).

```
                    ┌──────────────────────┐
  ░░░░░░░░░░░░░░░░░ │  Modal Title         │ ░░░
  ░░░░░░░░░░░░░░░░░ │  ──────────────────  │ ░░░
  ░░░ backdrop ░░░░ │  Content goes here.  │ ░░░
  ░░░░░░░░░░░░░░░░░ │  This is the modal   │ ░░░
  ░░░░░░░░░░░░░░░░░ │  body area.          │ ░░░
  ░░░░░░░░░░░░░░░░░ │  ──────────────────  │ ░░░
  ░░░░░░░░░░░░░░░░░ │  [Cancel]  [Confirm] │ ░░░
  ░░░░░░░░░░░░░░░░░ └──────────────────────┘ ░░░
```

### Exercises

1. Use `<dialog>` with `open` attribute. Clicking a "Open Modal" button adds/removes `open` (you may use a tiny inline `onclick` attribute for this — it is one of the few acceptable uses before learning JavaScript)
2. Style `::backdrop` for the overlay: `background: rgba(0,0,0,0.5)` with a `backdrop-filter: blur(4px)` effect
3. Animate the modal in: `@keyframes` from `opacity: 0; translateY(-20px)` to normal
4. Create a proper header, body, and footer inside the modal with clear visual separation
5. The modal must be centered — `<dialog>` centers itself by default, but verify and style it

## Acceptance Criteria

- [ ] `<dialog>` element is used (not a `<div>` pretending to be a modal)
- [ ] `::backdrop` is styled with blur effect
- [ ] Modal animates in on open
- [ ] Footer has Cancel and Confirm buttons
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: dialog element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)
- [MDN: ::backdrop](https://developer.mozilla.org/en-US/docs/Web/CSS/::backdrop)
- [MDN: @keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes)
- [MDN: backdrop-filter](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
