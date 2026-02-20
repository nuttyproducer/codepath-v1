<table>
  <tr>
    <td width="15%" align="center" valign="middle">
      <img src="https://raw.githubusercontent.com/nuttyproducer/nuttyproducer/main/codepathlogo.svg" width="60" height="60" alt="Codepath Logo" />
    </td>
    <td width="85%" valign="middle">
      <h1>HYF Assignments Collection</h1>
      A comprehensive, progressive curriculum for learning HTML, CSS, JavaScript, and Git workflow through hands-on assignments.
    </td>
  </tr>
</table>

## 🎯 What is This?

This repository contains a complete learning path with **60+ assignments** organized in progressive difficulty levels. Each assignment series has 4 branches that build upon each other, teaching you to iterate and improve your code just like professional developers do.

Perfect for:
- Self-taught developers
- Coding bootcamps and instructors
- Anyone wanting to master HTML/CSS fundamentals
- Learning Git workflow with pull requests and code reviews

## 📚 What You'll Learn

- **HTML:** Semantic markup, forms, accessibility, document structure
- **CSS:** Layouts (Flexbox, Grid), styling, animations, responsive design
- **Git:** Branching, pull requests, code reviews, version control
- **Problem Solving:** Progressive challenges from beginner to advanced

## 🚀 Getting Started

### Step 1: Fork This Repository

1. Click the **Fork** button at the top right of this page
2. This creates your own copy of the repository under your GitHub account
3. You now have full control to make changes, create branches, and submit PRs

### Step 2: Clone to Your Local Machine

**Open your terminal** (we strongly encourage using Git from the command line!) and run:

```bash
# Clone YOUR forked repository (replace YOUR-USERNAME with your GitHub username)
git clone https://github.com/YOUR-USERNAME/assignments-collection.git

# Navigate into the project folder
cd assignments-collection
```

### Step 3: Verify Your Setup

```bash
# Check that you're in the right directory
pwd

# View the repository status
git status

# See the current branch (should be 'main')
git branch

# View the remote repository URL
git remote -v
```

## 🤖 Copilot AI Agents — Your Built-In Tutors

This repository includes **3 custom GitHub Copilot agents** that act as specialised teaching assistants inside VS Code. They are configured to guide you with hints and questions rather than just giving you answers — because the best way to learn is to figure things out yourself with a little nudge.

| Agent | Focus | Best Used For |
|---|---|---|
| 🎨 **frontend-mentor** | HTML & CSS | Layout debugging, responsive design, semantic HTML |
| 💛 **javascript-coach** | JavaScript | Learning JS concepts, debugging errors, guided hints |
| 🔧 **git-guide** | Git & Version Control | Git commands, fixing mistakes, understanding workflow |

### Quick Setup

Copy the agent files into your VS Code user prompts folder, then restart VS Code:

**macOS / Linux:**
```bash
cp .github/copilot-agents/frontend-mentor.agent.md ~/Library/Application\ Support/Code/User/prompts/
cp .github/copilot-agents/javascript-coach.agent.md ~/Library/Application\ Support/Code/User/prompts/
cp .github/copilot-agents/git-guide.agent.md ~/Library/Application\ Support/Code/User/prompts/
```

**Windows (PowerShell):**
```powershell
$dest = "$env:APPDATA\Code\User\prompts"
Copy-Item .github\copilot-agents\frontend-mentor.agent.md $dest
Copy-Item .github\copilot-agents\javascript-coach.agent.md $dest
Copy-Item .github\copilot-agents\git-guide.agent.md $dest
```

Then in VS Code, open Copilot Chat (**Cmd+Shift+I** / **Ctrl+Shift+I**), click the mode selector, and choose your agent.

📄 **Full setup guide:** [`.github/copilot-agents/SETUP.md`](.github/copilot-agents/SETUP.md)

---

## 📋 Assignment Series Overview

This curriculum features **10 progressive series** with **4 difficulty levels** each:

