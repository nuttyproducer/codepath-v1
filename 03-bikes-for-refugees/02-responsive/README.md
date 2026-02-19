# Bikes for Refugees — Responsive 🟡

**Branch:** `bikes-for-refugees-responsive`  
**Prerequisite:** Complete `bikes-for-refugees` (Branch 1) first.

## Learning Objectives

- [ ] Understand and apply mobile-first CSS
- [ ] Use CSS media queries to adapt layouts
- [ ] Implement CSS Grid for article layouts
- [ ] Use responsive images with `srcset`
- [ ] Apply `clamp()`, `min()`, `max()` for fluid typography
- [ ] Build a hamburger menu using CSS only

## Task

The Bikes for Refugees website looks great on desktop, but it breaks on mobile and tablet. Your job is to make it **fully responsive** — it should look polished on any screen size.

You will continue working with the same HTML from Branch 1. Start by studying how the page currently behaves on small screens using DevTools Device Toolbar (F12 → Ctrl+Shift+M).

### Exercise 1) Adopt a mobile-first approach

Rewrite the CSS so that the **base styles are for mobile**, and media queries add complexity for larger screens. This is the professional standard.

Ask yourself:
- What does this page look like on a 375px screen?
- What changes at 768px (tablet)?
- What changes at 1200px (desktop)?

### Exercise 2) Responsive navigation

On small screens the horizontal navigation takes up too much space. Create a **hamburger menu** using only HTML and CSS:
- Hide the navigation links by default on mobile
- Show a `☰` (hamburger) icon using a `<label>` and hidden `<input type="checkbox">`
- Toggle the menu open/closed when the icon is clicked
- On desktop, always show the navigation horizontally

### Exercise 3) CSS Grid for articles

Replace the current articles layout with **CSS Grid**:
- Mobile: 1 column
- Tablet (≥768px): 2 columns
- Desktop (≥1200px): 3 columns
- Use `auto-fit` with `minmax()` so it adapts automatically

### Exercise 4) Fluid typography

Replace fixed `px` font sizes with fluid ones using `clamp()`.
Apply this to headings and body text so they scale with the viewport.

### Exercise 5) Responsive images

Update the hero image and article thumbnails:
- Use `max-width: 100%` so images never overflow
- Add `srcset` to the logo for retina displays
- Use the `<picture>` element to serve a different hero crop on mobile vs desktop

### Bonus: Responsive sidebar

On mobile, move the sidebar **below** the main content. On desktop, show it alongside. Use CSS Grid or Flexbox with `order` to achieve this without changing the HTML.

## Acceptance Criteria

- [ ] Page looks good on 375px, 768px, and 1280px wide screens
- [ ] No horizontal scrollbar appears on any screen size
- [ ] Navigation collapses into a hamburger menu on mobile
- [ ] Articles section uses a responsive grid
- [ ] Typography scales fluidly between breakpoints
- [ ] Images never overflow their containers
- [ ] Lighthouse Accessibility score is still 100
- [ ] HTML is not modified (CSS changes only, unless adding `srcset`)

## Resources

- [MDN: Media Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries)
- [MDN: clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp)
- [CSS Grid: auto-fit vs auto-fill](https://css-tricks.com/auto-sizing-columns-css-grid-auto-fill-vs-auto-fit/)
- [Responsive Images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
- [CSS-only hamburger menu](https://css-tricks.com/three-css-alternatives-to-javascript-navigation/)

💡 **Stuck?** Ask an AI assistant — describe what you’re trying to achieve and let it explain the concept.
