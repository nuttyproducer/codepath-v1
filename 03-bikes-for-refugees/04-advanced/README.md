# Bikes for Refugees — Advanced 🔴

**Branch:** `bikes-for-refugees-advanced`  
**Prerequisite:** Complete `bikes-for-refugees-animations` (Branch 3) first.

## Learning Objectives

- [ ] Implement dark mode using CSS custom properties and `prefers-color-scheme`
- [ ] Build CSS-only interactive components (accordion, multi-step form)
- [ ] Use advanced CSS selectors (`:has()`, `:is()`, `:where()`)
- [ ] Create complex CSS Grid named area layouts
- [ ] Write a print-friendly stylesheet
- [ ] Apply WCAG 2.1 AA accessibility standards

## Task

This is the most challenging branch. You now have a responsive, animated website. The goal is to add **advanced features** that push the limits of what CSS alone can do, while maintaining full accessibility. There is minimal guidance — you will need to problem-solve and research independently.

### Exercise 1) Dark Mode

Implement a complete dark mode that:
- Activates automatically via `@media (prefers-color-scheme: dark)` for users who have dark mode set in their OS
- ALSO provides a manual toggle using a `<input type="checkbox">` in the header — no JavaScript
- All colours switch using CSS custom properties — you only need to redefine `:root` variables
- The toggle must be fully keyboard accessible and labelled correctly

Define a full dark palette. The current palette to invert:
- `--grey-dark: #292b2c` → becomes your light colour in dark mode
- `--grey-light: #e4e4e4` → becomes your dark background
- `--orange-dark: #c05326` → can remain, or adjust for contrast
- `--orange-light: #f7eae4` → needs a dark equivalent

### Exercise 2) CSS-only Accordion FAQ

Add a new FAQ section below the articles. Build the accordion using **only HTML and CSS** (no JavaScript). Requirements:
- At least 5 question/answer pairs
- Only one answer visible at a time (use `:checked` on radio buttons inside the accordion)
- Smooth open/close transition using `max-height` and `overflow: hidden`
- Accessible — use proper heading levels and `<details>`/`<summary>` elements instead of the checkbox trick if you prefer (research both approaches and pick one, explaining your choice in a code comment)
- On mobile: full width. On desktop: 2-column grid of questions

### Exercise 3) Advanced masonry-style Grid

Refactor the "Learn more" articles section to use a **masonry-style grid**:
- Use CSS Grid with `grid-row: span` to create a varied layout where different cards take different heights
- First card spans 2 rows (featured article)
- Remaining cards are single height
- Use `grid-template-areas` with named lines for the outer page layout
- Document your grid structure in a comment above the CSS

### Exercise 4) Donation multi-step form

Add a 3-step donation form to the page using **only HTML and CSS** to manage the steps:
- **Step 1:** Choose donation amount (radio buttons: £5, £10, £25, £50, custom)
- **Step 2:** Enter name and email
- **Step 3:** Confirmation summary and submit button
- Use `:checked` on hidden radio buttons to show/hide each step
- Show a progress bar (3 steps, current step highlighted)
- Each step must be fully accessible with proper labels and fieldsets
- Do NOT use JavaScript

### Exercise 5) Print stylesheet

Add a `@media print` stylesheet that:
- Removes navigation, buttons, sidebar, and animations
- Sets font to a readable serif, black on white
- Ensures images print correctly (no background images)
- Adds the page URL after all links: `a::after { content: " (" attr(href) ")"; }`
- Adds a page break before the footer
- Hides the dark mode toggle

### Bonus: Advanced selectors

Refactor your CSS to use modern selectors where appropriate:
- Use `:is()` to group selectors cleanly
- Use `:where()` for low-specificity utility classes
- Use `:has()` to style a parent based on its children (e.g., style a card differently if it contains an image)

## Acceptance Criteria

- [ ] Dark mode works both automatically (OS preference) and via manual toggle
- [ ] All custom properties switch correctly in dark mode — no hardcoded colours remain
- [ ] CSS-only accordion works with smooth transitions and is accessible
- [ ] Articles section uses named CSS Grid areas with a masonry-style layout
- [ ] Donation form has 3 steps controllable via CSS only (no JavaScript)
- [ ] Progress bar shows current step correctly
- [ ] Print stylesheet produces a clean, readable printed page
- [ ] Lighthouse Accessibility score is 100
- [ ] Lighthouse Best Practices score is 100
- [ ] No JavaScript is used anywhere

## Resources

- [MDN: prefers-color-scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)
- [MDN: CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [CSS-only accordion with details/summary](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details)
- [CSS Grid named areas](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-areas)
- [MDN: :has()](https://developer.mozilla.org/en-US/docs/Web/CSS/:has)
- [Print stylesheets](https://www.smashingmagazine.com/2011/11/how-to-set-up-a-print-style-sheet/)
- [WCAG 2.1 AA Checklist](https://www.w3.org/WAI/WCAG21/quickref/)

💡 **Stuck?** Ask an AI assistant — describe what you’re trying to achieve and let it explain the concept.
