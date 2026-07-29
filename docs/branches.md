# Git Branches 🌿

Branches are one of the most powerful features of Git.

A branch allows developers to create an independent line of development without affecting the main project.

Branches make it possible to work on new features, fix bugs, and experiment safely.

---

# Understanding Branches

A branch is a movable pointer to a commit.

The default branch in modern Git repositories is usually called:

main

Example:

main
 |
 A --- B --- C


When creating a new branch:

main
 |
 A --- B --- C
          \
           D --- E
           feature


The feature branch can be developed separately.

---

# Why Use Branches? 🤔

Branches are useful for:

- Developing new features
- Fixing bugs
- Testing ideas
- Working with teams
- Keeping the main code stable

---

# Viewing Branches 🔍

Show all local branches:

git branch


Example:

main

feature-login


Show local and remote branches:

git branch -a

---

# Creating a New Branch 🚀

Create a new branch:

git branch branch-name


Example:

git branch feature-login


This creates a branch but does not switch to it.

---

# Switching Branches 🔄

Move to another branch:

git checkout branch-name


Example:

git checkout feature-login


Modern Git also supports:

git switch branch-name

---

# Creating and Switching Together

Create a new branch and switch to it:

git checkout -b branch-name


Example:

git checkout -b feature-profile


Modern version:

git switch -c feature-profile

---

# Checking Current Branch

To see your current branch:

git branch


The active branch is marked with:

*

Example:

* main

feature-login

---

# Renaming a Branch

Rename the current branch:

git branch -m new-name


Example:

git branch -m main

---

# Deleting a Branch 🗑️

Delete a merged branch:

git branch -d branch-name


Example:

git branch -d feature-login


Force delete:

git branch -D branch-name


Use force delete carefully because it removes unmerged work.

---

# Merging Branches 🔀

Branches are combined using merge.

First switch to the destination branch:

git switch main


Then merge:

git merge branch-name


Example:

git merge feature-login

---

# Branch Workflow Example 🚀

A common development workflow:

1. Start from main:

git switch main


2. Create a feature branch:

git switch -c feature-search


3. Make changes.


4. Create commits:

git add .

git commit -m "Add search feature"


5. Return to main:

git switch main


6. Merge changes:

git merge feature-search

---

# Feature Branch Workflow

Many professional teams use feature branches.

Example:

main

develop

feature-login

feature-payment

bugfix-header


Each task gets its own branch.

---

# Remote Branches ☁️

List remote branches:

git branch -r


Download remote branch information:

git fetch


Create a local branch from remote:

git checkout branch-name

---

# Pushing a New Branch

Upload a branch:

git push origin branch-name


Example:

git push origin feature-login


Set upstream tracking:

git push -u origin feature-login

---

# Branch Best Practices 💡

- Keep branches focused on one task.
- Use descriptive branch names.
- Do not make changes directly on main.
- Delete old branches after merging.
- Commit small and meaningful changes.

---

# Common Branch Naming Examples

Feature:

feature/user-profile


Bug fix:

fix/login-error


Documentation:

docs/update-readme


Experiment:

experiment/new-design

---

# Useful Branch Commands 📚

git branch

List branches.


git switch

Change branches.


git checkout

Switch or create branches.


git merge

Combine branches.


git branch -d

Delete branches.


git push

Upload branches.

---

# Next Steps 🚀

Continue to:

Merging Guide
