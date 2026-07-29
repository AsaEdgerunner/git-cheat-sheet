# Git Undo ↩️

Git provides several ways to undo changes.

Depending on the situation, you may want to:

- Remove uncommitted changes
- Undo staged files
- Modify commits
- Reverse published commits
- Recover lost work

Choosing the correct command is important because some actions are destructive.

---

# Understanding Undo in Git

Git has different areas where changes can exist:

Working Directory

↓

Staging Area

↓

Local Repository

↓

Remote Repository


Different undo commands affect different areas.

---

# Git Restore 🔄

`git restore` is used to discard changes in the working directory.

Example:

You modified a file but want to remove those changes:

git restore filename


Example:

git restore README.md


The file returns to the last committed version.

---

# Restoring Multiple Files

Restore all modified files:

git restore .


Warning:

This permanently removes uncommitted changes.

---

# Unstaging Files 📦

If you added a file with:

git add filename


but want to remove it from staging:

git restore --staged filename


Example:

git restore --staged README.md


The changes remain, but the file is no longer staged.

---

# Git Reset 🔙

`git reset` moves the current branch pointer.

It is commonly used to undo commits locally.

There are three main types:

- Soft reset
- Mixed reset
- Hard reset

---

# Soft Reset

Soft reset removes commits but keeps changes staged.

Command:

git reset --soft commit-id


Example:

git reset --soft HEAD~1


Result:

Commit removed.

Changes remain staged.

---

# Mixed Reset

Mixed reset is the default reset mode.

Command:

git reset commit-id


Example:

git reset HEAD~1


Result:

Commit removed.

Changes remain in working directory.

Files become unstaged.

---

# Hard Reset ⚠️

Hard reset removes commits and deletes changes.

Command:

git reset --hard commit-id


Example:

git reset --hard HEAD~1


Warning:

This permanently deletes changes.

Use carefully.

---

# HEAD References

Git provides shortcuts for commits.

Current commit:

HEAD


Previous commit:

HEAD~1


Two commits before:

HEAD~2


Example:

git reset --soft HEAD~2

---

# Undoing the Last Commit

Keep changes:

git reset --soft HEAD~1


Remove commit but keep files:

git reset HEAD~1


Delete everything:

git reset --hard HEAD~1

---

# Git Revert ↩️

`git revert` creates a new commit that reverses another commit.

Example:

git revert commit-id


Unlike reset, revert does not remove history.

---

# Reset vs Revert

| Command | Purpose | Safe for Shared Branches |
|---|---|---|
| restore | Remove file changes | Yes |
| reset | Move branch history | No |
| revert | Create reverse commit | Yes |

---

# When To Use Reset

Use reset when:

- Working alone
- Fixing local history
- Before pushing changes
- Cleaning commits

Example:

You created three bad local commits.

You can reset:

git reset --soft HEAD~3

---

# When To Use Revert

Use revert when:

- Working with a team
- Commit is already pushed
- History should remain visible

Example:

A bug was introduced in production.

Create a reverse commit:

git revert abc123

---

# Recovering Lost Commits 🛠️

Sometimes commits appear lost after reset.

Git keeps records through reflog.

Check:

git reflog


Find the old commit:

git checkout commit-id


Recover:

git reset --hard commit-id

---

# Undo Last Push

If you already pushed a bad commit:

Recommended:

git revert commit-id


Avoid rewriting shared history.

---

# Common Undo Scenarios 🚀

## Scenario 1: Modified Wrong File

Problem:

You changed a file accidentally.

Solution:

git restore filename


---

## Scenario 2: Added Wrong File

Problem:

You staged a file by mistake.

Solution:

git restore --staged filename


---

## Scenario 3: Wrong Commit Message

Change the latest commit:

git commit --amend -m "new message"


---

## Scenario 4: Remove Last Commit

Keep changes:

git reset --soft HEAD~1


---

## Scenario 5: Remove Published Commit

Use:

git revert commit-id

---

# Undo Best Practices 💡

- Prefer restore for file changes.
- Prefer revert for shared branches.
- Avoid hard reset unless necessary.
- Check git status before destructive commands.
- Create backups before rewriting history.
- Understand where your changes exist.

---

# Quick Reference 📚

git restore file

Discard file changes.


git restore --staged file

Remove file from staging.


git reset --soft

Remove commit, keep staged changes.


git reset

Remove commit, keep changes.


git reset --hard

Delete commit and changes.


git revert

Create reverse commit.


git reflog

Recover lost history.

---

# Next Steps 🚀

Continue to:

Aliases Guide
