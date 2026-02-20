# Wireframe — Complex Blog Layout 🟡

**Branch:** `wireframe-complex-layout`  
**Prerequisite:** Complete `wireframe-to-webcode` (Branch 1) first.

## The Wireframe

```
┌────────────────────────────────────────────────────────┐
│  HEADER                                                │
│  [Logo]  Home | About | Blog | Contact  [Subscribe]    │ 
├────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Blog > HTML & CSS > This Post      │
├────────────────────────────────┬───────────────────────┤
│                                │                       │
│  [Featured Image — full width] │  SIDEBAR (sticky)     │
│                                │  ┌─────────────────┐  │
│  Blog Post Title (h1)          │  │  About the      │  │
│  By Author Name  ·  Date       │  │  Author         │  │
│  ⏱ 5 min read                 │  │  [Photo]        │  │
│                                │  │  Name           │  │
│  Introduction paragraph...     │  │  Short bio...   │  │
│  More text continues here...   │  └─────────────────┘  │
│                                │  ┌─────────────────┐  │
│  ## Subheading (h2)            │  │  Categories     │  │
│  More content...               │  │  • HTML (12)    │  │
│                                │  │  • CSS (8)      │  │
│  > Blockquote: "A great quote  │  │  • Git (5)      │  │
│  from someone important."      │  └─────────────────┘  │
│                                │  ┌─────────────────┐  │
│  Final paragraph...            │  │  Newsletter     │  │
│                                │  │  Stay updated   │  │
│  Tags: #html  #css  #web       │  │  [email input]  │  │
│                                │  │  [Subscribe]    │  │
│  ─────────────────────────     │  └─────────────────┘  │
│  Related Posts:                │                       │
│  [Card] [Card] [Card]          │                       │
│                                │                       │
└────────────────────────────────┴───────────────────────┤
│  FOOTER                                                │
│  © 2026 · Privacy · Terms · Social links               │
└────────────────────────────────────────────────────────┘
```

## Learning Objectives

- [ ] Implement a two-column layout using CSS Grid
- [ ] Use `position: sticky` for a sidebar
- [ ] Style rich text content (blockquotes, code, lists)
- [ ] Build a breadcrumb navigation component
- [ ] Create reusable card components
- [ ] Implement a full page layout with named grid areas

## Task

Using the wireframe above, build a blog post page. Write content about **what you've learned so far in this curriculum** — make it real and personal!

### Exercise 1) Plan your HTML structure first

Before writing any code, sketch out the HTML hierarchy on paper:
- What semantic elements will you use?
- What will your CSS class naming strategy be?
- Which elements need IDs vs classes?

Write your plan as a comment block at the top of your HTML file before starting.

### Exercise 2) Two-column layout with CSS Grid

Implement the layout using CSS Grid with named template areas. The sidebar should be `300px` wide, the main content takes the rest with `1fr`.

### Exercise 3) Sticky sidebar

The sidebar should stick to the top as the user scrolls:
- Use `position: sticky` with `top: 1rem`
- The sidebar should not exceed the viewport height (`max-height: calc(100vh - 2rem)`)
- If the sidebar content is taller than the viewport, add `overflow-y: auto`

### Exercise 4) Rich text styling

Style the article content:
- Blockquotes: left border, italic, slightly indented with a background tint
- Ordered and unordered lists: proper spacing, custom markers
- Inline `<code>`: monospace font, light background, border-radius
- Links: underline on hover only, with a colour transition
- The first paragraph after a heading: slightly larger font size using `:first-of-type`

### Exercise 5) Related posts cards

Create a 3-column grid of related post cards. Each card must contain:
- A placeholder image (use a coloured `<div>` or placeholder SVG)
- A title (h3)
- A short description
- A "Read more" link
- Hover: lift the card with `translateY` and deepen `box-shadow`

## Acceptance Criteria

- [ ] Page matches the wireframe layout on desktop (1200px+)
- [ ] Sidebar sticks during scroll and doesn't overflow the viewport
- [ ] Breadcrumb navigation is present and semantically correct (`<nav aria-label="breadcrumb">`)
- [ ] Blockquotes, lists, and inline code are styled distinctly
- [ ] Related posts grid uses 3 columns on desktop, 1 on mobile
- [ ] Page is fully responsive (1 column on mobile, 2 on desktop)
- [ ] Lighthouse Accessibility score is 100
- [ ] All text content is real (not lorem ipsum) — write about the curriculum!

## Resources

- [CSS Grid named areas](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-areas)
- [position: sticky](https://developer.mozilla.org/en-US/docs/Web/CSS/position#sticky)
- [Breadcrumb pattern](https://www.w3.org/WAI/ARIA/apg/patterns/breadcrumb/)
- [Styling blockquotes](https://css-tricks.com/quoting-in-html-quotations-citations-and-blockquotes/)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
