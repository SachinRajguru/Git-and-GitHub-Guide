
# Git & GitHub Complete Study Guide | Practical Lab Manual | Technical Handbook

## Table of Contents
1. [Introduction to Git & GitHub](#introduction)
2. [What is Git?](#what-is-git)
3. [Why Use Git?](#why-use-git)
4. [GitHub Introduction](#github-introduction)
5. [Git vs GitHub](#git-vs-github)
6. [Creating GitHub Account](#github-account)
7. [Creating First Repository](#first-repo)
8. [Setting Up Git Locally](#git-setup)
9. [Basic Git Commands](#basic-commands)
10. [Git Workflow](#git-workflow)
11. [Branches & Merging](#branches)
12. [Merge Conflicts](#merge-conflicts)
13. [Undoing Changes](#undoing)
14. [Forking](#forking)
15. [Git Cheat Sheet](../02-cheat-sheets/01-git-cheat-sheet.md)
16. [Interview Questions](#interview)

---

## 1. Introduction to Git & GitHub

**Scenario**: You're working on college projects or company projects. You need to track code changes, collaborate with teams, and showcase work in resumes.

**Key Learning Objectives**:
- Understand Git as Version Control System
- GitHub as cloud platform for code storage
- Complete workflow from scratch to advanced

**Analogy**: 
```
Git = Bank Account Statement (tracks every transaction/history)
GitHub = Instagram Profile (showcase your portfolio publicly)
```

---

## 2. What is Git?

### Definition
**Git** is a **Version Control System (VCS)**.
**Version Control System (VCS)** is a tool that helps to track changes in code.

### Analogy
```
Like a Bank Account:
- Credit = New file added
- Debit = File deleted  
- Tax = Line modified
Git maintains complete transaction history
```

---

## 3. Why Use Git?

| **Reason** | **Details** |
|------------|-------------|
| **Most Popular** | Used worldwide (Microsoft, Google, Facebook) |
| **Free & Open Source** | No licensing costs |
| **Fast & Scalable** | Works for small & massive projects |

### Core Purpose 
```
# 2 Major Use Cases

1. Track Code History
   - Never lose previous versions
   - Easy rollback to working state

2. Collaboration
   - Multiple developers on same project
   - Track WHO changed WHAT
   - Prevent overwrites
```

### Scenario Example
```
You're building a website:
Day 1: Add signup page ✓
Day 2: Add buttons ✓  
Day 3: Help form (problematic) ✗

→ Want to revert to Day 2 state without manual deletion
→ Git tracks history → Revert automatically
```

#### Code History Tracking:
```bash
# Git remembers:
- New files added
- Files deleted  
- Line-by-line code changes
- WHO made changes
- WHEN changes happened
```

---

## 4. GitHub Introduction

### Definition
**GitHub** is a **Website** (github.com) that allows developers to **store and manage** their code using Git.
- **Store** code remotely
- **Manage** projects using Git
- **Collaborate** with teams
- **Showcase** portfolio in resumes

### Key Terms
```
Repository (Repo) = Project folder containing code
Public Repo = Visible to everyone (like public Instagram)
Private Repo = Only you can see (like private story)
```

**Analogy**
```
GitHub = Instagram (public profile)
Repositories = Photos in your gallery
```

**Repository (Repo)**: Folder containing project code + history
**Short form**: "Repos"

## 5. Git vs GitHub

| **Aspect** | **Git** | **GitHub** |
|------------|---------|------------|
| **Type** | Local software | Cloud website |
| **Purpose** | Version control | Code storage/sharing |
| **Location** | Your computer | github.com |
| **Commands** | `git clone`, `git commit` | Web UI, Pull Requests |
| **Analogy** | Calculator app | Online calculator service |

---

## 6. Creating GitHub Account

### Step-by-Step Lab Guide

1. **Visit**: `github.com`
2. **Click**: `Sign up` 
3. **Enter**:
   ```
   Email: student@yourcollege.in
   Password: (strong password)
   Username: student-yourcollege
   ```

4. **Verification**:
   ```
   Check email → Copy 6-digit code (e.g., 123456)
   Paste code → Continue
   ```

5. **Setup Preferences**:
   ```
   Team size: "Just me (student)"
   Skip student benefits → Continue → Free plan
   ```

### Dashboard Navigation
```
Top Right Corner:
├── Your Profile (shows activity/contributions)
├── Repositories (your projects)
└── New (create new repo)
```

**Contributions**: Green squares = days you made commits

---

## 7. Creating First Repository

### **Practical Steps**

```bash
# 1. Go to Profile → Repositories → "New" button
# 2. Fill details:
Repository name: git-demo
Description: This is my first Git repository
[] Visibility: Public ✓ (Everyone can see)
[] Initialize with README ✓ (Special info file)
# 3. Create Repository
```

### README.md Explained
```
Special file containing:
- Project description
- Installation instructions  
- Features list
- Usage guide
```

**Markdown Example**:
```markdown
# Git Demo Repository
This is my first Git repository

**Author**: Sachin Rajguru
```

**Edit on GitHub**:
```
1. Click pencil icon (✏️) on README.md
2. Add: "Author: Sachin Rajguru"
3. Commit changes → "Update README.md"
```

**HTML in README**:
```markdown
# Git Demo Repository
This is my first Git repository

<br>  <!-- Next line -->
**Author**: Sachin Rajguru
```

---

## 8. Setting Up Git Locally

### Prerequisites Download

| **OS** | **Required Tools** |
|--------|--------------------|
| **Windows** | VS Code + Git Bash |
| **Mac** | VS Code + Terminal (pre-installed) |
| **Linux** | VS Code + Terminal |

### Verify Git Installation
```bash
git --version
# Output: git version 2.x.x
```

### Configure Git (Global)
```bash
# Set your name
git config --global user.name "student-yourcollege"

# Set your email (SAME as GitHub)
git config --global user.email "student@yourcollege.in"

# Verify configuration
git config --list
```

**Output**:
```
user.name=student-yourcollege
user.email=student@yourcollege.in
```

**Two Configuration Levels**:
```
Global: Applies to all repositories on your system (recommended for beginners)
Local: Applies only to a specific repository (overrides global settings if configured)
```

### VS Code Integration
```
1. Open VS Code
2. File → Open Folder → git-demo
3. Terminal → New Terminal (Ctrl+`)
```

---

## 9. Basic Git Commands

### 9.1 Clone Command

**Definition**: Copy remote repo to local machine

```bash
git clone <repo-url>
```

**Terminal Commands**:
```bash
# Copy GitHub repo to local
git clone https://github.com/student-yourcollege/git-demo.git

# Note: Copy HTTPS link from GitHub (Code → HTTPS).  
# HTTPS is the easiest way for beginners.

# Navigate into cloned folder
cd git-demo

# List files
ls
# Output: README.md

# List hidden files (shows .git folder)
ls -a
# Output: . .. .git README.md
```

**`.git` folder**: Contains all Git history/metadata (Git's internal database storing all history)

### 9.2 Status Command

**Definition**: Shows current repo state

```bash
git status
```

**4 File States**:
```
1. Untracked (new files)      → RED in VS Code
2. Modified (changed files)   → RED in VS Code  
3. Staged (git add done)      → GREEN in VS Code
4. Committed (git commit)     → History ✓
```

**Example**:
```bash
# Create & modify files
echo "Done by Sachin" >> README.md
touch index.html

git status
# Output:
# Modified: README.md (red)
# Untracked: index.html (red)
```

### 9.3 Add Command

**Definition**: Stage changes for commit (Engagement phase).
Adds new or changed files in your working directory to the Git staging area.

```bash
git add <file-name>
```

```bash
# Add specific file
git add index.html

# Add all changes
git add .

# Add multiple files
git add README.md index.html
```

**After `git add`**:
```bash
git status
# Output: Changes to be committed (green)
```

**Analogy**: 
```
Working Directory → Staging Area (git add)
Staging Area → Repository (git commit)
```

### 9.4 Commit Command

**Definition**: Create snapshot of staged changes (Wedding phase).
It is the record of change.

```bash
git commit -m "some message"
```

**Best Practices**:
```
✗ "Update files"             ← BAD
✓ "Add signup button"        ← GOOD  
✓ "Fix login bug"            ← GOOD
✓ "Add new feature"          ← GOOD
```

**Complete Flow**:
```bash
# 1. Check status
git status

# 2. Stage changes  
git add .

# 3. Commit with message
git commit -m "Add new paragraph"

# 4. Verify
git status
# Output: nothing to commit, working tree clean
```

### 9.5 Push Command

**Definition**: Upload local repo content to remote repo

```bash
git push origin main
# origin/main = Default remote tracking branch
# 'origin' is the name we give to GitHub repos by convention
```

```bash
# First push (sets upstream)
git push -u origin main

# Subsequent pushes
git push
```

**Authentication** (First time):
```
1. VS Code will ask permission
2. Click "Open in VS Code" → Authorize
```

---

## 10. Git Workflow

### Standard Workflow (Recommended)

```
GitHub Repo → Clone → Edit → Add → Commit → Push
               ↑         ↑      ↑    ↑       ↑
            Remote    Local   Stage Snapshot Remote

1. Clone: git clone <repo-url>
2. Change code
3. Status: git status
4. Add: git add .
5. Commit: git commit -m "message"
6. Push: git push
```

### Creating Local Repo (Local Project → GitHub)

```bash
# 1. Create folder
mkdir local-repo
cd local-repo

# 2. Initialize Git
git init
# Output: Initialized empty Git repository

# 3. Add files
touch index.html style.css
# Edit files...

# 4. Add & commit
git add .
git commit -m "Add initial files"

# 5. Create GitHub repo (empty, no README)
# 6. Link local to remote (Connect remote)
git remote add origin https://github.com/student-yourcollege/local-repo.git
# We call this 'origin' by convention.

# 7. Push
git push -u origin main
```

**Terminal Helper Commands**:
```bash
ls -a          # List hidden files (.git)
cd ..          # Go up one directory
cd foldername  # Enter directory (Tab for autocomplete)
clear          # Clear terminal
```

---

## 11. Branches & Merging

### What are Branches?

**Definition**: Independent lines of development (Separate copies for parallel development)

**Analogy**: 
```
Tree trunk (main) → Multiple branches (features)
Each team works on separate branch
Finally merge back to trunk
```

**Scenario:** 3 Teams Working Simultaneously
```
main ──┬─ Feature Team 1 (login)
       ├─ Feature Team 2 (payment)  
       └─ Bug Fix Team
```

### Branch Commands

```bash
# List branches
git branch
# * main (current branch marked with *)

# Create & switch to new branch
git checkout -b feature-1

# Switch branch
git checkout main

# Rename branch
git branch -m master main  # Rename master to main
# We do this because master → main everywhere now

# Delete branch (must not be on it)
git checkout main
git branch -d feature-1
```

**Note**: "Earlier, 'master' was the default branch. Now Git uses 'main' as the default."

### Push Branch to GitHub
```bash
git push origin feature-1
```

### **Branch Workflow**
```bash
# 1. Create feature branch
git checkout -b feature-1

# 2. Make changes
# Edit files...

# 3. Commit changes
git add .
git commit -m "Add new feature"

# 4. Push branch to GitHub
git push origin feature-1
```

### Merge via GitHub Pull Request

**Steps**:
```
1. Push feature branch
2. GitHub → "Compare & Pull Request"
3. Add title: "Add new feature"
4. Click "Create pull request"
5. "Merge pull request" → "Confirm merge"
```

**Benefits**:
- Code review by senior developers
- Comments & suggestions
- Prevents breaking main branch

### Merge via Command Line
```bash
# Compare branches
git diff main..feature-1

# Merge (on target branch)
git checkout main
git merge feature-1
```

---

## 12. Merge Conflicts

### **Definition**
When Git can't automatically combine changes from different branches.

```
When SAME LINE in SAME FILE is changed in 2 branches
Git can't auto-resolve → Manual resolution needed
```

**Scenario**:
```
main branch:     <button>Click me</button>
feature branch:  <select><option>Choose</option></select>
Same line → CONFLICT!
```

### Resolving Conflicts in VS Code

```
1. Git shows conflict markers:
<<<<<<< HEAD (current branch)
<button>Click me</button>
=======
<select><option>Choose</option></select>
>>>>>>> feature-1 (incoming branch)

2. Choose:
   - Accept Current (keep HEAD changes)
   - Accept Incoming (keep feature changes)  
   - Accept Both (manual edit)

3. Remove conflict markers (<<<<<<<, =======, >>>>>>>)
4. Save → git add . → git commit
```

**Example Resolution**:
```html
<!-- BEFORE (conflict) -->
<<<<<<< HEAD
<button>Click me</button>
=======
<select><option>Choose</option></select>
>>>>>>> feature-1

<!-- AFTER (resolved) -->
<button>Click me</button>
<select><option>Choose</option></select>
```

---

## 13. Undoing Changes

### Case 1: Unstage Changes (Added but not committed - Before Commit)
```bash
# Unstage specific file
git reset <file-name>

# Unstage everything
git reset
```

### Case 2: Undo Last Commit (Soft reset)
```bash
git reset HEAD~1
# Go back 1 commit - Keeps changes in staging area
```

### Case 3: Undo Multiple Commits (Using HASH)
```bash
# View commit history
git log --oneline

# Reset to specific commit (copy HASH)
git reset <commit-hash>
```

### Case 4: Hard Reset (Discard all changes)
```bash
git reset --hard HEAD~1
# ⚠️ Permanently deletes changes!
```

**View History**:
```bash
git log --oneline
# Shows: hash | message | author | date
```

---

## 14. Forking

### Definition
Create a copy of someone else's repository under your account.

**Use Cases**:
- Contribute to open source
- Learn from others' code
- Experiment safely

### Fork Workflow
```
1. GitHub → Search "express"
2. Find repo → Click "Fork"
3. Clone YOUR fork: git clone <your-fork-url>
4. Make changes → Push to your fork
5. Create Pull Request to original repo
```

**Example**:
```
Original: expressjs/express
Your fork: student-yourcollege/express
→ Make useful changes → PR back to original
```

---

## 15. Git Cheat Sheet

➤ [Open Git Cheat Sheet](../02-cheat-sheets/01-git-cheat-sheet.md)

---

## 16. Interview Questions & Answers

### Q1: What is Git? Difference between Git & GitHub?
```
Git: Local version control system
GitHub: Cloud platform to store/share Git repos
Git = Software | GitHub = Website
```

### Q2: Explain Git workflow (add → commit → push)
```
1. git add .     → Stage changes (Engagement)
2. git commit -m → Snapshot changes (Wedding)  
3. git push      → Upload to remote (Share publicly)
```

### Q3: What are the 4 stages of a file in Git?
```
1. Untracked (new file)
2. Modified (changes made)
3. Staged (git add done)
4. Committed (git commit done)
```

### Q4: How to resolve merge conflicts?
```
1. Git marks conflicts with <<<<<<<, =======, >>>>>>>
2. Manually edit file (choose changes)
3. Remove conflict markers
4. git add . → git commit → git push
```

### Q5: Difference between `git merge` & Pull Request?
```
git merge: Direct command line merge
Pull Request: GitHub feature with review process
PR = merge + code review + comments
```

### Q6: What is `git reset --hard`? Risks?
```
Resets to specific commit, deletes all changes after
⚠️ IRREVERSIBLE - Use carefully!
```

---

## Pro Tips

1. **Always** use meaningful commit messages
2. **Start** projects on GitHub → Clone locally
3. **Use branches** for every new feature
4. **Pull Request** for all merges (even solo projects)
5. **Daily**: `git pull origin main` before starting work
6. **VS Code** = Best Git integration

## ✓ Lab Practice Tasks

```
1. Create GitHub account + 2 repos
2. Clone → Add HTML/CSS → Commit → Push
3. Create feature branch → Add button → PR → Merge
4. Intentionally create merge conflict → Resolve
5. Practice undoing: add/reset/commit/reset
6. Fork popular repo → Make change → Create PR
```
---

**"Git is not just a tool, it's a skill every developer must master!"**