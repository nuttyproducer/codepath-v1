# Accessibility — ARIA Attributes 🟠

**Branch:** `accessibility-aria`  
**Prerequisite:** Complete `accessibility-keyboard` (Branch 2) first.

## Learning Objectives

- [ ] Understand when to use ARIA and when NOT to (first rule of ARIA)
- [ ] Use `aria-label`, `aria-labelledby`, and `aria-describedby` correctly
- [ ] Implement `aria-expanded`, `aria-hidden`, and `aria-current`
- [ ] Create live regions with `aria-live` and `aria-atomic`
- [ ] Use ARIA roles to correct semantic meaning

## Background

**The first rule of ARIA:**  
> *"If you can use a native HTML element or attribute with the semantics and behaviour you require already built in, instead of re-purposing an element and adding an ARIA role, state or property to make it accessible, then do so."*

ARIA is for **filling gaps** in HTML's semantics — not replacing them.

```
❌ <div role="button" tabindex="0" onclick="...">Click me</div>
✅ <button type="button">Click me</button>
```

## Task

Build an **ARIA Showcase** — a page demonstrating the correct use of ARIA in real UI patterns.

### Exercise 1: Labelling

Three examples of correct labelling:

**1. Icon-only button:**
```html
<!-- The icon provides no text — ARIA label is essential -->
<button aria-label="Close dialog">
  <svg aria-hidden="true" ...>✕</svg>
</button>
```

**2. Input with visible label:**
```html
<!-- Use <label> — not aria-label — when a visible label exists -->
<label for="email">Email address</label>
<input id="email" type="email" aria-describedby="email-hint">
<p id="email-hint">We'll never share your email.</p>
```

**3. Sectioned landmarks:**
```html
<!-- Multiple navs need aria-label to distinguish them -->
<nav aria-label="Main navigation"> ... </nav>
<nav aria-label="Breadcrumb"> ... </nav>
```

### Exercise 2: Dynamic States

Implement `aria-expanded` on a dropdown:
```html
<button aria-expanded="false" aria-controls="dropdown-menu">
  Options
</button>
<ul id="dropdown-menu" hidden>...</ul>
```
Use a CSS `[aria-expanded="true"] + ul { display: block; }` selector alongside a checkbox trick. The `aria-expanded` attribute should change in tandem with the checkbox state using a CSS sibling label approach and a tiny inline attribute update note (document that full dynamic ARIA requires JavaScript).

### Exercise 3: Live Regions

Build a **form with live validation feedback**:
```html
<div aria-live="polite" aria-atomic="true" id="status-message" role="status">
  <!-- Status messages are injected here by JavaScript -->
</div>
```
Since we are CSS-only, instead demonstrate:
- A CSS-only character counter using CSS Grid trick with custom properties
- An error state that appears via `:invalid` and is announced via `role="alert"` on the container
- Document in comments what `aria-live="polite"` vs `aria-live="assertive"` means

### Exercise 4: ARIA Roles on Custom Components

The `role` attribute corrects or adds semantic meaning. Demonstrate:
- `role="status"` — for success messages (non-urgent)
- `role="alert"` — for error messages (urgent, interrupts screen reader)
- `role="tooltip"` — on tooltip content
- `role="separator"` — on decorative `<hr>` elements
- `aria-hidden="true"` — on ALL decorative icons, SVGs, and `::before` icons

Create a CSS-only **star rating display** (read-only, not interactive):
```html
<div role="img" aria-label="Rating: 4 out of 5 stars">
  <span aria-hidden="true">★★★★☆</span>
</div>
```

## Acceptance Criteria

- [ ] All icon-only buttons have `aria-label`
- [ ] All decorative SVGs have `aria-hidden="true"`
- [ ] Multiple `<nav>` elements are differentiated with `aria-label`
- [ ] `aria-describedby` is used for at least one form hint
- [ ] `aria-expanded` is present on dropdown toggle button
- [ ] `role="alert"` is on the error message container
- [ ] `role="status"` is on the success message container
- [ ] Star rating uses `role="img"` with descriptive `aria-label`
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: ARIA roles](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles)
- [MDN: aria-label](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-label)
- [MDN: aria-expanded](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-expanded)
- [MDN: aria-live](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-live)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
