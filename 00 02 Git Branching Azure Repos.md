# Git, GitHub & Azure Repos Practice Guide

## Version Control Systems (VCS)

Version Control Systems help developers track code changes, collaborate with teams, maintain history, and manage software releases.

### Popular Programming Technologies

| Technology  | Purpose                                              |
| ----------- | ---------------------------------------------------- |
| C           | System Programming                                   |
| C++         | OOP, Games, High Performance Applications            |
| Python      | Data Science, Statistics, Machine Learning, AI       |
| Flask       | Python Web Application Framework                     |
| Golang (Go) | Cloud Native Applications, Microservices             |
| Java        | Object-Oriented Programming, Enterprise Applications |
| .NET        | Microsoft Development Platform, Visual Studio        |
| Node.js     | Backend Development                                  |
| React.js    | Frontend Development                                 |
| Full Stack  | Node.js + React.js                                   |
| Git         | Version Control & Open Source Collaboration          |

---

# GitHub Repository Types

## Public Repository

```text
Developer
    ↓
GitHub Public Repository
    ↓
Anyone Can View
Anyone Can Clone
Anyone Can Fork
```

### Use Cases

* Open Source Projects
* Learning Projects
* Portfolio Projects
* Community Contributions

---

## Private Repository

```text
Developer
    ↓
Private Repository
    ↓
Only Authorized Users
```

### Use Cases

* Production Applications
* Company Projects
* Confidential Code
* Enterprise Applications

---

## Organization Repositories

```text
Organization
    │
    ├── Project-A
    ├── Project-B
    ├── Project-C
    └── Teams & Permissions
```

### Benefits

* Centralized Code Management
* Team Collaboration
* Role-Based Access Control
* Enterprise Governance

---

# Markdown Syntax

## Headings

```markdown
# Heading 1

## Heading 2

### Heading 3
```

Output:

# Heading 1

## Heading 2

### Heading 3

---

## Bullet Points

```markdown
- Item 1
- Item 2
- Item 3
```

---

## Code Blocks

````markdown
```python
print("Hello World")
```
````

Output:

```python
print("Hello World")
```

---

# Git Architecture

```text
Developer
    ↓
Working Directory
    ↓ git add
Staging Area
    ↓ git commit
Local Repository
    ↓ git push
Remote Repository (GitHub/Azure Repos)
```

---

# Basic Git Commands

## Pull Latest Code

```bash
git pull
```

Downloads and merges latest changes from remote repository.

---

## View Branches

```bash
git branch
```

Example Output:

```text
* main
  dev
```

---

## Create New Branch

```bash
git branch branch-name
```

Example:

```bash
git branch dev
```

---

## Switch Branch

```bash
git checkout branch-name
```

Example:

```bash
git checkout dev
```

---

## Stage Files

```bash
git add .
```

Stages all modified files.

---

## Commit Changes

```bash
git commit -m "commit message"
```

Example:

```bash
git commit -m "Added login page"
```

---

## Push Changes

```bash
git push origin dev
```

Pushes local branch changes to remote repository.

---

# GitHub Desktop

Download and Install:

```text
https://desktop.github.com/download/
```

### Benefits

* GUI Based Git Operations
* Easy Commit & Push
* Branch Management
* Merge & Pull Requests

---

# GitHub Practice Lab

## Clone Repository

```bash
git clone https://github.com/atulkamble/mynewproject.git
```

```bash
cd mynewproject
```

```bash
code .
```

---

## Configure Git

### Set Username

```bash
git config --global user.name "First Last"
```

### Set Email

```bash
git config --global user.email "email@example.com"
```

### Verify Configuration

```bash
git config --list
```

---

# Branching Practice

## Create Branch

```bash
git branch mayank
```

## Switch Branch

```bash
git checkout mayank
```

### Windows

```powershell
New-Item mayank.txt
```

### Linux/Mac

```bash
touch mayank.txt
```

---

## Add File

```bash
git add mayank.txt
```

---

## Edit File

### Windows

```powershell
notepad mayank.txt
```

### Linux/Mac

```bash
nano mayank.txt
```

---

## Commit Changes

```bash
git add mayank.txt

git commit -m "edited by mayank"
```

---

## Push Branch

```bash
git push origin mayank
```

---

# GitHub Personal Access Token (PAT)

## Create PAT

```text
GitHub
    ↓
Settings
    ↓
Developer Settings
    ↓
Personal Access Tokens
    ↓
Tokens (Classic)
    ↓
Generate New Token (Classic)
```

### Purpose

* Git Authentication
* CI/CD Integration
* API Access
* Secure Repository Access

