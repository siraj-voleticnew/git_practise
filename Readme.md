# Git & GitHub — A Beginner's Guide

This README gives a concise introduction to Git (the distributed version control system) and GitHub (a cloud hosting/service for Git repositories). Learn the basic commands and workflows to start tracking code, collaborating, and contributing.

## What is Git?
- Git is a version control system that records changes to files over time. It lets you track history, create branches, and collaborate with others.

## What is GitHub?
- GitHub is a platform that hosts Git repositories, provides collaboration tools (pull requests, issues, code review), and integrates with CI/CD and project management.

## Quick Setup
Configure your name and email (runs once):

```bash
git config --global user.name "Your Name"
git config --global user.email you@example.com
```

## Create or Clone a Repository
- Initialize a new local repo:

```bash
git init
```

- Clone an existing GitHub repo:

```bash
git clone https://github.com/username/repo.git
```

## Basic Local Workflow
1. Check status:

```bash
git status
```

2. Stage changes:

```bash
git add file.txt        # add one file
git add .               # add all changed files
```

3. Commit staged changes:

```bash
git commit -m "Short, descriptive message"
```

4. View history:

```bash
git log --oneline
```

Tips: write clear commit messages, and make small, focused commits.

## Branching & Merging
- Create and switch to a branch:

```bash
git branch feature-x
git switch feature-x     # or: git checkout -b feature-x
```

- Merge back to main (on `main` branch):

```bash
git switch main
git merge feature-x
```

- Delete a branch when done:

```bash
git branch -d feature-x
```

## Working with Remotes (GitHub)
- Add a remote (only if not cloned):

```bash
git remote add origin https://github.com/username/repo.git
```

- Push your branch and set upstream:

```bash
git push -u origin feature-x
```

- Fetch and integrate upstream changes:

```bash
git pull origin main
```

## Typical GitHub Flow
1. Fork (optional) and clone the repository.
2. Create a topic branch for your work.
3. Commit changes locally and push the branch to GitHub.
4. Open a Pull Request (PR) on GitHub to request merging.
5. Request reviews, address comments, and merge when approved.

## .gitignore
Use a `.gitignore` file to exclude files you don't want in the repo (build outputs, secrets, system files). Example:

```
# Python
__pycache__/
*.pyc

# Node
node_modules/

# Editor
.vscode/
```

## Best Practices
- Pull before you push to avoid conflicts.
- Keep commits small and focused.
- Use branches for features and fixes.
- Review PRs carefully; include tests where possible.

## Helpful Resources
- Official Git docs: https://git-scm.com/doc
- GitHub Guides: https://docs.github.com/en/get-started
- Interactive tutorial: https://learngitbranching.js.org/

---
If you'd like, I can also:
- commit this file for you and create an initial commit,
- add a `.gitignore` tailored to your project,
- or expand the README with screenshots and GitHub PR examples.

