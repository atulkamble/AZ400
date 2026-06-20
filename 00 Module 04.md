# Module 04: Azure Repos - Complete Master Guide

---

# 1. Azure Repos Overview

Azure Repos is a source code management service in Azure DevOps that provides:

| Feature             | Description                   |
| ------------------- | ----------------------------- |
| Git Repositories    | Distributed Version Control   |
| TFVC                | Centralized Version Control   |
| Branching           | Create isolated code versions |
| Pull Requests       | Code Review Process           |
| Repository Security | Role-based access             |
| Integration         | Boards, Pipelines, Test Plans |

---

## Azure Repos Architecture

```text
Developer
    │
    ▼
Local Repository
    │
    ├── Commit
    │
    ▼
Azure Repos (Remote)
    │
    ├── Pull Requests
    ├── Code Reviews
    ├── Branch Policies
    │
    ▼
Azure Pipelines
    │
    ▼
Deployment
```

---

# 2. What is .gitignore?

A `.gitignore` file tells Git which files or folders should NOT be tracked.

---

## Example .gitignore

### Python Project

```bash
__pycache__/
*.pyc
venv/
.env
*.log
```

### NodeJS Project

```bash
node_modules/
.env
dist/
coverage/
```

### Azure DevOps Project

```bash
.vscode/
*.user
*.tmp
bin/
obj/
```

---

## Why Use .gitignore?

| Benefit              | Description              |
| -------------------- | ------------------------ |
| Security             | Avoid committing secrets |
| Cleaner Repo         | Ignore temp files        |
| Faster Push          | Smaller repository       |
| Better Collaboration | Consistent codebase      |

---

# 3. Team Foundation Version Control (TFVC)

Before Git became popular, Microsoft introduced TFVC.

---

## Git vs TFVC

| Feature      | Git               | TFVC        |
| ------------ | ----------------- | ----------- |
| Architecture | Distributed       | Centralized |
| Offline Work | Yes               | Limited     |
| Branching    | Easy              | Complex     |
| Speed        | Faster            | Slower      |
| Popularity   | Industry Standard | Legacy      |

---

## TFVC Architecture

```text
Developer Machine
        │
        ▼
Check Out File
        │
        ▼
TFVC Server
        │
        ▼
Check In Changes
```

---

## TFVC Commands

### Get Latest

```bash
tf get
```

### Checkout

```bash
tf checkout file.txt
```

### Checkin

```bash
tf checkin
```

---

# 4. Azure Boards Integration with GitHub

Azure Boards can track GitHub work.

---

## Integration Architecture

```text
GitHub Repository
       │
       ▼
Commit / Pull Request
       │
       ▼
Azure Boards Work Item
       │
       ▼
Sprint Tracking
```

---

## Demo Steps

### Step 1

Open:

```text
Azure DevOps
→ Project Settings
→ GitHub Connections
```

---

### Step 2

Connect GitHub Account

```text
Authorize GitHub
Select Repository
```

---

### Step 3

Link Work Item

Commit Example:

```bash
git commit -m "Added login page AB#101"
```

Azure Board ID:

```text
101
```

Automatically linked.

---

# 5. Azure Repos Fork

Fork creates a personal copy of a repository.

---

## Fork Architecture

```text
Main Repository
       │
       ▼
Fork Repository
       │
       ▼
Feature Development
       │
       ▼
Pull Request
       │
       ▼
Main Repository
```

---

## Demo Steps

```text
Repos
→ Select Repository
→ Fork
→ Choose Project
→ Create
```

---

# 6. Git Credentials

Git requires authentication.

---

## Credential Types

| Method            | Recommended |
| ----------------- | ----------- |
| PAT Token         | Yes         |
| SSH Key           | Yes         |
| Username Password | No          |
| Service Principal | Automation  |

---

## Create PAT Token

```text
Azure DevOps
→ User Settings
→ Personal Access Tokens
→ New Token
```

Permissions:

```text
Code Read & Write
```

---

## Configure Git Credentials

```bash
git config --global user.name "Atul Kamble"

git config --global user.email "atul@example.com"
```

Verify

```bash
git config --list
```

---

# 7. Clone Azure Repos Repository

---

## Clone Using HTTPS

```bash
git clone https://dev.azure.com/org/project/_git/app
```

---

## Clone Using SSH

```bash
git clone git@ssh.dev.azure.com:v3/org/project/app
```

---

## Verify

```bash
cd app

git remote -v
```

---

# 8. Import GitHub Repository into Azure Repos

---

## Azure Portal Steps

```text
Azure DevOps
→ Repos
→ Import Repository
```

---

Enter GitHub URL

```text
https://github.com/username/project.git
```

---

## Architecture

```text
GitHub Repo
      │
      ▼
Import
      │
      ▼
Azure Repos
```

---

# 9. Push Branches to Remote Repository

---

## Create Branch

```bash
git checkout -b feature-login
```

---

