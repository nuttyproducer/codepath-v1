# Frequently Asked Questions

Common questions and solutions for CodePath learners.

## Table of Contents

- [Getting Started](#getting-started)
- [Git & GitHub](#git--github)
- [Coding Questions](#coding-questions)
- [Workflow](#workflow)
- [Troubleshooting](#troubleshooting)

---

## Getting Started

### What do I need to get started?

- **Git** installed on your computer ([download](https://git-scm.com/downloads))
- **GitHub account** ([sign up](https://github.com/join))
- **Code editor** (we recommend [VS Code](https://code.visualstudio.com/))
- **Web browser** (Chrome, Firefox, Safari, or Edge)
- Basic terminal/command line knowledge

### Where should I start?

We recommend starting with **Wireframe to Webcode - Foundation** (`01-wireframe/01-foundation/`), but any Foundation-level assignment works as a starting point.

### Do I need to complete assignments in order?

Not strictly, but we recommend:
1. Complete all 🟢 Foundation assignments before 🟡 Enhancement
2. Or complete one full series (all 4 levels) before starting another
3. See [Curriculum Guide](./CURRICULUM.md) for learning path options

### How long does it take to complete CodePath?

- **Beginner pace:** 4-6 months (2-3 assignments/week)
- **Intermediate pace:** 2-3 months (5-7 assignments/week)
- **Intensive pace:** 1-1.5 months (10+ assignments/week)

Focus on learning deeply, not completing quickly!

### Is this course free?

Yes! CodePath is completely free and open source. Fork it, modify it, share it!

---

## Git & GitHub

### I can't push to the repository

**Error:** `Permission denied` or `403 Forbidden`

**Solution:**
```bash
# Check your remote URL
git remote -v

# Should show YOUR username
# If it shows "nuttyproducer", update it:
git remote set-url origin https://github.com/YOUR-USERNAME/codepath.git
```

### I accidentally committed to main

**Solution:**
```bash
# Create a branch with your changes
git branch my-feature-branch

# Reset main to origin
git reset --hard origin/main

# Switch to your new branch
git checkout my-feature-branch
```

### How do I undo my last commit?

```bash
# Keep changes but undo commit (safest)
git reset --soft HEAD~1

# Completely remove commit and changes (careful!)
git reset --hard HEAD~1
```

### What if I have a merge conflict?

```bash
# Pull to see the conflict
git pull origin main

# Open conflicting files, look for:
<<<<<<< HEAD
Your changes
=======
Their changes
>>>>>>> branch-name

# Edit to keep what you want, remove conflict markers

# Stage and commit
git add .
git commit -m "Resolve merge conflict"
```

### Should I use `git mv` or regular `mv`?

If files are already tracked by Git, use `git mv`. Otherwise, regular `mv` works fine.

### Can I delete a branch after merging?

Yes! In fact, you should:
```bash
# Delete local branch
git branch -d branch-name

# Delete remote branch (optional)
git push origin --delete branch-name
```

---

## Coding Questions

### Can I use CSS frameworks like Bootstrap or Tailwind?

Not recommended for these assignments. The goal is to learn CSS fundamentals. Use frameworks in your own projects after mastering the basics!

### Can I use AI assistants (ChatGPT, Copilot, etc.)?

Yes, **BUT**:
- ✅ Use them to explain concepts
- ✅ Ask for hints, not complete solutions
- ✅ Understand every line before using it
- ❌ Don't blindly copy/paste without understanding

### My code works but looks different from the wireframe

That's okay! Wireframes are guides, not pixel-perfect requirements. Focus on:
- Meeting acceptance criteria
- Semantic HTML
- Accessible code
- Clean, readable CSS

### Should I use CSS variables?

Yes! CSS custom properties are encouraged:
```css
:root {
  --color-primary: #007bff;
  --spacing-unit: 1rem;
}
```

### Can I use CSS Grid AND Flexbox together?

Absolutely! Use Grid for 2D layouts (rows AND columns), Flexbox for 1D layouts (rows OR columns). They work great together.

### What about browser compatibility?

Focus on modern browsers (Chrome, Firefox, Safari, Edge - latest 2 versions). Don't worry about IE11 unless specifically mentioned.

---

## Workflow

### Do I need to create a PR for every assignment?

Yes! PRs are part of the learning experience. They teach you:
- Professional workflows
- Code review processes
- Documentation skills
- Git branching

### Can I work on multiple assignments at once?

Technically yes, but not recommended. Finish one assignment (including PR and merge) before starting another to avoid confusion.

### What if I get stuck?

1. **Read error messages** carefully - they usually tell you what's wrong
2. **Use browser DevTools** - Inspect elements, check console
3. **Ask AI assistants** - Describe your problem, ask for hints
4. **Search online** - MDN, CSS-Tricks, Stack Overflow
5. **Take a break** - Sometimes fresh eyes help
6. **Review earlier assignments** - Reinforce fundamentals

### Should I review my own PRs before submitting?

Yes! This is a valuable habit:
- Read through your code as if you're reviewing someone else's
- Check against acceptance criteria
- Test in multiple browsers
- Run accessibility checks

### Can I skip assignments I already know?

You can, but we recommend at least reviewing them. Even "easy" assignments often teach subtle techniques or best practices.

---

## Troubleshooting

### My changes aren't showing in the browser

**Checklist:**
- [ ] Did you save the file? (Check for dot in tab)
- [ ] Did you refresh the browser? (Cmd+R / Ctrl+R)
- [ ] Are you viewing the right HTML file?
- [ ] Check browser console for errors (F12)
- [ ] Try hard refresh (Cmd+Shift+R / Ctrl+Shift+R)
- [ ] Clear browser cache if needed

### HTML validator shows errors but my page looks fine

Visual appearance doesn't mean valid HTML. Validators catch:
- Missing closing tags
- Incorrect nesting
- Invalid attributes
- Accessibility issues

Fix all validator errors - they often cause problems you haven't noticed yet!

### My Lighthouse accessibility score is below 100

Common issues:
- Missing `alt` text on images
- Low color contrast ratios
- Missing form labels
- Improper heading hierarchy
- Links without descriptive text

Run Lighthouse and read the specific issues it reports.

### My CSS isn't being applied

**Common causes:**
```css
/* Typo in selector */
.buton { }  /* Should be .button */

/* More specific rule overriding */
.card { color: blue; }
.card.special { color: red; }  /* This wins */

/* Wrong file linked in HTML */
<link rel="stylesheet" href="style.css">  /* Check path! */

/* CSS syntax error above the rule */
.broken {
  color: red;  /* Missing semicolon causes next rule to fail */
```

Use browser DevTools to:
1. Inspect the element
2. Check which styles are applied
3. See which styles are crossed out (overridden)

### My images aren't loading

**Check:**
```html
<!-- Correct relative path? -->
<img src="images/photo.jpg" alt="Description">

<!-- Case-sensitive filenames -->
<img src="Photo.JPG" alt="Description">  <!-- Won't work on Linux/Mac if file is photo.jpg -->

<!-- Image file exists in project? -->
```

### My layout breaks on mobile

**Common issues:**
- No viewport meta tag:
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```
- Fixed widths without media queries
- Overflow issues (check for elements wider than viewport)
- Missing responsive styles

Test with browser DevTools device toolbar!

### I'm getting CORS errors

You're probably opening HTML files directly (`file:///`). This can cause issues with some features.

**Solutions:**
1. Use VS Code Live Server extension
2. Or run a simple server:
   ```bash
   # Python 3
   python3 -m http.server 8000
   
   # Then visit http://localhost:8000
   ```

---

## Still Stuck?

- 📖 Read the [Getting Started Guide](./GETTING_STARTED.md)
- 🔀 Check the [Git Workflow Guide](./GIT_WORKFLOW.md)
- 📚 Review the [Full Curriculum](./CURRICULUM.md)
- 💬 Ask in [GitHub Discussions](https://github.com/nuttyproducer/codepath/discussions)
- 🐛 Report bugs via [GitHub Issues](https://github.com/nuttyproducer/codepath/issues)

**Remember:** Every expert was once a beginner. Keep learning, keep building! 🚀
