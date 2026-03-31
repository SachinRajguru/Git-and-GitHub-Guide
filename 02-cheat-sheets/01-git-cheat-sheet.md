
# Git & GitHub Complete CHEAT SHEET
## Professional Reference Guide | Print-Ready | All Commands Covered

```
═══════════════════════════════════════════════════════════════════════════════
                    GIT & GITHUB MASTER CHEAT SHEET
═══════════════════════════════════════════════════════════════════════════════
```

## INSTALLATION & GUIS
```bash
GitHub for Windows
https://windows.github.com

GitHub for Mac
https://mac.github.com

For Linux and Solaris platforms, the latest release is available on 
the official Git web site.

Git for All Platforms
http://git-scm.com

# Verify installation
git --version
```

---

## SETUP
```bash
# Configuring user information (Global - ONCE)
git config --global user.name "[firstname lastname]"    # Set identifiable name
git config --global user.email "[valid-email]"          # Set email for history
git config --global color.ui auto                       # Enable command coloring

# Verify
git config --list                                       # Show all config
```

---

## SETUP & INIT
```bash
# Initialize repositories
git init                                    # Initialize existing directory as Git repo
git clone [url]                             # Clone entire repo from URL

# Check status/version
git status                                  # See repo status
git --version                               # Check Git version
```

---

## STAGE & SNAPSHOT
```
File States: Untracked → Modified → Staged → Committed
```

```bash
# Status Check
git status                                  # See current state

# Staging (Engagement Phase)
git add file.txt                            # Stage single file
git add .                                   # Stage all changes
git add *.html                              # Stage pattern

# Unstage
git reset file.txt                          # Unstage single file
git reset                                   # Unstage everything

# Diffs
git diff                                    # See unstaged changes
git diff --staged                           # See staged changes

# Commit (Wedding Phase)  
git commit -m "Descriptive message"         # Commit with message
git commit -am "Add & commit"               # Auto-add tracked files
```

---


## BRANCHES & MERGING
```bash
# List Branches
git branch                                  # Local branches (* = current)
git branch -a                               # All branches (remote + local)

# Create & Switch
git checkout -b feature-branch              # Create AND switch
git checkout branch-name                    # Switch to existing

# Rename
git branch -m old-name new-name             # Rename branch

# Delete  
git branch -d branch-name                   # Safe delete
git branch -D branch-name                   # Force delete

# Merge
git checkout main                           # Switch to target branch
git merge feature-branch                    # Merge into current
```

---

## SHARE & UPDATE
```bash
# Add remote repository
git remote add [alias] [url]                # Add git URL as alias

# Fetch updates
git fetch [alias]                           # Fetch all branches from remote

# Update local branch
git merge [alias]/[branch]                  # Merge remote branch
git pull                                    # Fetch + merge (shortcut)

# Push changes
git push [alias] [branch]                   # Push local commits to remote
```

---


## TRACKING PATH CHANGES
```bash
# Remove file
git rm [file]                               # Delete AND stage removal

# Rename/move file
git mv [existing-path] [new-path]           # Move AND stage

# View path changes in history
git log --stat -M                           # Show moved files in logs
```

---

## IGNORING PATTERNS
```bash
logs/ 
*.notes 
pattern*/ 
# Save a file with desired patterns as .gitignore with either direct string matches or wildcard globs.

# Global ignore
git config --global core.excludesfile [file]    # System-wide ignore
```

---

## HISTORY & LOGS
```bash
# View History
git log                                     # Full commit history
git log --oneline                           # One line per commit
git log --graph --oneline --all             # Visual branch graph
git log --stat                              # Show file changes

# Compare
git diff main..feature                      # Branch differences
git diff HEAD~1                             # vs previous commit

# Show Commit
git show <commit-hash>                      # Show commit details
```

---


## UNDOING CHANGES
```bash
# Unstage (Keep changes)
git reset HEAD file.txt                     # Unstage file
git reset HEAD~1                            # Soft reset last commit

# Hard Reset (💥 Lose changes!)
git reset --hard HEAD~1                     # Destroy last commit
git reset --hard <commit-hash>              # Reset to specific commit

# Revert (Safe - creates new commit)
git revert <commit-hash>                    # Undo with new commit

# Clean untracked files
git clean -fd                               # Delete untracked files
```

---

## TEMPORARY COMMITS
```bash
# Stash changes temporarily
git stash                                   # Save modified/staged changes

# Manage stashes
git stash list                              # List all stashes
git stash pop                               # Restore top stash
git stash drop                              # Delete top stash
```

---

## INSPECT & COMPARE
```bash
# History views
git log                                     # Current branch history
git log branchB..branchA                    # Commits in A not in B
git log --follow [file]                     # File history (tracks renames)

# Diffs
git diff branchB...branchA                  # What's unique to branchA
git show [SHA]                              # Show any Git object
```

---

## REWRITE HISTORY
```bash
# Rebase commits
git rebase [branch]                         # Rebase current onto branch

# Reset everything
git reset --hard [commit]                   # Hard reset to commit
```

---

## GITHUB-SPECIFIC
```bash
Repository Types:
├── Public    → Everyone can see
└── Private   → Only you + collaborators

Key Features:
├── README.md → Project documentation
├── Issues    → Bug tracking  
├── Pull Requests → Code review
└── Actions   → CI/CD automation
```

**GitHub Education**:
```bash
Free for students/teachers
https://education.github.com
Email: education@github.com
```

---

## PRO WORKFLOW
```bash
# Daily Routine
git pull origin main                         # Start fresh
git checkout -b feature/xyz                  # New feature branch
# Work → test → 
git add .                                    # Stage all
git commit -m "feat: add xyz"                # Commit
git push origin feature/xyz                  # Push branch
# Create PR on GitHub

# Before Push Always
git status                                   # Check status
git log --oneline -5                         # Check recent commits
```

---

## COMMON ERRORS & FIXES

| **Error** | **Solution** |
|-----------|--------------|
| `not a git repository` | `git init` or `cd` into repo |
| `no such remote origin` | `git remote add origin <url>` |
| `merge conflict` | Edit files → remove `<<<<<<<` → `git add` → `git commit` |
| `detached HEAD` | `git checkout main` |
| `nothing to commit` | `git status` → check unstaged changes |

---

## MOBILE-FRIENDLY COMMANDS
```bash
# Most Used (90% of work)
git status                                  # Check status
git add .                                   # Stage all
git commit -m "..."                         # Commit
git push                                    # Push
git pull                                    # Pull

# Branch Essentials
git checkout -b feature                     # New branch
git checkout main                           # Main branch
git merge feature                           # Merge
```

---

```
═══════════════════════════════════════════════════════════════════════════════
           PRINT THIS | KEEP HANDY | MASTER GIT IN 30 DAYS
═══════════════════════════════════════════════════════════════════════════════

⭐ Made with ❤️ for College Students & Professionals
⭐ Next: Learn GitHub Actions & Advanced Workflows

```

**Pro Tip**: **Practice daily** → 15 mins = Git Master in 1 month!