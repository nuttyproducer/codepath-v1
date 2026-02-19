# Typography & Content — Basic Typography 🟢

**Branch:** `typography-basic`

## Learning Objectives

- [ ] Set font families using `font-family` stacks (system fonts and Google Fonts)
- [ ] Understand `font-size`, `line-height`, `letter-spacing`, and `font-weight`
- [ ] Apply text alignment, decoration, and transformation
- [ ] Create a simple but complete typographic hierarchy
- [ ] Know the difference between `px`, `em`, and `rem` for font sizing

## Background

Typography is the foundation of all web design. Before adding colour or layout, a page with good typography already feels polished.

**The type scale** — a system of proportional sizes:
| Name    | Size (rem) | Usage |
|---------|-----------|-------|
| `xs`    | 0.75rem   | Labels, captions |
| `sm`    | 0.875rem  | Secondary text |
| `base`  | 1rem      | Body text |
| `lg`    | 1.125rem  | Large body |
| `xl`    | 1.25rem   | Small headings |
| `2xl`   | 1.5rem    | H3 |
| `3xl`   | 1.875rem  | H2 |
| `4xl`   | 2.25rem   | H1 |

## Task

Build a **Typography Specimen** page — a single page that showcases all typographic styles.

### Exercise 1: Font Selection

Import two fonts from Google Fonts:
- A **serif** font for headings (options: Playfair Display, Lora, Merriweather)
- A **sans-serif** font for body text (options: Inter, Source Sans 3, Nunito)

Define them as CSS custom properties in your `:root`.

### Exercise 2: Heading Hierarchy

Display all 6 heading levels (h1–h6) with:
- Clear size reduction from h1 to h6
- Consistent `line-height` (tighter for large headings: `1.1`, looser for small: `1.4`)
- `letter-spacing: -0.02em` on h1 and h2 (large headings benefit from tighter tracking)
- A horizontal rule between each heading and its placeholder paragraph

### Exercise 3: Body Text Styles

Show a full article body section with:
- Regular paragraph text: `font-size: 1rem`, `line-height: 1.6`, `max-width: 65ch` (the golden measure)
- A **lead paragraph**: slightly larger, first paragraph of an article
- `<strong>` bold emphasis
- `<em>` italic emphasis
- `<small>` for footnotes/captions
- `<code>` inline code with monospace font and subtle background

### Exercise 4: Text Utilities

A utility classes section that demonstrates:
- `.text-left`, `.text-center`, `.text-right`
- `.text-uppercase`, `.text-lowercase`, `.text-capitalize`
- `.truncate` — single line with `overflow: hidden; text-overflow: ellipsis; white-space: nowrap`
- `.line-clamp-2` — 2-line clamp with `-webkit-line-clamp`
- `.text-muted` — reduced opacity secondary text

## Acceptance Criteria

- [ ] Two Google Fonts are imported and applied to headings and body respectively
- [ ] All 6 heading levels are displayed with clear hierarchy
- [ ] Body text `max-width: 65ch` is applied for readable line length
- [ ] All 4 utility class groups are shown and working
- [ ] `font-family`, `line-height`, `font-weight` are defined as CSS custom properties
- [ ] Lighthouse Accessibility score is 100

## Resources

- [Google Fonts](https://fonts.google.com/)
- [MDN: font-family](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)
- [MDN: line-height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
- [MDN: CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
