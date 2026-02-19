# Form Controls — Checkout & Mastery 🔴

**Branch:** `form-controls-validation`  
**Prerequisite:** Complete `form-controls-dynamic` (Branch 3) first.

## Learning Objectives

- [ ] Build a complete multi-step checkout form (HTML/CSS only)
- [ ] Implement WCAG 2.1 AA form accessibility fully
- [ ] Use ARIA attributes for error messages and live regions
- [ ] Apply advanced pseudo-classes (`:user-invalid`, `:placeholder-shown`, `:has()`)
- [ ] Create a data summary page using CSS `content` and `attr()`
- [ ] Design conditional required fields and progressive disclosure at scale

## Task

You are building a **complete e-commerce checkout** — the most complex form type on the web. This is a real-world challenge. You must plan the HTML structure first, then implement CSS. There is minimal skeleton provided — you design and build from scratch, informed by everything you've learned in branches 1-3.

### Exercise 1) Full three-section checkout form

Create a form with three sections navigated by CSS (using the `:checked` trick from Branch 3):

**Section 1 — Billing Information:**
- Full name (`autocomplete="billing name"`)
- Email (`autocomplete="email"`)
- Phone (`autocomplete="tel"`)
- Billing address — Street, City, Postcode, Country (`autocomplete` attributes for all)
- "Same as shipping" checkbox — if checked, shipping fields are pre-filled visually (CSS content trick) and the shipping section collapses

**Section 2 — Shipping Information:**
- Delivery method: Standard (free, 5-7 days), Express (€5.99, 1-2 days), Pick-up in store
- If "Pick-up" selected → show store selector dropdown, hide address fields
- If Standard or Express → show address fields (pre-filled from billing if "same" checked)
- Preferred delivery date (`type="date"`)

**Section 3 — Review & Pay:**
- Read-only summary of all entered information (use `readonly` inputs or CSS `content: attr()` trick)
- Order total display with breakdown
- Terms and conditions checkbox (required)
- Newsletter opt-in checkbox (optional)
- Submit button (disabled visually until Terms are accepted — CSS `:has()` trick)

### Exercise 2) Progress bar and section navigation

- Fixed progress bar at the top: `Billing (1) → Shipping (2) → Review (3)`
- Active section highlighted, completed sections marked with ✓
- "Next" and "Back" navigation between sections using CSS `:checked` trick
- Progress bar segments fill as user moves forward

### Exercise 3) Complete WCAG 2.1 AA compliance

For every single form field:
- `aria-required="true"` on all required inputs
- `aria-describedby` linking to both the hint text AND the error message
- Error messages use `role="alert"` so screen readers announce them
- All error messages are visible as CSS-generated text on `:invalid` state
- Every `<fieldset>` has a descriptive `<legend>`
- All interactive elements have `:focus-visible` styles that meet 3:1 contrast ratio
- Colour is never the only means of conveying information (pair with icons or text)

### Exercise 4) Advanced pseudo-class validation

Use the most modern CSS validation tools:
- `:user-invalid` — only shows invalid styling after the user has interacted (better than combining `:invalid` + `:not(:placeholder-shown)`)
- `:user-valid` — shows success styling after valid interaction
- `:has(:user-invalid)` on a fieldset — highlight the entire section if it contains an invalid field
- `:has(input:checked[value="pickup"])` — target the shipping section based on delivery selection

### Exercise 5) Submission disabled state

The submit button must be visually disabled until terms are accepted. Use `form:not(:has(#terms:checked))` to target the submit button when the terms checkbox is unchecked. Also disable the button if any required field is `:invalid`.

Research how `pointer-events: none` and `cursor: not-allowed` combine with `opacity` to communicate a disabled state.

## Acceptance Criteria

- [ ] Three-section checkout form works with CSS-only section switching
- [ ] "Same as billing" correctly collapses shipping address section
- [ ] Delivery method selection shows/hides relevant fields
- [ ] Progress bar accurately reflects the active section
- [ ] Every field has `aria-required`, `aria-describedby` to hint and error
- [ ] Error messages use `role="alert"` and are announced properly
- [ ] `:user-invalid` is used instead of `:invalid` + `:not(:placeholder-shown)`
- [ ] Submit button is visually disabled until terms accepted and form is valid
- [ ] All focus styles meet WCAG 2.1 AA contrast ratio
- [ ] No colour-only information (all status indicators have icons or text too)
- [ ] Lighthouse Accessibility score is 100
- [ ] No JavaScript is used anywhere

## Resources

- [MDN: :user-invalid](https://developer.mozilla.org/en-US/docs/Web/CSS/:user-invalid)
- [MDN: :has()](https://developer.mozilla.org/en-US/docs/Web/CSS/:has)
- [ARIA in forms](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/forms)
- [WCAG 2.1 — Understanding Forms](https://www.w3.org/WAI/tutorials/forms/)
- [autocomplete attribute values](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete)
- [Accessible form validation patterns](https://www.smashingmagazine.com/2023/02/guide-accessible-form-validation/)

💡 **Stuck?** Ask an AI assistant — describe what you’re trying to achieve and let it explain the concept.
