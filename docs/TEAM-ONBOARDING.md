# Team Onboarding Checklist

Comprehensive checklist for onboarding new team members to the MSL Strategic Management vault.

## Pre-Onboarding (Administrator Tasks)

### Repository Setup
- [ ] **Create GitHub repository** (if not done)
- [ ] **Configure repository settings** per [GitHub Setup Guide](GITHUB-SETUP.md)
- [ ] **Add team member as collaborator** with appropriate permissions
- [ ] **Prepare onboarding package** (links and instructions)

### Account Preparation  
- [ ] **Verify team member has GitHub account**
- [ ] **Send repository invitation** via GitHub
- [ ] **Provide personal access token instructions**
- [ ] **Share repository URL** and access credentials

## Team Member Onboarding Steps

### 📋 Step 1: Initial Setup (Day 1)
- [ ] **Accept GitHub repository invitation**
- [ ] **Install required software:**
  - [ ] Git ([installation guide](SETUP.md#git))
  - [ ] Obsidian ([download link](https://obsidian.md))
- [ ] **Configure Git with personal details:**
  ```bash
  git config --global user.name "Your Full Name"
  git config --global user.email "your.email@example.com"
  ```
- [ ] **Create personal access token** ([instructions](GITHUB-SETUP.md#creating-personal-access-tokens))

### 📥 Step 2: Clone and Setup (Day 1)
- [ ] **Clone the repository** to local machine
- [ ] **Open vault in Obsidian** (File → Open folder as vault)
- [ ] **Verify all folders and templates** are visible
- [ ] **Test templates functionality** in Obsidian settings

### 🧪 Step 3: Practice Workflow (Day 1-2)
- [ ] **Read collaboration guide** thoroughly
- [ ] **Practice daily workflow:**
  - [ ] `git pull origin main` (get updates)
  - [ ] Create/edit a test file
  - [ ] `git add .` (stage changes)
  - [ ] `git commit -m "Test commit"` (save changes)
  - [ ] `git push origin main` (share changes)
- [ ] **Create test meeting note** using template
- [ ] **Successfully commit and push** test content
- [ ] **Delete test files** and commit cleanup

### 📚 Step 4: Knowledge Transfer (Week 1)
- [ ] **Schedule 30-minute walkthrough** with team lead
- [ ] **Review existing strategic plans** and meeting notes
- [ ] **Understand team conventions:**
  - [ ] File naming patterns
  - [ ] Folder organization
  - [ ] Commit message style
  - [ ] Meeting note standards
- [ ] **Ask questions** about unclear processes

### ✅ Step 5: First Real Contribution (Week 1)
- [ ] **Attend first meeting** and take notes using template
- [ ] **Contribute to strategic planning** document
- [ ] **Review and link** related documents appropriately
- [ ] **Follow proper commit practices** with meaningful messages

## Skill Validation Checklist

### Git Proficiency
- [ ] Can clone repository successfully
- [ ] Understands pull → work → commit → push cycle
- [ ] Can resolve simple merge conflicts
- [ ] Knows how to check status and history
- [ ] Can undo recent commits if needed

### Obsidian Proficiency  
- [ ] Can navigate vault folder structure
- [ ] Can create new notes from templates
- [ ] Understands internal linking with `[[]]`
- [ ] Can attach files to notes appropriately
- [ ] Knows how to organize and tag content

### Collaboration Proficiency
- [ ] Follows team naming conventions
- [ ] Writes clear commit messages
- [ ] Organizes content in appropriate folders
- [ ] Links related documents properly
- [ ] Communicates effectively about changes

## Common First-Week Issues

### Technical Issues
**"Can't push changes"**
- Solution: Run `git pull origin main` first
- Prevention: Always pull before starting work

**"Obsidian won't open vault"**
- Solution: Check folder location, try "Open another vault"
- Prevention: Bookmark vault location

**"Template not working"**
- Solution: Check Settings → Templates → Template folder
- Prevention: Verify templates plugin is enabled

### Process Issues
**"Don't know where to put this file"**
- Solution: Check folder README files for guidance
- Prevention: Review folder structure during onboarding

**"Merge conflict error"**
- Solution: Follow [troubleshooting guide](TROUBLESHOOTING.md)
- Prevention: Communicate about simultaneous edits

## 30-Day Check-in

### Week 2 Review
- [ ] **Technical setup working smoothly**
- [ ] **Contributed to at least 3 documents**
- [ ] **No major technical issues**
- [ ] **Comfortable with daily workflow**

### Week 4 Assessment
- [ ] **Independent contributor** (no constant help needed)
- [ ] **Follows all team conventions** consistently
- [ ] **Contributes meaningfully** to strategic content
- [ ] **Helps onboard newer members**

## Onboarding Support Resources

### Documentation
- **Quick Start:** [QUICK-START.md](../QUICK-START.md)
- **Complete Setup:** [SETUP.md](SETUP.md)
- **Daily Workflow:** [COLLABORATION.md](COLLABORATION.md)
- **Problem Solving:** [TROUBLESHOOTING.md](TROUBLESHOOTING.md)

### Support Contacts
- **Technical Issues:** Repository administrator
- **Process Questions:** Team lead or experienced contributor
- **Content Questions:** Subject matter experts

### Training Resources
- **Git Tutorial:** [Git Handbook](https://guides.github.com/introduction/git-handbook/)
- **Obsidian Help:** [Official Documentation](https://help.obsidian.md)
- **Markdown Guide:** [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)

## Success Metrics

### Individual Success
- **Week 1:** Can complete full workflow independently
- **Week 2:** Contributes regularly without technical issues  
- **Week 4:** Helps mentor newer team members
- **Month 3:** Recognized as proficient contributor

### Team Success
- **Response Time:** <24 hours for onboarding questions
- **Success Rate:** >90% of new members fully onboarded within 2 weeks
- **Retention:** New members actively contributing after 30 days
- **Knowledge Transfer:** Existing members can effectively mentor newcomers

## Feedback and Improvement

### Feedback Collection
- **Day 3:** Quick technical check-in
- **Week 1:** Process and workflow feedback
- **Week 2:** Content and collaboration feedback
- **Month 1:** Overall experience assessment

### Common Feedback Themes
- Documentation clarity and completeness
- Technical setup difficulty
- Learning curve for Git/Obsidian
- Team support and responsiveness

### Continuous Improvement
- Update onboarding based on feedback
- Streamline technical setup process
- Enhance documentation clarity
- Improve team support processes

## Administrator Notes

### Preparation Checklist
- [ ] Repository properly configured
- [ ] All documentation up to date
- [ ] Support team identified and available
- [ ] Onboarding timeline communicated

### Monitoring New Contributors
- [ ] Check GitHub contributions daily (first week)
- [ ] Provide proactive help for common issues
- [ ] Schedule regular check-ins
- [ ] Document any process improvements needed

Remember: Successful onboarding creates productive long-term contributors and strengthens the entire collaborative process.