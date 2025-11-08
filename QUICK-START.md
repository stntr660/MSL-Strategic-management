# 🚀 Quick Start Guide

Get up and running with the MSL Strategic Management vault in 5 minutes.

## For Repository Owner (First Setup)

### 1. Create GitHub Repository
1. Go to [GitHub](https://github.com) → New Repository
2. Name: `MSL-Strategic-management`
3. Set to **Private** (recommended for strategic content)
4. Don't initialize with README (we have one)
5. Click "Create repository"

### 2. Push Your Vault
```bash
# In your vault folder
git remote set-url origin https://YOUR_TOKEN@github.com/YOUR-USERNAME/MSL-Strategic-management.git
git push -u origin main
```

### 3. Invite Collaborators
1. Go to repository → Settings → Manage access
2. Click "Invite a collaborator"
3. Add team members' GitHub usernames
4. Send them the repository URL

## For Team Members (Contributors)

### Option A: I'm New to Git (Recommended)
Follow the complete [Setup Guide](docs/SETUP.md) - it walks through everything step by step.

### Option B: I Know Git (Quick Setup)
```bash
# Clone repository
git clone https://github.com/USERNAME/MSL-Strategic-management.git
cd MSL-Strategic-management

# Open in Obsidian
# File → Open folder as vault → Select this folder
```

## Daily Workflow (Everyone)

### 📥 Start Your Day
```bash
git pull origin main
```

### ✏️ Work in Obsidian
- Edit files normally
- Create new notes
- Use templates from `templates/` folder

### 📤 End Your Session  
```bash
git add .
git commit -m "Your descriptive message"
git push origin main
```

## Essential Commands

| Task | Command |
|------|---------|
| Get latest changes | `git pull origin main` |
| See what changed | `git status` |
| Save your work | `git add . && git commit -m "message"` |
| Share with team | `git push origin main` |
| See history | `git log --oneline` |

## 🆘 Quick Help

**Error pushing?** → Run `git pull origin main` first
**Merge conflict?** → See [Troubleshooting Guide](docs/TROUBLESHOOTING.md)
**Lost?** → Check [Collaboration Guide](docs/COLLABORATION.md)

## 📋 Your First Tasks

1. **Clone the repository** using method above
2. **Create your first note** using a template
3. **Practice the daily workflow** with a test commit
4. **Read the** [Collaboration Guide](docs/COLLABORATION.md) for detailed workflows

## 🎯 Success Checklist

- [ ] Repository cloned locally
- [ ] Vault opens in Obsidian
- [ ] Can see templates and folder structure  
- [ ] Successfully made a test commit and push
- [ ] Team members have access and can collaborate

**Need more help?** Check the complete [Setup Guide](docs/SETUP.md) or [Troubleshooting](docs/TROUBLESHOOTING.md).