# Git Remotes ☁️

A remote is a connection between a local Git repository and a repository stored on another server.

Remote repositories allow developers to upload, download, and collaborate on projects with others.

Platforms like GitHub, GitLab, and Bitbucket use remote repositories.

---

# Local Repository vs Remote Repository

Local Repository 💻

A repository stored on your own computer.

It contains:

- Project files
- Commits
- Branches
- History


Remote Repository ☁️

A repository stored on a remote server.

It is used for:

- Backup
- Collaboration
- Sharing code
- Team development

---

# Understanding Origin

When cloning a repository, Git usually creates a remote called:

origin


Origin is the default name for the main remote repository.

Example:

origin -> https://github.com/user/project.git

---

# Viewing Remote Connections 🔍

Show remote names:

git remote


Example:

origin


Show detailed information:

git remote -v


Example:

origin  https://github.com/user/project.git (fetch)

origin  https://github.com/user/project.git (push)

---

# Adding a Remote Repository 🚀

Add a remote connection:

git remote add name url


Example:

git remote add origin https://github.com/user/project.git


The name "origin" is commonly used for the main remote.

---

# Removing a Remote

Remove a remote connection:

git remote remove remote-name


Example:

git remote remove origin

---

# Changing Remote URL

Update an existing remote URL:

git remote set-url origin new-url


Example:

git remote set-url origin https://github.com/user/new-project.git

---

# Fetching Changes 📥

Fetch downloads information from a remote repository without changing your files.

Command:

git fetch


Fetch from a specific remote:

git fetch origin


Fetch updates:

- New branches
- New commits
- Remote history

---

# Pulling Changes 📥

Pull downloads changes and automatically integrates them.

Command:

git pull


Equivalent to:

git fetch

git merge


Example:

git pull origin main

---

# Pushing Changes 📤

Push uploads local commits to a remote repository.

Command:

git push


Push to a specific remote branch:

git push origin main


Example:

git push origin feature-login

---

# Setting Upstream Branch

An upstream branch connects a local branch with a remote branch.

Command:

git push -u origin branch-name


Example:

git push -u origin main


After this, Git remembers the remote branch.

Future pushes can use:

git push

---

# Tracking Branches 🌿

A tracking branch automatically knows which remote branch it follows.

View tracking information:

git branch -vv


Example:

main abc123 [origin/main] Latest changes

---

# Cloning Remote Repositories

Clone downloads a complete repository.

Command:

git clone repository-url


Example:

git clone https://github.com/user/project.git


After cloning:

- Remote named origin is created.
- Remote branches become available.
- Local main branch tracks origin/main.

---

# Remote Branches

List remote branches:

git branch -r


List all branches:

git branch -a


Remote branches are references to branches stored on the server.

---

# Deleting Remote Branches 🗑️

Delete a remote branch:

git push origin --delete branch-name


Example:

git push origin --delete feature-old

---

# Renaming Remote Branch

Rename a branch locally:

git branch -m old-name new-name


Push the new branch:

git push origin new-name


Delete the old remote branch:

git push origin --delete old-name

---

# Common Remote Workflow 🚀

Clone project:

git clone repository-url


Create changes:

git add .

git commit -m "Add new feature"


Upload changes:

git push


Download updates:

git pull

---

# Remote Best Practices 💡

- Keep remote URLs correct.
- Pull changes before starting new work.
- Push commits regularly.
- Use meaningful branch names.
- Protect main branch.
- Avoid force pushing shared branches.
- Review changes before pushing.

---

# Useful Remote Commands 📚

git remote

List remote repositories.


git remote -v

Show remote URLs.


git remote add

Add a remote.


git fetch

Download remote information.


git pull

Download and merge changes.


git push

Upload commits.


git branch -r

Show remote branches.

---

# Next Steps 🚀

Continue to:

Stash Guide
