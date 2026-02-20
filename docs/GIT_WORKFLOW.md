# Git Workflow Guide

Complete guide to using Git professionally with CodePath assignments.

## Table of Contents

- [Branch Management](#branch-management)
- [Making Commits](#making-commits)
- [Working with Remotes](#working-with-remotes)
- [Pull Requests](#pull-requests)
- [Troubleshooting](#troubleshooting)
- [Command Reference](#command-reference)

## Branch Management

### Why Branches?

**Never work directly on `main`!** Branches allow you to:
- Work on features independently
- Experiment safely
- Practice professional workflows
- Keep your main branch clean

### Creating Branches

```bash
# Always start from updated main
git checkout main
git pull origin main

# Create and switch to new branch
git checkout -b branch-name

# Naming conventions
git checkout -b wireframe-to-webcode      # ✅ Good
git checkout -b form-controls-advanced    # ✅ Good
git checkout -b navigation-mobile-menu    # ✅ Good
git checkout -b stuff                     # ❌ Too vague
git checkout -b my_branch                 # ❌ Use hyphens, not underscores
```

### Switching Branches

```bash
# Switch to existing branch
git checkout branch-name

# Switch back to main
git checkout main

# See all branches
git branch

# See current branch
git branch --show-current
```

### Deleting Branches

```bash
# Delete merged branch (safe)
git branch -d branch-name

# Force delete unmerged branch (careful!)
git branch -D branch-name

# Delete remote branch
git push origin --delete branch-name
```

## Making Commits

### The Commit Workflow

```bash
# 1. Check what changed
git status

# 2. See detailed changes
git diff

# 3. Stage files for commit
git add .                    # Stage all changes
git add file.html           # Stage specific file
git add folder/             # Stage entire folder

# 4. Review staged changes
git diff --staged

# 5. Commit with message
git commit -m "Add responsive navigation"

# 6. View commit history
git log
git log --oneline           # Compact view
```

### Writing Good Commit Messages

**Format:** `<verb> <what changed>`

**Good examples:**
```bash
git commit -m "Add semantic HTML structure to header"
git commit -m "Fix broken image links in gallery"
git commit -m "Update button styles to match wireframe"
git commit -m "Remove unused CSS rules"
git commit -m "Refactor navigation to use Flexbox"
```

**Bad examples:**
```bash
git commit -m "changes"           # ❌ Too vague
git commit -m "fixed stuff"       # ❌ What stuff?
git commit -m "asdfasdf"         # ❌ Not descriptive
git commit -m "Added some html and css and fixed things"  # ❌ Too much in one commit
```

### Commit Best Practices

**✅ DO:**
- Commit often (after each logical change)
- Write clear, descriptive messages
- Use present tense ("Add" not "Added")
- Start with a verb
- Keep messages under 50 characters

**❌ DON'T:**
- Commit broken code
- Make huge commits with many unrelated changes
- Use vague messages
- Commit commented-out code
- Commit unnecessary files (.DS_Store, node_modules, etc.)

### Amending Commits

```bash
# Forgot to add a file to your last commit?
git add forgotten-file.css
git commit --amend --no-edit

# Want to change the commit message?
git commit --amend -m "New improved message"
```

⚠️ **Warning:** Never amend commits that have been pushed!

## Working with Remotes

### Pushing Changes

```bash
# Push current branch to GitHub
git push origin branch-name

# First push requires upstream setting
git push --set-upstream origin branch-name
# Or shorter:
git push -u origin branch-name

# After first push, just use:
git push
```

### Pulling Changes

```bash
# Pull latest changes from main
git checkout main
git pull origin main

# Pull changes from another branch
git pull origin branch-name
```

### Checking Remote Status

```bash
# View remote URLs
git remote -v

# See remote branches
git branch -r

# See all branches (local + remote)
git branch -a
```

## Pull Requests

### Creating a PR

1. **Push your branch:**
   ```bash
   git push origin branch-name
   ```

2. **On GitHub:**
   - Go to your repository
   - Click "Compare & pull request" (yellow banner)
   - Or: Pull requests tab → New pull request

3. **Fill out PR description:**
   - Title: Brief summary
   - Description: What you built, testing done, questions
   - Use the checklist from assignment README

4. **Create the PR**

### PR Review Process

**If self-learning:**
- Wait a day, review with fresh eyes
- Check against acceptance criteria
- Test in multiple browsers
- Merge when satisfied

**If working with instructor:**
- Wait for feedback
- Make requested changes on same branch
- Push updates (PR updates automatically)
- Respond to comments
- Merge after approval

### After Merging

```bash
# Switch back to main
git checkout main

# Pull the merged changes
git pull origin main

# Delete local branch (it's merged!)
git branch -d branch-name

# Optional: Delete remote branch
git push origin --delete branch-name
```

## Troubleshooting

### "I can't push to the repository"

**Problem:** `Permission denied` or `403 error`

**Solution:**
```bash
# Check your remote URL
git remote -v

# Should show YOUR username, not nuttyproducer
# If wrong, update it:
git remote set-url origin https://github.com/YOUR-USERNAME/codepath.git
```

### "My changes aren't showing up"

**Checklist:**
- [ ] Did you save the file? (Check for dot in editor tab)
- [ ] Did you refresh the browser? (Cmd+R / Ctrl+R)
- [ ] Are you viewing the right file?
- [ ] Check browser DevTools console for errors

### "I need to undo my last commit"

```bash
# Undo commit but keep changes (safest)
git reset --soft HEAD~1

# Undo commit and unstage changes
git reset HEAD~1

# Undo commit and discard changes (DANGEROUS!)
git reset --hard HEAD~1
```

### "I accidentally committed to main"

```bash
# Create a branch with your changes
git branch my-feature-branch

# Reset main to match remote
git reset --hard origin/main

# Switch to your new branch
git checkout my-feature-branch

# Now push the branch
git push origin my-feature-branch
```

### "Merge conflict on pull"

```bash
# Pull latest changes
git pull origin main
# You'll see: CONFLICT (content): Merge conflict in file.html

# Open the conflicting file in your editor
# Look for conflict markers:
<<<<<<< HEAD
Your changes
=======
Their changes
>>>>>>> branch-name

# Choose which changes to keep (or combine them)
# Remove the conflict markers

# Stage the resolved file
git add file.html

# Complete the merge
git commit -m "Resolve merge conflict in file.html"
```

### "I need to get the latest main into my branch"

```bash
# Make sure you're on your branch
git checkout my-branch

# Pull latest main
git pull origin main

# If conflicts, resolve them (see above)

# Push updated branch
git push origin my-branch
```

### "I want to discard all my changes"

```bash
# Discard changes in one file
git checkout -- file.html

# Discard all uncommitted changes (CAREFUL!)
git reset --hard HEAD

# Discard untracked files
git clean -fd
```

### "I pushed bad code and need to undo it"

```bash
# If you HAVEN'T created a PR yet:
git reset --hard HEAD~1  # Undo last commit
git push origin branch-name --force  # Force push

# If PR is already created:
# Better to make a new commit that fixes the issue
git add fixed-files.html
git commit -m "Fix bug in previous commit"
git push origin branch-name
```

## Command Reference

### Essential Commands

```bash
# Status & Information
git status                  # What changed?
git diff                    # See detailed changes
git log                     # Commit history
git log --oneline          # Compact history

# Branching
git branch                  # List branches
git checkout -b name        # Create and switch to branch
git checkout name           # Switch to branch
git branch -d name          # Delete merged branch

# Staging & Committing
git add .                   # Stage all changes
git add file.html          # Stage specific file
git commit -m "message"    # Commit staged changes
git commit --amend         # Modify last commit

# Remote Operations
git push origin branch     # Push branch to GitHub
git pull origin main       # Pull latest from main
git remote -v              # View remote URLs

# Undoing Things
git checkout -- file       # Discard file changes
git reset HEAD file        # Unstage file
git reset --soft HEAD~1    # Undo commit, keep changes
git reset --hard HEAD~1    # Undo commit, discard changes
```

### Advanced Commands

```bash
# Stashing (temporary storage)
git stash                  # Save changes temporarily
git stash pop              # Restore stashed changes
git stash list             # See all stashes

# Viewing History
git log --graph --oneline  # Visual branch history
git show commit-hash       # View specific commit
git blame file.html        # Who changed what line

# Comparing
git diff branch1 branch2   # Compare branches
git diff main...my-branch  # Changes in my-branch since main

# Rebasing (advanced)
git rebase main           # Replay commits on top of main
git rebase --continue     # Continue after conflict
git rebase --abort        # Cancel rebase
```

## Git Best Practices

### ✅ DO:
- Commit early, commit often
- Write clear commit messages
- Pull before you push
- Work on feature branches
- Review your own code before PRs
- Keep main branch stable
- Use `.gitignore` for generated files

### ❌ DON'T:
- Commit directly to main
- Push broken code
- Force push to main
- Commit sensitive data (passwords, API keys)
- Commit large binary files
- Rewrite history that's been pushed
- Make huge commits with unrelated changes

## Getting Help

```bash
# General help
git help

# Help for specific command
git help commit
git help branch

# Quick command info
git commit --help
```

## Next Steps

- 📘 Review [Getting Started Guide](./GETTING_STARTED.md) for setup
- 📚 See [Full Curriculum](./CURRICULUM.md) for all assignments
- ❓ Check [FAQ](./FAQ.md) for common questions

**Practice makes perfect!** The more you use Git, the more natural it becomes.
