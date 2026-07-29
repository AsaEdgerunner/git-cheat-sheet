# Git Commits 📝

A commit is a snapshot of changes in a Git repository.

Commits allow developers to save the current state of their project, track history, and return to previous versions when needed.

A good commit history makes projects easier to understand, maintain, and collaborate on.

---

# Understanding Commits

Every commit contains:

- Changed files
- Author information
- Date and time
- A unique commit identifier
- A commit message

Each commit receives a unique hash.

Example:

a8d7e63

This identifier allows Git to find and reference specific changes.

---

# The Basic Commit Workflow 🚀

A normal Git workflow has three steps:

1. Modify files

Change your project files.

2. Stage changes

Command:

git add filename


3. Create a commit

Command:

git commit -m "Your message"


Example:

git add README.md

git commit -m "Update README documentation"

---

# Checking Commit History 🔍

View previous commits:

git log


Short version:

git log --oneline


Example:

a8d7e63 Update README

0522e49 Add configuration guide

bb0f578 Add repository guide

---

# Viewing a Specific Commit

To see details about a commit:

git show commit-id


Example:

git show a8d7e63


This displays:

- Changed files
- Added lines
- Removed lines
- Commit information

---

# Writing Good Commit Messages ✍️

A commit message should explain what changed.

Good examples:

Add user authentication feature

Fix login validation bug

Update installation documentation


Bad examples:

changes

update

fix stuff

---

# Conventional Commits 📚

Many professional projects use Conventional Commits.

Format:

type: description


Common types:

feat

A new feature.


Example:

feat: add dark mode support


fix

A bug fix.


Example:

fix: resolve login error


docs

Documentation changes.


Example:

docs: update installation guide


style

Code formatting changes.


refactor

Code improvements without changing behavior.


test

Adding or updating tests.


chore

Maintenance tasks.


Example:

chore: update dependencies

---

# Changing the Last Commit 🔄

Modify the latest commit:

git commit --amend


Change only the message:

git commit --amend -m "New commit message"


Use this carefully because it changes commit history.

---

# Undoing a Commit

Create a new commit that reverses changes:

git revert commit-id


Example:

git revert a8d7e63


This is safer than deleting history.

---

# Removing the Last Commit

Move back one commit:

git reset HEAD~1


Warning:

Reset changes history and should be used carefully.

---

# Comparing Commits

Compare changes between commits:

git diff commit1 commit2


Example:

git diff a8d7e63 bb0f578

---

# Commit Best Practices 💡

- Make small and focused commits.
- Write clear commit messages.
- Commit often.
- Do not commit unfinished work.
- Do not include passwords or secrets.
- Keep commits related to one purpose.

---

# Useful Commit Commands 📚

git add

Prepare changes for commit.


git commit

Create a new commit.


git log

View commit history.


git show

Show commit details.


git revert

Safely undo a commit.


git diff

Compare changes.

---

# Next Steps 🚀

Continue to:

Branches Guide
