# Data Tables — Data Dashboard Table 🔴

**Branch:** `tables-dashboard`  
**Prerequisite:** Complete `tables-advanced` (Branch 3) first.

## Learning Objectives

- [ ] Build a complete data management interface with multiple table features combined
- [ ] Create expandable rows using CSS `:checked` technique
- [ ] Implement inline data visualisation within table cells (mini bar charts)
- [ ] Build a pagination component that works with the table
- [ ] Create a search/filter bar that integrates with the table UI (visual only)

## Task

Build a **sales analytics table** — the most complex table assignment. This simulates a real business intelligence dashboard.

```
  ┌─────────────────────────────────────────────────────────────┐
  │ 🔍 Search products...  [Filter ▾]  [Export]  Showing 1-10  │
  ├──┬────────────────┬────────┬────────┬──────────────┬────────┤
  │▶ │ Product        │ Sales  │ Growth │ Performance  │ Stock  │
  ├──┼────────────────┼────────┼────────┼──────────────┼────────┤
  │▶ │ Nike Air Zoom  │ 1,234  │ +12%↑  │ ████████░░   │  89   │
  │  │ ↳ Black (42)  │   523  │        │              │  32   │  ← expanded row
  │  │ ↳ White (40)  │   411  │        │              │  28   │
  │  │ ↳ Red (41)    │   300  │        │              │  29   │
  │▶ │ Adidas Ultra  │   987  │  -3%↓  │ ██████░░░░   │ 142   │
  ├──┴────────────────┴────────┴────────┴──────────────┴────────┤
  │  ← 1  [2]  [3]  [4]  ...  [12] →                          │
  └─────────────────────────────────────────────────────────────┘
```

### Exercises

1. **Expandable rows:** Clicking the `▶` toggle expands the row to show sub-rows. Use `<input type="checkbox">` inside the `<td>` and sibling CSS to show/hide the sub-rows. The `▶` rotates to `▼` when open
2. **Mini bar chart cells:** The "Performance" column contains a small bar chart — a `<div>` with `width: var(--perf)` set inline, styled as a coloured progress bar inside the cell
3. **Growth indicator:** Positive growth = green text + ↑ arrow; negative = red + ↓. A `.growth` wrapper with a `data-trend="up|down"` attribute drives the styling via `[data-trend="up"]` and `[data-trend="down"]` selectors
4. **Pagination:** Build a full pagination component below the table: Previous, numbered pages (1-5 shown), ellipsis for gap, last page, Next. Active page is highlighted. Document that real pagination requires JavaScript
5. **Filter/search bar:** Design the search input and filter dropdown above the table. They don't need to function — style them to look like a real interface and add `:focus-within` effects

## Acceptance Criteria

- [ ] Rows expand/collapse on toggle click using CSS `:checked` technique
- [ ] Sub-rows are indented and clearly child items
- [ ] Performance bar chart scales correctly with `--perf` custom property
- [ ] Growth direction styling uses `data-trend` attribute selectors
- [ ] Pagination component is present and styled (active, hover, disabled states)
- [ ] Search/filter bar is present and has `:focus-within` styling
- [ ] Table remains accessible — expanded rows are in logical DOM order
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [MDN: :checked](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked)
- [MDN: CSS attribute selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)
- [MDN: :focus-within](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus-within)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
