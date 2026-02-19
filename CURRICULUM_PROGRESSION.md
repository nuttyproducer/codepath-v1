# HYF Assignments - Progressive Learning Path

This document outlines the complete curriculum structure with progressive difficulty levels for each assignment category.

## 📐 Learning Philosophy

Each assignment series follows a **4-step progression model**:
1. **Foundation** - Learn the basics and core concepts
2. **Enhancement** - Add complexity and refine techniques
3. **Integration** - Combine multiple concepts and solve harder problems
4. **Mastery** - Advanced techniques with minimal guidance

---

## 🎯 Current Assignments & Their Progression Paths

### 1️⃣ BIKES FOR REFUGEES SERIES
**Core Skills:** HTML Structure, CSS Styling, Layout, Semantic HTML

#### **Branch 1: bikes-for-refugees** (Foundation) 🟢
**Current State:** COMPLETE
**Learning Objectives:**
- Semantic HTML elements
- Basic CSS styling (colors, fonts, spacing)
- Flexbox basics for navigation
- Image handling and `alt` attributes
- Button styling and hover effects
- Box model (padding, margin)

**Key Challenges:**
- Replace `<div>` with semantic tags
- Fix broken image links
- Style buttons to match design
- Add spacing with padding/margin
- Use Flexbox for header layout

---

#### **Branch 2: bikes-for-refugees-responsive** (Enhancement) 🟡
**New Requirements:**
- Make the website fully responsive (mobile, tablet, desktop)
- Implement a hamburger menu for mobile navigation
- Add CSS Grid for the "Learn more" articles section
- Create a responsive image gallery
- Use media queries for breakpoints
- Add a mobile-first approach

**Key Challenges:**
- Convert fixed layouts to fluid/responsive
- Handle navigation collapse on small screens
- Use `clamp()`, `min()`, `max()` for responsive typography
- Implement Grid with `auto-fit` or `auto-fill`
- Test on multiple device sizes

**Technical Skills:**
- CSS Media Queries
- Mobile-first CSS
- CSS Grid advanced (auto-placement)
- Responsive images (`srcset`, `picture` element)
- Viewport units (`vw`, `vh`, `vmin`, `vmax`)

---

#### **Branch 3: bikes-for-refugees-animations** (Integration) 🟠
**New Requirements:**
- Add CSS animations and transitions
- Implement smooth scroll behavior
- Create animated statistics counter (CSS only, using `@keyframes`)
- Add parallax scrolling effect to hero section
- Implement skeleton loading states
- Add micro-interactions (button press effects, card lifts)

**Key Challenges:**
- Create complex keyframe animations
- Control animation timing functions (ease, cubic-bezier)
- Implement scroll-triggered animations using CSS `animation-timeline`
- Balance performance with visual effects
- Use CSS custom properties for dynamic animations

**Technical Skills:**
- CSS Animations (`@keyframes`)
- CSS Transitions
- Transform properties (translate, scale, rotate)
- Animation timing functions
- CSS custom properties (variables)
- Performance optimization (will-change, transform)

---

#### **Branch 4: bikes-for-refugees-advanced** (Mastery) 🔴
**New Requirements:**
- Add a donation form with multi-step wizard (3 steps)
- Implement CSS-only accordion for FAQ section
- Create an interactive map section (styled, no JS yet)
- Add dark mode toggle (CSS custom properties + `prefers-color-scheme`)
- Implement advanced Grid layout (masonry-style article grid)
- Add print stylesheet for printer-friendly version
- Implement accessibility improvements (focus states, skip links)

**Key Challenges:**
- Multi-step form with CSS `:checked` pseudo-class tricks
- Complex state management with CSS only
- Advanced selectors and pseudo-elements
- Theme switching with CSS custom properties
- Complex Grid layouts with named areas
- WCAG 2.1 AA compliance

