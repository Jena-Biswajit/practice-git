# Git Commands Cheat Sheet

## 🔹 Git Configuration Commands

| Command | What It Does | When To Use |
|--------|---------------|-------------|
| `git config --global user.name "Your Name"` | Sets your Git username | When setting up Git for the first time |
| `git config --global user.email "your@email.com"` | Sets your Git email | When setting up Git for the first time |
| `git config --list` | Shows current Git config | To confirm settings |

---

## 🔹 Repository Initialization

| Command | What It Does | Where & When To Use |
|---------|--------------|---------------------|
| `git init` | Initializes a new local Git repo | Inside a new project folder |
| `git clone <url>` | Clones a remote repo to your local system | When starting with existing Git project |

---

## 🔹 File Tracking & Staging

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git status` | Shows changes staged/unstaged/untracked | Always before `commit` to review status |
| `git add <file>` | Stages a file | After editing a file |
| `git add .` | Stages all changed files | For quick staging of everything |
| `git reset <file>` | Unstages a staged file | If you accidentally added it |

---

## 🔹 Committing Changes

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git commit -m "message"` | Commits staged changes with a message | After staging changes |
| `git commit -a -m "message"` | Commits all tracked file changes | When you want to skip `add` step |

---

## 🔹 Branching and Merging

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git branch` | Lists all branches | Anytime |
| `git branch <name>` | Creates a new branch | Before working on a new feature |
| `git checkout <branch>` | Switches to a branch | To work on that branch |
| `git checkout -b <branch>` | Creates and switches to a branch | Shorter version of create + switch |
| `git merge <branch>` | Merges branch into current one | After feature is done |
| `git branch -d <branch>` | Deletes a branch | After merge completed |

---

## 🔹 Viewing Changes

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git diff` | Shows unstaged changes | Before staging to see what's changed |
| `git diff --staged` | Shows staged changes | Before committing |
| `git log` | Shows commit history | To trace changes |
| `git show <commit>` | Shows details of a specific commit | When investigating history |

---

## 🔹 Remote Repositories

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git remote -v` | Shows remote URLs | To verify remote config |
| `git remote add origin <url>` | Adds a remote repo | When linking local to remote |
| `git push -u origin main` | Pushes local branch and sets upstream | First time push |
| `git push` | Pushes commits to remote | After committing |
| `git pull` | Fetches & merges remote changes | To sync local repo |
| `git fetch` | Fetches changes (no merge) | To see changes without merging |
| `git clone <repo>` | Clones full remote repo | When starting from remote |

---

## 🔹 Stashing Changes

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git stash` | Temporarily saves uncommitted changes | Before switching branches |
| `git stash apply` | Re-applies last stash | After you’re ready to resume work |
| `git stash pop` | Applies and removes last stash | Shortcut for apply + delete |
| `git stash list` | Shows all stashed entries | To manage stashes |

---

## 🔹 Reset, Revert & Clean

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git reset` | Unstages changes | When undoing `git add` |
| `git reset --hard` | Resets working directory & index | ⚠ DANGEROUS – removes changes |
| `git revert <commit>` | Creates a new commit to undo changes | Safer alternative to reset |
| `git clean -fd` | Removes untracked files/dirs | ⚠ Use with caution |

---

## 🔹 Rebase & Cherry Pick

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git rebase <branch>` | Reapplies commits from current to base | For linear history |
| `git cherry-pick <commit>` | Applies a specific commit to current branch | For selective commit transfer |

---

## 🔹 Tags

| Command | What It Does | When To Use |
|---------|--------------|-------------|
| `git tag` | Lists all tags | Version review |
| `git tag <v1.0>` | Creates a new tag | After stable release |
| `git push origin <tag>` | Pushes a tag to remote | For releases |

---

## 🔹 Git Undo Commands (Summary)

| Use Case | Command |
|----------|---------|
| Undo staged but uncommitted file | `git reset <file>` |
| Undo last commit (keep changes) | `git reset --soft HEAD~1` |
| Undo last commit (discard changes) | `git reset --hard HEAD~1` |
| Remove all untracked files | `git clean -fd` |