---

# Azure DevOps Overview

Azure DevOps is Microsoft's DevOps platform providing:

| Service          | Purpose            |
| ---------------- | ------------------ |
| Azure Repos      | Git Repositories   |
| Azure Boards     | Agile Planning     |
| Azure Pipelines  | CI/CD              |
| Azure Test Plans | Testing            |
| Azure Artifacts  | Package Management |

---

# Azure DevOps Architecture

```text
Azure DevOps Organization
           │
           ▼
      Project
           │
 ┌─────────┼─────────┐
 ▼         ▼         ▼
Repos    Boards   Pipelines
```

Example URL:

```text
https://dev.azure.com/cloudnautic/project
```

---

# Azure DevOps Setup

## Step 1: Create Organization

```text
Azure DevOps
    ↓
Create Organization
```

Example:

```text
cloudnautic
```

---

## Step 2: Create Project

```text
Project Name:
project
```

---

## Step 3: Create Repository

```text
Azure Repos
    ↓
Initialize Repository
```

---

# Azure Repos Practice

## Clone Repository

```bash
git clone https://cloudnautic@dev.azure.com/cloudnautic/project/_git/project
```

```bash
cd project
```

---

## Create File

### Linux/Mac

```bash
touch b.txt
```

### Windows

```powershell
New-Item b.txt
```

---

## Commit Changes

```bash
git add b.txt

git commit -m "added b.txt"
```

---

## Push Code

```bash
git push origin main
```

---

# Azure DevOps Personal Access Token (PAT)

```text
Organization
      ↓
Organization Settings
      ↓
Personal Access Tokens
      ↓
New Token
```

### Uses

* Git Authentication
* Pipeline Authentication
* Automation Scripts
* Azure CLI Integration

---

# Git Branching Practice

## Verify Branch

```bash
git branch
```

---

## Push Main

```bash
git push origin main
```

---

## Edit File

```bash
nano b.txt
```

---

## Commit Updates

```bash
git add .

git commit -m "update"

git push origin main
```

---

## Pull Latest Changes

```bash
git pull
```

---

## Switch/Create Branch

```bash
git checkout -b new
```

---

## Verify Branch

```bash
git branch
```

---

## Verify Files

```bash
ls
```

---

## Modify File

```bash
nano a.txt
```

---

## Commit Branch Changes

```bash
git add .

git commit -m "added new branch"
```

---

## Push New Branch

```bash
git push origin new
```

---

# Complete Git Workflow

```text
Create Repository
        │
        ▼
git clone
        │
        ▼
Create Branch
        │
        ▼
Modify Code
        │
        ▼
git add
        │
        ▼
git commit
        │
        ▼
git push
        │
        ▼
Create Pull Request
        │
        ▼
Code Review
        │
        ▼
Merge to Main
```

---

# Important Commands Cheat Sheet

```bash
git clone <repo-url>
git status
git add .
git commit -m "message"
git push origin main
git pull
git branch
git checkout dev
git checkout -b feature
git merge feature
git log --oneline
git diff
git remote -v
git config --list
```

---

# Interview Questions

### What is Git?

A distributed version control system used to track source code changes.

### Difference Between Git and GitHub?

| Git                  | GitHub                 |
| -------------------- | ---------------------- |
| Version Control Tool | Cloud Hosting Platform |
| Installed Locally    | Hosted Online          |
| Tracks Changes       | Stores Repositories    |

### What is a Branch?

An independent line of development used to work on features without affecting main code.

### What is a Commit?

A snapshot of code changes saved in Git history.

### What is a Pull Request?

A request to merge changes from one branch into another.

### What is Azure Repos?

A Git-based source code management service provided by Azure DevOps.

---

# Points to Remember

✅ Always pull latest code before starting work

```bash
git pull
```

✅ Create feature branches instead of working directly on main

```bash
git checkout -b feature-login
```

✅ Commit frequently with meaningful messages

```bash
git commit -m "Added login functionality"
```

✅ Push code regularly

```bash
git push origin branch-name
```

✅ Never share PAT tokens publicly

✅ Use Pull Requests for code reviews

✅ Keep production repositories private

✅ Use public repositories for open-source projects

✅ Follow Git Flow or Branching Strategy in teams

---

# Real World Branching Strategy

```text
main
 │
 ├── dev
 │
 ├── feature-login
 │
 ├── feature-payment
 │
 └── bugfix-auth
```

**main** → Production Code
**dev** → Development Integration
**feature** → New Features
**bugfix** → Issue Resolution
**release** → Production Releases
