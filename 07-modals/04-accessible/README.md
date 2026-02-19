# Modals & Overlays — Accessible Modal System 🔴

**Branch:** `modals-accessible`  
**Prerequisite:** Complete `modals-interactive` (Branch 3) first.

## Learning Objectives

- [ ] Implement full WCAG 2.1 AA compliance for all modal patterns
- [ ] Use `<dialog>` correctly with all required ARIA attributes
- [ ] Create visual focus trapping indication (CSS-only preparation for JS)
- [ ] Build a tooltip system with CSS only
- [ ] Document every accessibility decision made

## Task

This branch is about **doing everything right**. Revisit all the modal components from branches 1-3 and apply the full accessibility treatment.

### Exercise 1) Audit and fix all modals

Go through every modal from the previous branches and check:
- [ ] `<dialog>` has `aria-labelledby` pointing to the modal title
- [ ] `<dialog>` has `aria-describedby` pointing to the modal body
- [ ] Close buttons have `aria-label="Close dialog"` (not just "✕")
- [ ] Destructive action buttons have `aria-describedby` pointing to the warning text
- [ ] Wizard steps use `aria-live="polite"` so screen readers announce step changes
- [ ] Every interactive element inside a modal is reachable by Tab key

### Exercise 2) Focus ring system

Create a consistent, beautiful focus ring system:
- All interactive elements: `2px solid` accent colour, `outline-offset: 3px`
- Only visible for keyboard users: use `:focus-visible` (not `:focus`)
- High contrast: the ring must pass 3:1 contrast against any background
- Style differently for different element types (button, input, link, select)

### Exercise 3) CSS-only tooltip system

Create a reusable tooltip component using only CSS:
- Triggered on hover AND focus (accessibility!)
- Content from `data-tooltip="Your text here"` attribute
- Appears above by default, flips below if near top of viewport (use `:focus` positioning)
- Accessible: `role="tooltip"` and `aria-describedby` on the trigger

```html
<button data-tooltip="Delete this item permanently" aria-describedby="tooltip-1">
  🗑️ <span role="tooltip" id="tooltip-1">Delete this item permanently</span>
</button>
```

### Exercise 4) Accessibility documentation

In a `ACCESSIBILITY.md` file inside this folder, document:
- Every ARIA attribute used and why
- Every keyboard interaction supported
- Every colour contrast ratio checked (use the WebAIM Contrast Checker)
- What CSS-only CAN and CANNOT do for accessibility (and where JavaScript is essential)
- Screen reader testing notes (test with NVDA, VoiceOver, or JAWS and document the results)

## Acceptance Criteria

- [ ] All modals from branches 1-3 have been audited and fixed
- [ ] Every `<dialog>` has `aria-labelledby` and `aria-describedby`
- [ ] `:focus-visible` is used everywhere (`:focus` removed)
- [ ] Focus rings pass 3:1 contrast ratio (documented in ACCESSIBILITY.md)
- [ ] Tooltip system works on hover and focus
- [ ] Tooltip uses `role="tooltip"` and `aria-describedby`
- [ ] ACCESSIBILITY.md documents every decision with rationale
- [ ] Lighthouse Accessibility score is 100 on ALL pages

## Resources

- [MDN: aria-labelledby](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby)
- [MDN: :focus-visible](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus-visible)
- [MDN: role=tooltip](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tooltip_role)
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
