# Git Troubleshooting Guide 🛠️

Git is a powerful version control system, but sometimes developers encounter errors and unexpected situations.

This guide explains common Git problems, their causes, and practical solutions.

---

# Repository Not Found ❌

GitHub cannot find the repository.

Error:

```bash
remote: Repository not found.
fatal: repository not found
```

Common causes:

- Wrong repository URL.
- Repository was deleted.
- Repository is private.
- User does not have permission.

---

# Checking Remote Repository

View current remote:

```bash
git remote -v
```

Example:

```bash
origin https://github.com/user/project.git
```

Change remote URL:

```bash
git remote set-url origin https://github.com/user/new-project.git
```

---

# Authentication Failed 🔐

Error:

```bash
remote: Authentication failed
```

Cause:

GitHub does not allow normal account passwords for Git authentication.

Solutions:

- Use Personal Access Token.
- Use SSH authentication.

---

# Setting Up SSH Authentication

Generate SSH key:

```bash
ssh-keygen -t ed25519 -C "email@example.com"
```

Start SSH agent:

```bash
eval "$(ssh-agent -s)"
```

Add SSH key:

```bash
ssh-add ~/.ssh/id_ed25519
```

Test connection:

```bash
ssh -T git@github.com
```

---

# Permission Denied 🚫

Error:

```bash
Permission denied (publickey)
```

Cause:

GitHub cannot find your SSH key.

Check SSH files:

```bash
ls ~/.ssh
```

Make sure your public key exists.

---

# Nothing To Commit 📦

Message:

```bash
nothing to commit, working tree clean
```

This is not an error.

It means:

- No changes exist.
- Everything is already committed.

Check status:

```bash
git status
```

---

# Failed To Push Changes 🚀

Error:

```bash
failed to push some refs
```

Cause:

The remote repository contains changes that your local repository does not have.

Solution:

Download remote changes:

```bash
git pull origin main
```

Then push again:

```bash
git push
```

---

# Push Rejected ⚠️

Error:

```bash
Updates were rejected because the remote contains work
```

Cause:

Another user pushed changes before you.

Solution:

```bash
git pull --rebase origin main
```

Then:

```bash
git push
```

---

# Merge Conflicts 🔀

A merge conflict happens when Git cannot automatically combine changes.

Example:

```text
<<<<<<< HEAD

Your changes

=======

Other changes

>>>>>>> branch-name
```

Solution:

1. Open the conflicted file.
2. Choose the correct changes.
3. Remove conflict markers.
4. Save the file.

Then:

```bash
git add filename
```

Commit:

```bash
git commit
```

---

# Detached HEAD State 🧩

Message:

```bash
HEAD detached at commit
```

This means you are viewing a commit directly instead of working on a branch.

Create a new branch:

```bash
git switch -c new-branch
```

Return to main:

```bash
git switch main
```

---

# Recover Deleted Files 🗑️

Restore a deleted file:

```bash
git restore filename
```

Restore all files:

```bash
git restore .
```

---

# Undo Last Commit ↩️

Keep changes:

```bash
git reset --soft HEAD~1
```

Remove commit and changes:

```bash
git reset --hard HEAD~1
```

Warning:

The `--hard` option permanently removes changes.

---

# Recover Lost Commits 🔎

Git keeps a record of previous HEAD movements.

View recovery history:

```bash
git reflog
```

Recover a commit:

```bash
git checkout commit-id
```

Create a recovery branch:

```bash
git switch -c recovery-branch commit-id
```

---

# Wrong Branch Problem 🌿

Check current branches:

```bash
git branch
```

Switch branch:

```bash
git switch branch-name
```

Create a new branch:

```bash
git switch -c feature-name
```

---

# Cleaning Untracked Files 🧹

Preview files that will be removed:

```bash
git clean -n
```

Remove untracked files:

```bash
git clean -f
```

Be careful because removed files cannot be easily recovered.

---

# Useful Debug Commands 🔍

Check repository status:

```bash
git status
```

View commit history:

```bash
git log --oneline
```

Compare changes:

```bash
git diff
```

View remote information:

```bash
git remote -v
```

---

# Troubleshooting Workflow ✅

When Git has a problem:

1. Check the current status.

```bash
git status
```

2. Read the error message carefully.

3. Check recent commits.

```bash
git log --oneline
```

4. Check branches.

```bash
git branch
```

5. Check remote settings.

```bash
git remote -v
```

6. Apply the safest solution.

---

# Troubleshooting Best Practices 💡

- Do not panic when Git shows errors.
- Read error messages carefully.
- Create commits before risky operations.
- Use branches for experiments.
- Avoid destructive commands unless you understand them.
- Keep regular backups for important projects.

---

# Common Troubleshooting Commands 📚

```bash
git status
```

Check current repository state.


```bash
git log
```

View commit history.


```bash
git reflog
```

Recover lost commits.


```bash
git restore
```

Restore files.


```bash
git switch
```

Change branches.


```bash
git pull
```

Download changes.


```bash
git push
```

Upload changes.

---

# Next Steps 🚀

Continue to:

Best Practices Guide
