# Modals & Overlays — Interactive Modals 🟠

**Branch:** `modals-interactive`  
**Prerequisite:** Complete `modals-variations` (Branch 2) first.

## Learning Objectives

- [ ] Build a multi-step wizard inside a modal
- [ ] Create a confirmation dialog with destructive action warning
- [ ] Design toast notification components
- [ ] Use CSS to build an interactive modal with internal tabs
- [ ] Combine multiple overlay techniques into one page

## Task

### Component 1: Multi-step Wizard Modal

A modal with 3 steps — like an onboarding flow:
```
┌────────────────────────────────────┐
│  Step 2 of 3 — Choose your plan   │
│  [──────●────────────○──────────○]│  ← progress dots
│  ──────────────────────────────── │
│  ○ Free    ● Pro    ○ Enterprise  │  ← radio cards
│    €0        €29        €99       │
│  ──────────────────────────────── │
│  [← Back]              [Next →]   │
└────────────────────────────────────┘
```
Use the `:checked` radio technique to control which step is visible. Progress dots fill based on checked state.

### Component 2: Confirmation / Destructive Dialog

```
┌──────────────────────────────────┐
│  ⚠️  Delete Account               │
│  ────────────────────────────── │
│  Are you sure? This action       │
│  cannot be undone. All your      │
│  data will be permanently        │
│  deleted.                        │
│  ────────────────────────────── │
│  [Cancel]      [Delete Account]  │  ← Delete button is RED
└──────────────────────────────────┘
```
The destructive button should have a warning colour (`#dc2626`). The cancel button is secondary style.

### Component 3: Toast Notifications

Toasts pop up in the corner of the screen — triggered by buttons on the page:
- 4 types: `success`, `error`, `warning`, `info`
- Position: fixed top-right
- Slide in from right, auto-dismiss after 4s using `animation-fill-mode: forwards` and `animation-delay`
- Stack: multiple toasts stack vertically with gap

```
                        ┌────────────────────┐
                        │ ✅ Changes saved!  │
                        ├────────────────────┤
                        │ ⚠️ Session expiring │
                        └────────────────────┘
```

### Component 4: Modal with Tabs

Combine modal + tab interface:
- A "User Profile" modal with 3 tabs: Profile, Security, Notifications
- Each tab shows different form fields
- Active tab has accent bottom border
- CSS `:checked` controls which panel shows

## Acceptance Criteria

- [ ] Wizard steps are navigable forward and backward
- [ ] Progress dots reflect current step
- [ ] Destructive confirmation modal has distinct red button
- [ ] 4 toast variants are present and visually distinct
- [ ] Toasts auto-dismiss with CSS animation
- [ ] Modal with tabs switches content correctly
- [ ] All components are keyboard accessible
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: :checked](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked)
- [MDN: animation-fill-mode](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-fill-mode)
- [MDN: position: fixed](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- [MDN: CSS sibling combinators](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_selectors/Selectors_and_combinators)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
