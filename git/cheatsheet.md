# Git Cheatsheet

> A structured reference for using Git on Ubuntu with Conda and VSCode.

---

## 1. Initial Setup

| Command | What it Does | Why You Would Use It |
|--------|---------------|----------------------|
| `git config --global user.name "Your Name"` | Sets your Git username globally | So all commits are tagged with your name |
| `git config --global user.email "you@example.com"` | Sets your Git email globally | Required to link commits to your GitHub account |
| `git config --global core.editor "code --wait"` | Sets VSCode as default Git editor | To edit commits or merge messages in VSCode |

---

## 2. Starting a Project

| Command | What it Does | Why You Would Use It |
|--------|---------------|----------------------|
| `git init` | Creates a new local Git repository | To start tracking a folder/project with Git |
| `git clone <url>` | Copies a GitHub repo to your local system | To work on an existing remote project |

---

## 3. Staging and Committing

| Command | What it Does | Why You Would Use It |
|--------|---------------|----------------------|
| `git status` | Shows modified/untracked files | To see what changes are staged or not |
| `git add <file>` | Stages a file for commit | Prepares a file to be included in the next commit |
| `git add .` | Stages all changes in the current directory | Faster way to prepare many files at once |
| `git commit -m "message"` | Commits staged files with a message | Saves a snapshot of your work |
| `git commit -am "message"` | Adds and commits tracked files in one step | Skips `git add` for already tracked files |

---

## 4. Branching and Merging

| Command | What it Does | Why You Would Use It |
|--------|---------------|----------------------|
| `git branch` | Lists all branches | To see what branches exist |
| `git branch <name>` | Creates a new branch | To isolate a feature or experiment |
| `git checkout <name>` | Switches to a branch | To work in a different context |
| `git checkout -b <name>` | Creates and switches to a new branch | Shortcut for starting new branches |
| `git merge <branch>` | Merges another branch into current one | To bring changes from one branch into another |
| `git rebase <branch>` | Moves current branch on top of another | To clean up history before merging |

---

## 5. Remote Collaboration

| Command | What it Does | Why You Would Use It |
|--------|---------------|----------------------|
| `git remote -v` | Lists linked remotes like origin | To verify where push/pull are going |
| `git push origin <branch>` | Uploads local commits to GitHub | To sync your changes online |
| `git pull origin <branch>` | Downloads and merges changes from GitHub | To update your local copy with new changes |
| `git fetch` | Downloads updates without merging | To preview or inspect remote changes safely |

---

## 6. Undo and Fix

| Command | What it Does | Why You Would Use It |
|--------|---------------|----------------------|
| `git log` | Shows commit history | To review past work |
| `git diff` | Shows file differences | To see what changed before committing |
| `git restore <file>` | Discards local changes to a file | To undo unstaged edits |
| `git reset HEAD <file>` | Unstages a file | To undo `git add` |
| `git reset --soft HEAD~1` | Undoes last commit but keeps changes | To rewrite history without losing work |
| `git reset --hard HEAD` | Resets all changes to last commit | To revert to a clean state |
| `git clean -fd` | Deletes untracked files/directories | To purge ignored or stray files |

---

## 7. Conflict Handling and Rewriting History

| Command | What it Does | Why You Would Use It |
|--------|---------------|----------------------|
| `git stash` | Temporarily saves uncommitted work | To switch branches or pull safely |
| `git stash pop` | Restores the last stashed changes | To resume where you left off |
| `git cherry-pick <hash>` | Applies a single commit from another branch | To selectively bring changes |
| `git revert <hash>` | Creates a new commit that undoes another | To safely reverse a commit without rewriting history |
| `git rebase -i HEAD~n` | Interactive rebase for last `n` commits | To squash, reorder, or fix commit messages |

---
