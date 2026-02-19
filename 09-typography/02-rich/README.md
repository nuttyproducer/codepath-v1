# Typography & Content — Rich Content Styles 🟡

**Branch:** `typography-rich`  
**Prerequisite:** Complete `typography-basic` (Branch 1) first.

## Learning Objectives

- [ ] Style complex editorial content (lists, blockquotes, tables in prose)
- [ ] Create beautiful pull quotes and callout components
- [ ] Style inline code, code blocks, and keyboard shortcuts
- [ ] Use `::first-letter`, `::first-line`, and `::selection` pseudo-elements
- [ ] Build a complete article/blog post design

## Task

Build a **full blog article page** — styled to the same standard as editorial publications like Medium, The Guardian, or CSS-Tricks.

### Exercise 1: Article Chrome

The article layout with:
- Category tag above the title
- H1 title with a drop cap on the first letter using `::first-letter`
- Author byline with avatar (use `<img>` or CSS letter avatar), name, date, and read time
- Hero image that spans full article width with `<figure>` and `<figcaption>`

### Exercise 2: Prose Content Elements

Style all these elements for reading comfort:
- **Ordered list**: styled with custom counter numbers, not browser defaults. Research CSS `counter-reset` and `counter-increment` to build your own numbering.
- **Unordered list**: custom bullet using `::before` with a decorative character (›, •, ◦)
- **Nested list**: indent second level, change bullet style
- **Definition list** (`<dl>`, `<dt>`, `<dd>`): styled for glossary use
- **Blockquote**: left border accent, larger italic text, `<cite>` styled below

### Exercise 3: Callout and Pull Quote Components

**Pull quote**: a highlighted sentence pulled from the article body — styled large, centred, and decorative:
```
        ❝
    Typography is the clothes
    your words wear.
        ❞
         — Robert Bringhurst
```

**Callout boxes** (4 types, each with an icon prefix via `::before` or `<span>`):
- 💡 Tip — blue background
- ⚠️ Warning — amber background
- ❌ Error — red background
- ✅ Success — green background

### Exercise 4: Code and Technical Content

Style technical/code content like a developer documentation page:
- **Inline code**: `<code>` with `font-family: 'JetBrains Mono', monospace`, rounded background pill
- **Code block**: `<pre><code>` with dark background, line-height `1.5`, horizontal scroll on overflow
- **Keyboard shortcut**: `<kbd>` styled to look like a real keyboard key — raised with `box-shadow: 0 2px 0 #999`, `border: 1px solid #ccc`
- **Diff output**: two `<code>` blocks side by side, lines prefixed with `+` (green) and `-` (red)

## Acceptance Criteria

- [ ] Drop cap using `::first-letter` is present in the article
- [ ] Ordered list uses CSS `counter-reset` / `counter-increment`
- [ ] Blockquote has left border accent and `<cite>`
- [ ] Pull quote is visually distinct from body text
- [ ] All 4 callout box variants are present
- [ ] `<kbd>` looks like a real keyboard key
- [ ] Code block has horizontal scroll on overflow (never breaks layout)
- [ ] `::selection` is styled to match the accent colour
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: ::first-letter](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter)
- [MDN: counter-reset](https://developer.mozilla.org/en-US/docs/Web/CSS/counter-reset)
- [MDN: blockquote element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote)
- [MDN: kbd element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
