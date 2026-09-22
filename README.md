# Git Practice Repository

This repository contains my hands-on practice while learning Git fundamentals as the first step toward DevOps.

I spent several weeks going through Git concepts step by step — from basic commands to more advanced operations like reset, revert, stash, rebase, cherry-pick, tags, and reflog.

---

## Mission 1 — Git Basics
**Init → Add → Commit → Push**

| Command | Definition |
|---------|------------|
| `git init` | Creates a new Git repository in the current folder |
| `git status` | Shows the current state of the repository |
| `git add <file>` | Stages a specific file for the next commit |
| `git add .` | Stages all changed files |
| `git commit -m "message"` | Saves staged changes as a commit |
| `git remote` | Shows connected remote repositories |
| `git remote -v` | Shows remote repository URLs |
| `git push` | Uploads local commits to the remote |
| `git push -u origin main` | Pushes main branch and sets upstream |

---

## Mission 2 — Branches & Switching
**Parallel Development**

| Command | Definition |
|---------|------------|
| `git branch` | Lists all local branches |
| `git switch <branch>` | Switches to an existing branch |
| `git switch -c <branch>` | Creates a new branch and switches to it |

---

## Mission 3 — Merge & Conflicts
**Combine Changes**

| Command | Definition |
|---------|------------|
| `git merge <branch>` | Combines changes from another branch into the current branch |
| `git status` | Helps identify files with merge conflicts |

**Merge Conflict**  
Happens when Git cannot automatically decide which changes to keep. You resolve them manually.

---

## Mission 4 — Restore & Staging
**Undo & Adjust**

| Command | Definition |
|---------|------------|
| `git restore <file>` | Discards unstaged changes in a file |
| `git restore --staged <file>` | Removes a file from staging area but keeps the changes |

---

## Mission 5 — Log & Commit Graph
**See Your History**

| Command | Definition |
|---------|------------|
| `git log` | Shows full commit history with details |
| `git log --oneline` | Shows commits in compact form |
| `git log --graph` | Displays commit history as a visual graph |
| `git log --oneline --graph` | Shows compact graphical commit history |

---

## Mission 6 — Git Diff
**See What Changed**

| Command | Definition |
|---------|------------|
| `git diff` | Shows unstaged changes |
| `git diff -U1` | Shows changes with 1 line of context |
| `git diff -U0` | Shows only changed lines (no context) |
| `git diff --staged` | Shows staged changes |
| `git diff --staged --stat` | Shows summary of staged changes |
| `git diff --staged --name-only` | Shows only names of staged files |

---

## Mission 7 — Checkout, Reset & Revert
**Go Back, Fix Forward**

| Command | Definition |
|---------|------------|
| `git checkout <commit>` | Moves HEAD to a specific commit |
| `git reset --soft HEAD\~1` | Moves back 1 commit, keeps changes staged |
| `git reset --mixed HEAD\~1` | Moves back 1 commit, leaves changes unstaged |
| `git reset --hard HEAD\~1` | Moves back 1 commit and removes the changes |
| `git reset --soft ORIG_HEAD` | Restores previous HEAD position after a reset |
| `git revert <commit>` | Creates a new commit that undoes an earlier commit |

---

## Mission 8 — Advanced Git

### Stash
| Command | Definition |
|---------|------------|
| `git stash` | Temporarily saves uncommitted changes |
| `git stash push -m "message"` | Saves changes with a custom message |
| `git stash list` | Lists all saved stashes |
| `git stash pop` | Restores the latest stash and removes it |

### Fetch
| Command | Definition |
|---------|------------|
| `git fetch` | Downloads remote updates without changing your branch |

### Rebase
| Command | Definition |
|---------|------------|
| `git rebase <branch>` | Replays your commits on top of another branch |

### Cherry-pick
| Command | Definition |
|---------|------------|
| `git cherry-pick <commit>` | Applies one specific commit to the current branch |

### Tags
| Command | Definition |
|---------|------------|
| `git tag <name> <commit>` | Creates a tag pointing to a specific commit |
| `git tag` | Lists all existing tags |
| `git push origin --delete <tag>` | Deletes a tag from the remote |

### Reflog
| Command | Definition |
|---------|------------|
| `git reflog` | Shows history of where HEAD and references have pointed |
| `HEAD@{n}` | Refers to a specific reflog entry |

---

## Hands-on Experiments

I practiced most of these commands by creating branches, making changes, resolving merge conflicts, using reset/revert, experimenting with detached HEAD, and recovering commits using reflog.

Example of real reflog history from this repository:
