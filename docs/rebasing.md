# Git Rebasing 🔥

Rebase is an advanced Git operation that allows developers to move or replay commits on top of another branch.

Rebase is commonly used to create a cleaner and more organized project history.

---

# Understanding Rebase

A rebase takes commits from one branch and applies them on top of another branch.

Example:

Before:

main

A --- B --- C


feature

A --- B --- D --- E


After rebase:

main

A --- B --- C


feature

A --- B --- C --- D' --- E'


The commits are recreated on top of the latest main branch.

---

# Why Use Rebase? 🤔

Rebase is useful for:

- Keeping commit history clean
- Updating feature branches
- Avoiding unnecessary merge commits
- Preparing code before merging
- Organizing development history

---

# Merge vs Rebase 🔀

Merge:

- Preserves complete history
- Creates merge commits
- Safer for shared branches


Rebase:

- Creates cleaner history
- Rewrites commits
- Better for local branches


Example:

Merge:

A --- B --- C ------ M

          \        /

           D --- E


Rebase:

A --- B --- C --- D' --- E'

---

# Basic Rebase Workflow 🚀

Update your main branch:

git switch main

git pull


Switch to your feature branch:

git switch feature-name


Start rebase:

git rebase main

---

# Simple Rebase Example

Create a feature branch:

git switch -c feature-search


Make changes:

git add .

git commit -m "Add search feature"


Update from main:

git rebase main

---

# Interactive Rebase 🛠️

Interactive rebase allows editing multiple commits.

Command:

git rebase -i HEAD~number


Example:

git rebase -i HEAD~3


This opens a list of recent commits.

You can:

- Reorder commits
- Rename commit messages
- Combine commits
- Remove commits

---

# Squashing Commits

Squashing combines multiple commits into one.

Example:

Before:

Add button

Fix button

Improve button style


After squash:

Add button feature


This creates cleaner history.

---

# Rebase Commands

Start rebase:

git rebase branch-name


Continue after conflict:

git rebase --continue


Cancel rebase:

git rebase --abort


Skip a problematic commit:

git rebase --skip

---

# Rebase Conflicts ⚠️

Conflicts can happen when Git cannot apply changes automatically.

Common reasons:

- Same file changed in multiple commits
- Conflicting code changes
- Deleted files

---

# Resolving Rebase Conflicts

Steps:

1. Check conflict status:

git status


2. Open conflicted files.

3. Fix the changes manually.

4. Add resolved files:

git add filename


5. Continue rebase:

git rebase --continue

---

# Aborting a Rebase

If something goes wrong:

git rebase --abort


This returns the repository to the state before the rebase started.

---

# Rebasing Shared Branches ⚠️

Avoid rebasing branches that other developers already use.

Why?

Because rebase changes commit history.

Good candidates:

- Personal feature branches
- Local experiments
- Private development branches

Avoid:

- main
- production branches
- Shared team branches

---

# Force Push After Rebase

After rebasing a published branch, Git may require:

git push --force


A safer option:

git push --force-with-lease


This protects against overwriting other people's changes.

---

# Rebase Best Practices 💡

- Understand rebase before using it.
- Never rewrite public history.
- Use rebase to clean local work.
- Pull latest changes before rebasing.
- Test your project after rebasing.
- Use force-with-lease instead of force when possible.

---

# Common Rebase Commands 📚

git rebase

Apply commits on top of another branch.


git rebase -i

Interactive rebase.


git rebase --continue

Continue after resolving conflicts.


git rebase --abort

Cancel rebase.


git push --force-with-lease

Safely update rewritten history.

---

# Next Steps 🚀

Continue to:

Remotes Guide
