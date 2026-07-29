# Git History 📜

Git history contains the complete record of changes made in a repository.

It allows developers to understand how a project evolved, find previous changes, debug problems, and track the development process.

---

# Understanding Git History

Every commit creates a point in project history.

Example:

A --- B --- C --- D

Each point represents a saved version of the project.

Git stores:

- Commit information
- Author
- Date
- Changed files
- Commit message

---

# Viewing Commit History 🔍

Show complete history:

git log


Example output:

commit a8d7e63

Author: Developer

Date: Today

Update README


---

# Short Commit History

Display commits in one line:

git log --oneline


Example:

a8d7e63 Update README

0522e49 Add configuration guide

31bfc42 Add tags guide

---

# Viewing History as a Graph 🌳

Show branches and commits visually:

git log --graph --oneline --all


Example:

* Add feature

|\
| * Fix bug

|/

* Update documentation


This is useful for understanding branch relationships.

---

# Limiting History Results

Show the latest commits:

git log -n number


Example:

git log -5


Show commits from a specific author:

git log --author="Name"


Example:

git log --author="Asa"

---

# Searching Commit Messages

Search commits by message:

git log --grep="keyword"


Example:

git log --grep="bug"


This helps find related changes quickly.

---

# Viewing File History 📁

Show changes for a specific file:

git log filename


Example:

git log README.md


This displays all commits that modified the file.

---

# Viewing Changes in a Commit

Show commit details:

git show commit-id


Example:

git show a8d7e63


Displays:

- Changed files
- Added lines
- Removed lines
- Commit information

---

# Comparing Changes 🔎

Compare current changes:

git diff


Compare two commits:

git diff commit1 commit2


Example:

git diff a8d7e63 31bfc42

---

# Checking Who Changed a Line

The blame command shows who changed each line.

Command:

git blame filename


Example:

git blame README.md


Shows:

- Author
- Commit
- Line changes

---

# Finding Bugs With History 🐛

Git history is useful for debugging.

Common workflow:

1. Find the problematic change.

2. Check previous commits.

3. Compare versions.

4. Identify the cause.

Useful commands:

git log

git show

git diff

git blame

---

# Searching Deleted Code

Search through all history:

git log -S "text"


Example:

git log -S "function_name"


This finds commits where specific text was added or removed.

---

# Restore Previous Versions

View an old commit:

git checkout commit-id


Example:

git checkout a8d7e63


Return to latest branch:

git switch main


---

# Reflog: Advanced History Recovery 🛠️

Git reflog records changes to HEAD.

Command:

git reflog


Useful for recovering:

- Deleted branches
- Lost commits
- Previous states

Example:

git reflog

git checkout recovered-commit

---

# History Best Practices 💡

- Write clear commit messages.
- Keep commits small.
- Review history before debugging.
- Use meaningful branches.
- Avoid rewriting shared history.
- Keep important releases tagged.

---

# Common History Commands 📚

git log

View commit history.


git log --oneline

Show short history.


git log --graph

Display branch graph.


git show

Show commit details.


git diff

Compare changes.


git blame

Find line authors.


git reflog

Recover lost history.

---

# Next Steps 🚀

Continue to:

Undo Guide