1. **🎨 Wireframe to Webcode** - Design interpretation, complex layouts
2. **📝 Form Controls** - Forms, inputs, validation
3. **🚲 Bikes for Refugees** - HTML structure, layouts, animations
4. **🗺️ Navigation** - Navbars, menus, mobile patterns
5. **🃏 Card Components** - Cards, variants, interactions
6. **📊 Data Tables** - Tables, responsive strategies
7. **🪟 Modals & Overlays** - Dialogs, drawers, accessibility
8. **✨ Animations** - Transitions, keyframes, choreography
9. **🔤 Typography** - Font systems, rich text, fluid type
10. **♿ Accessibility** - WCAG compliance, semantic HTML, ARIA

Each series builds from 🟢 Foundation → 🟡 Enhancement → 🟠 Integration → 🔴 Mastery

📁 **Folder Structure:** `{01-10}-{series-name}/{01-04}-{level-name}/`

## 🔄 Git Workflow - IMPORTANT

**For each assignment, you MUST work on a separate branch and create a pull request for review.**

This simulates real-world professional development workflows. You'll practice:
- Creating feature branches
- Making commits with clear messages
- Pushing branches to GitHub
- Creating pull requests
- Reviewing code
- Merging approved changes

### 💻 Command Line First!
```bash
# Make sure you're on the main branch first
git checkout main

# Pull the latest changes (important if you've merged previous PRs)
git pull origin main

# Create and switch to a new branch for your assignment
git checkout -b bikes-for-refugees

# Verify you're on the correct branch
git branch
# You should see: * bikes-for-refugees
```

**Branch naming conventions:**
- Use descriptive, lowercase names
- Separate words with hyphens
- Examples: `bikes-for-refugees`, `form-controls-advanced`, `wireframe-dashboard`

```bash
# Push your branch to YOUR forked repository on GitHub
git push origin bikes-for-refugees

# If it's the first push, Git might ask you to set the upstream:
git push --set-upstream origin bikes-for-refugees
```

After pushing, you'll see a URL in the terminal to create a pull request. You can click it or follow the next step.

#### 6. Create a Pull Request (PR)

1. **Go to YOUR forked repository on GitHub** (github.com/YOUR-USERNAME/assignments-collection)
2. You'll see a yellow banner saying "**Your-branch-name** had recent pushes" with a button **"Compare & pull request"** - click it
3. Or click the **"Pull requests"** tab, then **"New pull request"**

**Fill out your PR description:**
```

**🔁 Repeat this cycle** for every assignment!

---

## 🧰 Essential Git Commands Reference

### Checking Status
```bash
git status              # See what files have changed
git diff                # See detailed changes
git log                 # View commit history
Each assignment series has **4 progressive branches** that build upon each other:

### 3️⃣ 🚲 Bikes for Refugees Series
**Skills:** HTML structure, CSS styling, layouts, semantic markup

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `bikes-for-refugees` | 🟢 Foundation | Semantic HTML, basic CSS, Flexbox |
| `bikes-for-refugees-responsive` | 🟡 Enhancement | Responsive design, CSS Grid, media queries |
| `bikes-for-refugees-animations` | 🟠 Integration | CSS animations, transitions, effects |
| `bikes-for-refugees-advanced` | 🔴 Mastery | Forms, dark mode, accessibility |

📂 Location: `03-bikes-for-refugees/`

---
## ✅ Before Submitting Your Pull Request

Use this checklist for every PR:

