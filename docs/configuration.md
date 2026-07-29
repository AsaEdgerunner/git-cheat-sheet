# Git Configuration ⚙️

After installing Git, the next step is configuring your identity and preferences.

Git uses this information to identify the author of commits and customize your workflow.

---

# Setting Your Identity 👤

## Configure Username

Set your Git username:

git config --global user.name "Your Name"

Example:

git config --global user.name "AsaEdgerunner"

---

## Configure Email

Set your Git email:

git config --global user.email "you@example.com"

Example:

git config --global user.email "your-email@example.com"

---

# Viewing Git Configuration 🔍

Show all Git settings:

git config --list

Example output:

user.name=Your Name

user.email=you@example.com

---

# Checking Specific Settings

Check username:

git config user.name


Check email:

git config user.email

---

# Changing Configuration 🔄

Change username:

git config --global user.name "New Name"


Change email:

git config --global user.email "new@email.com"

---

# Default Branch Configuration 🌿

Modern Git repositories usually use the main branch.

Set default branch:

git config --global init.defaultBranch main

---

# Setting Git Editor ✏️

Set Nano as Git editor:

git config --global core.editor nano

---

# Git Aliases 🚀

Aliases create shortcuts for common commands.

Create status shortcut:

git config --global alias.st status

Now:

git st

is the same as:

git status


---

Create checkout shortcut:

git config --global alias.co checkout


Create branch shortcut:

git config --global alias.br branch


Create commit shortcut:

git config --global alias.cm commit

---

# Removing Configuration 🗑️

Remove username:

git config --global --unset user.name

Remove email:

git config --global --unset user.email

---

# Best Practices 💡

- Use the same email as your GitHub account.
- Keep your username professional.
- Configure Git before creating commits.
- Review your configuration regularly.

---

# Next Steps 🚀

Continue to:

Repositories Guide
