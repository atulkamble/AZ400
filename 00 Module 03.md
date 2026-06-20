# Module 03 – GitHub & Version Control System (Complete Training Guide)

---

# 1. What is Version Control System (VCS)?

A Version Control System tracks changes made to source code, documents, and configuration files over time.

### Without VCS

```text
Project
│
├── Final_Code.zip
├── Final_Code_V2.zip
├── Final_Code_Latest.zip
├── Final_Code_Really_Final.zip
```

Problems:

❌ No history

❌ Difficult rollback

❌ Team conflicts

❌ Lost code

---

### With VCS

```text
Developer
     │
     ▼
Git Repository
     │
     ▼
History of Changes
     │
     ▼
Rollback Anytime
```

Benefits:

✅ Change Tracking

✅ Team Collaboration

✅ Backup

✅ Branching

✅ Rollback

---

# 2. What is Git?

Git is a Distributed Version Control System (DVCS) created by Linus Torvalds.

Git stores:

* Source Code
* Configuration Files
* Documentation
* Infrastructure as Code

Examples:

```bash
Terraform
CloudFormation
ARM Templates
Bicep
Kubernetes YAML
Dockerfiles
```

---

# 3. What is GitHub?

GitHub is a cloud-hosted platform that stores Git repositories.

Git = Version Control Tool

GitHub = Repository Hosting Platform

---

## Git vs GitHub

| Feature        | Git      | GitHub         |
| -------------- | -------- | -------------- |
| Type           | Software | Cloud Platform |
| Works Offline  | Yes      | No             |
| Stores History | Yes      | Yes            |
| Collaboration  | Limited  | Excellent      |
| Pull Requests  | No       | Yes            |
| Code Review    | No       | Yes            |

---

# 4. Distributed Version Control System (DVCS)

Traditional System:

```text
Developer
    │
    ▼
Central Server
```

If server fails → work stops.

---

Git Architecture

```text
Developer 1
      │
Developer 2
      │
Developer 3
      ▼
 Complete Copy of Repository
```

Every developer has:

* Full history
* Branches
* Commits

Can work offline.

---

# 5. Git Architecture

```text
                GitHub Repository
                        │
          ┌─────────────┼─────────────┐
          │             │             │
          ▼             ▼             ▼
     Developer1    Developer2    Developer3
        Git Repo      Git Repo      Git Repo
```

---

# 6. Install Git

## Ubuntu

```bash
sudo apt update
sudo apt install git -y
```

Verify:

```bash
git --version
```

---

## Windows

Download:

```text
https://git-scm.com/downloads
```

Verify:

```powershell
git --version
```

---

# 7. Configure Git

```bash
git config --global user.name "Atul Kamble"

git config --global user.email "atul@example.com"
```

Check:

```bash
git config --list
```

---

# 8. Create Local Git Repository

## Step 1: Create Project

```bash
mkdir myproject

cd myproject
```

---

## Step 2: Initialize Git

```bash
git init
```

Output:

```text
Initialized empty Git repository
```

---

## Step 3: Create File

```bash
echo "Hello Git" > app.py
```

---

## Step 4: Check Status

```bash
git status
```

Output:

```text
Untracked files:
app.py
```

---

## Step 5: Add File

```bash
git add app.py
```

or

```bash
git add .
```

---

## Step 6: Commit

```bash
git commit -m "Initial Commit"
```

---

# Local Repository Architecture

```text
Working Directory
       │
git add
       ▼
Staging Area
       │
git commit
       ▼
Local Repository
```

---

# 9. Push Code from Local Repository to Central Repository

---

## Create Repository in GitHub

```text
GitHub
 └── New Repository
      └── myproject
```

---

## Connect Local Repo

```bash
git remote add origin https://github.com/user/myproject.git
```

Verify:

```bash
git remote -v
```

---

## Push Code

```bash
git push -u origin main
```

---

Architecture:

```text
Developer Laptop
       │
       ▼
 Local Git Repo
       │ git push
       ▼
 GitHub Repository
```

---

# Azure Demonstration

## Create GitHub Repository

```text
GitHub
 └── Create Repo
```

---

## Create Azure DevOps Project

```text
Azure DevOps
    └── New Project
```

---

## Clone Repository

```bash
git clone https://github.com/user/demo.git
```

---

## Make Changes

```bash
echo "Azure DevOps Demo" > app.py
```

---

## Commit

```bash
git add .

git commit -m "Added App"
```

---

## Push

```bash
git push origin main
```

---

Verify in:

```text
Azure Repos
OR
GitHub Repository
```

---

# 10. Identify Commits Not Pushed to Remote Repository

## Check Status

```bash
git status
```

Example:

```text
Your branch is ahead of origin/main by 2 commits.
```

---

## Compare Local vs Remote

```bash
git log origin/main..HEAD
```

Shows:

```text
Local commits not pushed
```

---

## Count Unpushed Commits

