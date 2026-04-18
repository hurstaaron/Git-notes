# Git CHEAT SHEET
## GIT CLONE - CLONING A REPO 
| Command | What It Does |
|---------|--------------|
| `git log --oneline` | Shows the log of commits made locally regardless of push status. |
| `git remote -v` | Points to the URL for fetching and pushing. |

**Example** `9465116 (HEAD -> main, origin/main, origin/HEAD) Initial commit`

**Key Concept:** `Key Concept: origin` is the nickname my PC gives the GitHub copy of my repo.

## GIT PUSH
| Command | What It Does |
|---------|--------------|
|`Golden Rule` | When done working, add, commit, and push, LAST before closing down for the day. |
| `git add .` | Packages changes made locally for push to GitHub (box packed but not ready to ship). |
| `git commit -m "message"` | Labels the changes (seals the box and puts the shipping label on it). |
| `git push` | Sends the local changes to GitHub (the only command that talks to the internet). |

## GIT PULL
| Command | What It Does |
|---------|--------------|
|`Golden Rule` | When sitting down to at a machine, git pull, FIRST before anything else. |
| `git pull` | Reaches into origin(GitHub) and downloads any new commits on GitHub but not on my local machine. |

## GIT INIT - CREATING A REPO FROM SCRATCH
| Command | What It Does |
|---------|--------------|
| `git init` | Creates a brand new, empty Git repo in the designated folder and makes a hidden .git folder. |
| `git remote add origin <URL>` | Manually sets up the connection to GitHub that clone does automatically. |

### git init Workflow
1. `mkdir C:\Dev\School\NewProject`
2. `cd C:\Dev\School\NewProject`
3. `git init`
4. `git remote add origin https://github.com/hurstaaron/NewProject.git`
5. `git add .`
6. `git commit -m "Initial Commit"`
7. `git push -u origin main`

## GitHub CLI (gh)
| Command | What It Does |
|---------|-------------|
| `gh --version` | Checks if GitHub CLI is installed and shows the version |
| `gh auth login` | Authenticates your machine with GitHub through the browser |
| `gh auth status` | Shows whether you're logged in and which account |
| `gh repo create owner/repo-name --public --clone` | Creates a new repo on GitHub AND clones it to your machine in one command |
| `gh repo delete owner/repo-name --yes` | Permanently deletes a repo from GitHub (cannot be undone) |
| `gh repo list owner` | Lists all repos under an account |
| `gh auth refresh -h github.com -s delete_repo` | Adds delete permission to your GitHub CLI authentication |

**Key Concept:** `gh` is not the same as `git`. `git` manages your code and history. `gh` manages GitHub-specific things like creating repos, deleting repos, and authentication. They work together but do different jobs.

## Branch Naming
| Command | What It Does |
|---------|-------------|
| `git branch -M main` | Renames your current branch (e.g., from master to main) |

**Key Concept:** GitHub defaults to `main`. Older versions of Git default to `master`. If they don't match, your push will create a separate branch instead of going where you expect. Use `git branch -M main` on first commit if needed.

## Important Rules

**Always be inside a repo folder.** Git commands only work when you're inside the repo's directory or a subfolder of it. If you get "not a git repository" it means you're in the wrong folder. Use `cd` to navigate into your repo first.

**`git push -u origin main`** is needed on the first push of a new repo. The `-u` tells Git to remember that `main` tracks `origin/main`. After the first time, plain `git push` works.
