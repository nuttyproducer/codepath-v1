# Data Tables — Responsive Table 🟡

**Branch:** `tables-responsive`  
**Prerequisite:** Complete `tables-basic` (Branch 1) first.

## Learning Objectives

- [ ] Make a data table work on small screens without losing data
- [ ] Implement horizontal scroll as a mobile strategy
- [ ] Build a card-style mobile view of tabular data
- [ ] Create sticky header and sticky first column
- [ ] Use `data-*` attributes to label cells in mobile card view

## Task

Tables are inherently not mobile-friendly. This branch explores the main strategies for responsive tables.

### Strategy 1: Horizontal Scroll Container

Wrap the table in a `<div class="table-scroll">` and apply `overflow-x: auto` with `-webkit-overflow-scrolling: touch`. Add a visual hint that the table scrolls (fade on the right edge using a gradient `::after`).

### Strategy 2: Sticky First Column

When the table scrolls horizontally, the first column (student name) should stay fixed:
- `position: sticky; left: 0` on the first `<th>` and `<td>` in each row
- Add a `box-shadow` to the right edge of the sticky column so it looks separated from scrolling content

### Strategy 3: Sticky Header

The `<thead>` row should stay visible as the user scrolls vertically through a long table:
- Add more rows to make the table tall enough to demonstrate this
- `position: sticky; top: 0` on the `<thead>` (or `<tr>` inside it)

### Strategy 4: Card-Style Mobile View

At ≤480px, transform the table into stacked cards using CSS:
- Hide the `<thead>` with `display: none`
- Make each `<tr>` display as a block card
- Each `<td>` should show its own label using `content: attr(data-label)` from a `::before` pseudo-element
- Add `data-label="HTML Score"` etc. to each `<td>` in HTML

## Acceptance Criteria

- [ ] Table scrolls horizontally on small screens with a visual scroll hint
- [ ] First column is sticky during horizontal scroll
- [ ] Header row is sticky during vertical scroll
- [ ] On ≤480px, table becomes stacked card layout
- [ ] Card layout uses `data-label` for cell identification
- [ ] All data is readable at every breakpoint
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: position sticky](https://developer.mozilla.org/en-US/docs/Web/CSS/position#sticky)
- [MDN: overflow](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)
- [MDN: attr() function](https://developer.mozilla.org/en-US/docs/Web/CSS/attr)
- [MDN: ::before](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