**Technical Skills:**
- Advanced CSS selectors (`:has()`, `:is()`, `:where()`)
- CSS Grid named areas and complex layouts
- CSS custom properties for theming
- Accessibility (ARIA, focus management)
- Print media queries
- Advanced pseudo-classes and pseudo-elements

---

### 2️⃣ FORM CONTROLS SERIES
**Core Skills:** HTML Forms, Validation, Input Types, Accessibility

#### **Branch 1: form-controls** (Foundation) 🟢
**Current State:** COMPLETE
**Learning Objectives:**
- Basic form structure
- Input types (text, email, radio, select)
- HTML5 validation (required, minlength, pattern)
- Labels and accessibility
- Fieldsets and legends
- Form submission basics

**Key Challenges:**
- Create a valid, accessible form
- Implement proper validation attributes
- Associate labels with inputs
- Use appropriate input types
- Achieve Lighthouse Accessibility score 100

---

#### **Branch 2: form-controls-advanced** (Enhancement) 🟡
**New Requirements:**
- Add more complex input types (date, range, color, file upload)
- Implement custom checkbox and radio button styles
- Add form field grouping with `<fieldset>`
- Create a multi-select with custom styling
- Add input masks/patterns for phone numbers
- Display custom validation messages
- Add progress indicator for multi-section form

**Key Challenges:**
- Style native form controls to match design
- Create accessible custom controls
- Use CSS pseudo-classes (`:valid`, `:invalid`, `:focus-within`)
- Handle file upload preview (image)
- Create visual feedback for validation states

**Technical Skills:**
- Advanced input types (date, file, color, range)
- Custom styling of form controls
- CSS pseudo-classes for form states
- Pattern attribute with regex
- CSS Grid/Flexbox for form layouts

---

#### **Branch 3: form-controls-dynamic** (Integration) 🟠
**New Requirements:**
- Add dependent form fields (show/hide based on selections)
- Implement a live order summary/calculation
- Create a rating system (star rating)
- Add quantity selectors with +/- buttons
- Implement a promo code field with validation
- Show real-time character counter for textarea
- Add password strength indicator

**Key Challenges:**
- Use CSS `:checked` and sibling selectors for conditional display
- Create interactive components with CSS only (as much as possible)
- Calculate and display totals (prep for JS later)
- Create accessible custom controls (star rating)
- Visual feedback for all interactions

**Technical Skills:**
- CSS combinators (adjacent, general sibling)
- `:checked` pseudo-class tricks
- CSS counters for numbering
- Complex form layouts
- Data attributes for storing values

---

#### **Branch 4: form-controls-validation** (Mastery) 🔴
**New Requirements:**
- Implement a complete checkout form (billing, shipping, payment)
- Add address autocomplete fields structure
- Create a multi-step form with progress bar
- Implement all WCAG form accessibility requirements
- Add custom error messages for each validation rule
- Create a form with conditional required fields
- Add loading states and disabled states
- Implement form data summary page before submission

**Key Challenges:**
- Manage complex form state with CSS only (preparation for JS)
- Advanced validation patterns (credit card, postal codes)
- Proper ARIA attributes for error messages
- Handle complex tab order and focus management
- Create a complete user flow

**Technical Skills:**
- Advanced HTML form attributes (formnovalidate, autocomplete)
- ARIA live regions for error announcements
- Complex CSS-only state management
- Form accessibility best practices (WCAG 2.1)
- Advanced pseudo-classes (`:user-invalid`, `:placeholder-shown`)

---

### 3️⃣ WIREFRAME TO WEBCODE SERIES
**Core Skills:** Interpreting Designs, HTML Structure, CSS Layout, Typography

#### **Branch 1: wireframe-to-webcode** (Foundation) 🟢
**Current State:** IN PROGRESS (Needs completion)
**Learning Objectives:**
- Read and interpret wireframes
- Plan HTML structure from visual design
- Create semantic document structure
- Basic CSS styling (typography, colors, spacing)
- Fixed footer positioning
- Article/content structure

