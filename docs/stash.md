# Git Stash 📦

Git stash is a feature that allows developers to temporarily save unfinished changes without committing them.

Stash is useful when you need to switch branches, update your project, or work on something else while keeping your current changes safe.

---

# Understanding Git Stash

Normally, Git requires you to commit changes before switching branches.

But sometimes you have unfinished work.

Example:

You are working on a new feature.

Your files are modified.

Suddenly, you need to fix an urgent bug on another branch.

Instead of creating an incomplete commit, you can use stash.

---

# Why Use Stash? 🤔

Git stash is useful for:

- Temporarily saving changes
- Switching branches safely
- Testing another feature
- Cleaning your working directory
- Avoiding unnecessary commits

---

# Creating a Stash 🚀

Save current changes:

git stash


Git stores your changes and returns your working directory to a clean state.

Example:

Before:

Modified files

↓

git stash

↓

Clean working directory

---

# Viewing Stashes 🔍

List all saved stashes:

git stash list


Example:

stash@{0}: WIP on main

stash@{1}: WIP on feature-login


Each stash receives an identifier.

---

# Applying a Stash

Restore changes without deleting the stash:

git stash apply


Apply a specific stash:

git stash apply stash@{0}


The changes return to your working directory.

---

# Popping a Stash

Restore changes and remove the stash:

git stash pop


Difference:

apply:

- Restores changes
- Keeps stash


pop:

- Restores changes
- Deletes stash

---

# Creating a Stash With a Message

Add a description:

git stash push -m "message"


Example:

git stash push -m "unfinished login feature"


View:

git stash list

---

# Including Untracked Files

By default, stash does not include new untracked files.

Include them:

git stash -u


or:

git stash --include-untracked

---

# Viewing Stash Changes

Show the latest stash:

git stash show


Show detailed changes:

git stash show -p


Example:

git stash show -p stash@{0}

---

# Removing a Stash 🗑️

Delete a specific stash:

git stash drop stash@{0}


Example:

git stash drop stash@{1}

---

# Clearing All Stashes

Remove all saved stashes:

git stash clear


Warning:

This permanently deletes all stashed changes.

---

# Stashing Specific Files

Stash selected files:

git stash push filename


Example:

git stash push README.md

---

# Applying Stash From Another Branch

A stash can be created on one branch and applied on another branch.

Example workflow:

Create stash:

git stash


Switch branch:

git switch another-branch


Apply changes:

git stash pop

---

# Real World Stash Workflow 🚀

Situation:

You are working on a feature.

An urgent bug appears.

Workflow:

Save current work:

git stash


Switch branch:

git switch main


Fix the bug.

Return:

git switch feature-branch


Restore work:

git stash pop

---

# Stash Best Practices 💡

- Use meaningful stash messages.
- Do not keep stashes forever.
- Remove old unused stashes.
- Remember that stash is temporary storage.
- Commit finished work instead of keeping it in stash.

---

# Common Stash Commands 📚

git stash

Save current changes.


git stash list

Show saved stashes.


git stash apply

Restore changes.


git stash pop

Restore and remove stash.


git stash drop

Delete a stash.


git stash clear

Delete all stashes.


git stash show

View stash details.

---

# Next Steps 🚀

Continue to:

Tags Guide
