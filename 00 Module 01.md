# Module 01 – Introduction to AZ-400 (Microsoft Azure DevOps Engineer Expert)

---

# Learning Objectives

After completing this module, students should be able to:

✅ Understand DevOps Fundamentals

✅ Understand Azure DevOps Services

✅ Create Azure DevOps Organization

✅ Create Projects and Teams

✅ Manage Users and Permissions

✅ Configure Azure AD Integration

✅ Understand Access Levels

✅ Connect Azure Subscription with Azure DevOps

---

# 1. What is Azure DevOps?

Azure DevOps is Microsoft's cloud-based DevOps platform used for:

| Service          | Purpose                |
| ---------------- | ---------------------- |
| Azure Repos      | Source Code Management |
| Azure Pipelines  | CI/CD Automation       |
| Azure Boards     | Agile Planning         |
| Azure Test Plans | Testing                |
| Azure Artifacts  | Package Management     |

---

## Azure DevOps Architecture

```text
                    Developers
                         |
                         v
                  Azure Repos
                         |
                         v
                 Azure Pipelines
                         |
      ---------------------------------
      |               |               |
      v               v               v
   Dev Env        Test Env      Prod Env
                         |
                         v
                    Monitoring
```

---

# Azure DevOps Complete Architecture

```text
+---------------------------------------------------+
|                   Azure DevOps                    |
+---------------------------------------------------+
|                                                   |
|  Azure Boards     Azure Repos                     |
|       |               |                           |
|       |               v                           |
|       |       Source Code Repository              |
|       |               |                           |
|       v               v                           |
|         Azure Pipelines (CI/CD)                   |
|                   |                               |
|                   v                               |
|           Build & Release                         |
|                   |                               |
|      ------------------------------               |
|      |             |             |                |
|      v             v             v                |
|    Dev           Test         Production          |
|                                                   |
+---------------------------------------------------+
```

---

# 2. Why DevOps?

Traditional Development

```text
Developer
     |
     v
Code Ready
     |
     |
Operations Team
     |
Deployment
```

Problems:

❌ Slow Releases

❌ Manual Deployments

❌ Human Errors

❌ Communication Gaps

---

DevOps Approach

```text
Plan
  ↓
Code
  ↓
Build
  ↓
Test
  ↓
Release
  ↓
Deploy
  ↓
Monitor
```

Benefits:

✔ Faster Delivery

✔ Better Quality

✔ Automation

✔ Reduced Failures

✔ Continuous Feedback

---

# Benefits of Azure DevOps

| Benefit       | Description           |
| ------------- | --------------------- |
| Automation    | CI/CD Pipelines       |
| Collaboration | Dev + Ops Together    |
| Scalability   | Cloud Native          |
| Security      | Role-Based Access     |
| Integration   | GitHub, Azure, AWS    |
| Monitoring    | End-to-End Visibility |

---

# Azure DevOps Services Overview

## Azure Boards

Used for:

* User Stories
* Sprint Planning
* Backlogs
* Task Management

Example:

```text
Epic
 ├── Feature
      ├── User Story
            ├── Task
```

---

## Azure Repos

Git-based repository.

Commands:

```bash
git init

git clone https://dev.azure.com/org/project/_git/repo

git add .

git commit -m "Initial Commit"

git push origin main
```

---

## Azure Pipelines

CI/CD Automation

Pipeline Flow

```text
Developer Pushes Code
          |
          v
 Azure Pipeline Triggered
          |
          v
 Build
          |
          v
 Test
          |
          v
 Deploy
```

---

## Sample Azure Pipeline YAML

```yaml
trigger:
- main

pool:
  vmImage: ubuntu-latest

steps:

- task: UsePythonVersion@0
  inputs:
    versionSpec: '3.12'

- script: |
    pip install -r requirements.txt
    python app.py
  displayName: Run Application
```

---

## Azure Artifacts

Store:

* NuGet Packages
* Maven Packages
* npm Packages
* Python Packages

---