**Key Challenges:**
- Translate wireframe to HTML
- Choose appropriate semantic tags
- Match layout with CSS
- Create 3 content articles
- Position footer at bottom
- Achieve Lighthouse 100

---

#### **Branch 2: wireframe-complex-layout** (Enhancement) 🟡
**New Requirements:**
- **New Wireframe:** Two-column blog layout with sidebar
- Implement sticky sidebar navigation
- Create a filterable tag system (visual only, no JS)
- Add breadcrumb navigation
- Implement pagination component
- Add author bio cards
- Create related posts section

**Wireframe Description:**
```
┌────────────────────────────────────────────────┐
│  HEADER: Logo | Nav | Search | [Subscribe]    │
├────────────────────────────────────────────────┤
│  Breadcrumb: Home > Blog > Category > Post    │
├─────────────────────────────┬──────────────────┤
│  [Featured Image Full Width]│                  │
│                             │  SIDEBAR (sticky)│
│  Blog Post Title            │  ┌─────────────┐ │
│  By Author | Date | 5 min  │  │ About Author│ │
│                             │  │ [Photo]     │ │
│  Paragraph 1...             │  │ Name        │ │
│  Paragraph 2...             │  │ Bio...      │ │
│                             │  └─────────────┘ │
│  ## Subheading              │  ┌─────────────┐ │
│  More content...            │  │ Categories  │ │
│                             │  │ • HTML (12) │ │
│  > Blockquote here          │  │ • CSS (8)   │ │
│                             │  │ • JS (15)   │ │
│  Final paragraph...         │  └─────────────┘ │
│                             │  ┌─────────────┐ │
│  Tags: #html #css #web      │  │ Newsletter  │ │
│                             │  │ Subscribe   │ │
│  ───────────────────────    │  │ [Email]     │ │
│  Related Posts:             │  │ [Button]    │ │
│  [Card] [Card] [Card]       │  └─────────────┘ │
└─────────────────────────────┴──────────────────┤
│  FOOTER: Links | Social | Copyright           │
└────────────────────────────────────────────────┘
```

**Key Challenges:**
- Create sticky sidebar with proper scrolling
- Implement two-column layout with CSS Grid
- Style rich text content (headings, blockquotes, lists)
- Create reusable card components
- Handle sidebar height relative to content

**Technical Skills:**
- `position: sticky`
- CSS Grid for two-column layout
- Typography hierarchy and rhythm
- Component-based CSS thinking
- Box shadows and depth

---

#### **Branch 3: wireframe-dashboard** (Integration) 🟠
**New Requirements:**
- **New Wireframe:** Admin dashboard with complex grid
- Create a multi-section dashboard layout
- Implement data visualization cards
- Add notification badges
- Create a collapsible sidebar menu
- Implement tabbed content sections
- Add user profile dropdown (visual only)
- Create status indicators and progress bars

**Wireframe Description:**
```
┌──────────────────────────────────────────────────────────┐
│ [≡] Logo    Dashboard     [🔔3] [👤 User ▼]             │
├────┬─────────────────────────────────────────────────────┤
│ 🏠 │  Welcome back, User!                                │
│    │  ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐      │
│ 📊 │  │ 👥     │ │ 💰     │ │ 📈     │ │ ⚡     │      │
│    │  │ Users  │ │ Revenue│ │ Growth │ │ Active │      │
│ 📁 │  │ 1,234  │ │ $45.2k │ │ +12%  │ │ 89%    │      │
│    │  │ +5.2%  │ │ +8.1%  │ │ ▲     │ │ ████░  │      │
│ ⚙️ │  └────────┘ └────────┘ └────────┘ └────────┘      │
│    │  ┌───────────────────────┐ ┌──────────────┐       │
│    │  │ Recent Activity       │ │ Quick Actions│       │
│    │  │ ┌──────────────────┐ │ │ [+ New User] │       │
│    │  │ │ ● User joined    │ │ │ [📤 Export]  │       │
│    │  │ │ ● Sale completed │ │ │ [⚙️ Settings]│       │
│    │  │ │ ● New message    │ │ │ [📊 Reports] │       │
│    │  │ └──────────────────┘ │ └──────────────┘       │
│    │  └───────────────────────┘                         │
│    │  ┌────────────────────────────────────────┐       │
│    │  │ Sales Chart [Day|Week|Month|Year]      │       │
│    │  │  ╭─────╮                                │       │
│    │  │  │     ╰─╮  ╭─╮                         │       │
│    │  │  │       ╰──╯ ╰─╮                       │       │
│    │  │ ─┴────────────────╰───────────          │       │
│    │  └────────────────────────────────────────┘       │
└────┴─────────────────────────────────────────────────────┘
```

