# GitHub Guide 🌐

GitHub is a platform that hosts Git repositories and provides tools for software development, collaboration, and open-source projects.

Git manages the version history of your code.

GitHub provides a place to store, share, review, and collaborate on Git projects.

---

# Git vs GitHub 🤔

Git:

- A distributed version control system.
- Runs locally on your computer.
- Tracks changes in files.
- Manages commits and branches.


GitHub:

- A cloud platform for Git repositories.
- Hosts remote repositories.
- Provides collaboration tools.
- Enables code review and project management.

---

# Creating a GitHub Repository 🚀

To start a project on GitHub:

1. Create a new repository.
2. Choose a repository name.
3. Add description.
4. Select visibility:
   - Public
   - Private
5. Create repository.

---

# Connecting Local Repository to GitHub

Create a local repository:

git init


Add remote repository:

git remote add origin repository-url


Example:

git remote add origin https://github.com/user/project.git


Check remote:

git remote -v

---

# Cloning a Repository 📥

Clone an existing repository:

git clone repository-url


Example:

git clone https://github.com/user/project.git


This downloads the repository to your computer.

---

# Pushing Changes to GitHub 🚀

Upload local commits:

git push


First push:

git push -u origin main


The `-u` option connects your local branch with the remote branch.

---

# Pulling Changes From GitHub 📥

Download new changes:

git pull


This combines remote changes with your local branch.

---

# Fetch vs Pull

Fetch:

git fetch


Downloads changes but does not merge them.


Pull:

git pull


Downloads and merges changes.

---

# GitHub Fork 🍴

A fork creates a personal copy of another repository.

Common workflow:

1. Find an open-source project.
2. Fork the repository.
3. Clone your fork.
4. Make changes.
5. Create a Pull Request.

---

# Pull Requests 🔀

A Pull Request (PR) is a request to merge changes into another repository.

Typical workflow:

Create branch:

git switch -c feature-name


Make changes.

Commit:

git commit -m "Add feature"


Push branch:

git push origin feature-name


Open Pull Request on GitHub.

---

# GitHub Issues 📌

Issues help track:

- Bugs
- Features
- Questions
- Tasks
- Improvements

Good issue reports include:

- Clear title
- Description
- Steps to reproduce
- Expected behavior
- Actual behavior

---

# GitHub Flow 🌊

A simple workflow:

main branch

↓

Create feature branch

↓

Make changes

↓

Commit changes

↓

Push branch

↓

Create Pull Request

↓

Review

↓

Merge

---

# SSH Authentication 🔐

SSH allows secure communication with GitHub without entering username and password repeatedly.

Generate SSH key:

ssh-keygen -t ed25519 -C "email@example.com"


Start SSH agent:

eval "$(ssh-agent -s)"


Add key:

ssh-add ~/.ssh/id_ed25519


Test connection:

ssh -T git@github.com

---

# Using SSH Remote

Change remote URL:

git remote set-url origin git@github.com:user/project.git


Check:

git remote -v

---

# GitHub Releases 📦

Releases are used to publish project versions.

Example:

v1.0.0

v1.1.0

v2.0.0


A release usually contains:

- Version tag
- Changelog
- Download files
- Documentation

---

# GitHub Actions ⚙️

GitHub Actions automates workflows.

Examples:

- Testing code
- Building projects
- Checking documentation
- Deploying applications

Workflow files are stored in:

.github/workflows/

Example:

.github/workflows/test.yml

---

# Collaborating With Teams 👥

Common team workflow:

1. Clone repository.

2. Create branch.

git switch -c feature


3. Make changes.

4. Commit.

git commit -m "Add feature"


5. Push branch.

git push origin feature


6. Create Pull Request.

---

# GitHub Best Practices 💡

- Write meaningful commit messages.
- Keep repositories organized.
- Use branches for features.
- Protect the main branch.
- Review Pull Requests.
- Add documentation.
- Keep secrets private.
- Use Issues for tracking work.

---

# Common GitHub Commands 📚

git clone

Download a repository.


git remote -v

Show remote repositories.


git push

Upload changes.


git pull

Download and merge changes.


git fetch

Download changes only.


git fork

Create a repository copy on GitHub.


git switch -c

Create a new branch.

---

# Next Steps 🚀

Continue to:

Troubleshooting Guide
