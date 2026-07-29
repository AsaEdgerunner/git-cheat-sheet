# Git Best Practices ⭐

Git is more than a tool for saving code changes.

Using Git correctly helps developers create cleaner projects, collaborate better with teams, and maintain a professional development workflow.

This guide explains the best practices used by experienced developers.

---

# Write Clear Commit Messages 📝

A commit message should explain what changed and why.

Bad:

```
update
fix
changes
```

Good:

```
docs: add installation guide

fix: resolve login validation issue

feat: add user profile page
```

A good commit message makes project history easier to understand.

---

# Use Conventional Commits 📌

A common professional format:

```
type: description
```

Examples:

```
feat: add new feature

fix: fix authentication bug

docs: update documentation

style: format code

refactor: improve code structure

test: add tests

chore: update dependencies
```

Benefits:

- Cleaner history
- Easier searching
- Better teamwork
- Professional workflow

---

# Make Small Commits 🔹

Avoid putting many unrelated changes into one commit.

Bad:

```
Added website
Fixed bug
Updated documentation
Changed styles
```

Better:

```
feat: add homepage

fix: fix navigation bug

docs: update README
```

Small commits are easier to review and undo.

---

# Commit Frequently ⏱️

Do not wait until the entire project is finished.

Good workflow:

1. Make a small change.
2. Test it.
3. Commit it.
4. Continue development.

Example:

```bash
git add file.py
git commit -m "feat: add search feature"
```

---

# Check Status Often 🔍

Before committing:

```bash
git status
```

This helps you understand:

- Modified files
- Untracked files
- Staged changes
- Current branch

Professional developers check status frequently.

---

# Review Changes Before Commit 👀

Before adding files:

```bash
git diff
```

Review exactly what changed.

Then:

```bash
git add filename
git commit -m "message"
```

This prevents accidental commits.

---

# Use Branches Properly 🌿

Do not develop everything directly on main.

Create branches:

```bash
git switch -c feature-name
```

Examples:

```
main
│
├── feature-login
├── feature-dashboard
└── bugfix-payment
```

Benefits:

- Safer development
- Easier testing
- Better collaboration

---

# Protect The Main Branch 🛡️

The main branch should always contain stable code.

Recommended workflow:

```
Feature Branch
        |
        v
Pull Request
        |
        v
Code Review
        |
        v
Main Branch
```

Avoid directly pushing experimental changes to main.

---

# Pull Before Push 🔄

Before uploading changes:

```bash
git pull
```

Then:

```bash
git push
```

This reduces conflicts with remote changes.

---

# Do Not Commit Sensitive Data 🔐

Never commit:

- Passwords
- API keys
- Private tokens
- Database credentials
- Personal information

Bad:

```
config.py

PASSWORD="123456"
```

Use environment variables instead.

Example:

```
.env
```

Add sensitive files to:

```
.gitignore
```

---

# Use .gitignore Correctly 📁

The `.gitignore` file tells Git which files to ignore.

Example:

```
node_modules/

.env

__pycache__/

*.log
```

Common ignored files:

- Dependencies
- Temporary files
- Build files
- Secrets

---

# Create Meaningful Branch Names 🌳

Avoid:

```
test
new
branch1
```

Use:

```
feature/user-login

fix/payment-error

docs/update-readme
```

Good names explain the purpose.

---

# Keep Your Repository Clean 🧹

Avoid storing:

- Temporary files
- Large unnecessary files
- Personal notes
- Generated files

A clean repository is easier to maintain.

---

# Write Good Documentation 📚

A professional project should include:

- README.md
- Installation guide
- Usage instructions
- Contribution guide
- License information

Documentation helps other developers understand the project.

---

# Use Tags For Releases 🏷️

Tags mark important versions.

Example:

```bash
git tag v1.0.0
```

Push tag:

```bash
git push origin v1.0.0
```

Example versions:

```
v1.0.0
v1.1.0
v2.0.0
```

---

# Backup Your Work ☁️

Remote repositories are backups.

Regularly push changes:

```bash
git push
```

A local project without backup is risky.

---

# Learn Recovery Commands 🛠️

Important recovery commands:

Undo changes:

```bash
git restore file
```

Recover commits:

```bash
git reflog
```

Reset commits:

```bash
git reset
```

Understanding recovery prevents panic.

---

# Avoid Force Push ⚠️

Command:

```bash
git push --force
```

can overwrite remote history.

Avoid using it on shared branches.

If necessary, use carefully:

```bash
git push --force-with-lease
```

---

# Review Before Merge 🔀

Before merging:

Check changes:

```bash
git diff main branch-name
```

Update branch:

```bash
git pull
```

Then merge:

```bash
git merge branch-name
```

---

# Professional Git Workflow 🚀

A common workflow:

```
Create Branch
      |
      v
Write Code
      |
      v
Commit Changes
      |
      v
Push Branch
      |
      v
Create Pull Request
      |
      v
Review
      |
      v
Merge
```

---

# Daily Git Checklist ✅

Before finishing work:

- Check git status
- Commit completed changes
- Push to remote
- Write meaningful messages
- Keep branches organized

---

# Common Best Practice Commands 📚

Check status:

```bash
git status
```

Review changes:

```bash
git diff
```

Create branch:

```bash
git switch -c branch-name
```

Update repository:

```bash
git pull
```

Upload changes:

```bash
git push
```

View history:

```bash
git log --oneline
```

---

# Final Advice 💡

Git becomes powerful when used correctly.

The goal is not memorizing commands.

The goal is creating a safe, understandable, and professional development workflow.

Good Git habits make projects easier to build, maintain, and collaborate on.

---

# Project Complete 🎉

You have completed the Git Cheat Sheet documentation.

Keep learning, keep building, and keep contributing to open source.