### Code Quality
- [ ] All acceptance criteria from the assignment README are met
- [ ] Code is properly indented and formatted
- [ ] No console errors in browser DevTools
- [ ] HTML is valid (check with [W3C Validator](https://validator.w3.org/))
## 🆘 Troubleshooting Common Issues

### "I can't push to the repository"
- Make sure you forked the repository first
- Check you're pushing to YOUR fork, not the original repo
- Verify: `git remote -v` should show YOUR username

### "My changes aren't showing up"
- Make sure you saved the files
- Refresh your browser (Cmd+R or Ctrl+R)
- Clear browser cache if needed
- Check you're viewing the right file

## 📅 Planning and Managing Your Work

### Track Your Progress

Create a simple progress tracker (use GitHub Issues, Projects, or a spreadsheet):

| Assignment | Branch | Status | Started | Completed | PR Link |
|-----------|--------|--------|---------|-----------|---------|
| Bikes for Refugees - Foundation | `bikes-for-refugees` | ✅ Done | 2026-02-01 | 2026-02-05 | [#1](link) |
| Bikes for Refugees - Responsive | `bikes-for-refugees-responsive` | 🔄 In Progress | 2026-02-06 | - | - |
| Form Controls - Foundation | `form-controls` | 📋 Todo | - | - | - |

### Study Schedule Suggestions

**Beginner Pace (2-3 assignments per week):**
- Day 1: Read assignment, plan approach
- Day 2-3: Build and test
- Day 4: Create PR, self-review
- Day 5: Revisions if needed, merge

**Intensive Pace (5-7 assignments per week):**
- 1-2 assignments per day
- Focus on one difficulty level per week

**Recommended Order:**
1. Complete all 🟢 Foundation assignments first
2. Then all 🟡 Enhancement assignments
3. Then all 🟠 Integration assignments
4. Finally all 🔴 Mastery assignments

This builds a strong foundation before advancing.

---

## 🎓 For Instructors & Bootcamps

### Using This Repository

1. **Fork** this repository to your organization
2. Students fork YOUR version
3. Students submit PRs to their own forks
4. They share PR links for review
5. You provide feedback on their forks

### Customization

Feel free to:
- Add your own assignments
- Modify existing ones
- Create cohort-specific branches
- Add automated testing
- Integrate with your LMS

### Issues & Contributions

Found a bug or have a suggestion? Please open an issue or submit a PR!

---

## 📜 License

This repository is open source and available for educational use. Feel free to fork, modify, and share!

---

## 🙏 Acknowledgments

Inspired by:
- [Hack Your Future Belgium](https://github.com/HackYourFutureBelgium)
- [Code Your Future](https://codeyourfuture.io/)
- Real-world professional development workflows

---

## 🌟 Show Your Progress!

Completed an assignment? Share it!
- Tweet your accomplishment with #100DaysOfCode
- Share your portfolio with the community
- Write a blog post about what you learned
- Help others by reviewing their PRs

---

**Happy Coding! 🚀**

*Remember: The goal isn't to complete assignments quickly—it's to learn deeply and build strong fundamentals. Take your time, ask questions, and enjoy the journey!*

---

## 📊 Repository Stats

- **Total Assignments:** 60+
- **Difficulty Levels:** 4 (Foundation → Mastery)
- **Technologies:** HTML, CSS, JavaScript (coming), SQL (coming)
- **Focus:** Progressive learning with real-world Git workflow

**Start your journey today! Fork this repo and create your first branch. 💪**

### "I need to undo my last commit"
```bash
# Undo commit but keep changes
git reset --soft HEAD~1

# Undo commit and discard changes (⚠️ be careful!)
git reset --hard HEAD~1
```

### "Merge conflict on pull"
```bash
# Fetch the latest changes
git fetch origin main

# Merge or rebase
git merge origin/main
# Or: git rebase origin/main

# Resolve conflicts in your editor
# Then: git add . && git commit
```

### "I accidentally committed to main"
```bash
# Create a new branch with your changes
git branch my-feature-branch

# Reset main to origin
git reset --hard origin/main

# Switch to your new branch
git checkout my-feature-branch
```

---

## 🆘 Getting Help

### Documentation
- Check the individual assignment README files for detailed requirements
- Review [`CURRICULUM_PROGRESSION.md`](./CURRICULUM_PROGRESSION.md) for the full learning path
- Read Git documentation: https://git-scm.com/doc

### Resources
- [MDN Web Docs](https://developer.mozilla.org/) - HTML/CSS reference
- [CSS-Tricks](https://css-tricks.com/) - CSS tutorials and guides
- [Git Documentation](https://git-scm.com/doc) - Official Git documentation
- [GitHub Docs](https://docs.github.com/) - GitHub-specific features
- [W3C Validator](https://validator.w3.org/) - HTML validation
- [Lighthouse](https://developers.google.com/web/tools/lighthouse) - Testing tool

### Community
- Ask questions in the repository discussions
- Review other learners' PRs to learn different approaches
- Join study groups or coding communities
- Share your progress on social media with #100DaysOfCode

---

## 🚫 Important Rules

### ✅ DO:
- **DO** work on feature branches, never directly on `main`
- **DO** commit often with clear, descriptive messages
- **DO** test your work thoroughly before creating a PR
- **DO** use Git from the terminal to build strong fundamentals
- **DO** review your own code before requesting review
- **DO** read error messages carefully - they usually tell you what's wrong
- **DO** ask questions if you're stuck

### ❌ DON'T:
- **DON'T** commit directly to the `main` branch
- **DON'T** merge your own PRs without review (unless self-learning)
- **DON'T** copy code you don't understand
- **DON'T** skip testing before committing
- **DON'T** commit unnecessary files (.DS_Store, node_modules, etc.)
- **DON'T** be afraid to make mistakes - that's how we learn!
- [ ] Branch is pushed to GitHub
- [ ] No unnecessary files committed (.DS_Store, node_modules, etc.)
- [ ] Commits are atomic (one feature/fix per commit)

### Documentation
- [ ] Pull request has a clear, detailed description
- [ ] Checklist in PR shows what was completed
- [ ] Any questions or challenges are noted
- [ ] Screenshots included (optional but helpful)t | Custom styling, complex inputs |
| `form-controls-dynamic` | 🟠 Integration | Dependent fields, live feedback |
| `form-controls-validation` | 🔴 Mastery | Multi-step forms, complete checkout |

📂 Location: `02-form-controls/`

---

### 1️⃣ 🎨 Wireframe to Webcode Series
**Skills:** Reading designs, HTML structure, CSS layout, typography

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `wireframe-to-webcode` | 🟢 Foundation | Basic wireframe interpretation |
| `wireframe-complex-layout` | 🟡 Enhancement | Blog layout, sticky sidebar |
| `wireframe-dashboard` | 🟠 Integration | Dashboard, complex grid |
| `wireframe-ecommerce` | 🔴 Mastery | Product page, advanced features |

📂 Location: `01-wireframe/`

---

### 4️⃣ 🗺️ Navigation Series
**Skills:** Navbars, dropdowns, mega menus, mobile hamburger menus

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `navigation-navbar` | 🟢 Foundation | Semantic nav, Flexbox, hover states |
| `navigation-mega-menu` | 🟡 Enhancement | Multi-level dropdowns, CSS Grid |
| `navigation-mobile-menu` | 🟠 Integration | Hamburger animation, slide-in panel |
| `navigation-advanced` | 🔴 Mastery | Docs-style nav system, sidebar accordion |

📂 Location: `04-navigation/`

---

### 5️⃣ 🃏 Card Components Series
**Skills:** Card layouts, variants, interactions, advanced card systems

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `cards-basic` | 🟢 Foundation | Semantic card, hover lift, CSS Grid |
| `cards-variations` | 🟡 Enhancement | Overlay, pricing, testimonial cards |
| `cards-interactive` | 🟠 Integration | Flip card, expandable, status badges |
| `cards-advanced` | 🔴 Mastery | Masonry, skeletons, filter, container queries |

📂 Location: `05-cards/`

---

### 6️⃣ 📊 Data Tables Series
**Skills:** Semantic tables, responsive strategies, complex table UIs

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `tables-basic` | 🟢 Foundation | Semantic HTML, zebra striping, scope |
| `tables-responsive` | 🟡 Enhancement | Sticky column/header, card-style mobile |
| `tables-advanced` | 🟠 Integration | Checkboxes, badges, bulk actions |
| `tables-dashboard` | 🔴 Mastery | Expandable rows, mini charts, pagination |

📂 Location: `06-tables/`

---

### 7️⃣ 🪟 Modals & Overlays Series
**Skills:** Dialog element, drawers, lightboxes, accessibility

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `modals-basic` | 🟢 Foundation | `<dialog>`, `::backdrop`, animation |
| `modals-variations` | 🟡 Enhancement | Sized modals, drawer, lightbox, bottom sheet |
| `modals-interactive` | 🟠 Integration | Wizard, toasts, confirmation dialogs |
| `modals-accessible` | 🔴 Mastery | WCAG compliance, focus rings, tooltips |

📂 Location: `07-modals/`

---

### 8️⃣ ✨ Animations & Transitions Series
**Skills:** CSS transitions, keyframes, complex choreography, performance

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `animations-transitions` | 🟢 Foundation | Hover states, easing, form transitions |
| `animations-keyframes` | 🟡 Enhancement | Spinners, skeletons, staggered entrances |
| `animations-complex` | 🟠 Integration | Parallax, scroll-driven, `@property` |
| `animations-advanced` | 🔴 Mastery | 3D flips, SVG animation, performance audit |

📂 Location: `08-animations/`

---

### 9️⃣ 🔤 Typography & Content Series
**Skills:** Font systems, rich text, fluid type, design tokens

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `typography-basic` | 🟢 Foundation | Font stacks, hierarchy, utility classes |
| `typography-rich` | 🟡 Enhancement | Drop caps, counters, callouts, `<kbd>` |
| `typography-advanced` | 🟠 Integration | `clamp()`, multi-column, OpenType features |
| `typography-system` | 🔴 Mastery | Variable fonts, design tokens, style guide |

📂 Location: `09-typography/`

---

### 🔟 ♿ Accessibility Series
**Skills:** Semantic HTML, keyboard navigation, ARIA, WCAG compliance

| Branch | Difficulty | Focus |
|--------|-----------|-------|
| `accessibility-semantic` | 🟢 Foundation | Landmarks, heading hierarchy, alt text |
| `accessibility-keyboard` | 🟡 Enhancement | Skip links, `:focus-visible`, tab order |
| `accessibility-aria` | 🟠 Integration | ARIA labels, live regions, custom roles |
| `accessibility-wcag` | 🔴 Mastery | Contrast ratios, reflow, full audit |

📂 Location: `10-accessibility/`

---

## 🎓 How to Use This Repository

### For Individual Learners:
1. Fork and clone the repository
2. Work through assignments in order (foundation → mastery)
3. Create PRs to practice the workflow
4. Review your own code after completion
5. Merge and move to the next assignment
6. Build a portfolio of completed projects

### For Study Groups:
1. One person forks the repository
2. Add collaborators (Settings → Collaborators)
3. Everyone clones the shared fork
4. Take turns reviewing each other's PRs
5. Practice code review and feedback
6. Learn from each other's approaches

### For Instructors:
1. Students fork this repository
2. Students submit PRs to their own forks
3. Share PR links for instructor review
4. Provide feedback directly on GitHub
5. Students iterate based on feedback
6. Track progress through completed branches

---

## 🎯 Learning Objectives

By completing these assignments, you will:

✅ Master semantic HTML and accessibility  
✅ Build responsive layouts with Flexbox and Grid  
✅ Create animations and transitions  
✅ Implement complex forms with validation  
✅ Read and implement wireframes accurately  
✅ Use Git professionally (branching, PRs, merging)  
✅ Write clean, maintainable code  
✅ Test and debug effectively  
✅ Build a portfolio of real projects  
✅ Prepare for JavaScript and backend development
```bash
git checkout main       # Switch to main branch
git checkout -b name    # Create and switch to new branch
git branch -d name      # Delete a merged branch
git branch -D name      # Force delete a branch
```

### Remote Operations
```bash
git push origin branch  # Push branch to GitHub
git pull origin main    # Pull latest changes from main
git fetch               # Download changes without merging
git remote -v           # View remote repository URLs
```

### Undoing Changes
```bash
git checkout -- file    # Discard changes to a file
git reset HEAD file     # Unstage a file
git reset --soft HEAD~1 # Undo last commit, keep changes
git reset --hard HEAD~1 # Undo last commit, discard changes (⚠️ dangerous)
```

### Getting Help
```bash
git help                # General help
git help <command>      # Help for specific command
git <command> --help    # Alternative help syntax
```

---

## 📁 Assignment Series Overviewe Accessibility score of 100

### Testing:
- Tested in Chrome, Firefox, and Safari
- Validated HTML with W3C validator
- Checked accessibility with Lighthouse

### Screenshots:
[Optional: Add screenshots of your work]

### Questions/Notes:
- Had trouble with Flexbox alignment at first, but figured it out
- Wondering if there's a better way to handle the image gallery?
```

4. **Request a review** (if working with a mentor/instructor)
5. Click **"Create pull request"**

#### 7. Code Review Process

**If you're learning solo:**
- Review your own code after a day or two
- Check against the acceptance criteria
- Look for opportunities to improve
- You can merge your own PR for practice

**If working with others:**
- Wait for review feedback
- Make requested changes on the same branch
- Commit and push updates
- The PR automatically updates
- Once approved, merge the PR

#### 8. Merge Your PR and Continue

After your PR is approved (or if self-reviewing):

```bash
# On GitHub, click "Merge pull request" → "Confirm merge"
# Optionally, delete the branch on GitHub after merging

# Back in your terminal, switch to main
git checkout main

# Pull the merged changes from GitHub
git pull origin main

# Delete your local branch (it's merged, you don't need it anymore)
git branch -d bikes-for-refugees

# Verify it's deleted
git branch
```

#### 9. Start the Next Assignment

Now you're back on `main` with your completed work merged. Start the next assignment:

```bash
# Create a new branch for the next level/assignment
git checkout -b bikes-for-refugees-responsive

# Or start a completely different assignment
git checkout -b form-controls
git status

# View the actual changes in detail
git diff

# View changes for a specific file
git diff path/to/file.html
```

#### 4. Commit Your Work

Commit regularly with clear, descriptive messages:
```bash
# Stage all your changes
git add .

# Or stage specific files
git add index.html styles/style.css

# Commit with a meaningful message
git commit -m "Add semantic HTML structure to header"

# Make more changes, then commit again
git commit -m "Style navigation bar with Flexbox"
git commit -m "Add responsive design for mobile devices"
git commit -m "Fix accessibility issues in form labels"
```

**Good commit messages:**
- Start with a verb (Add, Fix, Update, Remove, Refactor)
- Be specific about what changed
- Keep it under 50 characters for the first line
- Use present tense

**Examples:**
- ✅ "Add responsive navigation menu"
- ✅ "Fix broken image links in gallery"
- ✅ "Update button styles to match wireframe"
- ❌ "changes"
- ❌ "fixed stuff"
- ❌ "updated files"

#### 5. Push Your Branch to GitHub
Make your changes, test your code, and commit regularly:
```bash
git add .
git commit -m "Add form validation"
git commit -m "Style form with CSS"
```

#### 4. Push your branch to GitHub
```bash
git push origin <your-branch-name>

# Examples:
# git push origin bike-for-refugees
# git push origin form-controls
# git push origin wireframe-to-webcode
```

#### 5. Create a Pull Request
- Go to your repository on GitHub
- Click "Compare & pull request" for your branch
- Write a clear description of what you've completed
- Request a review from your mentor/instructor
- Wait for feedback before merging

#### 6. After approval, merge and start the next assignment
```bash
# Switch back to main
git checkout main

# Pull the latest changes (after your PR is merged)
git pull origin main

# Create a new branch for the next assignment
git checkout -b <next-assignment-name>
```

## 📁 Assignment Details

### 🎨 wireframe-to-webcode
Navigate to `01-wireframe/01-foundation/` and check the README for requirements.

**Branch name:** `wireframe-to-webcode`

### 📝 form-controls
Navigate to `02-form-controls/01-foundation/` and check the README for requirements.

**Branch name:** `form-controls`

### 🚲 bike-for-refugees
Navigate to `03-bikes-for-refugees/01-foundation/` and check the README for requirements.

**Branch name:** `bike-for-refugees`

## ✅ Before Submitting Your Pull Request

- [ ] All acceptance criteria from the assignment README are met
- [ ] Code has been tested in a browser
- [ ] Lighthouse Accessibility score is 100
- [ ] HTML is valid (check with [W3C Validator](https://validator.w3.org/))
- [ ] All files are committed and pushed to your branch
- [ ] Pull request has a clear description

## 🆘 Need Help?

- Check the individual assignment README files for detailed requirements
- Review the prep materials in your curriculum
- Ask your mentor or classmates for support

## 🚫 Important Rules

- **DO NOT** work directly on the `main` branch
- **DO NOT** merge your own pull requests without approval
- **DO** commit often with clear commit messages
- **DO** test your work thoroughly before requesting review

## 📅 Planning and managing your work

All the coursework is listed as issues on this repo. 

You will copy these issues to your Coursework Planner, which is one repo that will hold all your coursework and assignments for the entire course.

If you do not already have your own Coursework Planner, set one up now:

https://github.com/HackYourFutureBelgium/My-Coursework-Planner

---


Good luck with your assignments! 🎉
