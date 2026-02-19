# Data Tables — Advanced Table Features 🟠

**Branch:** `tables-advanced`  
**Prerequisite:** Complete `tables-responsive` (Branch 2) first.

## Learning Objectives

- [ ] Add sortable column indicators (visual only, CSS)
- [ ] Create status badges inside table cells
- [ ] Build a table with action buttons and icon buttons
- [ ] Implement row selection with checkboxes
- [ ] Create a fixed-column table with complex CSS

## Task

Build a **user management table** — a common component in web apps.

```
  ┌──┬───────────────┬─────────────┬─────────┬──────────┬───────┐
  │☐ │ Name          │ Email       │ Role    │ Status   │ ─ ─ ─ │
  ├──┼───────────────┼─────────────┼─────────┼──────────┼───────┤
  │☑ │ Ana Martinez  │ ana@...     │ Admin   │ ● Active │ ✏️ 🗑️ │  ← selected row
  │☐ │ Ben Johnson   │ ben@...     │ Editor  │ ● Active │ ✏️ 🗑️ │
  │☐ │ Cara Lee      │ cara@...    │ Viewer  │ ○ Paused │ ✏️ 🗑️ │
  │☐ │ David Kim     │ david@...   │ Editor  │ ✕ Banned │ ✏️ 🗑️ │
  └──┴───────────────┴─────────────┴─────────┴──────────┴───────┘
```

### Exercises

1. **Row checkboxes:** Custom-styled checkboxes in the first column. When checked, the row gets a blue tint background using `:has(input:checked)` on the `<tr>`
2. **Status badges:** Pill-shaped badges with colour-coded dot indicator (`Active` = green, `Paused` = yellow, `Banned` = red). Don't use colour alone — add the text label too
3. **Sortable column headers:** Add an up/down arrow indicator to headers. Use classes `.sort--asc` and `.sort--desc` to show the current sort direction. Add a hover state to all sortable headers indicating they are clickable (even without JS)
4. **Action buttons:** Icon-only Edit and Delete buttons in the last column. They must have `aria-label` for screen readers. On hover, show a tooltip using CSS `::after`
5. **Bulk action bar:** When any checkbox is checked (use `:has(input:checked)` on the table wrapper), show a bulk action bar above the table: "X selected — [Delete] [Export] [Assign Role]"

## Acceptance Criteria

- [ ] Row is highlighted when its checkbox is checked (`:has()` technique)
- [ ] Status badges use colour + text (not colour alone)
- [ ] Sortable headers show direction arrows and pointer cursor
- [ ] Action buttons have `aria-label` and CSS tooltips
- [ ] Bulk action bar appears only when at least one row is checked
- [ ] Table is still responsive (from Branch 2)
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: :has()](https://developer.mozilla.org/en-US/docs/Web/CSS/:has)
- [MDN: aria-label](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-label)
- [MDN: CSS attribute selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)
- [MDN: ::after pseudo-element](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