**Key Challenges:**
- Create complex grid layout with different sized cells
- Implement CSS-only collapsible sidebar
- Create stat cards with icons and visual hierarchy
- Design data visualization using CSS (bar charts, progress)
- Handle notification badges positioning
- Create tabbed interface with `:target` or `:checked`

**Technical Skills:**
- Advanced CSS Grid (grid-template-areas, spanning)
- CSS-only interactive components
- Data visualization with CSS
- Icon integration (SVG or icon fonts)
- Notification badge positioning (absolute/relative)
- Complex state management with CSS

---

#### **Branch 4: wireframe-ecommerce** (Mastery) 🔴
**New Requirements:**
- **New Wireframe:** E-commerce product page with advanced features
- Create a product image gallery with thumbnails
- Implement size/color selector with visual feedback
- Add quantity selector
- Create a sticky "Add to Cart" section on scroll
- Implement product tabs (Description, Reviews, Shipping)
- Add product recommendations carousel layout
- Create breadcrumb navigation
- Add wishlist/compare buttons
- Show stock status indicators

**Wireframe Description:**
```
┌─────────────────────────────────────────────────────────┐
│ Logo | Search | Cart(0) | Account                       │
├─────────────────────────────────────────────────────────┤
│ Home > Men > Shoes > Running Shoes                      │
├────────────────────────┬────────────────────────────────┤
│  ┌──────────────────┐  │ Nike Air Zoom Pegasus         │
│  │                  │  │ ⭐⭐⭐⭐⭐ 4.8 (1,234 reviews)  │
│  │  MAIN IMAGE      │  │                                │
│  │                  │  │ $129.99 $99.99 (-23%)         │
│  │                  │  │ ✓ In Stock                     │
│  └──────────────────┘  │                                │
│  [📷][📷][📷][📷]     │ Color: ⚫ ⚪ 🔴 🔵            │
│                        │ (selected: Black)              │
│                        │                                │
│                        │ Size:  7  8  9  10  11  12    │
│                        │       (selected: 10)           │
│                        │                                │
│                        │ Quantity: [-] 1 [+]           │
│                        │                                │
│                        │ [🛒 Add to Cart]              │
│                        │ [❤️ Wishlist] [⚖️ Compare]   │
├────────────────────────┴────────────────────────────────┤
│ [Description] [Reviews] [Shipping] [Size Guide]        │
├─────────────────────────────────────────────────────────┤
│ Product Description                                     │
│ • Feature 1                                             │
│ • Feature 2                                             │
│ • Feature 3                                             │
├─────────────────────────────────────────────────────────┤
│ You May Also Like                                       │
│ [Product] [Product] [Product] [Product] [→]            │
└─────────────────────────────────────────────────────────┘
```

**Key Challenges:**
- Create image gallery with thumbnail selection (CSS `:target` or `:checked`)
- Implement custom radio buttons for color/size selection
- Create quantity counter with styled buttons
- Make sticky add-to-cart bar that appears on scroll
- Implement tab interface without JavaScript
- Create carousel layout for recommendations
- Handle complex pricing display (sale, original, discount badge)
- Show visual feedback for all selections

