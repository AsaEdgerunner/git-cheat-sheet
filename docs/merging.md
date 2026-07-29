# Git Merging 🔀

Merging is the process of combining changes from one branch into another branch.

Merge allows developers to bring completed work from feature branches into the main development line.

It is one of the most important operations in Git workflows.

---

# Understanding Merge

When working with branches, each branch has its own history.

Example:

main

A --- B --- C


feature

A --- B --- C --- D --- E


After merging:

main

A --- B --- C ------- F

              \     /

              D --- E


The changes from the feature branch become part of the main branch.

---

# Why Use Merge? 🤔

Merge is useful for:

- Combining completed features
- Integrating team members' work
- Adding bug fixes
- Updating the main branch
- Maintaining project history

---

# Basic Merge Workflow 🚀

First, switch to the branch that will receive changes.

Example:

git switch main


Then merge another branch:

git merge branch-name


Example:

git merge feature-login

---

# Fast-Forward Merge ⚡

A fast-forward merge happens when the target branch has no new commits.

Example:

Before:

main

A --- B


feature

A --- B --- C --- D


After merge:

main

A --- B --- C --- D


Git simply moves the branch pointer forward.

---

# Three-Way Merge 🔀

A three-way merge happens when both branches have new commits.

Example:

main

A --- B --- C


feature

A --- B --- D


Git creates a new merge commit:

A --- B --- C --- M

          \     /

            D


The merge commit combines both histories.

---

# Performing a Merge

Example:

Create a feature branch:

git switch -c feature-login


Make changes and commit:

git add .

git commit -m "Add login feature"


Return to main:

git switch main


Merge:

git merge feature-login

---

# Viewing Merge History

Show commit history:

git log --oneline


Show branch graph:

git log --graph --oneline --all


Example:

*   Merge feature-login
|\
| * Add login page
| * Add login validation
|
* Update README

---

# Merge Conflicts ⚠️

A merge conflict happens when Git cannot automatically combine changes.

Common reasons:

- Two branches modify the same line
- A file was deleted in one branch
- Changes are incompatible

---

# Example Conflict

Git may show:

<<<<<<< HEAD

Current branch changes

=======

Incoming branch changes

>>>>>>> feature-branch


You must manually choose the correct content.

---

# Resolving Merge Conflicts 🛠️

Steps:

1. Open the conflicted file.

2. Find conflict markers.

3. Edit the file and keep the correct version.

4. Add the resolved file:

git add filename


5. Complete the merge:

git commit

---

# Checking Merge Status

Check current merge state:

git status


Git will show:

- Conflicted files
- Files waiting for resolution
- Merge progress

---

# Aborting a Merge

If you want to cancel a merge:

git merge --abort


This returns your repository to the state before the merge started.

---

# Deleting a Merged Branch

After a successful merge:

git branch -d branch-name


Example:

git branch -d feature-login

---

# Merge Best Practices 💡

- Pull the latest changes before merging.
- Keep branches small and focused.
- Resolve conflicts carefully.
- Write meaningful merge commit messages.
- Test the project after merging.
- Do not merge broken code into main.

---

# Common Merge Commands 📚

git merge

Combine branches.


git merge --abort

Cancel a merge.


git log --graph

View branch history.


git status

Check merge status.


git branch -d

Delete merged branches.

---

# Next Steps 🚀

Continue to:

Rebasing Guide