## Add Files

```bash
git add .
```

---

## Commit

```bash
git commit -m "Login feature added"
```

---

## Push Branch

```bash
git push origin feature-login
```

---

## Verify

```bash
git branch -a
```

---

# 10. Pull from Remote Repository

---

## Pull Latest Changes

```bash
git pull origin main
```

---

## Fetch Only

```bash
git fetch
```

---

## Fetch + Merge

```bash
git pull
```

---

## Workflow

```text
Remote Repository
       │
       ▼
Git Fetch
       │
       ▼
Local Repository
       │
       ▼
Git Pull
```

---

# 11. Pull Request (PR)

Pull Request is a code review mechanism.

---

## PR Workflow

```text
Feature Branch
      │
      ▼
Push
      │
      ▼
Create PR
      │
      ▼
Code Review
      │
      ▼
Approval
      │
      ▼
Merge to Main
```

---

## Create Pull Request

```text
Repos
→ Pull Requests
→ New Pull Request
```

---

### Source

```text
feature-login
```

### Target

```text
main
```

---

## Branch Policy

```text
Minimum Reviewers = 2
Build Validation = Required
Comments Resolution = Required
```

---

# 12. Working with Git Repository Using Visual Studio

---

## Clone Repository

```text
Visual Studio
→ Git
→ Clone Repository
```

Paste URL:

```text
https://dev.azure.com/org/project/_git/app
```

---

## Create Branch

```text
Git
→ New Branch
```

Example:

```text
feature-login
```

---

## Commit Changes

```text
Git Changes
→ Enter Message
→ Commit All
```

---

## Push Changes

```text
Git Changes
→ Push
```

---

# 13. Create GitHub Branches Using Visual Studio

---

## Steps

```text
Git
→ Manage Branches
→ New Branch
```

Branch Name:

```text
feature-payment
```

---

## Visual Studio Equivalent

CLI:

```bash
git checkout -b feature-payment
```

---

# 14. Push Code to Azure Repos Using Visual Studio

---

## Workflow

```text
Code Changes
      │
      ▼
Commit
      │
      ▼
Push
      │
      ▼
Azure Repos
```

---

## Visual Studio Steps

```text
Git Changes
→ Commit All
→ Push
```

---

## Command Line Equivalent

```bash
git add .

git commit -m "Updated code"

git push origin main
```

---

# Complete Azure Repos Hands-On Lab

## Lab Architecture

```text
Developer Machine
        │
        ▼
Git Installed
        │
        ▼
Azure Repos
        │
 ┌──────┴───────┐
 │              │
 ▼              ▼
Branch A      Branch B
 │              │
 └──────┬───────┘
        ▼
Pull Request
        ▼
Main Branch
```

---

# End-to-End Demo

## Create Repository

```text
Azure DevOps
→ Repos
→ New Repository
→ azure-repos-lab
```

---

## Clone

```bash
git clone https://dev.azure.com/ORG/PROJECT/_git/azure-repos-lab

cd azure-repos-lab
```

---

## Create File

```bash
echo "Azure Repos Demo" > index.html
```

---

## Commit

```bash
git add .

git commit -m "Initial Commit"
```

---

## Push

```bash
git push origin main
```

---

## Create Branch

```bash
git checkout -b feature-homepage
```

---

## Modify

```bash
echo "<h1>Welcome Azure DevOps</h1>" >> index.html
```

---

## Push Branch

```bash
git add .

git commit -m "Homepage Added"

git push origin feature-homepage
```

---

## Create PR

```text
Repos
→ Pull Requests
→ New PR
→ Review
→ Complete Merge
```

---

# Azure Repos Interview Questions

| Question                           | Answer                                   |
| ---------------------------------- | ---------------------------------------- |
| What is Azure Repos?               | Source Code Management Service           |
| Difference between Git and TFVC?   | Distributed vs Centralized               |
| What is .gitignore?                | Ignore unwanted files                    |
| What is Fork?                      | Copy of repository                       |
| What is Pull Request?              | Code review mechanism                    |
| What is PAT?                       | Personal Access Token                    |
| Difference between Fetch and Pull? | Fetch downloads, Pull downloads + merges |
| What is Branch Policy?             | Repository governance rules              |
| Why use Feature Branches?          | Isolated development                     |
| What is Merge Conflict?            | Conflicting code changes                 |

---

# Points to Remember (Exam & Interview)

✅ Azure Repos supports Git and TFVC

✅ Git is the recommended version control system

✅ Always use feature branches

✅ Use Pull Requests before merging

✅ Configure Branch Policies

✅ Never store passwords in repositories

✅ Use `.gitignore`

✅ Use PAT or SSH for authentication

✅ Commit frequently with meaningful messages

✅ Pull latest code before pushing changes

✅ Azure Boards can be linked using `AB#WorkItemID`

✅ Azure Repos integrates seamlessly with Azure Pipelines for CI/CD automation.
