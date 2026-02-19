# Data Tables — Basic Table 🟢

**Branch:** `tables-basic`

## Learning Objectives

- [ ] Write semantic table HTML (`table`, `thead`, `tbody`, `tfoot`, `th`, `td`, `caption`)
- [ ] Use `scope` attribute on header cells for accessibility
- [ ] Apply fundamental table styling (borders, spacing, zebra striping)
- [ ] Distinguish between row and column headers
- [ ] Style a table `caption` properly

## The Design

Build a data table showing student assignment scores:

```
  Assignment Scores — Spring 2026
  ┌───────────────┬──────┬───────┬───────┬───────┬─────────┐
  │ Student       │ HTML │  CSS  │  Git  │  JS   │ Average │
  ├───────────────┼──────┼───────┼───────┼───────┼─────────┤
  │ Ana Martinez  │  92  │  88   │  95   │  79   │  88.5   │
  │ Ben Johnson   │  78  │  91   │  82   │  88   │  84.8   │
  │ Cara Lee      │  95  │  97   │  90   │  92   │  93.5   │
  │ David Kim     │  65  │  70   │  75   │  68   │  69.5   │
  ├───────────────┼──────┼───────┼───────┼───────┼─────────┤
  │ Class Average │  82  │  86   │  85   │  82   │  83.8   │
  └───────────────┴──────┴───────┴───────┴───────┴─────────┘
```

### Exercises

1. Write the full semantic HTML — `<caption>`, `<thead>` with `<th scope="col">`, `<tbody>` with `<th scope="row">` for student names, `<tfoot>` for averages
2. Style with `border-collapse: collapse` and consistent cell padding
3. Add zebra striping: alternate row background colours using `tbody tr:nth-child(even)`
4. Style the `<tfoot>` differently — bold, slightly darker background
5. Highlight the highest score in each column using a CSS class `.score--high` (manually add to HTML) with an accent colour

## Acceptance Criteria

- [ ] All semantic table elements are used correctly
- [ ] `scope` attribute is on every `<th>` cell
- [ ] `<caption>` is present and visible
- [ ] Zebra striping is applied to `<tbody>` rows only
- [ ] `<tfoot>` is visually distinct
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: table element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
- [MDN: scope attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th#scope)
- [MDN: :nth-child()](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child)
- [WebAIM: Creating Accessible Tables](https://webaim.org/techniques/tables/data)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