**Technical Skills:**
- CSS-only image gallery (`:target` pseudo-class)
- Custom form control styling (radio buttons as swatches)
- Sticky positioning with scroll awareness
- CSS-only tabs (`:checked` or `:target`)
- Badge positioning and styling
- Complex grid layouts for products
- State visualization (selected, disabled, out of stock)
- Advanced pseudo-classes and combinators

---

## 🚀 Additional Assignment Series (To Be Created)

### 4️⃣ NAVIGATION & MENUS SERIES
Progressive development of navigation patterns

#### Branch 1: Simple Navigation Bar (Foundation) 🟢
- Horizontal navigation with links
- Active state styling
- Hover effects
- Logo integration

#### Branch 2: Mega Menu (Enhancement) 🟡
- Multi-level dropdown
- Grid-based mega menu
- Icon integration
- Mobile considerations

#### Branch 3: Animated Mobile Menu (Integration) 🟠
- Hamburger menu animation
- Slide-in navigation
- Overlay and backdrop
- CSS-only toggle

#### Branch 4: Complex Navigation System (Mastery) 🔴
- Multi-level with sub-menus
- Search integration
- Notification badges
- User menu with dropdown
- Breadcrumb trail

---

### 5️⃣ CARD COMPONENTS SERIES
Master the most common UI pattern

#### Branch 1: Basic Card (Foundation) 🟢
- Image, title, description, button
- Box shadow and borders
- Hover effects
- Responsive sizing

#### Branch 2: Card Variations (Enhancement) 🟡
- Horizontal cards
- Overlay cards (text over image)
- Pricing cards
- Testimonial cards

#### Branch 3: Interactive Cards (Integration) 🟠
- Flip cards (front/back)
- Expandable cards
- Cards with badges
- Card hover animations

#### Branch 4: Advanced Card System (Mastery) 🔴
- Masonry grid layout
- Filterable cards (CSS only prep)
- Cards with tabs
- Skeleton loading states

---

### 6️⃣ DATA TABLES SERIES
Working with tabular data

#### Branch 1: Basic Table (Foundation) 🟢
- Semantic table markup
- Table styling (borders, spacing)
- Header styling
- Zebra striping

#### Branch 2: Responsive Table (Enhancement) 🟡
- Mobile-friendly table patterns
- Horizontal scroll container
- Card-style mobile view
- Sticky headers

#### Branch 3: Advanced Table Features (Integration) 🟠
- Sortable column indicators
- Highlighted rows on hover
- Status badges in cells
- Action buttons column
- Fixed columns

#### Branch 4: Data Dashboard Table (Mastery) 🔴
- Complex nested tables
- Expandable rows
- Inline editing styles
- Pagination component
- Filter/search bar integration

---

### 7️⃣ MODAL & OVERLAY SERIES
Focus on layering and accessibility

#### Branch 1: Simple Modal (Foundation) 🟢
- Modal structure
- Overlay backdrop
- Close button
- Centered positioning

#### Branch 2: Modal Variations (Enhancement) 🟡
- Different sizes (small, medium, large, full)
- Slide-in modals from edges
- Modal with header, body, footer
- Image lightbox modal

#### Branch 3: Interactive Modals (Integration) 🟠
- Modal with tabs
- Multi-step wizard modal
- Confirmation modal with actions
- Toast notifications

#### Branch 4: Accessible Modal System (Mastery) 🔴
- Full ARIA implementation
- Focus trap (CSS prep)
- Keyboard navigation indicators
- Nested modals
- Modal queue system (visual only)

---

### 8️⃣ ANIMATION & TRANSITIONS SERIES
Bring life to interfaces

#### Branch 1: Basic Transitions (Foundation) 🟢
- Hover transitions
- Color transitions
- Size/scale transitions
- Opacity fades

#### Branch 2: Keyframe Animations (Enhancement) 🟡
- Loading spinners
- Pulse animations
- Bounce effects
- Slide animations

