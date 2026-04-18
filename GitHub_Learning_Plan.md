# GitHub Mastery: Beginner to Expert
### A PowerShell-First Learning Plan for Aaron
---

## Phase 1: Foundation (Weeks 1–2)
**Goal:** Understand what Git actually is, how it differs from GitHub, and get comfortable with the core loop.

### 1.1 — Core Concepts (Theory)
- What is version control and why it exists
- Git (local tool) vs GitHub (remote platform) — the critical distinction
- Repositories, commits, branches, and remotes — the four pillars
- The three Git zones: Working Directory → Staging Area → Repository
- How Git stores data (snapshots, not diffs — and why that matters)

### 1.2 — Environment Setup (PowerShell)
- Installing Git for Windows (and verifying with `git --version`)
- Configuring your identity: `git config --global user.name` / `user.email`
- SSH key generation: `ssh-keygen` and adding to GitHub
- HTTPS vs SSH authentication — when to use which
- Setting your default editor and other useful config options
- PowerShell aliases and profile customization for Git

### 1.3 — The Core Loop (Daily Driver Commands)
- `git init` — creating a repo from scratch
- `git clone` — pulling down an existing repo
- `git status` — your best friend (check it constantly)
- `git add` — staging changes (file-level and hunk-level with `-p`)
- `git commit -m` — saving snapshots with meaningful messages
- `git push` / `git pull` — syncing with GitHub
- `git log` — reading your project's history

### 1.4 — Hands-On Project
- Clean up your existing repos (delete the junk, rename the keepers)
- Practice the full clone → edit → stage → commit → push cycle
- Write your first proper README.md

---

## Phase 2: Branching & Collaboration (Weeks 3–4)
**Goal:** Work with branches confidently and understand how teams use Git.

### 2.1 — Branching
- What branches actually are (pointers to commits)
- `git branch` — listing, creating, deleting branches
- `git checkout` / `git switch` — moving between branches
- `git merge` — combining work (fast-forward vs three-way)
- `git branch -d` vs `git branch -D` — safe delete vs force delete

### 2.2 — Merge Conflicts
- Why conflicts happen (and why they're not scary)
- Reading conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
- Resolving conflicts manually in your editor
- `git merge --abort` — the escape hatch
- Practice: intentionally creating and resolving conflicts

### 2.3 — Remote Collaboration
- `git remote -v` — understanding your remotes
- `git fetch` vs `git pull` — the important difference
- `git push -u origin <branch>` — tracking branches
- Forking vs cloning — when to use each
- Pull Requests (PRs) — creating, reviewing, and merging on GitHub

### 2.4 — Hands-On Project
- Create a feature branch on one of your course repos
- Make changes, push the branch, open a PR on GitHub
- Merge it yourself and delete the branch (both remote and local)

---

## Phase 3: History & Undoing Mistakes (Weeks 5–6)
**Goal:** Navigate and rewrite history. Fix mistakes without panic.

### 3.1 — Reading History
- `git log --oneline --graph --all` — visualizing the tree
- `git log --author`, `--since`, `--grep` — filtering history
- `git diff` — comparing working directory, staging, and commits
- `git show <commit>` — inspecting a specific commit
- `git blame` — finding who changed what and when

### 3.2 — Undoing Things (The Safety Net)
- `git restore` — discarding working directory changes
- `git restore --staged` — unstaging files
- `git commit --amend` — fixing the last commit
- `git revert` — safely undoing a commit (creates a new commit)
- `git reset --soft`, `--mixed`, `--hard` — the three reset modes
- The golden rule: never rewrite history that's been pushed (unless you know exactly what you're doing)

### 3.3 — Stashing
- `git stash` — shelving work temporarily
- `git stash list` / `git stash pop` / `git stash apply`
- `git stash drop` / `git stash clear`
- When stashing saves your life (mid-feature branch switches)

### 3.4 — Hands-On Project
- Practice amending commits, reverting, and resetting on a test repo
- Use `git reflog` to recover a "lost" commit
- Stash workflow exercise: interrupt work, switch branches, come back

---

## Phase 4: Intermediate Workflows (Weeks 7–8)
**Goal:** Adopt professional workflows and organize your GitHub presence.

### 4.1 — .gitignore & Repository Hygiene
- Writing `.gitignore` files (and why they matter enormously)
- Global `.gitignore` for your machine
- Common patterns: `__pycache__/`, `*.o`, `.env`, `node_modules/`
- Removing tracked files that should have been ignored: `git rm --cached`
- Repository naming conventions and organization strategy

### 4.2 — Commit Discipline
- Writing good commit messages (imperative mood, why not just what)
- Atomic commits — one logical change per commit
- `git add -p` — staging specific hunks for cleaner commits
- Squashing messy commits before pushing

### 4.3 — Git Workflow Models
- Feature Branch Workflow (what most teams use)
- Git Flow (develop/main/release/hotfix branches)
- Trunk-Based Development (what big tech often uses)
- When to use which — and why it depends on team size

