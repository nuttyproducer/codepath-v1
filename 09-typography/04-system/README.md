# Typography & Content — Typography Design System 🔴

**Branch:** `typography-system`  
**Prerequisite:** Complete `typography-advanced` (Branch 3) first.

## Learning Objectives

- [ ] Design and implement a complete, reusable typography design token system
- [ ] Use variable fonts to control multiple axes with CSS
- [ ] Build a documentation style guide for typography
- [ ] Implement vertical rhythm and optical sizing
- [ ] Apply typography in a real multi-page-style layout

## Background

A **design token** is a named value that represents a design decision. Instead of hardcoding values like font sizes directly in selectors, you define them as CSS custom properties in `:root` with meaningful names. This makes your system easy to update, document, and reuse. For example, a modular type scale can be built by multiplying a base size by a fixed ratio at each step.

## Task

Build a complete **Typography Design System** — a living style guide that documents and demonstrates every typographic decision.

### Exercise 1: Variable Font Control

Use a variable font (try: [Recursive](https://fonts.google.com/specimen/Recursive) or [Roboto Flex](https://fonts.google.com/specimen/Roboto+Flex)) and expose its axes as CSS custom properties in `:root`. Then use `font-variation-settings` to apply those variables on your elements.

Create an interactive "Font Explorer" section where CSS `:checked` radio buttons change the custom property values to demonstrate different font variation combinations.

### Exercise 2: Complete Design Token System

Define a complete token system in `:root`:
- **Scale**: 8-step modular scale with named steps
- **Line heights**: 3 values (tight: 1.1, normal: 1.5, loose: 1.8)
- **Letter spacing**: 5 values (tightest → widest)
- **Font families**: heading, body, mono
- **Font weights**: thin, regular, medium, semibold, bold, black (using font-variation-settings)
- **Text colours**: primary, secondary, tertiary, disabled, inverse

### Exercise 3: Vertical Rhythm System

Implement baseline grid typography:
- Set a `--baseline: 1.5rem` (24px assuming 16px base)
- All vertical spacing (margins, padding) must be a multiple of `--baseline`
- Headings must align to the grid: calculate `margin-bottom` values so text sits on grid lines
- Use CSS `background-image: repeating-linear-gradient()` to show the baseline grid as a toggle (use a `<body class="show-grid">` CSS hook)

### Exercise 4: Typography Style Guide Page

Build a documentation page that would serve as a real design system reference:
```
┌─────────────────────────────────────────────────────┐
│  📝 Typography System                               │
│  ─────────────────────────────────────────────────  │
│  [Type Scale] [Headings] [Body] [Utilities] [Code]  │
│  ─────────────────────────────────────────────────  │
│  TYPE SCALE                                         │
│  4xl  The quick brown fox                  3.82rem  │
│  3xl  The quick brown fox                  3.05rem  │
│  2xl  The quick brown fox                  2.44rem  │
│  xl   The quick brown fox                  1.95rem  │
│  lg   The quick brown fox                  1.56rem  │
│  base The quick brown fox                  1.25rem  │
│  sm   The quick brown fox                   1rem    │
│  xs   The quick brown fox                  0.75rem  │
└─────────────────────────────────────────────────────┘
```
The page must:
- Show every type scale step with its name, example, and computed px/rem value
- Use the CSS tab interface (`:checked`) to switch between sections
- Include a token reference table for every value
- Display the variable font axes with interactive controls

## Acceptance Criteria

- [ ] Variable font is used with `font-variation-settings`
- [ ] At least 3 font variation axis combinations are demonstrable
- [ ] All design token categories are defined in `:root` with clear naming
- [ ] Vertical rhythm grid can be toggled with a CSS class
- [ ] Style guide page shows all type scale steps in a table
- [ ] Tab navigation works with CSS `:checked` technique
- [ ] All computed values (px equivalent) are shown alongside rem values
- [ ] Lighthouse Accessibility score is 100

## Resources

- [Google Fonts — Variable Fonts](https://fonts.google.com/?vfonly=true)
- [MDN: font-variation-settings](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variation-settings)
- [MDN: CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [MDN: repeating-linear-gradient()](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/repeating-linear-gradient)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
