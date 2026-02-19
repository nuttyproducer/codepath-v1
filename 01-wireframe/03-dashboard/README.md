# Wireframe — Dashboard Layout 🟠

**Branch:** `wireframe-dashboard`  
**Prerequisite:** Complete `wireframe-complex-layout` (Branch 2) first.

## The Wireframe

```
┌──────────────────────────────────────────────────────────────┐
│ TOPBAR                                                       │
│ [≡] Logo · Admin Dashboard          [🔔 3] [👤 User ▼]     │
├──────┬───────────────────────────────────────────────────────┤
│      │  Good morning, User!  ·  Thursday, 19 Feb 2026        │
│  🏠  │                                                       │
│  📊  │  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────┐ │
│  👥  │  │ 👥 Users │  │ 💰 Sales │  │ 📦 Orders│  │ ⭐   │ │
│  📁  │  │  1,234   │  │ €45,200  │  │   89     │  │ 4.8  │ │
│  ⚙️  │  │  +5.2%↑  │  │  +8.1%↑ │  │  +2.1%↑ │  │/5.0  │ │
│      │  └──────────┘  └──────────┘  └──────────┘  └──────┘ │
│      │                                                       │
│      │  ┌─────────────────────────┐  ┌────────────────────┐ │
│      │  │  Recent Activity        │  │  Quick Actions     │ │
│      │  │  ● User signed up  now  │  │  [+ Add User]      │ │
│      │  │  ● Order #1042   2m ago │  │  [📤 Export CSV]   │ │
│      │  │  ● Message from Ana 5m  │  │  [📊 View Reports] │ │
│      │  │  ● System backup   1h   │  │  [⚙️ Settings]     │ │
│      │  └─────────────────────────┘  └────────────────────┘ │
│      │                                                       │
│      │  ┌───────────────────────────────────────────────┐   │
│      │  │  [Day] [Week] [Month] [Year]  ← tab controls  │   │
│      │  │                                               │   │
│      │  │  Sales Performance                            │   │
│      │  │  ████▓▓░░  ████████  ▓▓████░░  ██████▓░      │   │
│      │  │  Mon      Tue       Wed        Thu            │   │
│      │  └───────────────────────────────────────────────┘   │
└──────┴───────────────────────────────────────────────────────┘
```

## Learning Objectives

- [ ] Build a complex CSS Grid layout with named areas
- [ ] Create a collapsible sidebar using CSS only
- [ ] Implement CSS-only tabs with `:checked` or `:target`
- [ ] Build a CSS bar chart using height and flexbox
- [ ] Position notification badges using `position: absolute`
- [ ] Create icon-only navigation with tooltips on hover

## Task

Build an admin dashboard. This is the most layout-complex assignment so far. Start by writing your grid structure first — every pixel should have a plan before you code.

### Exercise 1) Sidebar + topbar layout

The page has two fixed elements and a scrollable content area:
- **Topbar:** fixed to the top, full width, height 60px, `z-index` above content
- **Sidebar:** fixed to the left, full height below topbar, width 220px
- **Content:** takes remaining width and height, scrollable, has padding

On mobile: sidebar is hidden by default, topbar shows a hamburger icon to toggle it (CSS `:checked` trick). The sidebar slides in as an overlay.

### Exercise 2) Stat cards with trend indicators

Create 4 stat cards in a responsive grid:
- Each card: icon, metric name, value, percentage change
- Percentage change: green + ↑ arrow for positive, red + ↓ for negative (use CSS classes)
- A subtle top border of the card changes colour based on the trend
- Cards use CSS Grid internally for alignment
- Hover: card lifts slightly

### Exercise 3) CSS-only tab interface for the chart

The chart section has tabs: Day, Week, Month, Year.
- Use hidden radio inputs — clicking a tab label checks the corresponding input
- Each tab shows a different "chart" — build 4 different bar chart configurations
- The active tab label is visually highlighted
- Smooth transition between tabs using opacity

### Exercise 4) CSS bar chart

Build the sales chart using only HTML and CSS:
- Use `<div>` elements inside a flex container for bars
- Each bar's height is driven by an inline CSS custom property set on the element
- Animate bars growing from the bottom on page load using `@keyframes`
- Label each bar below with the day name

### Exercise 5) Notification badge + user dropdown

Add to the topbar:
- A bell icon with a badge showing `3` new notifications
- Badge uses `position: absolute` relative to the icon
- A user avatar with name, and a dropdown arrow
- On hover, show a dropdown menu (CSS `visibility` + `opacity` transition trick)
- Dropdown contains: Profile, Settings, Logout

## Acceptance Criteria

- [ ] Topbar is fixed to the top; sidebar is fixed to the left
- [ ] Content area fills remaining space and scrolls independently
- [ ] Sidebar collapses to icon-only or hides on mobile (CSS toggle)
- [ ] 4 stat cards display in a responsive grid (4 col desktop, 2 col tablet, 1 col mobile)
- [ ] Tabs switch chart content without JavaScript
- [ ] CSS bar chart uses `--bar-height` custom properties for values
- [ ] Bars animate in on page load (respecting prefers-reduced-motion)
- [ ] Notification badge is positioned correctly
- [ ] User dropdown appears on hover
- [ ] Lighthouse Accessibility score is 100

## Resources

- [CSS Grid Template Areas](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-areas)
- [CSS-only tabs](https://css-tricks.com/the-checkbox-hack/#tabs)
- [CSS custom properties for dynamic values](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [Building a bar chart in CSS](https://css-tricks.com/css-charts-grid-custom-properties/)
- [Fixed vs sticky positioning](https://developer.mozilla.org/en-US/docs/Web/CSS/position)

💡 **Stuck?** Ask an AI assistant — describe what you're trying to achieve and let it explain the concept.