```bash
git rev-list --count origin/main..HEAD
```

Output:

```text
2
```

---

## One-Line View

```bash
git log --oneline origin/main..HEAD
```

Output:

```text
34bc56 Added Login
67cd78 Fixed Bug
```

---

# 11. Working with Branches

---

## View Branches

```bash
git branch
```

---

## Create Branch

```bash
git branch dev
```

---

## Switch Branch

```bash
git checkout dev
```

OR

```bash
git switch dev
```

---

## Create and Switch

```bash
git checkout -b feature-login
```

OR

```bash
git switch -c feature-login
```

---

## Push Branch

```bash
git push origin feature-login
```

---

Branch Architecture

```text
main
 │
 ├── feature-login
 │
 ├── feature-payment
 │
 └── feature-cart
```

---

# Real Azure DevOps Branch Workflow

```text
main
 │
 ├── dev
 │     │
 │     └── feature-login
 │
 └── release
```

Workflow:

```text
Feature Branch
      │
      ▼
Pull Request
      │
      ▼
Dev Branch
      │
      ▼
Main Branch
```

---

# 12. Switch from One Commit to Another

---

## View Commit History

```bash
git log --oneline
```

Example:

```text
a1234 Initial Commit
b5678 Added Login
c9876 Fixed Bug
```

---

## Checkout Specific Commit

```bash
git checkout b5678
```

Detached HEAD State:

```text
HEAD detached at b5678
```

---

## Return to Main

```bash
git checkout main
```

---

## Create Branch from Old Commit

```bash
git checkout -b hotfix b5678
```

---

# Rollback Architecture

```text
Commit1
   │
Commit2
   │
Commit3
   │
Commit4
   │
   ▼
Rollback to Commit2
```

---

# 13. Useful Git Commands

| Command       | Purpose          |
| ------------- | ---------------- |
| git init      | Create repo      |
| git clone     | Copy repo        |
| git status    | Check changes    |
| git add .     | Add files        |
| git commit -m | Save changes     |
| git push      | Upload code      |
| git pull      | Download changes |
| git fetch     | Fetch updates    |
| git branch    | List branches    |
| git checkout  | Switch branch    |
| git merge     | Merge branches   |
| git log       | View history     |
| git reset     | Undo changes     |
| git revert    | Rollback commit  |

---

# Git Workflow Cheat Sheet

```bash
git clone REPO_URL

git status

git add .

git commit -m "New Feature"

git push origin main
```

---

# GitHub + Azure DevOps Architecture

```text
Developer
    │
    ▼
Local Git Repository
    │
    ▼
GitHub / Azure Repos
    │
    ▼
Pull Request
    │
    ▼
Code Review
    │
    ▼
Merge
    │
    ▼
Azure Pipeline
    │
    ▼
Deployment
```

---

# Interview Questions

### Q1. What is Git?

A distributed version control system used to track source code changes.

---

### Q2. Difference between Git and GitHub?

Git = Tool

GitHub = Hosting Platform

---

### Q3. What is Commit?

A snapshot of code changes.

---

### Q4. What is Branch?

An isolated development line.

---

### Q5. What is Merge?

Combining branch changes.

---

### Q6. Difference between Fetch and Pull?

| Fetch             | Pull                |
| ----------------- | ------------------- |
| Downloads changes | Downloads + Merges  |
| Safe              | Modifies local code |

---

### Q7. What is HEAD?

Current active commit pointer.

---

### Q8. What is Detached HEAD?

Viewing an old commit directly without being on a branch.

---

### Q9. How to identify commits not pushed?

```bash
git log origin/main..HEAD
```

---

### Q10. What is Pull Request?

A request to merge code after review.

---

# Important Points to Remember

✅ Git is Distributed VCS

✅ Every commit has unique SHA ID

✅ git add → Stage Changes

✅ git commit → Save Changes

✅ git push → Upload Changes

✅ git pull → Download Changes

✅ Feature branches improve collaboration

✅ Never commit secrets/passwords

✅ Use `.gitignore` for sensitive files

✅ Always pull latest code before pushing

✅ Pull Requests should be reviewed before merge

---

# Hands-On Lab

### Lab 1 – Create Local Repository

```bash
mkdir gitlab1
cd gitlab1
git init
touch app.py
git add .
git commit -m "Initial Commit"
```

---

### Lab 2 – Push to GitHub

```bash
git remote add origin REPO_URL

git push -u origin main
```

---

### Lab 3 – Branching

```bash
git checkout -b feature-login

echo "Login Module" >> app.py

git add .
git commit -m "Added Login"

git push origin feature-login
```

---

### Lab 4 – Find Unpushed Commits

```bash
git log origin/main..HEAD

git rev-list --count origin/main..HEAD
```

This module provides the foundation required for GitHub, Azure Repos, Azure DevOps Pipelines, CI/CD, Terraform collaboration, Infrastructure as Code, and enterprise DevOps workflows.
