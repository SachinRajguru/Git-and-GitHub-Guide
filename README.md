
# Git & GitHub Guide

Practical lab manual + technical handbook for mastering Git version control and GitHub collaboration workflows.

## Quick Navigation

* [Main Guide](./01-handbook/01-complete-git-and-github-guide.md)
* [Cheat Sheet](./02-cheat-sheets/01-git-cheat-sheet.md)

---

## Repository Structure

```bash
git-and-github-guide/
│
├── 01-handbook/
│   └── 01-complete-git-and-github-guide.md     # Detailed guide
│
├── 02-cheat-sheets/
│   └── 01-git-cheat-sheet.md                   # Quick reference
└── README.md                                   # You are here
```

---

## Learning Path

### Phase 1: Git Fundamentals
**Goal**: Understand version control basics
* What is Git & GitHub
* Local setup and configuration
* Basic workflow (clone → add → commit → push)
* File states and staging area

### Phase 2: Collaboration Workflow
**Goal**: Master team development patterns
* Branches and merging
* Pull requests and code review
* Merge conflict resolution
* Forking and open source contribution

### Phase 3: Advanced Operations
**Goal**: Handle complex scenarios professionally
* Undoing changes (reset, revert)
* Git history navigation
* Production workflows

---

## What You Will Learn

* Track code changes with Git version control
* Collaborate using GitHub pull requests
* Resolve merge conflicts professionally
* Manage branches for parallel development
* Contribute to open source projects
* Debug and recover from Git mistakes
* Build resume-worthy GitHub portfolio

---

## Who This Guide Is For

* Software developers (beginner to intermediate)
* DevOps engineers
* Computer science students
* Technical team leads
* Anyone preparing for developer interviews

---

## Prerequisites

### Environment Setup
```bash
Windows: Git Bash + VS Code (Recommended)
Mac: Native Terminal + VS Code
Linux: Native Terminal + VS Code
```

### Verify Installation
```bash
git --version
# Expected output: git version 2.x.x
```

---

## How to Use This Repository

```bash
# Clone repository
git clone https://github.com/yourusername/git-and-github-guide.git
cd git-and-github-guide
```

### Recommended Workflow
```bash
1. READ      → 01-handbook/01-complete-git-and-github-guide.md
2. PRACTICE  → Follow lab exercises step-by-step
3. REFERENCE → 02-cheat-sheets/01-git-cheat-sheet.md
4. APPLY     → Create your own GitHub projects
```

---

## Core Git Workflow

```bash
# Standard workflow
git clone <repo-url>
git status                    # Check current state
git add .                     # Stage changes
git commit -m "Clear message" # Create snapshot
git push origin main          # Upload to remote

# Branch workflow
git checkout -b feature-branch
# Make changes → add → commit → push origin feature-branch
git push origin feature-branch
# Create Pull Request on GitHub
```

---

## Interview Preparation

### Key Topics Covered

| Level | Topics |
|-------|--------|
| **Beginner** | Git workflow, staging area, basic commands |
| **Intermediate** | Branches, merge conflicts, pull requests |
| **Advanced** | Reset strategies, fork workflow, history navigation |

### Sample Questions
```
1. Explain Git's 4 file states
2. How do you resolve merge conflicts?
3. Difference between git merge vs Pull Request?
4. What does git reset --hard do?
5. How to contribute to open source?
```

---

## Lab Practice Checklist

```
□ Create GitHub account and first repository
□ Configure Git locally (name, email)
□ Clone → modify → add → commit → push workflow
□ Create feature branch and Pull Request
□ Resolve merge conflict in VS Code
□ Practice git reset (soft, hard, mixed)
□ Fork repository and create PR
□ Review git log --oneline output
```

---

## Pro Tips

* **Always** use descriptive commit messages
* **Branch** for every new feature (`git checkout -b feature-name`)
* **Pull** before pushing (`git pull origin main`)
* **VS Code** provides excellent Git integration
* **Practice** on real projects, not just tutorials
* **Contributions** calendar = resume feature

---

## License
MIT License — Free for personal and commercial use

---

## Start Learning

➤ [Complete Git & GitHub Guide](./01-handbook/01-complete-git-and-github-guide.md)