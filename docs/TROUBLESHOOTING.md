# Troubleshooting Guide

Common issues and solutions for the MSL Strategic Management vault.

## Git Issues

### "Permission denied" or "Authentication failed"

**Symptoms:** Can't push or pull from GitHub
**Solutions:**
1. **Check your credentials:**
   ```bash
   git config --global user.name
   git config --global user.email
   ```

2. **Update stored credentials:**
   ```bash
   git config --global credential.helper store
   ```
   Next push/pull will ask for username and token again.

3. **Verify remote URL:**
   ```bash
   git remote -v
   ```
   Should show: `https://github.com/yourusername/MSL-Strategic-management.git`

### "Repository not found"

**Cause:** Wrong repository URL or no access
**Solution:**
```bash
git remote set-url origin https://github.com/yourusername/MSL-Strategic-management.git
```

### "Your local changes would be overwritten"

**Cause:** Local changes conflict with remote changes
**Solution:**
```bash
# Save your work first
git stash

# Pull latest changes
git pull origin main

# Restore your work
git stash pop

# Resolve any conflicts, then commit
git add .
git commit -m "Merge local changes with remote updates"
```

### "Failed to push"

**Common causes and fixes:**
1. **Someone else pushed first:**
   ```bash
   git pull origin main
   git push origin main
   ```

2. **Divergent branches:**
   ```bash
   git pull origin main --rebase
   git push origin main
   ```

## Obsidian Issues

### Vault won't open
1. **Check folder location** - make sure you're opening the correct folder
2. **Try "Open another vault"** → Browse to your cloned folder
3. **Restart Obsidian** and try again

### Changes not saving
1. **Check file permissions** - make sure you can write to the folder
2. **Close and reopen** the problematic file
3. **Restart Obsidian**

### Templates not working
1. **Check templates folder exists** in vault
2. **Enable Templates plugin** in Settings → Core plugins
3. **Set template folder** in Settings → Templates → Template folder location

### Links broken after moving files
1. **Use Obsidian's file rename** instead of manual rename
2. **Update links manually** or use Find & Replace
3. **Check for case sensitivity** in filenames

## Merge Conflicts

### What they look like
```markdown
# Strategic Goals

<<<<<<< HEAD
Our primary goal is market expansion.
=======
Our primary goal is customer retention.
>>>>>>> main
```

### How to resolve
1. **Open the file** in Obsidian or text editor
2. **Choose which version to keep** or combine them
3. **Remove the conflict markers** (`<<<<<<<`, `=======`, `>>>>>>>`)
4. **Save the file**
5. **Commit the resolution:**
   ```bash
   git add .
   git commit -m "Resolve merge conflict in strategic goals"
   ```

## File Issues

### "File not found" errors
1. **Check spelling** and case sensitivity
2. **Use relative paths** in Obsidian links: `[[filename]]`
3. **Check .gitignore** - make sure files aren't being ignored

### Large files won't commit
**Git has size limits. For large files:**
1. **Use attachment folder** for organization
2. **Consider external storage** for very large files (>50MB)
3. **Compress files** when possible

## Workflow Issues

### "I forgot to pull before editing"
```bash
# If you haven't committed yet:
git stash
git pull origin main
git stash pop

# If you already committed:
git pull origin main
# Resolve any conflicts
git push origin main
```

### "I committed to the wrong branch"
```bash
# Create new branch from current commit
git branch correct-branch

# Reset current branch to previous state
git reset --hard HEAD~1

# Switch to correct branch
git checkout correct-branch
```

### "I want to undo my last commit"
```bash
# If you haven't pushed yet:
git reset --soft HEAD~1  # Keep changes
# or
git reset --hard HEAD~1  # Lose changes

# If you already pushed:
git revert HEAD  # Creates new commit that undoes the last one
```

## Getting Help

### Check status and history
```bash
# See current state
git status

# See recent commits
git log --oneline -10

# See what changed in last commit
git show

# See all branches
git branch -a
```

### Recovery commands
```bash
# Find lost commits
git reflog

# Restore deleted file from last commit
git checkout HEAD -- filename.md

# Reset to specific commit
git reset --hard commit-hash
```

## Prevention Tips

1. **Always pull before starting work:** `git pull origin main`
2. **Commit frequently** with descriptive messages
3. **Test your setup** with small changes first
4. **Keep backups** of important local changes
5. **Communicate** with team about major changes
6. **Use branches** for experimental work

## Emergency Contacts

If you can't resolve an issue:
1. **Contact the repository maintainer**
2. **Create an issue** on GitHub with error details
3. **Ask team members** who have used Git before

## Still Need Help?

Include this information when asking for help:
- Your operating system
- The exact error message
- What you were trying to do
- Output of `git status` and `git log --oneline -5`