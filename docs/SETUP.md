# Complete Setup Guide

This guide will walk you through setting up the MSL Strategic Management vault from scratch, even if you've never used Git or GitHub before.

## Prerequisites

### 1. Install Required Software

#### Obsidian
1. Download from [obsidian.md](https://obsidian.md)
2. Install and create an account (optional but recommended)

#### Git
**Windows:**
1. Download from [git-scm.com](https://git-scm.com)
2. Install with default settings
3. Open "Git Bash" from Start menu

**Mac:**
1. Install via Homebrew: `brew install git`
2. Or download from [git-scm.com](https://git-scm.com)
3. Open Terminal

**Linux:**
```bash
# Ubuntu/Debian
sudo apt install git

# CentOS/RHEL
sudo yum install git
```

### 2. Configure Git (First Time Only)

Open Terminal/Git Bash and run:
```bash
git config --global user.name "Your Full Name"
git config --global user.email "your.email@example.com"
```

## Step-by-Step Setup

### Step 1: Clone the Repository

1. **Choose a location** for your vault (e.g., Desktop, Documents)
2. **Open Terminal/Git Bash** in that location
3. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/MSL-Strategic-management.git
   ```
4. **Navigate to the folder:**
   ```bash
   cd MSL-Strategic-management
   ```

### Step 2: Open in Obsidian

1. **Open Obsidian**
2. **Click "Open folder as vault"**
3. **Select the `MSL-Strategic-management` folder** you just cloned
4. **Trust the vault** when prompted

### Step 3: Verify Setup

You should see the following in Obsidian:
- README.md file
- Folders: docs, strategic-plans, meeting-notes, templates, attachments
- This setup guide in the docs folder

## Authentication Setup

### Using Personal Access Token (Recommended)

1. **Go to GitHub** → Settings → Developer settings → Personal access tokens
2. **Generate new token** with `repo` permissions
3. **Copy the token** (you won't see it again!)
4. **Configure Git to use the token:**
   ```bash
   git config --global credential.helper store
   ```

When you first push/pull, Git will ask for:
- Username: Your GitHub username
- Password: Use your personal access token (not your GitHub password)

### Alternative: SSH Keys (Advanced)

If you prefer SSH:
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Add to GitHub
cat ~/.ssh/id_ed25519.pub
# Copy output and add to GitHub → Settings → SSH keys

# Update remote URL
git remote set-url origin git@github.com:yourusername/MSL-Strategic-management.git
```

## Verification Test

Test your setup:
```bash
# Check current status
git status

# Create a test file
echo "Test setup" > test.md

# Add and commit
git add test.md
git commit -m "Test setup"

# Push to GitHub
git push origin main

# Clean up
rm test.md
git add test.md
git commit -m "Remove test file"
git push origin main
```

## Next Steps

✅ Setup complete! Now read the [Collaboration Guide](COLLABORATION.md) to start contributing.

## Common Issues

**"Permission denied" error?** → Check your authentication setup
**"Repository not found"?** → Verify the repository URL
**Obsidian won't open vault?** → Make sure you selected the correct folder

See [TROUBLESHOOTING.md](TROUBLESHOOTING.md) for more help.