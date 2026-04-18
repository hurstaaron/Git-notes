# Git CHEAT SHEET
## git clone - CLONING A REPO 
| Command | What It Does |
|---------|--------------|
| `git log --oneline` | Shows the log of commits made locally regardless of push status. |
| `git remote -v` | Points to the URL for fetching and pushing. |
**Example** `9465116 (HEAD -> main, origin/main, origin/HEAD) Initial commit`
**Key Concept:** `Key Concept: origin` is the nickname my PC gives the GitHub copy of my repo.

## git push
| Command | What It Does |
|---------|--------------|
|`Golden Rule` | When done working, add, commit, and push, LAST before closing down for the day. |
| `git add .` | Packages changes made locally for push to GitHub (box packed but not ready to ship). |
| `git commit -m "message"` | Labels the changes (seals the box and puts the shipping label on it). |
| `git push` | Sends the local changes to GitHub (the only command that talks to the internet). |

## git pull
| Command | What It Does |
|---------|--------------|
|`Golden Rule` | When sitting down to at a machine, git pull, FIRST before anything else. |
| `git pull` | Reaches into origin(GitHub) and downloads any new commits on GitHub but not on my local machine. |

## git init - CREATING A REPO FROM SCRATCH
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


