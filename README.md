<p align="center">
  <img src="./images/banner.png" alt="Git Cheat Sheet Banner">
</p>

<h1 align="center">
  Git Cheat Sheet 🚀
</h1>

<p align="center">
  A beautifully organized and practical Git reference for developers.
</p>

<p align="center">

<img src="https://img.shields.io/badge/Git-Version%20Control-orange?style=for-the-badge&logo=git">

<img src="https://img.shields.io/badge/Open%20Source-Yes-success?style=for-the-badge&logo=github">

<img src="https://img.shields.io/badge/Documentation-Active-blue?style=for-the-badge">

</p>

---

## Introduction 📖

Git is one of the most important tools in modern software development.

It allows developers to track changes, collaborate with teams, manage different versions of their projects, and build software with confidence.

However, learning Git can be challenging because of the number of commands, concepts, and workflows involved.

This project provides a structured and practical Git reference that helps developers understand Git concepts instead of simply memorizing commands.

---

## Why This Project? 🤔

Many Git cheat sheets focus only on listing commands without explaining when and why they should be used.

**Git Cheat Sheet** was created to provide a complete learning resource with:

- Clear explanations
- Practical examples
- Real-world workflows
- Beginner-friendly learning path
- Professional Git practices
- Easy navigation between topics

The goal is simple:

> Learn Git properly, not just memorize commands.

---

## Features ✨

- ✅ Beginner-friendly explanations
- ✅ Practical command examples
- ✅ Git workflow diagrams
- ✅ Branching and merging guides
- ✅ GitHub workflow documentation
- ✅ Troubleshooting common problems
- ✅ Best practices for professional development
- ✅ Open-source documentation structure

---

## Documentation 📚

Detailed guides are available in the `docs` directory:

| Topic | Description |
|---|---|
| Installation | Installing Git on different systems |
| Configuration | Setting up Git preferences |
| Repositories | Creating and managing repositories |
| Commits | Understanding Git commits |
| Branches | Working with branches |
| Merging | Combining changes |
| Rebasing | Advanced history management |
| Remotes | Working with remote repositories |
| Stash | Temporarily saving changes |
| Tags | Managing project versions |
| History | Exploring Git history |
| Undo | Recovering from mistakes |
| Aliases | Creating Git shortcuts |
| GitHub | Using Git with GitHub |
| Troubleshooting | Solving common problems |
| Best Practices | Professional Git workflow |

---

## Git Workflow Overview 🌳

```mermaid
flowchart LR

A[Working Directory]
B[Staging Area]
C[Local Repository]
D[Remote Repository]

A -->|git add| B
B -->|git commit| C
C -->|git push| D

D -->|git pull| C
