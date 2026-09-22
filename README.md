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

  
| Commit Hash | HEAD Reference | Action Timestamp | Commit Timestamp | Description |
| :--- | :--- | :--- | :--- | :--- |
| **0b62c09** | `HEAD@{Sun Sep 20 12:21:06 2026}` | Sun Sep 20 12:21:06 2026 | Sun Sep 20 12:14:28 2026 | reset: moving to 0b62c09 |
| **b966ae6** | `HEAD@{Sun Sep 20 12:15:43 2026}` | Sun Sep 20 12:15:43 2026 | Sat Sep 19 16:39:48 2026 | reset: moving to HEAD~1 |
| **0b62c09** | `HEAD@{Sun Sep 20 12:14:28 2026}` | Sun Sep 20 12:14:28 2026 | Sun Sep 20 12:14:28 2026 | commit: Reflog time machine experiment |
| **b966ae6** | `HEAD@{Sat Sep 19 17:32:36 2026}` | Sat Sep 19 17:32:36 2026 | Sat Sep 19 16:39:48 2026 | reset: moving to b966ae623b87415c168e262568823c35e7e24ee7 |
| **b966ae6** | `HEAD@{Sat Sep 19 17:14:40 2026}` | Sat Sep 19 17:14:40 2026 | Sat Sep 19 16:39:48 2026 | checkout: moving from main to cherry-pick-practice |
| **b966ae6** | `HEAD@{Sat Sep 19 16:43:26 2026}` | Sat Sep 19 16:43:26 2026 | Sat Sep 19 16:39:48 2026 | checkout: moving from navbar-update to main |
| **b966ae6** | `HEAD@{Sat Sep 19 16:42:46 2026}` | Sat Sep 19 16:42:46 2026 | Sat Sep 19 16:39:48 2026 | rebase (finish): returning to refs/heads/navbar-update |
| **b966ae6** | `HEAD@{Sat Sep 19 16:42:46 2026}` | Sat Sep 19 16:42:46 2026 | Sat Sep 19 16:39:48 2026 | rebase (start): checkout main |
| **e570d2b** | `HEAD@{Sat Sep 19 16:40:33 2026}` | Sat Sep 19 16:40:33 2026 | Thu Sep 3 21:41:33 2026 | checkout: moving from main to navbar-update |
| **b966ae6** | `HEAD@{Sat Sep 19 16:39:48 2026}` | Sat Sep 19 16:39:48 2026 | Sat Sep 19 16:39:48 2026 | commit: This contain the content of stash mission |
| **2083a1c** | `HEAD@{Mon Sep 14 17:41:59 2026}` | Mon Sep 14 17:41:59 2026 | Sat Sep 12 16:45:52 2026 | reset: moving to HEAD |
| **2083a1c** | `HEAD@{Sun Sep 13 23:13:33 2026}` | Sun Sep 13 23:13:33 2026 | Sat Sep 12 16:45:52 2026 | reset: moving to HEAD |
| **2083a1c** | `HEAD@{Sun Sep 13 22:45:28 2026}` | Sun Sep 13 22:45:28 2026 | Sat Sep 12 16:45:52 2026 | checkout: moving from navbar-update to main |
| **e570d2b** | `HEAD@{Sun Sep 13 21:01:51 2026}` | Sun Sep 13 21:01:51 2026 | Thu Sep 3 21:41:33 2026 | checkout: moving from main to navbar-update |
| **2083a1c** | `HEAD@{Sun Sep 13 20:59:40 2026}` | Sun Sep 13 20:59:40 2026 | Sat Sep 12 16:45:52 2026 | checkout: moving from navbar-update to main |
| **e570d2b** | `HEAD@{Sun Sep 13 20:58:15 2026}` | Sun Sep 13 20:58:15 2026 | Thu Sep 3 21:41:33 2026 | checkout: moving from main to navbar-update |
| **2083a1c** | `HEAD@{Sun Sep 13 20:44:15 2026}` | Sun Sep 13 20:44:15 2026 | Sat Sep 12 16:45:52 2026 | reset: moving to HEAD |
| **2083a1c** | `HEAD@{Sat Sep 12 16:45:52 2026}` | Sat Sep 12 16:45:52 2026 | Sat Sep 12 16:45:52 2026 | revert: Reapply "Testing revert" |
| **8d17af3** | `HEAD@{Sat Sep 12 16:33:59 2026}` | Sat Sep 12 16:33:59 2026 | Sat Sep 12 16:33:59 2026 | revert: Revert "Testing revert" |
| **88fc71a** | `HEAD@{Sat Sep 12 16:25:21 2026}` | Sat Sep 12 16:25:21 2026 | Sat Sep 12 16:25:21 2026 | commit: Testing revert |
| **a55bce2** | `HEAD@{Sat Sep 12 16:12:20 2026}` | Sat Sep 12 16:12:20 2026 | Wed Sep 9 22:59:25 2026 | reset: moving to ORIG_HEAD |
| **9349b2a** | `HEAD@{Sat Sep 12 15:47:16 2026}` | Sat Sep 12 15:47:16 2026 | Sun Sep 6 20:08:03 2026 | reset: moving to HEAD~1 |
| **a55bce2** | `HEAD@{Sat Sep 12 15:46:19 2026}` | Sat Sep 12 15:46:19 2026 | Wed Sep 9 22:59:25 2026 | reset: moving to ORIG_HEAD |
| **9349b2a** | `HEAD@{Sat Sep 12 15:36:48 2026}` | Sat Sep 12 15:36:48 2026 | Sun Sep 6 20:08:03 2026 | reset: moving to HEAD~1 |
| **a55bce2** | `HEAD@{Sat Sep 12 15:33:14 2026}` | Sat Sep 12 15:33:14 2026 | Wed Sep 9 22:59:25 2026 | reset: moving to ORIG_HEAD |
| **9349b2a** | `HEAD@{Wed Sep 9 23:06:49 2026}` | Wed Sep 9 23:06:49 2026 | Sun Sep 6 20:08:03 2026 | reset: moving to HEAD~1 |
| **a55bce2** | `HEAD@{Wed Sep 9 23:00:26 2026}` | Wed Sep 9 23:00:26 2026 | Wed Sep 9 22:59:25 2026 | reset: moving to HEAD |
| **a55bce2** | `HEAD@{Wed Sep 9 22:59:25 2026}` | Wed Sep 9 22:59:25 2026 | Wed Sep 9 22:59:25 2026 | commit: to learn rest --soft command |
| **9349b2a** | `HEAD@{Sun Sep 6 20:15:37 2026}` | Sun Sep 6 20:15:37 2026 | Sun Sep 6 20:08:03 2026 | checkout: moving from 1373efa60fb67cf3ec56f6e1a4b8d041ccc8c947 to main |
| **1373efa** | `HEAD@{Sun Sep 6 20:14:26 2026}` | Sun Sep 6 20:14:26 2026 | Sun Sep 6 20:14:26 2026 | commit: Detached Head experimer |
| **1fbcb17** | `HEAD@{Sun Sep 6 20:09:44 2026}` | Sun Sep 6 20:09:44 2026 | Sun Aug 30 16:12:27 2026 | checkout: moving from main to 1fbcb17 |
| **9349b2a** | `HEAD@{Sun Sep 6 20:08:03 2026}` | Sun Sep 6 20:08:03 2026 | Sun Sep 6 20:08:03 2026 | commit: changing h2 to h3 |
| **30c9478** | `HEAD@{Sat Sep 5 18:27:38 2026}` | Sat Sep 5 18:27:38 2026 | Thu Sep 3 21:50:04 2026 | checkout: moving from main to main |
| **30c9478** | `HEAD@{Thu Sep 3 21:50:04 2026}` | Thu Sep 3 21:50:04 2026 | Thu Sep 3 21:50:04 2026 | commit (merge): Resolved merge conflict between main and navbar branches |
| **25c6658** | `HEAD@{Thu Sep 3 21:42:03 2026}` | Thu Sep 3 21:42:03 2026 | Mon Aug 31 20:27:50 2026 | checkout: moving from navbar-update to main |
| **e570d2b** | `HEAD@{Thu Sep 3 21:41:33 2026}` | Thu Sep 3 21:41:33 2026 | Thu Sep 3 21:41:33 2026 | commit: successfully removed h1 from navbar branch |
| **9cc8bd5** | `HEAD@{Thu Sep 3 21:30:04 2026}` | Thu Sep 3 21:30:04 2026 | Thu Sep 3 21:26:26 2026 | checkout: moving from main to navbar-update |
| **25c6658** | `HEAD@{Thu Sep 3 21:29:13 2026}` | Thu Sep 3 21:29:13 2026 | Mon Aug 31 20:27:50 2026 | reset: moving to HEAD |
| **25c6658** | `HEAD@{Thu Sep 3 21:27:42 2026}` | Thu Sep 3 21:27:42 2026 | Mon Aug 31 20:27:50 2026 | checkout: moving from navbar-update to main |
| **9cc8bd5** | `HEAD@{Thu Sep 3 21:27:35 2026}` | Thu Sep 3 21:27:35 2026 | Thu Sep 3 21:26:26 2026 | checkout: moving from main to navbar-update |
| **25c6658** | `HEAD@{Thu Sep 3 21:27:04 2026}` | Thu Sep 3 21:27:04 2026 | Mon Aug 31 20:27:50 2026 | checkout: moving from navbar-update to main |
| **9cc8bd5** | `HEAD@{Thu Sep 3 21:26:26 2026}` | Thu Sep 3 21:26:26 2026 | Thu Sep 3 21:26:26 2026 | commit: fixing the code by removing one extra body form the existing code |
| **a5c2582** | `HEAD@{Thu Sep 3 20:55:44 2026}` | Thu Sep 3 20:55:44 2026 | Thu Sep 3 20:55:44 2026 | commit: fixing the merge |
| **3313683** | `Tue Sep 1 17:10:10 2026` | Tue Sep 1 17:10:10 2026 | Sun Aug 30 17:21:48 2026 | checkout: moving from main to navbar-update |
| **25c6658** | `HEAD@{Tue Sep 1 17:10:01 2026}` | Tue Sep 1 17:10:01 2026 | Mon Aug 31 20:27:50 2026 | checkout: moving from navbar-update to main |
| **3313683** | `HEAD@{Tue Sep 1 17:07:12 2026}` | Tue Sep 1 17:07:12 2026 | Sun Aug 30 17:21:48 2026 | checkout: moving from main to navbar-update |
| **25c6658** | `HEAD@{Mon Aug 31 20:27:50 2026}` | Mon Aug 31 20:27:50 2026 | Mon Aug 31 20:27:50 2026 | commit: Adding heading to main branch |
| **1fbcb17** | `HEAD@{Mon Aug 31 20:26:22 2026}` | Mon Aug 31 20:26:22 2026 | Sun Aug 30 16:12:27 2026 | checkout: moving from navbar-update to main |
| **3313683** | `HEAD@{Mon Aug 31 13:06:46 2026}` | Mon Aug 31 13:06:46 2026 | Sun Aug 30 17:21:48 2026 | checkout: moving from main to navbar-update |
| **1fbcb17** | `HEAD@{Mon Aug 31 13:06:34 2026}` | Mon Aug 31 13:06:34 2026 | Sun Aug 30 16:12:27 2026 | checkout: moving from navbar-update to main |
| **3313683** | `HEAD@{Mon Aug 31 13:05:56 2026}` | Mon Aug 31 13:05:56 2026 | Sun Aug 30 17:21:48 2026 | checkout: moving from main to navbar-update |
| **1fbcb17** | `HEAD@{Mon Aug 31 13:04:35 2026}` | Mon Aug 31 13:04:35 2026 | Sun Aug 30 16:12:27 2026 | checkout: moving from navbar-update to main |
| **3313683** | `HEAD@{Sun Aug 30 17:21:48 2026}` | Sun Aug 30 17:21:48 2026 | Sun Aug 30 17:21:48 2026 | commit: Added navbar to the code |
| **1fbcb17** | `HEAD@{Sun Aug 30 17:17:50 2026}` | Sun Aug 30 17:17:50 2026 | Sun Aug 30 16:12:27 2026 | checkout: moving from main to navbar-update |
| **1fbcb17** | `HEAD@{Sun Aug 30 16:14:43 2026}` | Sun Aug 30 16:14:43 2026 | Sun Aug 30 16:12:27 2026 | Branch: renamed refs/heads/master to refs/heads/main |
| **1fbcb17** | `HEAD@{Sun Aug 30 16:12:27 2026}` | Sun Aug 30 16:12:27 2026 | Sun Aug 30 16:12:27 2026 | commit (initial): frist commit |
