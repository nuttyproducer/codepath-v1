# Form Controls — Advanced Inputs 🟡

**Branch:** `form-controls-advanced`  
**Prerequisite:** Complete `form-controls` (Branch 1) first.

## Learning Objectives

- [ ] Use advanced HTML input types (`date`, `range`, `file`, `color`, `tel`)
- [ ] Style native form controls with CSS
- [ ] Apply CSS pseudo-classes for validation states (`:valid`, `:invalid`, `:focus-within`)
- [ ] Create accessible custom checkboxes and radio buttons
- [ ] Use CSS Grid for structured form layouts
- [ ] Provide visual feedback for all interaction states

## Task

You have a basic working form. Now you will expand it significantly with more input types, better visual design, and richer user feedback — all using HTML and CSS only.

### Exercise 1) Extend the form with new input types

Add the following fields to your t-shirt order form:
- **Phone number** — `type="tel"` with a `pattern` for Belgian phone numbers (+32 or 04xx)
- **Delivery date** — `type="date"` with `min` set to today and `max` set to 30 days from now
- **Gift message** — `<textarea>` with `maxlength="200"` and `rows="4"`
- **Quantity** — `type="number"` with `min="1"`, `max="10"`, `step="1"`
- **T-shirt fit** — `type="range"` with labels from "Slim" to "Relaxed" (5 steps)

All new fields must be required where it makes sense, and all must have proper labels.

### Exercise 2) Custom checkboxes and radio buttons

The default browser checkboxes and radio buttons look different in every browser. Style them consistently:
- Visually **hide** the native input (`appearance: none` or `opacity: 0` + `position: absolute`)
- Create a custom styled element using `::before` or a sibling element
- On `:checked` state, show a checkmark or fill the circle
- On `:focus-visible`, show a clear outline (don't remove focus styles!)
- The hit area must be at least 44px × 44px (WCAG touch target)

### Exercise 3) Validation state styling

Style the form fields to give instant visual feedback:
- `:invalid` — red border + icon in the input (use `background-image` with an SVG icon)
- `:valid` — green border + checkmark icon
- `:focus-within` on a field wrapper — highlight the entire label/input group
- `:placeholder-shown` — style fields differently when they haven't been touched yet (combine with `:not(:placeholder-shown):invalid` to only show errors after user interaction)
- Required fields should have a visual indicator (but not just `*` alone — pair it with `aria-required`)

### Exercise 4) CSS Grid form layout

Restructure the form layout using CSS Grid:
- Mobile: single column
- Tablet+: two columns, with some fields spanning the full width (e.g., gift message, submit button)
- Group related fields visually with spacing and dividers
- Create a proper form header with title and required fields note

### Exercise 5) Character counter for textarea

Using only CSS, create a visual progress indicator for the gift message textarea:
- The `maxlength` is 200 characters
- Style the textarea border to change colour as it approaches the limit
- Use `outline` and `box-shadow` changes to indicate warning (160+) and danger (190+) states
- Note: A true live counter requires JavaScript. For now, style the states as distinct CSS classes (`.counter--warning`, `.counter--danger`) and document that JavaScript would toggle these classes

## Acceptance Criteria

- [ ] All 5 new input types are present and functional
- [ ] All inputs have associated labels and are accessible
- [ ] Custom checkboxes and radio buttons are visually consistent across browsers
- [ ] Custom controls are keyboard navigable with visible focus states
- [ ] Touch targets are at least 44×44px
- [ ] Validation states (:valid/:invalid) are styled clearly and helpfully
- [ ] Errors only show after user interaction (not on page load)
- [ ] Form uses CSS Grid layout (single column mobile, two column tablet+)
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: Input types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
- [MDN: :valid and :invalid](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid)
- [MDN: :focus-within](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus-within)
- [MDN: :placeholder-shown](https://developer.mozilla.org/en-US/docs/Web/CSS/:placeholder-shown)
- [Styling custom checkboxes](https://css-tricks.com/the-checkbox-hack/)
- [WCAG touch target size](https://www.w3.org/WAI/WCAG21/Understanding/target-size.html)

💡 **Stuck?** Ask an AI assistant — describe what you’re trying to achieve and let it explain the concept.
