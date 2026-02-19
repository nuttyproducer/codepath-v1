# Modals & Overlays — Modal Variations 🟡

**Branch:** `modals-variations`  
**Prerequisite:** Complete `modals-basic` (Branch 1) first.

## Learning Objectives

- [ ] Create different modal sizes and positions
- [ ] Build a slide-in drawer from any edge
- [ ] Implement an image lightbox
- [ ] Use CSS `max-height` and `overflow-y` for scrollable modals
- [ ] Build a bottom sheet (mobile pattern)

## Task

Build a showcase page demonstrating 4 modal/overlay patterns.

### Pattern 1: Sized Modals
Three trigger buttons: Small, Medium, Large modal. All use the same `<dialog>` base component with modifier classes:
- `.modal--sm`: `max-width: 400px`
- `.modal--md`: `max-width: 600px` (default)
- `.modal--lg`: `max-width: 900px`, two-column layout inside

### Pattern 2: Slide-in Drawer
A panel that slides in from the **right side** — common for shopping carts, sidebars, and settings:
```
┌───────────────────────────────────┬──────────────────┐
│                                   │  DRAWER          │
│  Main page content                │  ─────────────── │
│                                   │  Content here    │
│                                   │  More content    │
│                                   │                  │
│                                   │  [Close ✕]       │
└───────────────────────────────────┴──────────────────┘
```
The drawer slides in from `translateX(100%)` to `translateX(0)` with a `0.3s` transition. Use `position: fixed`, `right: 0`, `height: 100vh`.

### Pattern 3: Image Lightbox

A grid of 6 thumbnail images. Clicking any thumbnail opens a full-screen lightbox:
- Dark backdrop
- Large image centered
- Caption below the image
- Previous/Next arrows (visual — use CSS `:target` for navigation if you want the challenge)
- Close button top-right

### Pattern 4: Bottom Sheet (Mobile)

A modal that appears from the **bottom** of the screen — standard on mobile:
- On mobile (≤640px): slides up from bottom, `border-radius` on top corners only, `max-height: 80vh`, scrollable
- On desktop: becomes a standard centered modal
- Has a drag handle indicator (short grey pill at the top)

## Acceptance Criteria

- [ ] All 4 patterns are on a single showcase page
- [ ] Sized modals work with modifier classes
- [ ] Drawer slides in from right with smooth transition
- [ ] Lightbox shows full-size image with caption
- [ ] Bottom sheet appears from bottom on mobile, center on desktop
- [ ] All modals have a close mechanism (button and/or clicking backdrop)
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: dialog element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)
- [MDN: position: fixed](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- [MDN: transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)
- [MDN: max-height](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
