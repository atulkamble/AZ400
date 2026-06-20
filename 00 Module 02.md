# Module 02 – Azure Boards, Work Items, Sprints & Queries

## Azure DevOps Complete Hands-On Guide

---

# 1. Azure Boards Overview

Azure Boards is a work tracking service in Azure DevOps used for:

| Feature         | Purpose                         |
| --------------- | ------------------------------- |
| Work Items      | Track Tasks, Bugs, User Stories |
| Backlogs        | Manage Product Requirements     |
| Sprint Planning | Agile Project Management        |
| Kanban Boards   | Visual Work Tracking            |
| Queries         | Search & Filter Work Items      |
| Dashboards      | Project Reporting               |

---

# Azure Boards Architecture

```text
Azure DevOps Organization
            │
            ▼
      Azure Project
            │
            ▼
      Azure Boards
            │
 ┌──────────┼──────────┐
 ▼          ▼          ▼
Backlogs   Sprints   Queries
 │          │          │
 ▼          ▼          ▼
User Stories Tasks    Reports
Bugs       Features
```

---

# 2. Azure Work Item Types

A Work Item represents work to be completed.

## Common Work Items

| Work Item  | Description                |
| ---------- | -------------------------- |
| Epic       | Large business requirement |
| Feature    | Major functionality        |
| User Story | User Requirement           |
| Task       | Development Activity       |
| Bug        | Defect                     |
| Issue      | Problem Tracking           |

---

# Work Item Hierarchy

```text
Epic
 │
 ├── Feature
 │     │
 │     ├── User Story
 │     │       │
 │     │       ├── Task
 │     │       ├── Task
 │     │       └── Bug
```

Example:

```text
Epic:
Online Shopping Platform

Feature:
Shopping Cart

User Story:
Customer can add product to cart

Tasks:
Create UI
Create API
Create Database Table

Bug:
Cart Quantity Not Updating
```

---

# 3. Azure Boards Demo

## Create Azure DevOps Project

### Step 1

Login

```text
https://dev.azure.com
```

### Step 2

Create New Project

```text
Project Name:
Cloudnautic-DevOps
```

### Step 3

Select

```text
Visibility:
Private
```

---

# 4. Basic Work Item Process

Microsoft provides 3 Processes.

| Process | Suitable For          |
| ------- | --------------------- |
| Agile   | Most Organizations    |
| Scrum   | Scrum Teams           |
| CMMI    | Enterprise Governance |

---

# Agile Process Workflow

```text
New
 │
 ▼
Active
 │
 ▼
Resolved
 │
 ▼
Closed
```

---

# Scrum Process Workflow

```text
New
 │
 ▼
Approved
 │
 ▼
Committed
 │
 ▼
Done
```

---

# CMMI Workflow

```text
Proposed
 │
 ▼
Active
 │
 ▼
Resolved
 │
 ▼
Closed
```

---

# 5. Create Work Item

## Azure Portal Steps

### Boards

```text
Boards
  → Work Items
      → New Work Item
          → User Story
```

### Example

```text
Title:
Customer Login

Assigned To:
Developer1

State:
New

Area:
WebApp

Iteration:
Sprint 1
```

Save.

---

# 6. Work Item Settings

Navigate

```text
Project Settings
     ↓
Boards
     ↓
Team Configuration
```

Configure:

| Setting        | Purpose           |
| -------------- | ----------------- |
| Area Path      | Team Ownership    |
| Iteration Path | Sprint Assignment |
| Working Days   | Capacity Planning |
| Backlog Levels | Work Hierarchy    |

---

# 7. Sprint Overview

Sprint = Fixed Time Period

Usually:

```text
1 Week
2 Weeks
3 Weeks
```

Example:

```text
Sprint 1
01 Jul – 14 Jul

Sprint 2
15 Jul – 28 Jul
```

---

# Sprint Architecture

```text
Product Backlog
       │
       ▼
Sprint Planning
       │
       ▼
Sprint Backlog
       │
       ▼
Development
       │
       ▼
Testing
       │
       ▼
Done
```

---

# 8. Create Sprint

## Steps

```text
Project Settings
      ↓
Boards
      ↓
Project Configuration
      ↓
Iterations
      ↓
New Child
```

Example:

```text
Sprint 1
Sprint 2
Sprint 3
```

---

# Azure CLI (Team Iteration)

```bash
az extension add --name azure-devops
```

```bash
az devops configure \
--defaults organization=https://dev.azure.com/cloudnautic \
project=AzureBoardsDemo
```

List Team Iterations

```bash
az boards iteration team list
```

---

# 9. Add Work Item Into Sprint

## Steps

```text
Boards
   ↓
Backlogs
   ↓
Drag User Story
   ↓
Sprint 1
```

OR

Open Work Item

```text
Iteration Path
     ↓
Sprint 1
```

Save.

---

# 10. Agile Work Item Process

## Example Project

E-Commerce Website

### Epic

```text
Online Shopping
```

### Feature

```text
Product Catalog
```

### User Story

```text
As a customer
I want product search
So that I can find products quickly
```

### Tasks

```text
Create Search API

Create UI

Write Test Cases
```

---

# Agile Board

```text
New
 │
 ▼
Active
 │
 ▼
Resolved
 │
 ▼
Closed
```

---

# 11. Scrum Work Item Process

## Product Backlog Item (PBI)

Example:

```text
Create Customer Dashboard
```

Workflow:

```text
New
 │
 ▼
Approved
 │
 ▼
Committed
 │
 ▼
Done
```

