# Git Aliases ⚡

Git aliases allow developers to create shortcuts for frequently used Git commands.

Instead of typing long commands repeatedly, you can create shorter and easier commands.

Example:

Instead of:

git status

You can create:

git st

---

# Why Use Git Aliases? 🤔

Git aliases help with:

- Faster command execution
- Less typing
- Better productivity
- Creating a personal Git workflow
- Simplifying complex commands

---

# Creating a Simple Alias

Syntax:

git config --global alias.name "command"


Example:

Create an alias for status:

git config --global alias.st status


Now you can use:

git st


Instead of:

git status

---

# Common Git Aliases 🚀

## Status Alias

Create:

git config --global alias.st status


Usage:

git st

---

## Commit Alias

Create:

git config --global alias.cm commit


Usage:

git cm -m "message"

---

## Checkout Alias

Create:

git config --global alias.co checkout


Usage:

git co branch-name

---

## Branch Alias

Create:

git config --global alias.br branch


Usage:

git br

---

# Advanced Log Alias 🌳

A very popular professional alias:

git config --global alias.lg "log --oneline --graph --decorate --all"


Usage:

git lg


Example output:

* a8d7e63 Update README
|\
| * Fix bug
|/
* Initial commit

---

# Creating a Better Status Alias

Create:

git config --global alias.s "status -sb"


Usage:

git s


Example:

## main

 M README.md

---

# Viewing Existing Aliases 🔍

Show all Git configuration:

git config --list


Show only aliases:

git config --get-regexp alias


Example:

alias.st=status

alias.lg=log --oneline --graph

---

# Removing an Alias 🗑️

Remove an alias:

git config --global --unset alias.name


Example:

git config --global --unset alias.st

---

# Useful Professional Aliases 💻

## Short Status

Command:

git config --global alias.s "status -sb"


---

## Pretty Log

Command:

git config --global alias.tree "log --graph --decorate --pretty=oneline --abbrev-commit"


Usage:

git tree

---

## Last Commit

Command:

git config --global alias.last "log -1 HEAD"


Usage:

git last

---

## Undo Last Commit Safely

Command:

git config --global alias.undo "reset HEAD~1 --mixed"


Usage:

git undo

---

# Creating Aliases With Multiple Commands

Git aliases can run shell commands.

Use:

!


Example:

git config --global alias.visual "!gitk"


Run:

git visual

---

# Project Specific Aliases

Aliases can also be stored only inside one repository.

Remove:

--global


Example:

git config alias.project "command"


This only affects the current repository.

---

# Global vs Local Aliases

Global:

git config --global

Available in all repositories.


Local:

git config

Available only in current repository.

---

# Recommended Developer Alias Setup ⭐

Example:

git config --global alias.st "status -sb"

git config --global alias.co checkout

git config --global alias.br branch

git config --global alias.cm commit

git config --global alias.lg "log --oneline --graph --decorate --all"


This creates a clean Git workflow.

---

# Alias Best Practices 💡

- Keep aliases short and memorable.
- Avoid replacing common Git commands.
- Document important aliases.
- Share useful aliases with your team.
- Do not create confusing shortcuts.

---

# Common Alias Commands 📚

git config --global alias.name command

Create an alias.


git config --get-regexp alias

List aliases.


git config --global --unset alias.name

Remove an alias.


---

# Next Steps 🚀

Continue to:

GitHub Guide
