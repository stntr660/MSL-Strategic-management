# GitHub Repository Setup Guide

Complete guide for setting up and managing the MSL Strategic Management repository on GitHub.

## Initial Repository Creation

### Step 1: Create the Repository
1. **Login to GitHub** with your account
2. **Click "+" → New repository**
3. **Repository name:** `MSL-Strategic-management`
4. **Description:** "MSL Strategic Management collaborative Obsidian vault"
5. **Visibility:** 
   - ✅ **Private** (recommended for strategic content)
   - ❌ Public (only if content is not sensitive)
6. **Initialize:** 
   - ❌ Don't add README (we have one)
   - ❌ Don't add .gitignore (we have one)
   - ❌ Don't add license
7. **Click "Create repository"**

### Step 2: Connect Your Local Vault
```bash
# In your vault directory
git remote set-url origin https://YOUR_TOKEN@github.com/YOUR-USERNAME/MSL-Strategic-management.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your actual GitHub username.

## Repository Settings Configuration

### Security Settings
1. **Go to:** Repository → Settings → General
2. **Features to disable:**
   - ❌ Wikis (we use Obsidian)
   - ❌ Projects (unless needed)
   - ❌ Discussions (use issues instead)
3. **Pull request settings:**
   - ✅ Allow merge commits
   - ✅ Allow rebase merging
   - ❌ Allow auto-merge (for safety)

### Branch Protection (Recommended for Production)
1. **Go to:** Settings → Branches
2. **Add rule for `main` branch:**
   - ✅ Require pull request reviews
   - ✅ Dismiss stale reviews
   - ❌ Require status checks (not needed for docs)
   - ✅ Include administrators

### Collaborator Management
1. **Go to:** Settings → Manage access
2. **For each team member:**
   - Click "Invite a collaborator"
   - Enter their GitHub username or email
   - Choose permission level:
     - **Write:** For regular contributors
     - **Maintain:** For team leads
     - **Admin:** For technical managers

## Access Token Management

### Creating Personal Access Tokens
1. **GitHub Profile** → Settings → Developer settings
2. **Personal access tokens** → Tokens (classic)
3. **Generate new token** with these permissions:
   - ✅ `repo` (full repository access)
   - ✅ `user:email` (access email)
4. **Set expiration:** 90 days (renew regularly for security)
5. **Copy token immediately** (you won't see it again)

### Token Security Best Practices
- ✅ Use tokens instead of passwords
- ✅ Set reasonable expiration dates
- ✅ Regenerate tokens regularly
- ❌ Never commit tokens to repository
- ❌ Don't share tokens via email/chat

## Backup and Recovery

### Repository Backup
GitHub provides built-in backup, but for additional security:
```bash
# Create local backup
git clone --mirror https://github.com/YOUR-USERNAME/MSL-Strategic-management.git MSL-backup.git
```

### Recovery Procedures
**If repository is accidentally deleted:**
1. Contact GitHub support immediately
2. Recreate repository with same name
3. Push from local backup:
   ```bash
   cd MSL-backup.git
   git push --mirror https://github.com/YOUR-USERNAME/MSL-Strategic-management.git
   ```

## Monitoring and Maintenance

### Regular Tasks
**Weekly:**
- Review commit activity
- Check for any security alerts
- Verify collaborator access is current

**Monthly:**
- Renew access tokens if needed
- Review repository settings
- Archive old branches if any

### Security Monitoring
1. **Enable:** Settings → Security & analysis
   - ✅ Dependency graph
   - ✅ Dependabot alerts
   - ✅ Secret scanning alerts

### Activity Monitoring
- **Insights tab:** View contribution activity
- **Security tab:** Monitor for vulnerabilities
- **Settings → Webhooks:** Set up notifications if needed

## Team Management

### Onboarding New Members
1. **Add to repository** with appropriate permissions
2. **Send onboarding package:**
   - Repository URL
   - [Quick Start Guide](../QUICK-START.md)
   - [Setup Guide](SETUP.md)
   - Personal access token instructions

### Offboarding Members
1. **Remove from repository** collaborators
2. **Revoke any shared tokens** they may have had access to
3. **Review recent commits** for any issues
4. **Update team documentation** if they had special roles

## Advanced Features

### GitHub Actions (Optional)
For automated workflows:
```yaml
# .github/workflows/backup.yml
name: Backup
on:
  schedule:
    - cron: '0 2 * * 0'  # Weekly backup
jobs:
  backup:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Create backup
        run: echo "Backup completed"
```

### Issue Templates (Optional)
Create `.github/ISSUE_TEMPLATE/` for standardized issues:
- Bug reports
- Feature requests
- Documentation updates

## Troubleshooting

### Common Repository Issues

**"Permission denied" on push:**
```bash
# Check remote URL includes token
git remote -v
# Update if needed
git remote set-url origin https://TOKEN@github.com/USER/REPO.git
```

**Repository size limits:**
- Individual files: 100MB limit
- Repository total: 1GB soft limit
- Use Git LFS for large files if needed

**Branch protection preventing pushes:**
- Check Settings → Branches
- Temporarily disable protection if needed
- Or create pull requests instead of direct pushes

### Getting Help
- **GitHub Support:** For repository-level issues
- **Team Lead:** For access and permission issues
- **IT Support:** For local Git configuration problems

## Security Checklist

- [ ] Repository set to private
- [ ] All team members added with appropriate permissions
- [ ] Access tokens created and distributed securely
- [ ] Branch protection enabled (if using PR workflow)
- [ ] Security alerts enabled
- [ ] Regular backup process established
- [ ] Team members trained on Git security practices

## Next Steps After Setup

1. **Test the workflow** with a small change
2. **Train team members** on Git basics
3. **Establish regular backup** routine
4. **Monitor repository** activity and security
5. **Review and update** access permissions monthly