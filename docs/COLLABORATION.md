# Collaboration Guide

Learn how to contribute to the MSL Strategic Management vault safely and effectively.

## Daily Workflow

### Before You Start Working

1. **Open Terminal in vault folder**
2. **Pull latest changes:**
   ```bash
   git pull origin main
   ```
3. **Check status:**
   ```bash
   git status
   ```

### While Working

- **Edit files in Obsidian** as normal
- **Create new notes** in appropriate folders
- **Use templates** from the templates folder
- **Save frequently** (Ctrl/Cmd + S)

### After Making Changes

1. **Check what changed:**
   ```bash
   git status
   ```

2. **Review your changes:**
   ```bash
   git diff
   ```

3. **Add your changes:**
   ```bash
   # Add specific files
   git add filename.md
   
   # Or add all changes
   git add .
   ```

4. **Commit with meaningful message:**
   ```bash
   git commit -m "Add strategic plan for Q2 2024"
   ```

5. **Push to share with team:**
   ```bash
   git push origin main
   ```

## Best Practices

### Commit Messages
Use clear, descriptive messages:
- ✅ "Add meeting notes from strategy session"
- ✅ "Update Q2 goals and objectives"
- ✅ "Create template for project proposals"
- ❌ "Update"
- ❌ "Changes"
- ❌ "Fix"

### File Organization
- **strategic-plans/**: Long-term strategic documents
- **meeting-notes/**: All meeting minutes and notes
- **templates/**: Reusable Obsidian templates
- **attachments/**: Images, PDFs, and other files

### Naming Conventions
- Use descriptive filenames: `Q2-2024-Strategic-Plan.md`
- Include dates: `2024-03-15-Board-Meeting.md`
- No spaces in folder names, use hyphens: `strategic-plans`
- Be consistent with existing naming patterns

## Collaboration Scenarios

### Scenario 1: Adding New Content

```bash
# Start fresh
git pull origin main

# Create your content in Obsidian
# Save your work

# Add and commit
git add .
git commit -m "Add competitive analysis report"
git push origin main
```

### Scenario 2: Updating Existing Content

```bash
# Get latest version
git pull origin main

# Make your edits in Obsidian
# Save changes

# Review what changed
git diff

# Commit your updates
git add .
git commit -m "Update financial projections in strategic plan"
git push origin main
```

### Scenario 3: Handling Conflicts

If someone else modified the same file:

```bash
# When you try to push and get an error:
git pull origin main

# Git will mark conflicts in files like this:
# <<<<<<< HEAD
# Your changes
# =======
# Their changes
# >>>>>>> branch-name

# Edit the file to resolve conflicts
# Remove the conflict markers
# Keep the best parts from both versions

# Commit the resolution
git add .
git commit -m "Resolve merge conflict in strategic plan"
git push origin main
```

## Working with Obsidian Features

### Links and References
- **Internal links**: Use `[[Note Name]]` to link to other notes
- **Tags**: Use `#tag` for categorization
- **Backlinks**: View in right sidebar to see connections

### Templates
1. **Go to** templates folder
2. **Copy a template** to appropriate folder
3. **Rename and customize**
4. **Commit as new content**

### Attachments
1. **Drag files** into Obsidian
2. **Files auto-save** to attachments folder
3. **Commit attachments** with your notes:
   ```bash
   git add .
   git commit -m "Add charts to quarterly report"
   ```

## Team Coordination

### Communication
- **Use meaningful commit messages** to communicate changes
- **Pull regularly** to stay current with team updates
- **Coordinate major changes** with team before implementing

### Backup Strategy
- **Git serves as backup** - all history is preserved
- **GitHub provides remote backup** - your work is safe
- **Local Obsidian vault** can be restored from GitHub anytime

## Quick Reference Commands

```bash
# Daily start
git pull origin main

# Check what's changed
git status
git diff

# Save your work
git add .
git commit -m "Descriptive message"
git push origin main

# Emergency: undo last commit (if not pushed yet)
git reset --soft HEAD~1

# See commit history
git log --oneline
```

## Need Help?

- **Can't push?** Try `git pull origin main` first
- **Merge conflicts?** See "Scenario 3" above
- **Lost work?** Check `git log` - it's probably still there
- **Other issues?** See [TROUBLESHOOTING.md](TROUBLESHOOTING.md)

Remember: Git preserves all history, so your work is always recoverable!