#### Branch 3: Complex Animations (Integration) 🟠
- Sequential animations
- Staggered animations
- Parallax effects
- Scroll-triggered animations (prep)

#### Branch 4: Advanced Animation Systems (Mastery) 🔴
- 3D transforms
- SVG animations
- Custom easing functions
- Animation performance optimization
- Reduced motion accessibility

---

### 9️⃣ TYPOGRAPHY & CONTENT SERIES
Master the art of readable content

#### Branch 1: Basic Typography (Foundation) 🟢
- Font families and fallbacks
- Font sizing and hierarchy
- Line height and spacing
- Text alignment

#### Branch 2: Rich Text Content (Enhancement) 🟡
- Headings hierarchy (h1-h6)
- Paragraphs, lists, blockquotes
- Inline code and code blocks
- Links and emphasis

#### Branch 3: Advanced Typography (Integration) 🟠
- Responsive typography with clamp()
- Drop caps and initial letters
- Columns for text
- Text shadows and effects
- Web fonts loading

#### Branch 4: Typography System (Mastery) 🔴
- Complete type scale
- Variable fonts
- Text truncation and line clamping
- Vertical rhythm system
- Internationalization considerations

---

### 🔟 ACCESSIBILITY SERIES
Make the web usable for everyone

#### Branch 1: Semantic HTML (Foundation) 🟢
- Proper heading structure
- Landmarks (header, nav, main, footer)
- Alt text for images
- Form labels

#### Branch 2: Keyboard Navigation (Enhancement) 🟡
- Focus styles
- Skip links
- Tab order considerations
- Visible focus indicators

#### Branch 3: ARIA Implementation (Integration) 🟠
- ARIA labels and descriptions
- ARIA live regions
- ARIA states and properties
- Role attributes

#### Branch 4: WCAG Compliance (Mastery) 🔴
- Color contrast testing
- Screen reader testing prep
- Focus management
- Error identification
- Complete WCAG 2.1 AA checklist

---

## 🎓 JavaScript Integration (Future)

After mastering HTML/CSS, each series will get JavaScript enhancement branches:

- **JS Branch 1:** Basic interactivity (event listeners, DOM manipulation)
- **JS Branch 2:** Dynamic data (fetch API, rendering lists)
- **JS Branch 3:** State management (form validation, cart functionality)
- **JS Branch 4:** Advanced features (localStorage, animations, complex logic)

---

## 📊 SQL Integration (Separate Series)

SQL will have its own focused series:
1. Basic queries (SELECT, WHERE, ORDER BY)
2. Joins and relationships
3. Aggregations and grouping
4. Subqueries and views
5. Database design and normalization

---

## 🎯 Assessment Criteria (Every Assignment)

Each branch includes:
- ✅ Clear acceptance criteria checklist
- 🎨 Visual design/wireframe reference
- 🧪 Testing requirements (Lighthouse, validation)
- 📝 Learning objectives
- 🔗 Relevant documentation links
- 💡 Bonus challenges (optional)

---

## 📈 Difficulty Indicators

- 🟢 **Foundation** - Basic concepts, heavily guided
- 🟡 **Enhancement** - More complex, moderate guidance
- 🟠 **Integration** - Combining concepts, minimal guidance
- 🔴 **Mastery** - Advanced techniques, problem-solving focus

---

## 🔄 Implementation Strategy

1. Students complete Branch 1 (Foundation)
2. Create PR and get review/approval
3. Merge to main
4. Create Branch 2 (Enhancement) from main
5. Build upon previous work
6. Repeat for all 4 branches per series

This ensures:
- Progressive skill building
- Git workflow practice
- Building real portfolio pieces
- Seeing evolution of same project
- Understanding refactoring and iteration

---

**Total Assignments Planned:** 10 series × 4 branches = **40 assignments**
**Plus:** JavaScript enhancements and SQL series = **60+ total assignments**

This curriculum provides a comprehensive, progressive learning path from HTML fundamentals to advanced web development techniques.