## Azure Test Plans

Supports:

* Manual Testing
* Automated Testing
* Regression Testing

---

# 3. Create Free Azure DevOps Account

## Prerequisites

### Microsoft Account

Examples:

```text
atul@hotmail.com
atul@gmail.com
```

---

## Demonstration Steps

### Step 1

Open:

```text
https://dev.azure.com
```

### Step 2

Sign in using Microsoft Account

### Step 3

Create Organization

Example:

```text
cloudnautic-org
```

### Step 4

Select Region

```text
Central India
```

### Step 5

Create First Project

```text
Cloudnautic-DevOps
```

---

# Azure DevOps Account Creation Flow

```text
Microsoft Account
        |
        v
Azure DevOps Sign In
        |
        v
Create Organization
        |
        v
Create Project
        |
        v
Invite Users
        |
        v
Start Development
```

---

# 4. Azure DevOps Organization

Organization is the top-level container.

Example:

```text
Organization
│
├── Project A
├── Project B
├── Project C
```

Example:

```text
Cloudnautic-Org
```

Contains:

* Users
* Projects
* Pipelines
* Repositories

---

# Create Organization

Portal:

```text
Azure DevOps
→ Organization Settings
→ New Organization
```

---

# 5. Azure DevOps Project

Project contains:

* Boards
* Repos
* Pipelines
* Artifacts
* Test Plans

Example:

```text
StudentManagement
```

---

## Create Project

```text
Organization
    |
    +-- New Project
```

Settings:

| Field             | Value             |
| ----------------- | ----------------- |
| Name              | StudentManagement |
| Visibility        | Private           |
| Version Control   | Git               |
| Work Item Process | Agile             |

---

# Project Structure

```text
Organization
     |
     +---- Project
               |
               +---- Boards
               +---- Repos
               +---- Pipelines
               +---- Artifacts
               +---- Test Plans
```

---

# 6. Teams & Permissions

Azure DevOps supports Role-Based Access Control (RBAC)

---

## Default Groups

| Group                  | Permission      |
| ---------------------- | --------------- |
| Project Administrators | Full Access     |
| Contributors           | Code Push       |
| Readers                | Read Only       |
| Build Administrators   | Pipeline Access |

---

## Add Team Member

```text
Project Settings
    |
Permissions
    |
Add User
```

Example:

```text
student1@gmail.com
```

---

# User Permission Architecture

```text
Organization
     |
     +---- Project
              |
              +---- Administrators
              +---- Contributors
              +---- Readers
```

---

# 7. Access Levels

Access level determines available features.

---

| Access Level       | Features              |
| ------------------ | --------------------- |
| Stakeholder        | Limited Access        |
| Basic              | Standard Access       |
| Basic + Test Plans | Full Testing Features |

---

## Check Access Level

```text
Organization Settings
      |
Users
      |
Access Level
```

---

# Access Level Comparison

| Feature    | Stakeholder | Basic | Basic+Test |
| ---------- | ----------- | ----- | ---------- |
| Boards     | Yes         | Yes   | Yes        |
| Repos      | No          | Yes   | Yes        |
| Pipelines  | No          | Yes   | Yes        |
| Test Plans | No          | No    | Yes        |

---

# 8. Azure Active Directory Integration

(New Name: Microsoft Entra ID)

---

## Why Integrate?

Benefits:

✔ Single Sign-On

✔ Centralized User Management

✔ Security

✔ MFA Support

✔ Group-Based Access

---

## Architecture

```text
Microsoft Entra ID
          |
          |
          v
Azure DevOps Organization
          |
          |
     Users & Groups
```

---

# Azure AD vs Azure DevOps

| Azure AD            | Azure DevOps    |
| ------------------- | --------------- |
| Identity Service    | DevOps Platform |
| User Authentication | CI/CD           |
| SSO                 | Source Control  |
| MFA                 | Pipelines       |
| User Management     | Deployment      |

---

# 9. Connect Azure DevOps with Azure AD

## Demonstration Steps