---

# 12. CMMI Work Item Process

Used in:

```text
Government Projects
Banking Projects
Defense Projects
Healthcare Projects
```

Workflow:

```text
Proposed
 │
 ▼
Active
 │
 ▼
Resolved
 │
 ▼
Closed
```

---

# 13. Azure DevOps Queries

Queries help search work items.

Examples:

```text
Show Open Bugs

Show Tasks Assigned To Me

Show Sprint 1 Work Items

Show Closed Stories
```

---

# Query Architecture

```text
Work Items
     │
     ▼
Query Filters
     │
     ▼
Result Set
     │
     ▼
Charts
```

---

# 14. Create New Query

## Azure Portal

```text
Boards
    ↓
Queries
    ↓
New Query
```

Example

```text
Work Item Type = Bug

AND

State <> Closed
```

Run Query.

---

# Query Example

| Field          | Operator | Value  |
| -------------- | -------- | ------ |
| Work Item Type | =        | Bug    |
| State          | <>       | Closed |

---

# Query Result

```text
Bug 101
Bug 102
Bug 103
```

---

# Shared Query Example

```text
Open Bugs

Assigned Tasks

Sprint 1 Items

High Priority Bugs
```

---

# 15. Azure DevOps CLI Commands

## Install Extension

```bash
az extension add --name azure-devops
```

---

## Login

```bash
az login
```

---

## Configure

```bash
az devops configure \
--defaults organization=https://dev.azure.com/cloudnautic \
project=AzureBoardsDemo
```

---

## List Projects

```bash
az devops project list
```

---

## List Teams

```bash
az devops team list
```

---

## List Areas

```bash
az boards area project list
```

---

## List Iterations

```bash
az boards iteration project list
```

---

## Show Work Item

```bash
az boards work-item show \
--id 10
```

---

## Create Work Item

```bash
az boards work-item create \
--title "Create Login Page" \
--type "Task"
```

---

## Update Work Item

```bash
az boards work-item update \
--id 10 \
--state Active
```

---

## Create Bug

```bash
az boards work-item create \
--title "Login Error" \
--type "Bug"
```

---

# 16. Inherited Process

Inherited Process allows customization of Azure Boards.

Microsoft Recommended Method.

```text
Agile
  │
  ▼
Create Inherited Process
  │
  ▼
Customize Fields
Customize Workflow
Customize Work Items
```

---

# Create Inherited Process

## Steps

```text
Organization Settings
        ↓
Process
        ↓
Agile
        ↓
Create Inherited Process
```

Example

```text
Cloudnautic Agile
```

---

# 17. Create New Work Item in Inherited Process

## Steps

```text
Organization Settings
       ↓
Process
       ↓
Cloudnautic Agile
       ↓
New Work Item Type
```

Example

```text
Training Request
```

Fields:

```text
Trainer Name

Training Date

Technology

Duration
```

---

# Custom Work Item Example

| Field        | Type    |
| ------------ | ------- |
| Trainer Name | String  |
| Technology   | String  |
| Duration     | Integer |
| Batch Size   | Integer |

---

# Azure Boards Real Project

## Project

Online Food Ordering System

### Epic

```text
Food Ordering Platform
```

### Features

```text
Customer Registration

Restaurant Search

Payment Gateway
```

### User Stories

```text
Customer can register

Customer can search restaurants

Customer can pay online
```

### Tasks

```text
Frontend Development

Backend API

Database Creation

Testing
```

### Sprint Allocation

```text
Sprint 1
Registration

Sprint 2
Search

Sprint 3
Payment
```

---

# Interview Questions

### What is Azure Boards?

Work tracking and project management service in Azure DevOps.

---

### Difference Between Agile and Scrum?

| Agile              | Scrum        |
| ------------------ | ------------ |
| Methodology        | Framework    |
| Flexible           | Time-boxed   |
| Multiple Practices | Sprint-Based |

---

### What is a Sprint?

Short development cycle used to deliver incremental work.

---

### What is a Work Item?

Unit of work such as Task, Bug, User Story, Feature, Epic.

---

### What is an Iteration Path?

Used to assign work items to specific sprints.

---

### What is Area Path?

Used to categorize ownership/team.

---

### What is an Inherited Process?

Customized process created from Agile/Scrum/CMMI template.

---

# Points to Remember

| Topic             | Remember              |
| ----------------- | --------------------- |
| Epic              | Highest Level         |
| Feature           | Business Capability   |
| User Story        | Requirement           |
| Task              | Work Unit             |
| Bug               | Defect                |
| Sprint            | Time Box              |
| Iteration Path    | Sprint Assignment     |
| Area Path         | Team Ownership        |
| Query             | Search Work Items     |
| Agile             | Most Common           |
| Scrum             | Sprint Focused        |
| CMMI              | Enterprise Governance |
| Inherited Process | Customization Method  |
| Boards            | Visual Tracking       |
| Backlogs          | Requirement Storage   |

---

# Module 02 Learning Outcome

After completing this module you should be able to:

✅ Create Azure Boards Project
✅ Create Agile/Scrum/CMMI Work Items
✅ Configure Area Paths and Iteration Paths
✅ Create and Manage Sprints
✅ Move Work Items into Sprint Backlogs
✅ Build Queries and Reports
✅ Customize Inherited Processes
✅ Create Custom Work Item Types
✅ Track Project Progress Using Boards and Dashboards
✅ Manage Real Agile Projects using Azure DevOps Boards
