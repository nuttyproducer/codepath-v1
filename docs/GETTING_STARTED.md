# Getting Started with CodePath

This guide will walk you through setting up CodePath and completing your first assignment.

## Prerequisites

- Git installed on your computer ([download here](https://git-scm.com/downloads))
- A GitHub account ([sign up here](https://github.com/join))
- A code editor (we recommend [VS Code](https://code.visualstudio.com/))
- Basic terminal/command line knowledge

## Step 1: Fork This Repository

1. Click the **Fork** button at the top right of the [CodePath repository](https://github.com/nuttyproducer/codepath)
2. This creates your own copy under your GitHub account
3. You now have full control to create branches, make commits, and practice PRs

## Step 2: Clone to Your Local Machine

Open your terminal and run:

```bash
# Clone YOUR forked repository (replace YOUR-USERNAME)
git clone https://github.com/YOUR-USERNAME/codepath.git

# Navigate into the project
cd codepath
```

## Step 3: Verify Your Setup

```bash
# Check you're in the right directory
pwd
# Should show: /path/to/codepath

# View repository status
git status
# Should show: On branch main, nothing to commit

# See current branch
git branch
# Should show: * main

# View remote URL
git remote -v
# Should show your GitHub username in the URL
```

## Step 4: Your First Assignment

### Choose Your Starting Point

We recommend starting with **Wireframe to Webcode - Foundation** (`01-wireframe/01-foundation/`), but you can start with any series at the foundation level.

### Create a Feature Branch

**NEVER work directly on `main`!** Always create a branch:

```bash
# Make sure you're on main
git checkout main

# Create and switch to a new branch
git checkout -b wireframe-to-webcode

# Verify you're on the new branch
git branch
# You should see: * wireframe-to-webcode
```

### Read the Assignment

```bash
# Open the assignment README
# Location: 01-wireframe/01-foundation/README.md
```

Read through:
- Learning objectives
- The wireframe/design
- Exercise tasks
- Acceptance criteria
- Resources

### Build Your Solution

1. **Plan first** - Sketch HTML structure on paper before coding
2. **Write HTML** - Start with semantic HTML structure
3. **Style with CSS** - Apply styling incrementally
4. **Test frequently** - Open `index.html` in your browser as you work
5. **Commit often** - Commit after each meaningful change

### Make Commits

```bash
# Stage your changes
git add .

# Commit with a clear message
git commit -m "Add semantic HTML structure"

# Make more changes, then commit again
git commit -m "Add CSS styling for header"
git commit -m "Make layout responsive"
```

**Good commit messages:**
- Start with a verb: Add, Fix, Update, Remove, Refactor
- Be specific about what changed
- Keep under 50 characters
- Use present tense

**Examples:**
- ✅ `Add responsive navigation menu`
- ✅ `Fix image alignment in gallery`
- ✅ `Update button hover states`
- ❌ `changes`
- ❌ `fixed stuff`
- ❌ `asdfasdf`

### Push Your Branch

```bash
# Push your branch to GitHub
git push origin wireframe-to-webcode

# First push might require:
git push --set-upstream origin wireframe-to-webcode
```

## Step 5: Create a Pull Request

### On GitHub:

1. Go to **your forked repository** on GitHub
2. You'll see a yellow banner: **"wireframe-to-webcode had recent pushes"**
3. Click **"Compare & pull request"**
4. Fill out the PR description:

```markdown
## Assignment Completed

**Assignment:** Wireframe to Webcode - Foundation  
**Branch:** `wireframe-to-webcode`

### What I Built
- [x] Semantic HTML structure with proper landmarks
- [x] CSS styling matching the wireframe
- [x] Responsive layout for mobile and desktop
- [x] Accessibility features (alt text, ARIA labels)

### Testing
- [x] Validated HTML with W3C validator
- [x] Tested in Chrome, Firefox, Safari
- [x] Lighthouse Accessibility score: 100

### Screenshots
[Optional: Add screenshots]

### Questions/Notes
- Had trouble with Flexbox alignment initially, but figured it out
- Wondering if there's a better way to structure the footer?
```

5. Click **"Create pull request"**

## Step 6: Code Review

### If Self-Learning:
- Wait a day, then review your own code
- Check against acceptance criteria
- Look for improvements
- Merge your own PR

### If Working with Mentor/Instructor:
- Wait for feedback
- Make requested changes on the same branch
- Push updates (PR updates automatically)
- Once approved, merge

## Step 7: Merge and Continue

After approval:

```bash
# On GitHub, click "Merge pull request" → "Confirm merge"
# Optionally delete the branch on GitHub

# In your terminal:
git checkout main
git pull origin main  # Pull your merged changes
git branch -d wireframe-to-webcode  # Delete local branch
```

## Step 8: Next Assignment

```bash
# Start the next assignment
git checkout -b wireframe-blog-layout

# Or jump to a different series
git checkout -b form-controls
```

## Quick Reference Card

```bash
# Common workflow
git checkout main                    # Switch to main
git pull origin main                 # Get latest changes
git checkout -b branch-name          # Create new branch
# ... make changes ...
git add .                           # Stage changes
git commit -m "Description"         # Commit
git push origin branch-name         # Push to GitHub
# ... create PR on GitHub ...
# ... after merge ...
git checkout main                   # Back to main
git pull origin main                # Get merged changes
git branch -d branch-name           # Delete old branch
```

## Tips for Success

1. **Work incrementally** - Don't try to complete everything at once
2. **Commit frequently** - Small commits are easier to review and revert
3. **Test constantly** - Refresh your browser frequently while coding
4. **Read error messages** - They usually tell you exactly what's wrong
5. **Use browser DevTools** - Inspect elements, check console for errors
6. **Ask for help** - Use the AI agents, discussions, or search online
7. **Review others' work** - Learn from different approaches
8. **Don't copy blindly** - Understand every line you write

## Next Steps

- 📖 Read the [Git Workflow Guide](./GIT_WORKFLOW.md) for detailed Git commands
- 📚 Browse the [Full Curriculum](./CURRICULUM.md) to see all assignments
- ❓ Check the [FAQ](./FAQ.md) for common issues

**Ready to dive deeper?** Complete all Foundation level assignments before moving to Enhancement level!