### 4.4 — GitHub Features
- Issues — tracking bugs and features
- Labels, milestones, and project boards
- GitHub Actions — intro to CI/CD (automated testing on push)
- Branch protection rules — preventing direct pushes to main
- CODEOWNERS file

### 4.5 — Hands-On Project
- Set up a proper `.gitignore` for each of your remaining repos
- Add GitHub Actions to run a simple test on one of your Python repos
- Create an Issue, link a PR to it, and close it via commit message

---

## Phase 5: Advanced Git (Weeks 9–11)
**Goal:** Power-user techniques that separate competent from expert.

### 5.1 — Rebasing
- `git rebase` — what it does and how it differs from merge
- Interactive rebase: `git rebase -i` (squash, reword, edit, drop)
- `git pull --rebase` — keeping a linear history
- When to rebase vs when to merge
- The danger zone: rebasing shared branches

### 5.2 — Cherry-Picking & Advanced Selection
- `git cherry-pick` — grabbing specific commits
- `git bisect` — binary search for the commit that broke things
- `git reflog` — the true safety net (recovering anything)
- `git tag` — marking releases and important commits

### 5.3 — Submodules & Subtrees
- When you need a repo inside a repo
- `git submodule add` / `update` / `init`
- Subtrees as an alternative (and when each is appropriate)
- Managing dependencies across your projects

### 5.4 — Advanced Remotes
- Working with multiple remotes (origin + upstream)
- Keeping a fork in sync with the original
- `git remote add upstream` → `git fetch upstream` → `git merge upstream/main`
- Force push safely: `git push --force-with-lease`

### 5.5 — Hands-On Project
- Interactive rebase to clean up a messy branch history
- Use `git bisect` to find a bug in a test repo
- Fork an open-source repo, sync it, and submit a PR

---

## Phase 6: GitHub Ecosystem & Automation (Weeks 12–14)
**Goal:** Use GitHub as a full development platform, not just a code host.

### 6.1 — GitHub Actions Deep Dive
- Workflow YAML syntax
- Triggers: push, pull_request, schedule, manual dispatch
- Building CI pipelines for C++ and Python projects
- Auto-testing, linting, and building on every push
- Secrets management for API keys

### 6.2 — GitHub Pages
- Hosting a portfolio site directly from a repo
- Setting up your `hurstaaron.github.io` personal page
- Deploying project documentation

### 6.3 — GitHub CLI (`gh`)
- Installing and authenticating
- `gh repo create`, `gh pr create`, `gh issue list`
- Managing your GitHub workflow entirely from PowerShell
- Scripting with `gh` for automation

### 6.4 — Templates & Automation
- Issue templates and PR templates
- Repository templates (for spinning up new course repos fast)
- Dependabot for security updates
- Release automation

### 6.5 — Hands-On Project
- Build a CI pipeline for your C++ and ML repos
- Deploy EnginuityIQ website via GitHub Pages
- Create a repo template for future coursework

---

## Phase 7: Expert & Teaching Preparation (Weeks 15–16)
**Goal:** Solidify mastery and prepare to teach others.

### 7.1 — Git Internals
- The object model: blobs, trees, commits, tags
- How the SHA-1 hash system works
- The `.git` directory — what every file and folder does
- Packfiles and garbage collection
- Understanding this makes debugging anything possible

### 7.2 — Troubleshooting & Recovery
- Common disaster scenarios and how to fix each one
- Detached HEAD state — what it means and how to recover
- Recovering deleted branches and lost commits
- Fixing a messed-up rebase
- Dealing with large files accidentally committed (BFG Repo Cleaner)

### 7.3 — Building Your Teaching Curriculum
- Creating a demo repository with intentional exercises
- Designing exercises that progressively build skill
- Common student mistakes and how to address them
- Cheat sheets and reference materials

### 7.4 — Portfolio & Professional Presence
- Organizing your GitHub profile for recruiters and collaborators
- Pinned repositories strategy
- Contribution graph — what it signals
- Writing READMEs that actually help people
- License selection for your projects

---

## Quick Reference: Command Progression

| Phase | Key Commands |
|-------|-------------|
| 1 | `git init, clone, status, add, commit, push, pull, log` |
| 2 | `git branch, switch, merge, remote, fetch` |
| 3 | `git restore, revert, reset, stash, diff, blame, reflog` |
| 4 | `git add -p, rm --cached, tag` |
| 5 | `git rebase -i, cherry-pick, bisect, submodule` |
| 6 | `gh repo, gh pr, gh issue` (GitHub CLI) |
| 7 | `git cat-file, git fsck, git gc` (internals) |

---

## Notes
- Each phase builds on the previous one — do not skip ahead
- Every concept will be taught with PowerShell commands first
- Theory is paired with immediate hands-on practice
- Your existing repos serve as our live training ground
- By the end, you will be able to teach this material to other students
