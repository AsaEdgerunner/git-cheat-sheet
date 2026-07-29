# Git Tags 🏷️

Git tags are references that point to specific commits in a repository.

Tags are commonly used to mark important points in project history, especially software releases.

Examples:

v1.0.0

v2.1.0

v3.0.0

---

# Understanding Tags

A tag is like a bookmark for a specific commit.

Unlike branches, tags usually do not move.

Example:

Before:

A --- B --- C --- D

Create a tag:

A --- B --- C --- D
              |
             v1.0.0

The tag always points to that commit.

---

# Why Use Tags? 🤔

Tags are useful for:

- Marking software releases
- Creating version points
- Tracking important milestones
- Preparing GitHub releases
- Identifying stable versions

---

# Listing Tags 🔍

Show all tags:

git tag


Example:

v1.0.0

v1.1.0

v2.0.0


Search tags:

git tag -l "pattern"


Example:

git tag -l "v1.*"

---

# Creating a Lightweight Tag

A lightweight tag is a simple pointer to a commit.

Create a tag:

git tag tag-name


Example:

git tag v1.0.0


This creates a tag on the current commit.

---

# Creating an Annotated Tag ⭐

Annotated tags store extra information:

- Author
- Date
- Message
- Tag description

Create an annotated tag:

git tag -a tag-name -m "message"


Example:

git tag -a v1.0.0 -m "First stable release"


Annotated tags are recommended for public projects.

---

# Viewing Tag Information

Show tag details:

git show tag-name


Example:

git show v1.0.0


Displays:

- Commit information
- Tag message
- Author
- Date

---

# Tagging an Older Commit

You can create a tag for a previous commit.

Command:

git tag -a tag-name commit-id -m "message"


Example:

git tag -a v1.0.0 a8d7e63 -m "Release version 1.0.0"

---

# Pushing Tags to Remote 🚀

Tags are not pushed automatically.

Push one tag:

git push origin tag-name


Example:

git push origin v1.0.0


Push all tags:

git push origin --tags

---

# Deleting Tags 🗑️

Delete a local tag:

git tag -d tag-name


Example:

git tag -d v1.0.0


Delete a remote tag:

git push origin --delete tag-name


Example:

git push origin --delete v1.0.0

---

# Checking Out a Tag

Switch to a specific tag:

git checkout tag-name


Example:

git checkout v1.0.0


This creates a detached HEAD state.

---

# Tags and Semantic Versioning 📌

Many projects use Semantic Versioning.

Format:

MAJOR.MINOR.PATCH


Example:

v2.4.1


Meaning:

MAJOR:

Breaking changes.

Example:

v2.0.0


MINOR:

New features without breaking changes.

Example:

v2.5.0


PATCH:

Bug fixes.

Example:

v2.5.1

---

# Release Workflow 🚀

A common release process:

1. Complete development.

2. Update version.

3. Create a tag:

git tag -a v1.0.0 -m "Release v1.0.0"


4. Push tag:

git push origin v1.0.0


5. Create a GitHub Release.

---

# Tags vs Branches 🌿

Branches:

- Continue moving with new commits.
- Used for development.
- Frequently changed.


Tags:

- Stay fixed.
- Mark important versions.
- Used for releases.

---

# Tag Best Practices 💡

- Use annotated tags for releases.
- Follow semantic versioning.
- Use meaningful tag names.
- Do not delete published tags.
- Tag stable versions only.
- Document major releases.

---

# Common Tag Commands 📚

git tag

List tags.


git tag -a

Create annotated tag.


git show

View tag details.


git push origin tag

Upload a tag.


git push origin --tags

Upload all tags.


git tag -d

Delete local tags.

---

# Next Steps 🚀

Continue to:

History Guide
