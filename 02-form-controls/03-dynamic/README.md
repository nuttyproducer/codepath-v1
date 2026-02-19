# Form Controls — Dynamic Interactions 🟠

**Branch:** `form-controls-dynamic`  
**Prerequisite:** Complete `form-controls-advanced` (Branch 2) first.

## Learning Objectives

- [ ] Use CSS `:checked` and sibling combinators for conditional display
- [ ] Create interactive UI components using CSS only
- [ ] Build a star rating widget with accessible markup
- [ ] Implement progressive disclosure (show/hide fields)
- [ ] Use CSS counters for numbering
- [ ] Understand the limits of CSS-only interactivity and when JavaScript is needed

## Task

This branch pushes CSS to its limits. You will use the `:checked` pseudo-class combined with sibling combinators (`~`, `+`) to create conditional interfaces — all without a single line of JavaScript. Think carefully about HTML structure, because CSS can only look **forward** through siblings, never backwards.

### Exercise 1) Show/hide dependent fields

The order form should show extra fields based on user selections:
- If the user selects "This is a gift" checkbox → show an additional "Recipient name" field below
- If the user selects colour "Custom" (add this option) → show a colour picker field (`type="color"`)
- If quantity is set to more than 1 → show a "Split delivery?" checkbox

**Key insight:** Your hidden input must come **before** the element you want to show/hide in the HTML. The CSS sibling selector `~` only looks forward, never backwards. Research how to use `:checked` with sibling combinators to reveal hidden elements.

### Exercise 2) Live order summary

Build a sidebar panel showing an order summary that updates based on selections:
- Show the selected colour name (use `:checked` + `::before` content on the label)
- Show the selected size
- Create colour swatch indicators — coloured circles that show based on which radio is checked
- Use CSS custom properties and `:checked` selectors to update the summary panel

This requires careful HTML ordering — plan your structure before you start coding.

### Exercise 3) Star rating widget

Create a 5-star rating component for "How did you hear about us?":
- 5 radio inputs (value 1-5), but display them as stars (★)
- Stars fill from left-to-right using the general sibling combinator
- On hover, all stars up to the hovered one should highlight
- The selected rating should persist (`:checked` state)
- The component must be fully keyboard accessible
- Clicking a label selects that rating

**Challenge:** The stars must go **right to left** in HTML but display left to right — research the `direction: rtl` trick or `flex-direction: row-reverse`.

### Exercise 4) Promo code field with validation

Add a promo code section:
- A text input for a promo code
- Use `pattern="[A-Z]{4}[0-9]{2}"` (e.g., "BIKE25") for validation
- When `:valid`, show a green success message using `::after` on the wrapper
- When `:invalid` and `:not(:placeholder-shown)`, show an error message
- Show a fake "10% discount applied!" message when the pattern matches

### Exercise 5) Multi-section form with step indicators

Reorganise the form into sections with a visual stepper:
- Use CSS to highlight the current active section using the `:focus-within` pseudo-class on each `<fieldset>`
- Create a fixed stepper navigation at the top showing: Personal → Product → Delivery → Review
- The active section's step indicator should be highlighted when any field inside it is focused
- Do NOT break the form into multiple pages (keep it a single scrolling form) — just provide visual tracking

## Acceptance Criteria

- [ ] Gift recipient field appears only when "is a gift" is checked
- [ ] Custom colour picker appears only when "Custom" colour is selected
- [ ] Order summary panel reflects selections (colour swatch, size display)
- [ ] Star rating works correctly — hover highlights, click selects, keyboard navigable
- [ ] Promo code shows success/error messages via CSS pseudo-elements
- [ ] Form sections have visual step indicator that highlights on focus
- [ ] No JavaScript is used anywhere
- [ ] All interactive elements are keyboard accessible
- [ ] Lighthouse Accessibility score is 100

## Resources

- [CSS :checked selector](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked)
- [CSS Combinators (~ and +)](https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_combinator)
- [CSS-only star rating](https://css-tricks.com/star-ratings/)
- [MDN: ::before and ::after](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)
- [CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [The :focus-within pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus-within)

💡 **Stuck?** Ask an AI assistant — describe what you’re trying to achieve and let it explain the concept.
