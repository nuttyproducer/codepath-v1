# Accessibility — Semantic HTML 🟢

**Branch:** `accessibility-semantic`

## Learning Objectives

- [ ] Use the correct HTML element for every purpose
- [ ] Understand the accessibility tree and how it differs from the DOM
- [ ] Write meaningful `alt` attributes for images
- [ ] Structure headings in a logical hierarchy
- [ ] Use HTML landmark elements correctly

## Background

The single biggest thing you can do for accessibility is **use the right HTML element**. A `<button>` is keyboard focusable, clickable, and announced as a button by screen readers — for free. A `<div>` with `onclick` is none of those things.

**The accessibility tree** is a version of the DOM that screen readers use. It only includes elements that have semantic meaning.

```
Semantic HTML → Browser → Accessibility Tree → Screen Reader → User
```

## Task

Audit and rebuild a "broken" page that uses non-semantic HTML, replacing every element with the correct one.

### Exercise 1: The Broken Page

The `index.html` starter file contains a page built entirely with `<div>` and `<span>` elements. Your job is to replace them with semantic equivalents. Examples of what you will find:
```html
<!-- BEFORE: meaningless -->
<div class="header"> ... </div>
<div class="nav"> <div onclick="...">Home</div> </div>
<div class="article"> <div class="title">My post</div> </div>
<div class="footer"> ... </div>

<!-- AFTER: semantic -->
<header> ... </header>
<nav> <a href="/">Home</a> </nav>
<article> <h2>My post</h2> </article>
<footer> ... </footer>
```

### Exercise 2: Landmark Elements

Ensure these landmark regions are present and used correctly:
- `<header>` — page header (not inside `<article>`)
- `<nav>` — navigation menus (can be multiple, use `aria-label` to differentiate)
- `<main>` — one per page, the main content
- `<aside>` — complementary content (sidebar, related articles)
- `<footer>` — page footer (or article footer)
- `<section>` — thematic grouping, MUST have a heading
- `<article>` — self-contained content that could stand alone

### Exercise 3: Heading Hierarchy

Check that headings form a correct outline:
- Only ONE `<h1>` per page
- No skipped levels (don't jump from h2 to h4)
- Headings describe the content that follows
- `<h1>` is not the site name — it is the page title

Run the [headingsMap Chrome extension](https://chrome.google.com/webstore/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi) and take a screenshot showing a perfect heading outline.

### Exercise 4: Image Alt Text

Write correct `alt` attributes for 5 types of images:
1. **Informative image**: describes what the image shows (`alt="Cyclist carrying a donated bike across a muddy field"`)
2. **Decorative image**: empty `alt=""` — tells screen readers to skip it
3. **Functional image** (button/link icon): describes the action (`alt="Search"`)
4. **Image of text**: repeats the text in the image
5. **Complex image** (chart/graph): short alt + `<figure>` with full `<figcaption>` describing the data

## Acceptance Criteria

- [ ] Zero `<div>` elements are used where a semantic element exists
- [ ] All 7 landmark elements are present and correctly placed
- [ ] Heading outline has no gaps (validated with headingsMap or similar)
- [ ] 5 image alt text patterns are demonstrated
- [ ] Decorative images use `alt=""`
- [ ] Screen reader reading order matches visual order
- [ ] Lighthouse Accessibility score is 100

## Resources

- [MDN: HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [MDN: ARIA landmarks](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/landmark_roles)
- [WebAIM: Alternative Text](https://webaim.org/techniques/alttext/)
- [Headings Map extension](https://chrome.google.com/webstore/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
