# Accessibility — WCAG Compliance 🔴

**Branch:** `accessibility-wcag`  
**Prerequisite:** Complete `accessibility-aria` (Branch 3) first.

## Learning Objectives

- [ ] Understand the WCAG 2.1 structure: Perceivable, Operable, Understandable, Robust (POUR)
- [ ] Meet all Level AA colour contrast requirements
- [ ] Pass all automated and manual accessibility testing
- [ ] Write an accessibility statement for your page
- [ ] Know what CSS can and cannot solve in accessibility

## Background

**WCAG 2.1 Level AA** is the legal standard in many countries (including Belgium, via the EU Web Accessibility Directive). It consists of 50 success criteria across 4 principles:

| Principle | Example criteria |
|---|---|
| **Perceivable** | 1.4.3 Contrast (min), 1.4.4 Resize text, 1.4.10 Reflow |
| **Operable** | 2.1.1 Keyboard, 2.4.7 Focus visible, 2.5.3 Label in name |
| **Understandable** | 3.1.1 Language of page, 3.3.1 Error identification |
| **Robust** | 4.1.2 Name, Role, Value |

## Task

Build the most accessible page you have built yet — a **complete contact form page** — and audit it against every applicable WCAG 2.1 AA criterion.

### Exercise 1: Colour Contrast System

Create a colour palette where every combination passes WCAG 2.1 AA:
- **Normal text** (< 18pt): minimum 4.5:1 contrast ratio against background
- **Large text** (≥ 18pt or bold ≥ 14pt): minimum 3:1 contrast ratio
- **UI components** (borders, icons): minimum 3:1 against adjacent colour
- **Focus rings**: minimum 3:1 against the element AND the background

Use [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) to verify every combination. Document all ratios in a `CONTRAST.md` file:
```
| Element                  | Foreground  | Background | Ratio  | Pass  |
|--------------------------|-------------|------------|--------|-------|
| Body text                | #1a1a1a     | #ffffff    | 19.3:1 | ✅ AA |
| Placeholder text         | #767676     | #ffffff    | 4.54:1 | ✅ AA |
| Disabled button text     | #767676     | #e5e7eb    | 2.8:1  | ❌    |
```

### Exercise 2: Reflow and Text Resizing

WCAG 1.4.10 Reflow: the page must not require horizontal scrolling at 320px wide (equivalent to 400% zoom on a 1280px screen).

WCAG 1.4.4 Resize text: all text must be readable at 200% browser zoom.

- Use `rem` for all font sizes (never `px`)
- Use relative units for all spacing (`em` or `rem` for margins/paddings)
- Test at 320px width — the form should be fully functional
- Test at 200% zoom — all text and UI must be visible and readable
- Document what breaks and how you fixed it

### Exercise 3: Error Identification and Suggestion

The contact form must meet WCAG 3.3.1 and 3.3.3:
- 3.3.1: Error identification — errors are identified in text (not just colour)
- 3.3.3: Error suggestion — specific fix is suggested

Each form field needs: a visible label, an error message region linked via `aria-describedby`, and an `aria-invalid` attribute that reflects the field’s state. Error messages must suggest a specific fix (e.g., "Please enter a valid email address (example: name@domain.com)") rather than a generic one.

Create CSS-only validation messages using `:invalid` + `:not(:placeholder-shown)` pattern. Document where JavaScript is required for a fully compliant error flow.

### Exercise 4: Accessibility Audit and Statement

**Automated audit:** Run Lighthouse, Axe (browser extension), and WAVE against your page. Fix every issue flagged.

**Manual audit:** Tab through every element. Document your findings.

**Accessibility Statement** — create an `ACCESSIBILITY.md` that includes:
1. Date of the last review
2. Conformance status (partially, fully, or not conforming to WCAG 2.1 AA)
3. List of known issues (none, ideally!)
4. List of technologies relied upon (HTML, CSS, browser features)
5. A list of the manual tests you performed
6. What CSS CANNOT fix (and would require JavaScript): focus trap in modals, dynamic aria-expanded, `aria-live` regions with dynamic content, keyboard arrow key navigation in menus

## Acceptance Criteria

- [ ] `CONTRAST.md` documents every foreground/background combination with ratios
- [ ] Every colour combination passes its applicable WCAG standard
- [ ] Page is fully functional at 320px viewport width (no horizontal scroll)
- [ ] Page is readable at 200% browser zoom
- [ ] Error messages include specific fix suggestions (not just "invalid")
- [ ] Error messages are identified by text, not just red colour
- [ ] Zero Axe violations on the completed page
- [ ] Zero WAVE errors on the completed page
- [ ] `ACCESSIBILITY.md` is complete with all required sections
- [ ] Lighthouse Accessibility score is 100

## Resources

- [WebAIM: Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [MDN: :invalid](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
- [Axe browser extension](https://www.deque.com/axe/browser-extensions/)
- [WAVE accessibility tool](https://wave.webaim.org/)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