### Azure Portal

```text
portal.azure.com
```

### Navigate

```text
Microsoft Entra ID
    |
Manage
    |
Users
```

---

### Azure DevOps

```text
Organization Settings
      |
Microsoft Entra ID
      |
Connect Directory
```

---

### Select Tenant

Example:

```text
cloudnautic.onmicrosoft.com
```

---

### Verify

```text
Users
Groups
Access Levels
```

Will be synchronized.

---

# 10. Add Existing Azure DevOps Users into Azure AD

Scenario:

```text
Existing Azure DevOps User
          |
          |
Not Available in Azure AD
```

Solution:

```text
Create User in Azure AD
          |
Assign License
          |
Add to Azure DevOps
```

---

## Azure CLI Example

Create User

```bash
az login

az ad user create \
  --display-name "Student One" \
  --password "Password@123" \
  --user-principal-name student1@cloudnautic.onmicrosoft.com \
  --force-change-password-next-login true
```

---

## List Users

```bash
az ad user list --output table
```

---

## Show User

```bash
az ad user show \
--id student1@cloudnautic.onmicrosoft.com
```

---

# 11. If Azure Portal Account and Azure DevOps Account are Different

## Common Scenario

```text
Azure Subscription
      |
      +-- company@company.com

Azure DevOps
      |
      +-- devops@gmail.com
```

Works?

✅ Yes

But not recommended.

---

## Recommended

```text
Same Entra ID Tenant
        |
Azure Portal
        |
Azure DevOps
```

Benefits:

✔ SSO

✔ Easy User Management

✔ Better Security

✔ Simplified Access Control

---

# AZ-400 Interview Questions

### Q1. What is Azure DevOps?

A platform for CI/CD, Agile planning, source control, testing, and package management.

---

### Q2. What are Azure DevOps Services?

* Boards
* Repos
* Pipelines
* Artifacts
* Test Plans

---

### Q3. Difference between Organization and Project?

| Organization        | Project               |
| ------------------- | --------------------- |
| Top Level Container | Child Container       |
| Multiple Projects   | Single Application    |
| User Management     | Application Resources |

---

### Q4. What is Access Level?

Determines feature availability for users.

---

### Q5. What is Azure AD Integration?

Integration of Azure DevOps with Microsoft Entra ID for authentication and centralized identity management.

---

# Important Points to Remember

| Topic        | Remember                          |
| ------------ | --------------------------------- |
| Organization | Top-Level Container               |
| Project      | Contains Repos, Pipelines, Boards |
| Boards       | Agile Planning                    |
| Repos        | Git Repository                    |
| Pipelines    | CI/CD Automation                  |
| Artifacts    | Package Management                |
| Test Plans   | Testing                           |
| Stakeholder  | Free Limited Access               |
| Basic        | Developer Access                  |
| Entra ID     | Identity Management               |
| Azure DevOps | DevOps Platform                   |
| Azure Portal | Cloud Resource Management         |

---

# Hands-On Lab

### Lab 1

Create Azure DevOps Organization

### Lab 2

Create Project

### Lab 3

Create Team

### Lab 4

Add Users

### Lab 5

Assign Contributor Permission

### Lab 6

Connect Azure DevOps to Microsoft Entra ID

### Lab 7

Create Git Repository

```bash
git clone https://dev.azure.com/<org>/<project>/_git/<repo>
```

### Lab 8

Push Code

```bash
git add .
git commit -m "AZ400 Lab"
git push origin main
```

---

# Module 01 Summary

```text
Azure DevOps
│
├── Boards
├── Repos
├── Pipelines
├── Artifacts
├── Test Plans
│
├── Organization
│     └── Projects
│
├── Teams
├── Permissions
├── Access Levels
│
└── Microsoft Entra ID Integration
```

This module forms the foundation for all upcoming AZ-400 topics such as Git, Azure Repos, Pipelines, CI/CD, Infrastructure as Code, Containers, Kubernetes, Security, Monitoring, and Release Management.
