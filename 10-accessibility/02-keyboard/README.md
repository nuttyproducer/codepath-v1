# Accessibility — Keyboard Navigation 🟡

**Branch:** `accessibility-keyboard`  
**Prerequisite:** Complete `accessibility-semantic` (Branch 1) first.

## Learning Objectives

- [ ] Navigate any web page using only a keyboard
- [ ] Design visible and beautiful `:focus-visible` styles
- [ ] Implement a skip navigation link
- [ ] Manage `tabindex` correctly
- [ ] Understand and fix tab order problems

## Background

**10% of web users** navigate primarily by keyboard — including people with motor impairments, power users, and screen reader users. Every interactive element must be reachable and usable with Tab, Enter, Space, and arrow keys.

The keyboard navigation contract:
| Key | Expected behaviour |
|---|---|
| `Tab` | Move focus to next interactive element |
| `Shift + Tab` | Move focus to previous interactive element |
| `Enter` | Activate links and buttons |
| `Space` | Activate buttons, toggle checkboxes |
| Arrow keys | Navigate within components (menus, radio groups, tabs) |
| `Escape` | Close modals, menus, dropdowns |

## Task

Take the semantic page from Branch 1 and make it fully keyboard navigable.

### Exercise 1: Skip Navigation Link

Add a "Skip to main content" link as the very first element in `<body>`:
```html
<a href="#main-content" class="skip-link">Skip to main content</a>
```
The skip link should be visually hidden by default but fully visible when focused by keyboard. It should appear at the top of the page with clear styling (background colour, padding, high `z-index`). Research how to use `transform: translateY()` or `position` techniques to show it only on focus.

### Exercise 2: Beautiful Focus Rings

Remove the browser default and build a custom focus ring system:
- Use `:focus-visible` only (not `:focus`, to avoid triggering on mouse click)
- Design a clear, high-contrast ring using `outline` and `outline-offset`
- Dark backgrounds: switch ring to a light colour
- Never use `outline: none` or `outline: 0` without providing an alternative
- Test every element type: `<a>`, `<button>`, `<input>`, `<select>`, `<textarea>`, `<details>`

### Exercise 3: Tab Order Audit

The page contains traps — fix all of them:
- `tabindex="-1"` is used to remove non-interactive elements from tab order
- `tabindex="0"` adds custom interactive elements to the natural tab order
- `tabindex="1"` or higher is FORBIDDEN — it breaks the natural flow (document this rule in a code comment)
- All modal dialog content is focusable when modal is open

Use Chrome DevTools → Accessibility panel → Tab order view to screenshot the correct tab order.

### Exercise 4: Custom Component Keyboard Patterns

Build an accessible **accordion** using only HTML and CSS:
```html
<details>
  <summary>Section 1: What is accessibility?</summary>
  <p>Content here...</p>
</details>
```
- Use `<details>` and `<summary>` — they are keyboard accessible by default
- Style `summary:focus-visible` with your custom focus ring
- Animate open/close with `max-height` transition
- Add `list-style: none` to `summary` and style a custom `▸` / `▾` indicator via `::before`

Also build an accessible **tab interface** (keyboard navigable with arrow keys — note: this one will require a small `onkeydown` attribute hack or acknowledgement that full keyboard arrow navigation requires JavaScript):
- Document in a code comment EXACTLY what JavaScript would need to add for full ARIA tab pattern compliance
- CSS handles all visual states — `:checked` for active tab

## Acceptance Criteria

- [ ] Skip link is present as the first element in `<body>`
- [ ] Skip link is hidden visually but visible on focus (NOT `display: none`)
- [ ] `:focus-visible` rings are applied on ALL interactive elements
- [ ] `outline: none` does not appear anywhere in the CSS without a replacement
- [ ] `tabindex` attributes use only `0` or `-1` (no positive values)
- [ ] Accordion uses `<details>` / `<summary>` with styled focus rings
- [ ] Tab through entire page — every interactive element receives visible focus
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: :focus-visible](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus-visible)
- [MDN: tabindex](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex)
- [WebAIM: Skip navigation links](https://webaim.org/techniques/skipnav/)
- [MDN: details element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
