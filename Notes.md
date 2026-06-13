# AZ-400 Notes – Module 1: Cloud, Azure & DevOps Fundamentals

Based on the uploaded AZ-400 training plan. 

---

# 1. Cloud Fundamentals

## What is Cloud Computing?

Cloud Computing is the delivery of IT resources over the internet on a pay-as-you-go basis.

Instead of purchasing physical servers and infrastructure, organizations can rent resources from cloud providers such as:

* Microsoft Azure
* Amazon Web Services AWS
* Google Cloud GCP

### Traditional Infrastructure

* Purchase Servers
* Purchase Storage
* Setup Networking
* Manage Data Center
* High Capital Expenditure (CAPEX)

### Cloud Infrastructure

* No hardware purchase
* On-demand provisioning
* Pay only for usage
* Global availability
* Operational Expenditure (OPEX)

---

## Benefits of Cloud Computing

### 1. Cost Savings

Traditional:

* Buy server for 5 years

Cloud:

* Pay per hour/per second

### 2. Scalability

Scale Up

* Increase CPU
* Increase Memory

Scale Out

* Add More Servers

### 3. High Availability

Applications remain available even if a server fails.

Example:

* Multiple VMs
* Load Balancer
* Availability Zones

### 4. Global Reach

Deploy applications worldwide within minutes.

Examples:

* India
* USA
* Europe
* Australia

### 5. Security

Cloud providers offer:

* Identity Management
* Encryption
* Network Security
* Compliance

---

# Cloud Service Models

## Infrastructure as a Service (IaaS)

Provider manages:

* Datacenter
* Network
* Hardware

Customer manages:

* Operating System
* Applications
* Data

Examples:

* Azure Virtual Machines
* AWS EC2

Use Cases:

* Lift and Shift Migration
* Custom Applications

---

## Platform as a Service (PaaS)

Provider manages:

* Infrastructure
* Operating System
* Runtime

Customer manages:

* Application
* Data

Examples:

* Azure App Service
* Azure SQL Database

Benefits:

* Faster deployment
* Less maintenance

---

## Software as a Service (SaaS)

Provider manages everything.

Examples:

* Microsoft 365
* Gmail
* Salesforce

Benefits:

* No infrastructure management
* Accessible from anywhere

---

# Cloud Deployment Models

## Public Cloud

Infrastructure owned by cloud provider.

Examples:

* Azure
* AWS
* GCP

Advantages:

* Low Cost
* Highly Scalable

---

## Private Cloud

Dedicated cloud environment.

Examples:

* VMware Datacenter
* OpenStack

Advantages:

* Greater Control
* Enhanced Security

---

## Hybrid Cloud

Combination of:

* Public Cloud
* Private Cloud

Examples:

* On-Premise + Azure

Benefits:

* Flexibility
* Gradual Migration

---

# 2. Azure Fundamentals

## What is Microsoft Azure?

Azure is Microsoft's cloud computing platform that provides:

* Compute
* Storage
* Networking
* Security
* AI Services
* Analytics

More than 200+ cloud services are available.

---

## Azure Portal

Azure Portal is a web-based management interface.

Functions:

* Create Resources
* Monitor Resources
* Configure Security
* Manage Billing

Portal URL:

* [https://portal.azure.com](https://portal.azure.com)

---

## Azure Subscription

A subscription is a billing and management boundary.

### Purpose

* Resource Tracking
* Cost Management
* Access Control

Examples:

* Free Trial Subscription
* Pay-As-You-Go
* Enterprise Agreement

---

## Resource Groups

A Resource Group is a logical container for Azure resources.

Example:

```
RG-PROD
├── VM01
├── Storage Account
├── Key Vault
└── Virtual Network
```

Benefits:

* Easy Management
* Cost Tracking
* Resource Organization

---

## Azure Virtual Machines

Virtual Machines provide Infrastructure as a Service.

Supported Operating Systems:

### Linux

* Ubuntu
* RHEL
* CentOS
* Debian

### Windows

* Windows Server 2025
* Windows Server 2022

Common Uses:

* Web Servers
* Application Servers
* Database Servers

---

## Azure Storage Accounts

Storage Account is used to store data.

Storage Types:

### Blob Storage

Stores:

* Images
* Videos
* Documents
* Backups

### File Storage

Provides SMB/NFS Shares.

### Queue Storage

Message Queues for Applications.

### Table Storage

NoSQL Storage.

---

## Azure Networking Basics

### Virtual Network (VNet)

Private network inside Azure.

Example:

```
VNet
├── Web Subnet
├── App Subnet
└── DB Subnet
```

---

### Subnet

Logical division of VNet.

Example:

```
10.0.0.0/16

Web : 10.0.1.0/24
App : 10.0.2.0/24
DB  : 10.0.3.0/24
```

---

### Network Security Group (NSG)

Controls inbound and outbound traffic.

Common Ports:

| Service | Port |
| ------- | ---- |
| SSH     | 22   |
| HTTP    | 80   |
| HTTPS   | 443  |
| RDP     | 3389 |

---

# 3. DevOps Fundamentals

## What is DevOps?

DevOps is a culture, practice, and set of tools that combines:

* Development (Dev)
* Operations (Ops)

Goal:

* Faster Delivery
* Better Quality
* Automation
* Collaboration

---

## Problems Before DevOps

### Development Team

* Builds application

### Operations Team

* Deploys application

Common Issues:

* Communication Gap
* Slow Releases
* Manual Deployments
* Frequent Failures

---

## DevOps Lifecycle

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
Operate
 ↓
Monitor
 ↓
Feedback
```

---

## SDLC (Software Development Life Cycle)

### 1. Requirement Gathering

Understand customer requirements.

### 2. Design

Application architecture.

### 3. Development

Coding phase.

### 4. Testing

Quality validation.

### 5. Deployment

Release to Production.

### 6. Maintenance

Bug fixes and enhancements.

---

## Agile Methodology

Agile is an iterative software development approach.

Benefits:

* Faster Delivery
* Continuous Feedback
* Better Collaboration

---

## Scrum Framework

Scrum Roles:

### Product Owner

Defines requirements.

### Scrum Master

Removes blockers.

### Development Team

Builds the application.

---

### Scrum Artifacts

* Product Backlog
* Sprint Backlog
* Increment

---

### Scrum Events

* Sprint Planning
* Daily Standup
* Sprint Review
* Sprint Retrospective

---

## Continuous Integration (CI)

Developers frequently merge code into a central repository.

Process:

```text
Code
 ↓
Build
 ↓
Test
 ↓
Artifact
```

Benefits:

* Early Bug Detection
* Automated Testing
* Faster Delivery

---

## Continuous Delivery (CD)

Automates release process.

```text
Build
 ↓
Test
 ↓
Approval
 ↓
Deploy
```

Benefits:

* Reliable Releases
* Reduced Risk

# Scrum vs Agile vs Waterfall – Points to Remember

## Quick Interview Answer

| Agile                     | Scrum                     | Waterfall                 |
| ------------------------- | ------------------------- | ------------------------- |
| Methodology/Mindset       | Framework under Agile     | Traditional Project Model |
| Flexible                  | Iterative & Incremental   | Sequential                |
| Continuous Feedback       | Sprint-based Feedback     | Feedback at End           |
| Adapts to Change          | Embraces Change           | Change is Costly          |
| Customer Involvement High | Customer Involvement High | Customer Involvement Low  |
| Multiple Agile Frameworks | One Agile Framework       | Single Linear Approach    |

---

## Relationship

```text
Project Management Approaches
│
├── Waterfall
│
└── Agile
      │
      ├── Scrum
      ├── Kanban
      ├── XP
      └── SAFe
```

**Remember:**

* Agile = Philosophy/Mindset
* Scrum = Agile Framework
* Waterfall = Traditional Model

---

# 1. Agile

### Definition

Agile is a project management and software development approach focused on:

* Continuous delivery
* Customer collaboration
* Frequent feedback
* Adaptability

### Example

Building an E-commerce Website

Instead of delivering after 6 months:

Month 1:

* Login Module

Month 2:

* Product Catalog

Month 3:

* Cart

Month 4:

* Payment Gateway

Customer can review after every iteration.

### Agile Principles

* Working software over documentation
* Customer collaboration over contracts
* Responding to change over following a plan
* Individuals and interactions over processes

### Points to Remember

✅ Flexible

✅ Fast feedback

✅ Customer involved

✅ Frequent releases

✅ Suitable for dynamic projects

---

# 2. Scrum

### Definition

Scrum is the most popular Agile framework.

It divides work into short cycles called **Sprints**.

Sprint Duration:

```text
1-4 Weeks
```

Most common:

```text
2 Weeks
```

---

## Scrum Roles

### Product Owner

Responsible for:

* Product Vision
* Product Backlog
* Prioritization

### Scrum Master

Responsible for:

* Removing blockers
* Facilitating meetings
* Following Scrum practices

### Development Team

Responsible for:

* Designing
* Coding
* Testing
* Delivering

---

## Scrum Events

### Sprint Planning

What to build?

### Daily Standup

15-minute meeting

Questions:

```text
What did I do yesterday?
What will I do today?
Any blockers?
```

### Sprint Review

Demo to stakeholders.

### Sprint Retrospective

What went well?
What can improve?

---

## Scrum Artifacts

### Product Backlog

Complete requirement list.

### Sprint Backlog

Current sprint tasks.

### Increment

Working product after sprint.

---

### Example

Mobile Banking App

Sprint 1:

* Login

Sprint 2:

* Account Summary

Sprint 3:

* Fund Transfer

Sprint 4:

* Bill Payment

Each sprint delivers usable functionality.

---

### Points to Remember

✅ Sprint Based

✅ Time Boxed

✅ Daily Standups

✅ Product Owner

✅ Scrum Master

✅ Product Backlog

✅ Sprint Backlog

---

# 3. Waterfall

### Definition

Traditional project management model.

Work flows in a sequence.

```text
Requirement
    ↓
Design
    ↓
Development
    ↓
Testing
    ↓
Deployment
    ↓
Maintenance
```

Next phase starts only after previous phase completes.

---

### Example

Building a Bridge

Requirements are fixed.

```text
Design Complete
↓
Construction
↓
Testing
↓
Opening
```

Changes during construction are expensive.

---

### Points to Remember

✅ Sequential

✅ Heavy Documentation

✅ Fixed Requirements

✅ Less Customer Interaction

✅ Changes are Difficult

✅ Suitable for Predictable Projects

---

# Real-Life Example

## Waterfall

Building a House

```text
Plan
↓
Design
↓
Construction
↓
Inspection
↓
Handover
```

Cannot easily change room locations midway.

---

## Agile

Building a Mobile App

```text
Version 1 → Login
Version 2 → Payments
Version 3 → Notifications
Version 4 → Reports
```

Users provide feedback after every release.

---

## Scrum

Developing a Food Delivery App

Sprint 1:

* Login

Sprint 2:

* Restaurant Listing

Sprint 3:

* Order Placement

Sprint 4:

* Payment

Sprint 5:

* Tracking

Delivered every 2 weeks.

---

# Interview One-Liner

### Agile

> Agile is a mindset that focuses on iterative development, collaboration, and responding to change.

### Scrum

> Scrum is an Agile framework that delivers work in short, time-boxed sprints using roles like Product Owner, Scrum Master, and Development Team.

### Waterfall

> Waterfall is a linear project management approach where each phase is completed before the next phase begins.

---

# Easy Memory Trick

```text
Agile    = Philosophy
Scrum    = Framework inside Agile
Waterfall = Traditional Sequential Model
```

**Formula for exams/interviews:**

```text
Agile > Scrum
Waterfall ≠ Agile

Agile = Flexible
Scrum = Agile + Sprints
Waterfall = Fixed Plan
```

---

## DevOps Toolchain

| Phase          | Tools                               |
| -------------- | ----------------------------------- |
| Planning       | Azure Boards, Jira                  |
| Source Control | Git, GitHub, Azure Repos            |
| Build          | Azure Pipelines, GitHub Actions     |
| Testing        | Selenium, JUnit                     |
| IaC            | Terraform, Bicep                    |
| Containers     | Docker                              |
| Orchestration  | Kubernetes, AKS                     |
| Monitoring     | Azure Monitor, Application Insights |

---

# Points to Remember (Interview Questions)

### Q1. What is Cloud Computing?

Delivery of computing resources over the internet on a pay-as-you-go model.

### Q2. Difference between IaaS, PaaS, and SaaS?

* IaaS → Infrastructure
* PaaS → Platform
* SaaS → Complete Software

### Q3. What is Azure Resource Group?

Logical container that holds Azure resources.

### Q4. What is DevOps?

Culture that combines development and operations using automation and collaboration.

### Q5. Difference between CI and CD?

* CI = Build and Test Automation
* CD = Deployment Automation

### Q6. What are the phases of DevOps?

Plan → Code → Build → Test → Release → Deploy → Operate → Monitor.

This completes **Module 1: Cloud, Azure & DevOps Fundamentals** from the AZ-400 course plan. 


# Module 2: Linux & Git Fundamentals

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module provides the Linux and Git foundation required for Azure DevOps, GitHub, CI/CD pipelines, Docker, Kubernetes, and Infrastructure as Code. 

---

# Linux Fundamentals

## What is Linux?

Linux is an open-source operating system widely used in:

* Cloud Computing
* DevOps
* Containers
* Kubernetes
* Web Hosting
* Enterprise Applications

Major cloud providers use Linux extensively:

* Azure Virtual Machines
* AWS EC2
* Google Compute Engine

---

# Linux Architecture

```text
+---------------------+
|     Applications    |
+---------------------+
|        Shell        |
+---------------------+
|       Kernel        |
+---------------------+
|      Hardware       |
+---------------------+
```

### Hardware

Physical resources:

* CPU
* Memory
* Disk
* Network

### Kernel

Core component of Linux.

Responsibilities:

* Process Management
* Memory Management
* Device Management
* Security
* Networking

### Shell

Interface between user and operating system.

Examples:

* Bash
* Zsh
* Ksh

### Applications

Examples:

* Docker
* Jenkins
* Nginx
* MySQL

---

# Linux Distributions

Popular Linux distributions:

| Distribution | Usage               |
| ------------ | ------------------- |
| Ubuntu       | Cloud & Development |
| RHEL         | Enterprise          |
| Rocky Linux  | Enterprise          |
| AlmaLinux    | Enterprise          |
| Debian       | Servers             |
| Amazon Linux | AWS                 |

---

# Linux File System

Linux follows a hierarchical structure.

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── opt
├── root
├── tmp
├── usr
└── var
```

---

## Important Directories

### /

Root directory.

Top level of filesystem.

---

### /home

Stores user data.

Example:

```bash
/home/atul
/home/student1
```

---

### /root

Home directory of root user.

```bash
/root
```

---

### /etc

Stores configuration files.

Examples:

```bash
/etc/passwd
/etc/ssh/sshd_config
```

---

### /var

Stores logs and variable data.

Examples:

```bash
/var/log/messages
/var/log/syslog
```

---

### /tmp

Temporary files.

---

### /opt

Third-party software installations.

---

# Essential Linux Commands

## Navigation Commands

### pwd

Print current directory.

```bash
pwd
```

Output:

```bash
/home/azureuser
```

---

### ls

List files.

```bash
ls
ls -l
ls -la
```

---

### cd

Change directory.

```bash
cd /etc
cd ~
cd ..
```

---

# File Management Commands

## Create Files

```bash
touch file1.txt
touch file2.txt
```

---

## Create Directory

```bash
mkdir devops
mkdir -p projects/app
```

---

## Copy Files

```bash
cp file1.txt backup.txt

cp -r source destination
```

---

## Move Files

```bash
mv file1.txt newfile.txt

mv file1.txt /tmp
```

---

## Delete Files

```bash
rm file1.txt

rm -rf folder
```

⚠️ Use rm -rf carefully.

---

# Viewing Files

## cat

```bash
cat file.txt
```

---

## less

```bash
less file.txt
```

---

## head

```bash
head file.txt
```

---

## tail

```bash
tail file.txt

tail -f /var/log/messages
```

Used for log monitoring.

---

# Searching Files

## find

```bash
find / -name "*.log"
```

---

## locate

```bash
locate nginx.conf
```

---

## grep

Search text.

```bash
grep "error" logfile.log
```

Case insensitive:

```bash
grep -i error logfile.log
```

---

# User Management

## Check Current User

```bash
whoami
```

---

## Create User

```bash
sudo useradd devops
```

---

## Set Password

```bash
sudo passwd devops
```

---

## Delete User

```bash
sudo userdel devops
```

---

# Groups

## Create Group

```bash
sudo groupadd developers
```

---

## Add User to Group

```bash
sudo usermod -aG developers devops
```

---

# Linux Permissions

Each file has:

* Owner
* Group
* Others

Example:

```bash
-rwxr-xr--
```

---

## Permission Values

| Permission | Value |
| ---------- | ----- |
| Read       | 4     |
| Write      | 2     |
| Execute    | 1     |

---

### Common Examples

| Value | Meaning         |
| ----- | --------------- |
| 777   | Full Access     |
| 755   | Standard Script |
| 644   | Normal File     |
| 600   | Private File    |

---

## chmod

Change permissions.

```bash
chmod 755 script.sh

chmod 644 file.txt
```

---

## chown

Change ownership.

```bash
sudo chown user:user file.txt
```

---

# Package Management

## Ubuntu

Update repository:

```bash
sudo apt update
```

Install package:

```bash
sudo apt install nginx -y
```

---

## RHEL/CentOS/Amazon Linux

```bash
sudo yum update -y

sudo yum install nginx -y
```

Modern systems:

```bash
sudo dnf install nginx -y
```

---

# Service Management

Linux uses systemd.

---

## Start Service

```bash
sudo systemctl start nginx
```

---

## Stop Service

```bash
sudo systemctl stop nginx
```

---

## Restart Service

```bash
sudo systemctl restart nginx
```

---

## Check Status

```bash
sudo systemctl status nginx
```

---

## Enable Service

```bash
sudo systemctl enable nginx
```

---

# Process Management

## View Processes

```bash
ps -ef
```

---

## Interactive View

```bash
top
```

or

```bash
htop
```

---

## Kill Process

```bash
kill PID

kill -9 PID
```

---

# Networking Commands

## Check IP

```bash
ip addr
```

---

## Check Connectivity

```bash
ping google.com
```

---

## Check Ports

```bash
ss -tulpn
```

or

```bash
netstat -tulpn
```

---

# Git Fundamentals

## What is Version Control?

Version Control System (VCS) tracks code changes over time.

Benefits:

* History Tracking
* Collaboration
* Rollback
* Branching

---

# Types of Version Control

## Centralized VCS

Examples:

* SVN
* TFS

Single central repository.

---

## Distributed VCS

Examples:

* Git
* Mercurial

Each developer has a complete copy.

Git uses Distributed Version Control.

---

# What is Git?

Git is an open-source distributed version control system created by Linus Torvalds.

Features:

* Fast
* Lightweight
* Distributed
* Reliable

---

# Git Installation

## Ubuntu

```bash
sudo apt update

sudo apt install git -y
```

---

## Amazon Linux

```bash
sudo yum install git -y
```

---

## Verify Installation

```bash
git --version
```

---

# GitHub Account Setup

GitHub is a cloud-hosted Git platform.

Common Uses:

* Source Code Hosting
* Collaboration
* Pull Requests
* CI/CD

GitHub URL:

```text
https://github.com
```

---

# Configure Git

Set username:

```bash
git config --global user.name "Atul Kamble"
```

Set email:

```bash
git config --global user.email "atul@example.com"
```

Verify:

```bash
git config --list
```

---

# Create Repository

```bash
mkdir demo

cd demo

git init
```

---

# Git Workflow

```text
Working Directory
       ↓
Staging Area
       ↓
Local Repository
       ↓
Remote Repository
```

---

# Git Commands

## Check Status

```bash
git status
```

---

## Add Files

Single file:

```bash
git add file.txt
```

All files:

```bash
git add .
```

---

## Commit Changes

```bash
git commit -m "Initial Commit"
```

---

## View Commit History

```bash
git log

git log --oneline
```

---

## Clone Repository

```bash
git clone https://github.com/user/project.git
```

---

## Connect Remote Repository

```bash
git remote add origin https://github.com/user/project.git
```

---

## Push Changes

```bash
git push origin main
```

---

## Pull Changes

```bash
git pull origin main
```

---

## Fetch Changes

```bash
git fetch
```

Difference:

* fetch = download only
* pull = download + merge

---

# SSH Authentication with GitHub

Generate SSH Key:

```bash
ssh-keygen -t rsa -b 4096
```

View Public Key:

```bash
cat ~/.ssh/id_rsa.pub
```

Add key to GitHub.

Test:

```bash
ssh -T git@github.com
```

---

# Git Best Practices

* Commit Frequently
* Use Meaningful Commit Messages
* Pull Before Push
* Protect Main Branch
* Use Pull Requests
* Never Commit Secrets
* Use .gitignore

Example:

```text
.env
*.log
node_modules/
terraform.tfstate
```

---

# Hands-On Lab

### Lab 1: Linux Basics

1. Create EC2/Azure Linux VM
2. Connect using SSH
3. Create users
4. Configure permissions
5. Install Nginx
6. Verify website

---

### Lab 2: Git Basics

1. Install Git
2. Create GitHub Repository
3. Clone Repository
4. Create Files
5. Commit Changes
6. Push to GitHub
7. Verify Repository

---

# Interview Questions

### Q1. Difference between Linux and Unix?

Linux is open-source, Unix is mostly proprietary.

---

### Q2. What is chmod 755?

Owner: Read, Write, Execute

Group: Read, Execute

Others: Read, Execute

---

### Q3. Difference between git fetch and git pull?

* fetch = downloads changes
* pull = downloads and merges changes

---

### Q4. What is Git?

Distributed version control system used to track source code changes.

---

### Q5. What is the difference between git clone and git init?

* clone = copies existing repository
* init = creates new repository

---

### Q6. What are the three stages in Git?

* Working Directory
* Staging Area
* Repository

---

### Q7. How do you view logs in Linux?

```bash
tail -f /var/log/messages
```

or

```bash
journalctl -xe
```

---

### Points to Remember

* Linux powers most cloud workloads.
* SSH uses port 22.
* Permissions = Read(4) + Write(2) + Execute(1).
* Git is a distributed VCS.
* Commit locally before pushing remotely.
* Pull before push to avoid conflicts.
* Git and Linux are foundational skills for Azure DevOps, Docker, Kubernetes, Terraform, and AZ-400 certification. 

# Module 3: Azure DevOps Fundamentals

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module introduces Azure DevOps services, organizations, projects, permissions, Microsoft Entra ID integration, and service connections. It forms the foundation for CI/CD, Git repositories, Boards, Pipelines, and DevSecOps implementation. 

---

# What is Azure DevOps?

Azure DevOps is a suite of development tools provided by [Microsoft Azure DevOps](https://azure.microsoft.com/en-us/products/devops?utm_source=chatgpt.com) that enables teams to:

* Plan Work
* Manage Source Code
* Build Applications
* Test Applications
* Deploy Applications
* Monitor Applications

It supports:

* Agile Development
* CI/CD
* DevSecOps
* Infrastructure as Code
* Multi-Cloud Deployments

---

# Why Azure DevOps?

## Business Benefits

### Faster Delivery

Automated pipelines reduce deployment time.

### Improved Quality

Automated testing catches issues early.

### Better Collaboration

Developers, QA, Security, and Operations work together.

### Traceability

Track every requirement, code change, build, and deployment.

### Automation

Reduces manual effort and human errors.

---

# Azure DevOps Architecture

```text
Organization
    │
    ├── Project A
    │      ├── Boards
    │      ├── Repos
    │      ├── Pipelines
    │      ├── Artifacts
    │      └── Test Plans
    │
    └── Project B
```

---

# Azure DevOps Services

Azure DevOps consists of five major services.

## 1. Azure Boards

Work Management System.

Features:

* Epics
* Features
* User Stories
* Tasks
* Sprint Planning
* Backlogs
* Dashboards

Purpose:

Manage project planning and tracking.

---

## 2. Azure Repos

Git-based source control repository.

Features:

* Git Repositories
* Branching
* Pull Requests
* Code Reviews
* Branch Policies

Purpose:

Store and manage source code.

---

## 3. Azure Pipelines

CI/CD platform.

Features:

* Continuous Integration
* Continuous Delivery
* YAML Pipelines
* Multi-stage Deployments
* Automated Testing

Purpose:

Automate software delivery.

---

## 4. Azure Artifacts

Package Management Service.

Supports:

* NuGet
* npm
* Maven
* Python Packages

Purpose:

Store and manage application packages.

---

## 5. Azure Test Plans

Testing Management Platform.

Features:

* Manual Testing
* Exploratory Testing
* Test Cases
* Test Suites

Purpose:

Quality Assurance and Validation.

---

# Azure DevOps Organization

## What is an Organization?

An Organization is the top-level container in Azure DevOps.

Example:

```text
Organization
├── Development Project
├── Production Project
├── QA Project
└── Shared Services Project
```

Organization manages:

* Users
* Billing
* Security
* Projects

---

## Create Azure DevOps Organization

Steps:

1. Login to Azure DevOps
2. Click New Organization
3. Select Region
4. Enter Organization Name
5. Create Organization

Example:

```text
cloudnautic-devops
```

Best Practice:

Create separate organizations for:

* Enterprise
* Training
* Testing

---

# Azure DevOps Projects

## What is a Project?

A Project is a logical container for:

* Repositories
* Boards
* Pipelines
* Artifacts
* Test Plans

Example:

```text
Azure-DevOps-Training
```

Contains:

```text
Azure-DevOps-Training
├── Boards
├── Repos
├── Pipelines
├── Artifacts
└── Test Plans
```

---

## Create a Project

Steps:

1. New Project
2. Enter Project Name
3. Visibility

Options:

* Private
* Public

4. Version Control

Options:

* Git
* TFVC

Recommended:

```text
Git
```

5. Work Item Process

Options:

* Agile
* Scrum
* CMMI
* Basic

Recommended:

```text
Agile
```

---

# Azure DevOps Teams

## What is a Team?

A Team is a group of users working together within a project.

Example:

```text
Project
│
├── Development Team
├── QA Team
├── DevOps Team
└── Security Team
```

Benefits:

* Sprint Management
* Capacity Planning
* Work Assignment

---

# Access Levels

Access Level determines what a user can do.

## Stakeholder

Free access.

Can:

* View Boards
* Create Work Items

Cannot:

* Access Repos
* Create Pipelines

---

## Basic

Most common license.

Can:

* Use Boards
* Use Repos
* Use Pipelines

---

## Basic + Test Plans

Includes:

* Full Testing Features

Used by QA teams.

---

# Azure DevOps Security Model

Security is controlled using:

* Users
* Groups
* Permissions
* Access Levels

Common Groups:

| Group                  | Purpose             |
| ---------------------- | ------------------- |
| Project Administrators | Full Control        |
| Contributors           | Development Work    |
| Readers                | Read Only           |
| Build Administrators   | Pipeline Management |

---

# Microsoft Entra ID Integration

Microsoft renamed Azure Active Directory to:

### Microsoft Entra ID

Used for:

* Authentication
* Authorization
* Identity Management

---

# Benefits of Entra Integration

### Single Sign-On (SSO)

One login for:

* Azure Portal
* Azure DevOps
* Microsoft 365

---

### Centralized User Management

Manage all users from Entra ID.

---

### Multi-Factor Authentication

Enhanced security.

Examples:

* Microsoft Authenticator
* SMS
* FIDO2 Keys

---

### Conditional Access

Restrict access based on:

* Device
* Location
* Risk

---

# Add Existing Entra Users

Steps:

1. Organization Settings
2. Users
3. Add Users
4. Enter Email Address
5. Assign Access Level
6. Assign Project

Example:

```text
atul@company.com
```

---

# Azure Subscription vs Azure DevOps Organization

Many beginners confuse these.

| Azure Subscription      | Azure DevOps Organization |
| ----------------------- | ------------------------- |
| Billing Boundary        | Development Platform      |
| Contains Resources      | Contains Projects         |
| Managed in Azure Portal | Managed in Azure DevOps   |
| VMs, Storage, Networks  | Boards, Repos, Pipelines  |

---

# Service Connections

## What is a Service Connection?

A Service Connection allows Azure DevOps to securely connect with external systems.

Examples:

* Azure Subscription
* GitHub
* Docker Hub
* Kubernetes
* AWS

---

# Why Service Connections?

Without Service Connection:

```text
Pipeline
   ↓
Cannot Access Azure Resources
```

With Service Connection:

```text
Pipeline
   ↓
Service Connection
   ↓
Azure Resources
```

---

# Types of Service Connections

## Azure Resource Manager (ARM)

Most commonly used.

Purpose:

Deploy Azure resources.

Examples:

* App Services
* AKS
* Virtual Machines
* Storage Accounts

---

## GitHub Service Connection

Used for:

* Source Code Integration
* GitHub Actions Integration

---

## Docker Registry

Used for:

* Docker Hub
* Azure Container Registry (ACR)

---

## Kubernetes Connection

Used for:

* AKS
* EKS
* Kubernetes Clusters

---

# Service Principal

Azure DevOps typically authenticates to Azure using a Service Principal.

Components:

* Client ID
* Tenant ID
* Secret

Used for:

* Secure Automation
* CI/CD Pipelines

---

# Managed Identity vs Service Principal

| Feature             | Managed Identity | Service Principal |
| ------------------- | ---------------- | ----------------- |
| Password Management | Automatic        | Manual            |
| Azure Native        | Yes              | Yes               |
| Pipeline Support    | Limited          | Common            |
| Security            | Higher           | Good              |

---

# Azure DevOps Agent

An Agent executes pipeline tasks.

---

## Microsoft Hosted Agent

Managed by Microsoft.

Advantages:

* No Maintenance
* Auto Updated

Examples:

```yaml
pool:
  vmImage: ubuntu-latest
```

---

## Self Hosted Agent

Installed on:

* Linux VM
* Windows VM
* On-Prem Server

Advantages:

* Full Control
* Custom Software
* Private Network Access

---

# Azure DevOps Workflow

```text
Developer
    │
    ▼
Azure Repos
    │
    ▼
Azure Pipelines
    │
    ▼
Build
    │
    ▼
Test
    │
    ▼
Deploy
    │
    ▼
Azure Resources
```

---

# Hands-On Lab 1

### Create Azure DevOps Organization

Tasks:

1. Create Organization
2. Create Project
3. Add Team Members
4. Configure Access Levels
5. Create Teams

---

# Hands-On Lab 2

### Create Service Connection

Tasks:

1. Create Azure Subscription
2. Create Resource Group
3. Create Service Connection
4. Validate Connection
5. Test Pipeline Access

---

# Hands-On Lab 3

### Explore Azure DevOps Services

Tasks:

1. Create Work Item
2. Create Git Repository
3. Create Pipeline
4. Publish Artifact
5. Create Test Plan

---

# Real-World Scenario

A company wants:

* Developers push code to Git
* Pipeline builds application
* Deploy to Azure App Service
* Monitor deployments

Azure DevOps Components Used:

| Requirement     | Azure DevOps Service |
| --------------- | -------------------- |
| Planning        | Azure Boards         |
| Source Control  | Azure Repos          |
| Build & Deploy  | Azure Pipelines      |
| Package Storage | Azure Artifacts      |
| Testing         | Azure Test Plans     |

---

# Interview Questions

### Q1. What are the five Azure DevOps services?

* Azure Boards
* Azure Repos
* Azure Pipelines
* Azure Artifacts
* Azure Test Plans

---

### Q2. What is an Azure DevOps Organization?

Top-level container that manages projects, users, permissions, and billing.

---

### Q3. What is a Service Connection?

Secure authentication mechanism used by Azure DevOps to access Azure or external systems.

---

### Q4. Difference between Azure Subscription and Azure DevOps Organization?

Subscription manages cloud resources; Organization manages DevOps projects and teams.

---

### Q5. What is Microsoft Entra ID?

Identity and access management service formerly known as Azure Active Directory.

---

### Q6. What is the difference between Microsoft Hosted Agent and Self Hosted Agent?

* Microsoft Hosted Agent → Managed by Microsoft.
* Self Hosted Agent → Managed by customer.

---

### Q7. What is a Service Principal?

A non-human identity used for automation and Azure resource access.

---

# Points to Remember

* Azure DevOps = Planning + Source Control + CI/CD + Testing + Package Management.
* Organization is the top-level container.
* Projects contain Boards, Repos, Pipelines, Artifacts, and Test Plans.
* Microsoft Entra ID provides authentication and authorization.
* Service Connections enable secure Azure deployments.
* Service Principals are widely used in CI/CD automation.
* Microsoft Hosted Agents are ideal for most projects.
* Understanding Organizations, Projects, Teams, Permissions, and Service Connections is critical for AZ-400 and real-world Azure DevOps implementations. 

# Module 4: Azure Boards

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. Azure Boards helps teams plan, track, manage, and discuss work across the entire software development lifecycle using Agile, Scrum, Kanban, and CMMI methodologies. 

---

# What is Azure Boards?

Azure Boards is a work management service in Azure DevOps used to:

* Plan Projects
* Track Requirements
* Manage Backlogs
* Execute Sprint Planning
* Monitor Progress
* Generate Reports

Azure Boards provides complete visibility from requirement gathering to deployment.

---

# Why Azure Boards?

Benefits:

* Agile Project Management
* Sprint Planning
* Team Collaboration
* Work Item Tracking
* Reporting & Dashboards
* End-to-End Traceability

---

# Azure Boards Architecture

```text
Portfolio
│
├── Epic
│
├── Feature
│
├── User Story
│
└── Task
```

---

# Work Item Hierarchy

Azure Boards organizes work using a hierarchy.

```text
Epic
 └── Feature
      └── User Story
            └── Task
```

---

# Example Project

## Online Shopping Application

### Epic

```text
E-Commerce Platform
```

### Features

```text
User Management
Product Management
Order Management
Payment Integration
```

### User Stories

```text
As a customer,
I want to register an account
so that I can place orders.
```

### Tasks

```text
Create Registration Page
Create Database Table
Develop API
Test Registration Module
```

---

# Azure Work Item Types

Work Items are used to track work.

Common Work Items:

* Epic
* Feature
* User Story
* Task
* Bug
* Issue

---

# Epic

An Epic represents a large business objective.

Examples:

* Build E-Commerce Platform
* Implement DevOps Platform
* Cloud Migration Project

Characteristics:

* Long-term objective
* Multiple Features
* High-level planning

---

# Feature

A Feature is a functional component of an Epic.

Example:

Epic:

```text
Online Shopping Platform
```

Features:

```text
User Registration
Product Search
Payment Gateway
```

---

# User Story

A User Story describes functionality from the user's perspective.

Format:

```text
As a <User>
I want <Requirement>
So that <Benefit>
```

Example:

```text
As a Customer

I want to reset my password

So that I can access my account
```

---

# Task

Tasks are implementation activities.

Example:

```text
Create Password Reset Page

Develop Backend API

Perform Testing
```

---

# Bug

Used to track defects.

Example:

```text
Login page not loading

Payment gateway timeout
```

---

# Azure Boards Processes

Azure DevOps supports multiple process templates.

---

# Basic Process

Simplified process.

Work Items:

* Epic
* Issue
* Task

Best For:

* Small Teams
* Beginners

---

# Agile Process

Most commonly used.

Work Items:

* Epic
* Feature
* User Story
* Task
* Bug

Best For:

* Agile Teams
* DevOps Projects

Recommended for AZ-400.

---

# Scrum Process

Work Items:

* Epic
* Feature
* Product Backlog Item (PBI)
* Task
* Bug

Best For:

* Scrum Teams

---

# CMMI Process

Work Items:

* Requirement
* Change Request
* Review
* Risk

Best For:

* Enterprise Governance
* Compliance Projects

---

# Comparison of Processes

| Feature               | Basic | Agile   | Scrum   | CMMI |
| --------------------- | ----- | ------- | ------- | ---- |
| User Stories          | No    | Yes     | No      | No   |
| PBI                   | No    | No      | Yes     | No   |
| Risk Management       | No    | No      | No      | Yes  |
| Enterprise Governance | No    | Limited | Limited | Yes  |

---

# Product Backlog

Product Backlog contains all project requirements.

Example:

```text
User Registration

Login Functionality

Shopping Cart

Payment Gateway

Order Tracking
```

Characteristics:

* Prioritized
* Continuously Updated
* Owned by Product Owner

---

# Sprint

A Sprint is a fixed time-boxed development cycle.

Typical Duration:

* 1 Week
* 2 Weeks
* 3 Weeks

Most organizations use:

```text
2 Weeks
```

---

# Sprint Lifecycle

```text
Sprint Planning
      ↓
Development
      ↓
Testing
      ↓
Review
      ↓
Retrospective
```

---

# Creating a Sprint

Steps:

1. Boards
2. Sprints
3. New Sprint
4. Define Dates

Example:

```text
Sprint 1

Start:
01-Jul-2026

End:
14-Jul-2026
```

---

# Sprint Planning

Purpose:

Select work from backlog for the upcoming sprint.

Activities:

* Prioritize Stories
* Estimate Effort
* Assign Team Members
* Define Sprint Goal

---

# Capacity Planning

Used to determine team workload.

Example:

| Team Member | Capacity |
| ----------- | -------- |
| Developer 1 | 40 Hours |
| Developer 2 | 40 Hours |
| Tester      | 30 Hours |

Total Capacity:

```text
110 Hours
```

---

# Story Points

Story Points estimate complexity.

Common Scale:

```text
1
2
3
5
8
13
21
```

(Fibonacci Sequence)

Example:

| Story               | Points |
| ------------------- | ------ |
| Login Page          | 2      |
| Payment Gateway     | 8      |
| Notification System | 13     |

---

# Kanban Board

Kanban provides visual workflow management.

Example:

```text
New
 ↓
Active
 ↓
Resolved
 ↓
Closed
```

---

# Benefits of Kanban

* Visual Tracking
* Continuous Flow
* Reduced Bottlenecks
* Faster Delivery

---

# Azure Board Example

```text
To Do

Create Login Page
Create Registration Page

In Progress

Develop API

Done

Database Setup
```

---

# Queries in Azure Boards

Queries help search and filter work items.

Examples:

* Open Bugs
* Active User Stories
* Assigned Tasks
* Sprint Work

---

# Types of Queries

## Flat List Query

Returns simple list.

Example:

```text
All Active Bugs
```

---

## Tree Query

Shows hierarchy.

Example:

```text
Epic
 └── Feature
      └── User Story
```

---

## Direct Links Query

Shows relationships.

Example:

```text
Feature
 ↔ User Story
```

---

# Creating a Query

Steps:

1. Boards
2. Queries
3. New Query
4. Define Conditions

Example:

```text
Work Item Type = Bug

State = Active
```

---

# Dashboards

Dashboards provide visual reporting.

Widgets include:

* Burndown Chart
* Sprint Progress
* Query Results
* Velocity
* Build Status

---

# Burndown Chart

Shows remaining work.

Example:

```text
Day 1 = 100 Hours

Day 5 = 60 Hours

Day 10 = 20 Hours

Day 14 = 0 Hours
```

Ideal Trend:

Work decreases steadily.

---

# Velocity Chart

Measures team productivity.

Example:

| Sprint   | Story Points |
| -------- | ------------ |
| Sprint 1 | 30           |
| Sprint 2 | 35           |
| Sprint 3 | 40           |

Velocity helps future sprint planning.

---

# Analytics Views

Used for:

* Power BI Integration
* Advanced Reporting
* Trend Analysis

Benefits:

* Historical Analysis
* Team Performance Tracking
* Project Forecasting

---

# Work Item Traceability

Traceability links requirements to implementation.

Example:

```text
Epic
 ↓
Feature
 ↓
User Story
 ↓
Task
 ↓
Commit
 ↓
Build
 ↓
Deployment
```

Benefits:

* Audit Compliance
* Change Tracking
* Impact Analysis

---

# Inherited Process

Organizations can customize process templates.

Examples:

* Create New Work Item Types
* Add Custom Fields
* Modify Workflow States

---

# Create Custom Work Item

Example:

```text
Security Review

Compliance Validation

Architecture Review
```

Steps:

1. Organization Settings
2. Process
3. Create Inherited Process
4. Add Work Item Type

---

# Hands-On Lab 1

## Create Agile Project

Tasks:

1. Create Azure DevOps Project
2. Select Agile Process
3. Create Team
4. Create Dashboard

---

# Hands-On Lab 2

## Create Work Items

Tasks:

1. Create Epic
2. Create Feature
3. Create User Story
4. Create Task
5. Link Work Items

Expected Hierarchy:

```text
Epic
 └── Feature
      └── User Story
            └── Task
```

---

# Hands-On Lab 3

## Sprint Planning

Tasks:

1. Create Sprint
2. Add User Stories
3. Estimate Story Points
4. Assign Team Members
5. Configure Capacity

---

# Hands-On Lab 4

## Queries & Dashboards

Tasks:

1. Create Bug Query
2. Create Sprint Query
3. Create Dashboard
4. Add Burndown Widget
5. Add Velocity Widget

---

# Real-World Scenario

A company is developing an Online Banking Application.

### Planning Structure

```text
Epic
 └── Digital Banking Platform

Feature
 └── Customer Login

User Story
 └── User Login using Mobile Number

Task
 └── Develop Login API
 └── Create UI
 └── Perform Testing
```

Development progress can be tracked from requirement to deployment.

---

# Interview Questions

### Q1. What is Azure Boards?

A project planning and work tracking service in Azure DevOps.

---

### Q2. Difference between Epic and Feature?

* Epic = Large business objective
* Feature = Functional component of an Epic

---

### Q3. What is a User Story?

Requirement written from the user's perspective.

Format:

```text
As a User
I want...
So that...
```

---

### Q4. What is Sprint Planning?

Process of selecting backlog items for a sprint.

---

### Q5. What is Kanban?

Visual workflow management system used to track work progress.

---

### Q6. What is a Burndown Chart?

Chart showing remaining work during a sprint.

---

### Q7. What is Velocity?

Number of story points completed in a sprint.

---

### Q8. What is Work Item Traceability?

Ability to track work from requirement to deployment.

---

# Points to Remember

* Azure Boards is the planning and tracking service of Azure DevOps.
* Recommended process for AZ-400: Agile.
* Work Item Hierarchy: Epic → Feature → User Story → Task.
* Sprints are time-boxed development cycles.
* Story Points estimate complexity, not time.
* Kanban Boards visualize workflow.
* Queries help locate and filter work items.
* Dashboards provide real-time project visibility.
* Traceability is critical for enterprise DevOps and compliance.
* Azure Boards integrates directly with Azure Repos, Pipelines, Test Plans, and GitHub for complete DevOps lifecycle management. 

# Module 5: Git & Branching Strategies

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module focuses on advanced Git operations, collaboration workflows, branching strategies, merge management, and best practices used in enterprise DevOps environments. 

---

# Introduction to Git

## What is Git?

Git is a distributed version control system (DVCS) used to track changes in source code and collaborate with multiple developers.

Created by:

Linus Torvalds

Benefits:

* Version Tracking
* Team Collaboration
* Branching & Merging
* Code History
* Rollback Capability
* Distributed Development

---

# Git Architecture

```text
Working Directory
        ↓
Staging Area
        ↓
Local Repository
        ↓
Remote Repository
```

---

# Git Workflow

```text
Developer
    ↓
git add
    ↓
git commit
    ↓
git push
    ↓
Remote Repository
```

---

# Branches in Git

## What is a Branch?

A branch is an independent line of development.

Benefits:

* Parallel Development
* Feature Isolation
* Safe Experimentation
* Easier Collaboration

---

## Default Branch

Common names:

```text
main
master
```

Modern repositories typically use:

```text
main
```

---

# View Branches

## Local Branches

```bash
git branch
```

Output:

```text
* main
```

---

## Remote Branches

```bash
git branch -r
```

---

## All Branches

```bash
git branch -a
```

---

# Create Branch

```bash
git branch dev
```

Verify:

```bash
git branch
```

---

# Switch Branch

```bash
git checkout dev
```

Modern method:

```bash
git switch dev
```

---

# Create and Switch Together

```bash
git checkout -b feature-login
```

or

```bash
git switch -c feature-login
```

---

# Branch Example

```text
main
 ├── feature-login
 ├── feature-payment
 └── feature-dashboard
```

Multiple developers can work independently.

---

# Merge Branches

## What is Merge?

Combines changes from one branch into another.

Example:

```text
main
  ↑
feature-login
```

---

## Merge Steps

Switch to target branch:

```bash
git checkout main
```

Merge:

```bash
git merge feature-login
```

---

# Fast Forward Merge

Occurs when no divergence exists.

```text
main
   \
feature
```

After merge:

```text
main
feature
```

Git simply moves pointer forward.

---

# Three-Way Merge

Occurs when both branches contain commits.

```text
main
  \
   \
 feature
```

Git creates a merge commit.

---

# Merge Conflict

Occurs when the same file and same lines are modified in different branches.

Example:

Developer A:

```python
app_name = "Azure App"
```

Developer B:

```python
app_name = "DevOps App"
```

Git cannot determine which version is correct.

---

# Resolve Merge Conflict

View status:

```bash
git status
```

Open conflicting file:

```text
<<<<<<< HEAD
Azure App
=======
DevOps App
>>>>>>> feature
```

Choose correct code.

Add file:

```bash
git add .
```

Commit:

```bash
git commit -m "Resolved merge conflict"
```

---

# Git Rebase

## What is Rebase?

Rebase moves commits from one branch onto another.

Example:

```text
Before

main
 └── A
 └── B

feature
 └── C
 └── D
```

After:

```text
main
 └── A
 └── B
 └── C
 └── D
```

History becomes linear.

---

# Rebase Command

```bash
git checkout feature-login

git rebase main
```

---

# Merge vs Rebase

| Merge                 | Rebase           |
| --------------------- | ---------------- |
| Creates Merge Commit  | No Merge Commit  |
| Preserves History     | Rewrites History |
| Easier                | Cleaner History  |
| Recommended for Teams | Advanced Usage   |

---

# Git Tags

## What is a Tag?

Tags mark important points in repository history.

Commonly used for releases.

Examples:

```text
v1.0
v1.1
v2.0
```

---

# Create Tag

```bash
git tag v1.0
```

---

# Push Tag

```bash
git push origin v1.0
```

---

# List Tags

```bash
git tag
```

---

# Git Revert

## What is Revert?

Creates a new commit that undoes previous changes.

Safe for shared repositories.

---

# Revert Example

View history:

```bash
git log --oneline
```

Revert:

```bash
git revert COMMIT_ID
```

---

# Git Reset

## What is Reset?

Moves branch pointer to an earlier commit.

---

# Soft Reset

Keeps changes staged.

```bash
git reset --soft HEAD~1
```

---

# Mixed Reset

Keeps changes unstaged.

```bash
git reset HEAD~1
```

---

# Hard Reset

Deletes changes permanently.

```bash
git reset --hard HEAD~1
```

⚠️ Use carefully.

---

# Revert vs Reset

| Revert             | Reset           |
| ------------------ | --------------- |
| Safe               | Risky           |
| Creates New Commit | Removes History |
| Shared Repository  | Local Changes   |

---

# Git Cherry Pick

## What is Cherry Pick?

Copies a specific commit from one branch to another.

Example:

```text
main

feature-login
 └── Commit A
```

Bring only Commit A into main.

---

# Cherry Pick Command

```bash
git cherry-pick COMMIT_ID
```

---

# Practical Scenario

Developer fixed production bug in hotfix branch.

Need same fix in:

* main
* release
* development

Use:

```bash
git cherry-pick
```

---

# Branching Strategies

Branching strategy defines how teams manage code changes.

---

# GitHub Flow

Simple workflow.

```text
main
  │
  └── feature
```

Process:

1. Create Branch
2. Make Changes
3. Create Pull Request
4. Review
5. Merge

Best For:

* Small Teams
* Continuous Deployment

---

# GitHub Flow Workflow

```text
main
   ↓
feature branch
   ↓
commit
   ↓
pull request
   ↓
merge
   ↓
deploy
```

---

# Feature Branch Workflow

Every feature gets its own branch.

Example:

```text
main
 ├── feature-login
 ├── feature-payment
 └── feature-search
```

Benefits:

* Isolation
* Easy Testing
* Better Reviews

---

# Trunk-Based Development

Modern DevOps approach.

All developers commit frequently to a shared branch.

```text
main
 ├── commit
 ├── commit
 ├── commit
```

Characteristics:

* Small Changes
* Frequent Integration
* Continuous Delivery

Used by:

* Google
* Netflix
* Large Cloud Teams

---

# GitFlow Strategy

Traditional enterprise workflow.

```text
main
 │
 ├── develop
 │
 ├── feature/*
 │
 ├── release/*
 │
 └── hotfix/*
```

---

# Main Branch

Production-ready code.

---

# Develop Branch

Integration branch.

---

# Feature Branch

New development.

Examples:

```text
feature-login
feature-search
feature-payment
```

---

# Release Branch

Release preparation.

Examples:

```text
release-1.0
release-2.0
```

---

# Hotfix Branch

Urgent production fixes.

Examples:

```text
hotfix-payment-bug
```

---

# Release Branch Example

```text
main
 │
 ├── develop
      │
      └── release-1.0
```

Purpose:

* Final Testing
* Bug Fixes
* Documentation

---

# Hotfix Workflow

Production Issue:

```text
main
  │
  └── hotfix
```

Fix:

```text
main
  ↑
hotfix
```

Deploy immediately.

---

# Branch Naming Standards

Recommended naming:

```text
feature/user-login

feature/payment-api

bugfix/login-error

release/v1.0

hotfix/security-patch
```

Benefits:

* Consistency
* Easier Management
* Better Automation

---

# Enterprise Git Best Practices

## Protect Main Branch

Prevent direct commits.

Require:

* Pull Requests
* Reviews
* Build Validation

---

## Use Pull Requests

Never merge directly.

Benefits:

* Code Review
* Quality Assurance
* Collaboration

---

## Small Commits

Good:

```text
Added login validation
```

Bad:

```text
Updated application
```

---

## Commit Frequently

Avoid large commits.

---

## Use Meaningful Messages

Example:

```text
feat: Added OAuth Authentication

fix: Resolved Login Issue

docs: Updated README
```

---

# Real-World Azure DevOps Branching Strategy

```text
main
│
develop
│
├── feature-login
├── feature-payment
├── feature-profile
│
release-v1.0
│
hotfix-security
```

Deployment Flow:

```text
Developer
    ↓
Feature Branch
    ↓
Pull Request
    ↓
Develop
    ↓
Release Branch
    ↓
Main
    ↓
Production
```

---

# Hands-On Lab 1

## Branch Management

Tasks:

1. Create Repository
2. Create Feature Branch
3. Add Code
4. Commit Changes
5. Push Branch

Commands:

```bash
git checkout -b feature-login

git add .

git commit -m "Added login feature"

git push origin feature-login
```

---

# Hands-On Lab 2

## Merge & Rebase

Tasks:

1. Create Two Branches
2. Generate Conflict
3. Resolve Conflict
4. Perform Merge
5. Perform Rebase

---

# Hands-On Lab 3

## Tags & Releases

Tasks:

1. Create Release Tag
2. Push Tag
3. Verify Release Version

Commands:

```bash
git tag v1.0

git push origin v1.0
```

---

# Interview Questions

### Q1. What is a Git Branch?

Independent line of development used to isolate changes.

---

### Q2. Difference between Merge and Rebase?

* Merge preserves history and creates merge commits.
* Rebase creates linear history without merge commits.

---

### Q3. What is Cherry Pick?

Copies a specific commit from one branch to another.

---

### Q4. What is Git Tag?

Marker used for releases and versioning.

---

### Q5. Difference between Revert and Reset?

* Revert creates a new undo commit.
* Reset moves branch pointer backward.

---

### Q6. What is GitFlow?

Branching strategy using:

* Main
* Develop
* Feature
* Release
* Hotfix

---

### Q7. What is Trunk-Based Development?

Developers commit small changes frequently to a shared branch.

---

### Q8. What causes Merge Conflicts?

When multiple branches modify the same file and same lines.

---

# Points to Remember

* Branches allow parallel development.
* Pull Requests improve code quality.
* Merge preserves history; Rebase creates cleaner history.
* Cherry Pick copies individual commits.
* Tags are used for releases.
* Revert is safer than Reset in shared repositories.
* GitHub Flow is simple and modern.
* Trunk-Based Development is preferred for modern DevOps.
* GitFlow is common in large enterprise projects.
* Branch protection policies are critical in Azure DevOps and GitHub environments. 

# Module 6: Azure Repos & GitHub

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers Azure Repos, GitHub, repository management, collaboration workflows, pull requests, branch policies, code reviews, and enterprise source control best practices. 

---

# Introduction to Source Control

## What is Source Control?

Source Control (Version Control) is a system used to track changes in source code and files over time.

Benefits:

* Code History
* Collaboration
* Rollback Capability
* Audit Trail
* Branching & Merging

---

# Why Source Control is Important

Without Source Control:

```text
Developer A
     ↓
Overwrites
     ↓
Developer B Code
```

Problems:

* Lost Changes
* No History
* Difficult Collaboration

---

With Source Control:

```text
Developer A
      ↓
Repository
      ↑
Developer B
```

Benefits:

* Collaboration
* Traceability
* Security
* Recovery

---

# Azure Repos Overview

## What is Azure Repos?

Azure Repos is a source code management service in Azure DevOps.

Supports:

* Git Repositories
* Team Foundation Version Control (TFVC)

Recommended:

```text
Git
```

---

# Azure Repos Architecture

```text
Azure DevOps Project
         │
         ▼
Azure Repos
         │
 ┌───────┼────────┐
 │       │        │
main   dev   feature/*
```

---

# Creating Azure Repository

Steps:

1. Open Azure DevOps Project
2. Select Repos
3. Initialize Repository
4. Clone Repository

---

# Clone Repository

HTTPS:

```bash
git clone https://dev.azure.com/company/project/_git/app
```

SSH:

```bash
git clone git@ssh.dev.azure.com:v3/company/project/app
```

---

# Azure Repo Structure

Example:

```text
WebApplication
│
├── src
├── tests
├── docs
├── terraform
├── pipelines
└── README.md
```

Best Practice:

* Separate Application Code
* Infrastructure Code
* Documentation
* Pipeline Files

---

# Import Existing Repository

Organizations often migrate repositories.

Supported Sources:

* GitHub
* Bitbucket
* GitLab
* Existing Git Repositories

---

# Import Repository

Steps:

1. Repos
2. Import Repository
3. Enter URL

Example:

```text
https://github.com/company/project.git
```

4. Import

---

# Git Credential Manager (GCM)

## What is GCM?

Git Credential Manager securely stores Git credentials.

Benefits:

* Secure Authentication
* Multi-Factor Authentication Support
* Avoid Password Storage

---

# Verify Git Credentials

```bash
git config --global credential.helper manager
```

---

# Authentication Methods

Azure Repos supports:

### Personal Access Token (PAT)

### SSH Keys

### Microsoft Entra Authentication

Recommended:

```text
Microsoft Entra ID
```

---

# Personal Access Token (PAT)

## What is PAT?

A Personal Access Token is an alternative to passwords.

Used For:

* Git Authentication
* Automation Scripts
* CI/CD Pipelines

---

# Create PAT

Steps:

1. User Settings
2. Personal Access Tokens
3. New Token
4. Select Scope
5. Generate

Example Scope:

```text
Code Read
Code Write
Build Read
```

---

# PAT Best Practices

* Use Minimum Permissions
* Set Expiry Dates
* Rotate Regularly
* Store Securely

Never:

```text
Commit PAT to Git Repository
```

---

# SSH Authentication

Generate SSH Key:

```bash
ssh-keygen -t rsa -b 4096
```

Display Public Key:

```bash
cat ~/.ssh/id_rsa.pub
```

Upload key to Azure DevOps.

Test:

```bash
ssh -T git@ssh.dev.azure.com
```

---

# Pull Requests (PR)

## What is a Pull Request?

A Pull Request is a request to merge code into another branch.

Example:

```text
feature-login
      ↓
Pull Request
      ↓
main
```

Purpose:

* Code Review
* Validation
* Collaboration

---

# Pull Request Workflow

```text
Developer
    ↓
Feature Branch
    ↓
Commit Code
    ↓
Push Branch
    ↓
Create Pull Request
    ↓
Review
    ↓
Approve
    ↓
Merge
```

---

# Creating Pull Request

Steps:

1. Push Feature Branch
2. Select Create Pull Request
3. Choose Source Branch
4. Choose Target Branch
5. Add Reviewers
6. Submit

Example:

```text
Source: feature-login

Target: main
```

---

# Pull Request Components

## Title

Example:

```text
Added User Login Module
```

---

## Description

Explain:

* Changes Made
* Impact
* Testing Performed

---

## Reviewers

Example:

```text
Lead Developer

DevOps Engineer
```

---

# Code Reviews

## What is Code Review?

Process of examining code before merging.

Purpose:

* Improve Quality
* Reduce Bugs
* Enforce Standards
* Share Knowledge

---

# Code Review Checklist

### Functionality

* Does code work?

### Security

* Any vulnerabilities?

### Performance

* Efficient implementation?

### Readability

* Easy to understand?

### Maintainability

* Future-proof design?

---

# Pull Request Policies

Organizations enforce PR policies.

Examples:

* Mandatory Reviews
* Successful Build
* Linked Work Item
* Comment Resolution

---

# Branch Policies

## What are Branch Policies?

Rules that protect important branches.

Commonly Applied To:

```text
main

release

production
```

---

# Why Branch Policies?

Prevent:

* Direct Commits
* Unreviewed Changes
* Failed Builds
* Low-Quality Code

---

# Configure Branch Policies

Steps:

1. Repos
2. Branches
3. Select Branch
4. Branch Policies

---

# Common Branch Policies

## Minimum Reviewers

Example:

```text
2 Approvers Required
```

---

## Build Validation

Require successful build.

Example:

```text
Pipeline Success Required
```

---

## Linked Work Items

Ensure code links to work items.

Example:

```text
User Story #105
```

---

## Comment Resolution

All review comments must be resolved.

---

# Protected Branches

Protected branches restrict modifications.

Example:

```text
main

release/v1.0
```

Only approved Pull Requests can merge.

---

# Build Validation

## What is Build Validation?

Automatically runs a pipeline before merge.

Workflow:

```text
Pull Request
      ↓
Build Pipeline
      ↓
Success
      ↓
Merge Allowed
```

---

# Example Validation

```yaml
trigger:
- main

pool:
  vmImage: ubuntu-latest

steps:
- script: echo Build Successful
```

---

# GitHub Overview

## What is GitHub?

GitHub is the world's most popular Git hosting platform.

Owned by:

Microsoft

Used For:

* Source Code Hosting
* Open Source Projects
* Collaboration
* CI/CD

---

# GitHub Components

## Repository

Stores source code.

---

## Issues

Track bugs and enhancements.

---

## Projects

Kanban-style project management.

---

## Pull Requests

Code Review Workflow.

---

## Actions

CI/CD Platform.

---

# GitHub Repository Management

## Create Repository

Options:

```text
Public

Private
```

---

# Repository Structure

```text
project
│
├── src
├── tests
├── docs
├── .github
└── README.md
```

---

# GitHub Issues

Used for:

* Bugs
* Enhancements
* Tasks

Example:

```text
Issue #101

Fix Login Timeout Error
```

---

# GitHub Discussions

Used for:

* Team Communication
* Community Support
* Feature Discussions

Benefits:

* Centralized Knowledge Sharing

---

# Azure Repos vs GitHub

| Feature                      | Azure Repos     | GitHub          |
| ---------------------------- | --------------- | --------------- |
| Integrated with Azure DevOps | Yes             | Partial         |
| Open Source Community        | Limited         | Massive         |
| Enterprise Governance        | Strong          | Strong          |
| Git Hosting                  | Yes             | Yes             |
| CI/CD                        | Azure Pipelines | GitHub Actions  |
| Project Planning             | Azure Boards    | GitHub Projects |

---

# GitHub Enterprise Best Practices

## Branch Protection

Protect:

```text
main
release
```

Require:

* Pull Requests
* Reviews
* Build Validation

---

## CODEOWNERS

Automatically assign reviewers.

Example:

```text
/src @team-devops
```

---

## README Documentation

Every repository should contain:

```text
README.md
```

Includes:

* Overview
* Installation
* Usage
* Architecture

---

## .gitignore

Exclude unnecessary files.

Example:

```text
.env

node_modules/

terraform.tfstate

*.log
```

---

# Real-World Workflow

```text
Developer
    ↓
Feature Branch
    ↓
Commit
    ↓
Push
    ↓
Pull Request
    ↓
Code Review
    ↓
Build Validation
    ↓
Merge
    ↓
Deployment Pipeline
```

---

# Hands-On Lab 1

## Azure Repos

Tasks:

1. Create Azure Repo
2. Clone Repository
3. Commit Code
4. Push Changes
5. Create Branch

---

# Hands-On Lab 2

## Pull Requests

Tasks:

1. Create Feature Branch
2. Add Changes
3. Push Branch
4. Create PR
5. Review PR
6. Merge PR

---

# Hands-On Lab 3

## Branch Policies

Tasks:

1. Protect Main Branch
2. Enable Build Validation
3. Require Approvers
4. Configure Comment Resolution

---

# Hands-On Lab 4

## GitHub Integration

Tasks:

1. Create GitHub Repository
2. Create Issue
3. Create Pull Request
4. Configure Branch Protection
5. Test Collaboration Workflow

---

# Real-Time Enterprise Scenario

An organization has:

```text
main
│
develop
│
feature/*
```

Requirements:

* No direct commit to main
* Minimum 2 reviewers
* Successful build before merge
* Linked work item mandatory

Solution:

* Branch Policies
* Pull Request Reviews
* Build Validation Pipeline
* Azure Boards Integration

---

# Interview Questions

### Q1. What is Azure Repos?

Git-based source control service within Azure DevOps.

---

### Q2. What is a Pull Request?

Request to merge changes from one branch into another after review and validation.

---

### Q3. What is Build Validation?

Automated pipeline execution before allowing code merge.

---

### Q4. What are Branch Policies?

Rules that protect branches and enforce governance.

---

### Q5. Difference between Azure Repos and GitHub?

Azure Repos is integrated with Azure DevOps, while GitHub is a broader collaboration and source hosting platform.

---

### Q6. What is a Personal Access Token (PAT)?

Token-based authentication method used instead of passwords.

---

### Q7. What is Code Review?

Process of reviewing code before merging to ensure quality and standards.

---

### Q8. Why use Protected Branches?

To prevent unauthorized changes and maintain code quality.

---

# Points to Remember

* Azure Repos provides enterprise-grade Git repository management.
* Pull Requests are central to collaboration and code quality.
* Branch Policies protect critical branches.
* Build Validation prevents broken code from being merged.
* PATs should be rotated regularly and never stored in repositories.
* GitHub and Azure Repos both support modern Git workflows.
* Code Reviews improve quality, security, and maintainability.
* Protected branches are mandatory in production environments.
* Repository governance is a major AZ-400 exam topic.
* Azure Repos + Azure Boards + Azure Pipelines form the foundation of enterprise DevOps workflows. 

# Module 7: Azure Pipelines (Continuous Integration)

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module focuses on Azure Pipelines, Continuous Integration (CI), YAML Pipelines, Multi-Stage Pipelines, Build Automation, Deployment Automation, Pipeline Security, Templates, Variables, Agents, and Enterprise CI/CD practices. 

---

# Introduction to Azure Pipelines

## What is Azure Pipelines?

Azure Pipelines is a CI/CD service within Azure DevOps that automates:

* Build
* Test
* Package
* Deploy

applications across multiple platforms.

Supported Platforms:

* Azure
* AWS
* GCP
* Kubernetes
* Docker
* Linux
* Windows

---

# Why Azure Pipelines?

Traditional Deployment:

```text
Developer
   ↓
Manual Build
   ↓
Manual Testing
   ↓
Manual Deployment
```

Problems:

* Human Errors
* Slow Releases
* Inconsistent Deployments

---

Azure Pipeline Workflow:

```text
Developer
   ↓
Git Commit
   ↓
Pipeline Trigger
   ↓
Build
   ↓
Test
   ↓
Artifact
   ↓
Deploy
```

Benefits:

* Automation
* Faster Delivery
* Consistent Deployments
* Improved Quality

---

# Continuous Integration (CI)

## What is CI?

Continuous Integration is the practice of automatically building and testing code whenever changes are committed.

Workflow:

```text
Developer
   ↓
Commit Code
   ↓
Repository
   ↓
Build
   ↓
Test
   ↓
Artifact
```

---

# CI Benefits

### Early Bug Detection

Issues identified immediately.

### Automated Testing

Reduces manual testing effort.

### Faster Releases

Frequent integrations reduce risk.

### Improved Code Quality

Continuous validation.

---

# Azure Pipeline Architecture

```text
Azure Repos / GitHub
          │
          ▼
Azure Pipeline
          │
 ┌────────┼────────┐
 │        │        │
Build   Test   Package
          │
          ▼
Artifact
```

---

# Pipeline Types

## Classic Pipeline

GUI-based pipeline creation.

Characteristics:

* Drag-and-Drop
* Easy for Beginners
* Limited Version Control

---

## YAML Pipeline

Pipeline as Code.

Characteristics:

* Stored in Git Repository
* Version Controlled
* Reusable
* Recommended

AZ-400 Focus:

```text
YAML Pipelines
```

---

# Creating a YAML Pipeline

Repository Structure:

```text
project
│
├── src
├── tests
└── azure-pipelines.yml
```

---

# Basic YAML Pipeline

```yaml
trigger:
- main

pool:
  vmImage: ubuntu-latest

steps:
- script: echo "Hello Azure Pipeline"
```

---

# YAML Structure

```yaml
trigger:
pool:
variables:
stages:
jobs:
steps:
```

---

# Pipeline Components

## Trigger

Defines when pipeline runs.

Example:

```yaml
trigger:
- main
```

Pipeline executes whenever code is pushed to main.

---

# Multiple Branch Triggers

```yaml
trigger:
  branches:
    include:
    - main
    - develop
```

---

# Exclude Branch

```yaml
trigger:
  branches:
    exclude:
    - feature/*
```

---

# Pool

Defines build agent.

Microsoft Hosted:

```yaml
pool:
  vmImage: ubuntu-latest
```

---

Windows Agent:

```yaml
pool:
  vmImage: windows-latest
```

---

# Steps

Individual pipeline tasks.

Example:

```yaml
steps:
- script: echo "Build Started"
```

---

Multiple Steps:

```yaml
steps:
- script: echo "Step 1"

- script: echo "Step 2"
```

---

# Variables

Used to store reusable values.

Example:

```yaml
variables:
  appName: webapp
```

Usage:

```yaml
steps:
- script: echo $(appName)
```

---

# Variable Types

## Pipeline Variables

```yaml
variables:
  environment: dev
```

---

## Variable Groups

Shared variables across pipelines.

Example:

```text
DEV-Variables

PROD-Variables
```

---

## Secret Variables

Used for:

* Passwords
* API Keys
* Tokens

Stored securely.

---

# Conditions

Control pipeline execution.

Example:

```yaml
steps:
- script: echo Deploy

  condition: succeeded()
```

---

# Common Conditions

Execute if successful:

```yaml
condition: succeeded()
```

---

Execute if failed:

```yaml
condition: failed()
```

---

Always execute:

```yaml
condition: always()
```

---

# Jobs

A Job contains multiple steps.

Example:

```yaml
jobs:
- job: Build
  steps:
  - script: echo Build
```

---

# Multiple Jobs

```yaml
jobs:
- job: Build

- job: Test
```

Jobs can run in parallel.

---

# Stages

Stages divide pipelines logically.

Example:

```text
Build
  ↓
Test
  ↓
Deploy
```

---

# Multi-Stage Pipeline

```yaml
stages:

- stage: Build

- stage: Test

- stage: Deploy
```

---

# Enterprise Multi-Stage Example

```text
Build
  ↓
Dev
  ↓
QA
  ↓
UAT
  ↓
Production
```

---

# Build Pipeline Example

Python Application:

```yaml
trigger:
- main

pool:
  vmImage: ubuntu-latest

steps:

- task: UsePythonVersion@0
  inputs:
    versionSpec: '3.11'

- script: pip install -r requirements.txt

- script: python -m pytest
```

---

# Node.js Build Pipeline

```yaml
steps:

- task: NodeTool@0
  inputs:
    versionSpec: '18.x'

- script: npm install

- script: npm test
```

---

# Artifact Management

## What is an Artifact?

Output generated by build.

Examples:

* ZIP File
* JAR File
* WAR File
* Docker Image

---

# Publish Artifact

```yaml
- task: PublishBuildArtifacts@1
  inputs:
    pathToPublish: '$(Build.ArtifactStagingDirectory)'
    artifactName: 'drop'
```

---

# Download Artifact

```yaml
- task: DownloadBuildArtifacts@0
```

---

# Templates

## Why Templates?

Avoid duplication.

Benefits:

* Reusability
* Standardization
* Maintainability

---

# Template Example

build-template.yml

```yaml
steps:
- script: echo Build Template
```

---

Main Pipeline

```yaml
steps:
- template: build-template.yml
```

---

# Parameters

Parameters make pipelines dynamic.

Example:

```yaml
parameters:
- name: environment
  type: string
```

Usage:

```yaml
echo ${{ parameters.environment }}
```

---

# Azure Pipeline Agents

Agents execute pipeline tasks.

---

# Microsoft Hosted Agent

Managed by Microsoft.

Advantages:

* No Maintenance
* Latest Tools
* Easy Setup

Example:

```yaml
pool:
  vmImage: ubuntu-latest
```

---

# Self Hosted Agent

Installed on:

* Azure VM
* AWS EC2
* On-Premises Server

Advantages:

* Custom Tools
* Internal Access
* Better Performance

---

# Install Self Hosted Agent

Steps:

1. Create VM
2. Agent Pools
3. New Agent
4. Download Agent
5. Configure Agent
6. Start Agent

---

# Deployment Jobs

Used for deployments.

Example:

```yaml
deployment: DeployWeb
```

Benefits:

* Environment Tracking
* Approval Support
* Audit History

---

# Environments

Logical deployment targets.

Examples:

```text
Development

QA

UAT

Production
```

---

# Environment Example

```yaml
environment: Production
```

---

# Approvals

Used before deployment.

Workflow:

```text
Build
  ↓
Approval
  ↓
Deploy
```

Benefits:

* Governance
* Change Control

---

# Manual Approval Scenario

Production Deployment:

```text
Developer
   ↓
Build Success
   ↓
Manager Approval
   ↓
Production Deployment
```

---

# Pipeline Security

Best Practices:

* Use Service Connections
* Use Managed Identities
* Store Secrets in Key Vault
* Use Secret Variables

Never:

```text
Store Passwords in YAML
```

---

# Azure Key Vault Integration

Retrieve secret:

```yaml
- task: AzureKeyVault@2
```

Benefits:

* Secure Secret Management
* Compliance
* Centralized Control

---

# Build Validation

Pull Request Workflow:

```text
Pull Request
      ↓
Build Validation
      ↓
Success
      ↓
Merge
```

Prevents broken code from merging.

---

# CI/CD Flow Example

```text
Developer
     ↓
Git Commit
     ↓
Azure Repos
     ↓
Pipeline Trigger
     ↓
Build
     ↓
Test
     ↓
Artifact
     ↓
Deployment
```

---

# Real-World Enterprise Pipeline

```text
Developer
    ↓
Pull Request
    ↓
Build Validation
    ↓
Merge
    ↓
Build Stage
    ↓
Security Scan
    ↓
Unit Tests
    ↓
Publish Artifact
    ↓
Deploy Dev
    ↓
Deploy QA
    ↓
Approval
    ↓
Deploy Production
```

---

# Hands-On Lab 1

## Create First Pipeline

Tasks:

1. Create Azure Repo
2. Create YAML File
3. Configure Trigger
4. Run Pipeline

---

# Hands-On Lab 2

## Build Validation

Tasks:

1. Create Pull Request
2. Configure Build Validation
3. Verify Automatic Build

---

# Hands-On Lab 3

## Multi-Stage Pipeline

Tasks:

1. Build Stage
2. Test Stage
3. Deploy Stage
4. Verify Pipeline Flow

---

# Hands-On Lab 4

## Artifact Management

Tasks:

1. Build Application
2. Publish Artifact
3. Download Artifact
4. Deploy Artifact

---

# Hands-On Lab 5

## Self Hosted Agent

Tasks:

1. Create Azure VM
2. Install Agent
3. Register Agent
4. Run Pipeline

---

# Real-Time Project

## Deploy Python Application to Azure App Service

Pipeline Stages:

```text
Source Code
      ↓
Build
      ↓
Unit Test
      ↓
Artifact
      ↓
Deploy Dev
      ↓
Deploy QA
      ↓
Approval
      ↓
Deploy Production
```

Technologies:

* Azure Repos
* Azure Pipelines
* Azure App Service
* Azure Key Vault
* Azure Monitor

---

# Interview Questions

### Q1. What is Azure Pipelines?

A CI/CD service that automates building, testing, and deployment of applications.

---

### Q2. Difference between Classic and YAML Pipelines?

| Classic            | YAML                     |
| ------------------ | ------------------------ |
| GUI Based          | Code Based               |
| Limited Versioning | Fully Version Controlled |
| Less Flexible      | More Flexible            |

---

### Q3. What is a Trigger?

A condition that starts a pipeline automatically.

---

### Q4. What is an Artifact?

Output generated by a build process.

Examples:

* ZIP
* JAR
* Docker Image

---

### Q5. What is a Stage?

Logical grouping of jobs within a pipeline.

---

### Q6. Difference between Job and Step?

* Job = Collection of Steps
* Step = Individual Task

---

### Q7. What are Variable Groups?

Shared variables used across multiple pipelines.

---

### Q8. Why use Self Hosted Agents?

To run pipelines in private networks and use custom tools.

---

### Q9. What is Build Validation?

Automatically validates code through a pipeline before merge.

---

### Q10. How do you secure secrets in Azure Pipelines?

* Azure Key Vault
* Secret Variables
* Service Connections
* Managed Identities

---

# Points to Remember

* Azure Pipelines is the CI/CD engine of Azure DevOps.
* YAML Pipelines are preferred over Classic Pipelines.
* Stages → Jobs → Steps is the pipeline hierarchy.
* Artifacts are outputs from build processes.
* Multi-stage pipelines support Dev → QA → UAT → Production deployments.
* Microsoft Hosted Agents are easiest to manage.
* Self Hosted Agents provide greater control.
* Templates improve reusability and standardization.
* Azure Key Vault is the recommended solution for secret management.
* Build Validation and Approvals are critical enterprise DevOps practices.
* Azure Pipelines is one of the most important topics in the AZ-400 certification exam. 


# Module 8: GitHub Actions

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers GitHub Actions, Workflows, Runners, CI/CD Automation, Secrets Management, OIDC Authentication, Self-Hosted Runners, and Enterprise GitHub DevOps practices. 

---

# Introduction to GitHub Actions

## What is GitHub Actions?

GitHub Actions is GitHub's built-in CI/CD and automation platform.

It allows developers to:

* Build Applications
* Run Tests
* Deploy Applications
* Automate Workflows
* Perform Security Scanning

without using external CI/CD tools.

---

# Why GitHub Actions?

Traditional Workflow:

```text
Developer
   ↓
Commit Code
   ↓
Manual Build
   ↓
Manual Testing
   ↓
Manual Deployment
```

Problems:

* Slow Releases
* Human Errors
* Inconsistent Deployments

---

GitHub Actions Workflow:

```text
Developer
   ↓
Git Push
   ↓
Workflow Trigger
   ↓
Build
   ↓
Test
   ↓
Deploy
```

Benefits:

* Automation
* Faster Releases
* Better Quality
* Reduced Errors

---

# GitHub Actions Architecture

```text
GitHub Repository
         │
         ▼
Workflow
         │
 ┌───────┼────────┐
 │       │        │
Build   Test   Deploy
```

---

# Key Components

## Workflow

Workflow is an automated process.

Stored in:

```text
.github/workflows/
```

Example:

```text
.github/workflows/build.yml
```

---

## Event

An event triggers a workflow.

Examples:

* push
* pull_request
* workflow_dispatch
* schedule

---

## Job

A job is a collection of steps.

Example:

```text
Build Job

Test Job

Deploy Job
```

---

## Step

A step performs a specific task.

Examples:

```text
Checkout Code

Install Packages

Run Tests
```

---

## Runner

Runner executes workflow jobs.

Types:

* GitHub Hosted Runner
* Self Hosted Runner

---

# Workflow File Structure

Location:

```text
.github
└── workflows
    └── ci.yml
```

---

# First Workflow

```yaml
name: First Workflow

on:
  push:

jobs:

  build:

    runs-on: ubuntu-latest

    steps:

    - name: Hello World

      run: echo "Hello GitHub Actions"
```

---

# Workflow Syntax

```yaml
name:
on:
jobs:
runs-on:
steps:
```

---

# Workflow Triggers

## Push Event

Runs when code is pushed.

```yaml
on:
  push:
```

---

## Pull Request Event

Runs when PR is created.

```yaml
on:
  pull_request:
```

---

## Multiple Events

```yaml
on:
  push:
  pull_request:
```

---

## Manual Trigger

```yaml
on:
  workflow_dispatch:
```

Run from GitHub UI.

---

## Scheduled Trigger

Runs automatically.

Example:

Daily at midnight.

```yaml
on:
  schedule:
  - cron: '0 0 * * *'
```

---

# Understanding Jobs

Single Job:

```yaml
jobs:

  build:

    runs-on: ubuntu-latest
```

---

Multiple Jobs:

```yaml
jobs:

  build:

  test:

  deploy:
```

---

Workflow Flow:

```text
Build
 ↓
Test
 ↓
Deploy
```

---

# Job Dependencies

```yaml
jobs:

  build:

  test:
    needs: build

  deploy:
    needs: test
```

Execution:

```text
Build
 ↓
Test
 ↓
Deploy
```

---

# Steps

Example:

```yaml
steps:

- name: Step 1
  run: echo Build

- name: Step 2
  run: echo Test
```

---

# GitHub Marketplace Actions

Reusable actions from GitHub Marketplace.

Examples:

* Checkout
* Setup Python
* Setup Node
* Docker Build

---

# Checkout Action

Downloads repository code.

```yaml
- uses: actions/checkout@v4
```

Almost every workflow starts with checkout.

---

# Setup Python

```yaml
- uses: actions/setup-python@v5

  with:
    python-version: '3.11'
```

---

# Setup Node.js

```yaml
- uses: actions/setup-node@v4

  with:
    node-version: '20'
```

---

# Python CI Workflow

```yaml
name: Python CI

on:
  push:

jobs:

  build:

    runs-on: ubuntu-latest

    steps:

    - uses: actions/checkout@v4

    - uses: actions/setup-python@v5
      with:
        python-version: '3.11'

    - run: pip install -r requirements.txt

    - run: pytest
```

---

# Node.js Workflow

```yaml
name: Node CI

on:
  push:

jobs:

  build:

    runs-on: ubuntu-latest

    steps:

    - uses: actions/checkout@v4

    - uses: actions/setup-node@v4
      with:
        node-version: '20'

    - run: npm install

    - run: npm test
```

---

# Variables

Used to store reusable values.

Example:

```yaml
env:

  APP_NAME: webapp
```

Usage:

```yaml
run: echo $APP_NAME
```

---

# Repository Variables

Configured from:

```text
Settings
 ↓
Secrets and Variables
 ↓
Variables
```

Examples:

```text
ENVIRONMENT=DEV

APP_NAME=WEBAPP
```

---

# Secrets

## What are Secrets?

Secure storage for:

* Passwords
* Tokens
* API Keys
* Connection Strings

---

# Creating Secret

Navigate:

```text
Repository Settings
 ↓
Secrets and Variables
 ↓
Actions
 ↓
New Secret
```

Examples:

```text
AZURE_CLIENT_ID

AZURE_TENANT_ID

DOCKER_PASSWORD
```

---

# Using Secrets

```yaml
env:

  PASSWORD: ${{ secrets.DB_PASSWORD }}
```

---

# Secret Best Practices

Never:

```yaml
PASSWORD=Admin123
```

inside workflow files.

Use:

```yaml
${{ secrets.PASSWORD }}
```

---

# GitHub Hosted Runners

Managed by GitHub.

Examples:

```yaml
runs-on: ubuntu-latest

runs-on: windows-latest

runs-on: macos-latest
```

Benefits:

* Free Minutes
* No Maintenance
* Automatic Updates

---

# Self Hosted Runners

Installed on:

* Azure VM
* AWS EC2
* On-Prem Server

Benefits:

* Full Control
* Custom Software
* Private Network Access

---

# Self Hosted Runner Architecture

```text
GitHub
   ↓
Workflow
   ↓
Self Hosted Runner
   ↓
Private Infrastructure
```

---

# Installing Self Hosted Runner

Steps:

1. Repository Settings
2. Actions
3. Runners
4. New Self Hosted Runner
5. Download Agent
6. Configure Runner
7. Start Runner

---

# Docker Build Workflow

```yaml
name: Docker Build

on:
  push:

jobs:

  build:

    runs-on: ubuntu-latest

    steps:

    - uses: actions/checkout@v4

    - run: docker build -t app .
```

---

# Docker Hub Login

```yaml
- uses: docker/login-action@v3

  with:
    username: ${{ secrets.DOCKER_USER }}

    password: ${{ secrets.DOCKER_PASSWORD }}
```

---

# Azure Deployment using GitHub Actions

Workflow:

```text
GitHub
   ↓
Build
   ↓
Authenticate Azure
   ↓
Deploy
```

---

# Azure Login Action

```yaml
- uses: azure/login@v2
```

Used for Azure authentication.

---

# Azure Web App Deployment

```yaml
- uses: azure/webapps-deploy@v3
```

Deploys application to Azure App Service.

---

# OIDC Authentication

## What is OIDC?

OpenID Connect authentication allows GitHub to access Azure without storing secrets.

Traditional Method:

```text
GitHub
   ↓
Secret
   ↓
Azure
```

OIDC Method:

```text
GitHub
   ↓
Temporary Token
   ↓
Azure
```

Benefits:

* More Secure
* No Stored Credentials
* Recommended by Microsoft

---

# OIDC Components

Required:

* GitHub Repository
* Azure App Registration
* Federated Credentials

---

# Security Scanning

GitHub provides built-in security features.

---

# Dependabot

Identifies vulnerable packages.

Example:

```text
Outdated package detected

Upgrade recommended
```

---

# CodeQL

Performs source code security scanning.

Detects:

* SQL Injection
* Cross Site Scripting
* Hardcoded Secrets

---

# CodeQL Workflow

```yaml
- uses: github/codeql-action/init@v3
```

---

# GitHub Environments

Used for deployment governance.

Examples:

```text
Development

QA

Production
```

---

# Environment Protection Rules

Production Example:

```text
Approval Required

Deployment Restricted
```

Workflow:

```text
Deploy
 ↓
Approval
 ↓
Production
```

---

# Matrix Strategy

Run jobs on multiple platforms.

Example:

```yaml
strategy:

  matrix:

    os:
      - ubuntu-latest
      - windows-latest
```

Runs workflow on multiple operating systems.

---

# Reusable Workflows

Used across repositories.

Benefits:

* Standardization
* Reusability
* Governance

---

# Enterprise GitHub Workflow

```text
Developer
     ↓
Feature Branch
     ↓
Pull Request
     ↓
GitHub Actions
     ↓
Build
     ↓
Unit Test
     ↓
Security Scan
     ↓
Package
     ↓
Deploy DEV
     ↓
Deploy QA
     ↓
Approval
     ↓
Deploy PROD
```

---

# Hands-On Lab 1

## Create First Workflow

Tasks:

1. Create GitHub Repository
2. Create Workflow File
3. Commit Code
4. Verify Workflow Execution

---

# Hands-On Lab 2

## Python CI Pipeline

Tasks:

1. Setup Python
2. Install Dependencies
3. Run Unit Tests
4. Verify Build

---

# Hands-On Lab 3

## GitHub Secrets

Tasks:

1. Create Secret
2. Use Secret in Workflow
3. Verify Secure Access

---

# Hands-On Lab 4

## Deploy Azure Web App

Tasks:

1. Create App Service
2. Configure Azure Login
3. Create Deployment Workflow
4. Verify Deployment

---

# Hands-On Lab 5

## OIDC Authentication

Tasks:

1. Create Azure App Registration
2. Configure Federated Credentials
3. Configure GitHub Workflow
4. Verify Passwordless Authentication

---

# Real-Time Project

## Deploy Flask Application using GitHub Actions

Architecture:

```text
GitHub Repository
       ↓
GitHub Actions
       ↓
Build Flask App
       ↓
Run Tests
       ↓
Build Docker Image
       ↓
Push to ACR
       ↓
Deploy to Azure App Service
```

Technologies:

* GitHub
* GitHub Actions
* Docker
* Azure Container Registry
* Azure App Service
* OIDC Authentication

---

# Interview Questions

### Q1. What is GitHub Actions?

GitHub's native CI/CD and workflow automation platform.

---

### Q2. What is a Workflow?

Automated process defined in YAML.

Stored under:

```text
.github/workflows
```

---

### Q3. What is a Runner?

A machine that executes workflow jobs.

---

### Q4. Difference between GitHub Hosted and Self Hosted Runner?

| GitHub Hosted     | Self Hosted         |
| ----------------- | ------------------- |
| Managed by GitHub | Managed by Customer |
| Easy Setup        | Full Control        |
| Public Network    | Private Network     |

---

### Q5. What are GitHub Secrets?

Secure storage for passwords, tokens, and credentials.

---

### Q6. What is OIDC?

OpenID Connect authentication that eliminates long-lived secrets.

---

### Q7. What is Dependabot?

Tool that identifies vulnerable and outdated dependencies.

---

### Q8. What is CodeQL?

Static Application Security Testing (SAST) tool for source code analysis.

---

### Q9. What are GitHub Environments?

Deployment targets with governance controls such as approvals.

---

### Q10. Why is OIDC preferred over Service Principal Secrets?

* More Secure
* No Secret Rotation
* Temporary Tokens
* Reduced Credential Exposure

---

# Points to Remember

* GitHub Actions is GitHub's built-in CI/CD platform.
* Workflows are stored in `.github/workflows`.
* Workflow hierarchy: Event → Workflow → Job → Step.
* GitHub Hosted Runners are easiest to use.
* Self Hosted Runners provide full control and private network access.
* Secrets should always be stored in GitHub Secrets.
* OIDC is the recommended authentication method for Azure deployments.
* Dependabot and CodeQL are essential DevSecOps tools.
* GitHub Environments provide deployment governance.
* GitHub Actions and Azure Pipelines are both important CI/CD tools covered in AZ-400. 

# Module 9: Azure Artifacts

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers Azure Artifacts, Package Management, Artifact Repositories, Feeds, Upstream Sources, Package Publishing, Package Consumption, Versioning, and Enterprise Artifact Management practices. 

---

# Introduction to Azure Artifacts

## What is Azure Artifacts?

Azure Artifacts is a package management service within Azure DevOps used to:

* Store Packages
* Share Packages
* Manage Dependencies
* Version Software Components

It enables teams to create private package repositories and consume packages securely across projects.

---

# Why Azure Artifacts?

Without Artifact Management:

```text
Developer A
   ↓
Email Package
   ↓
Developer B
```

Problems:

* No Version Control
* Security Risks
* Difficult Dependency Management
* Manual Distribution

---

With Azure Artifacts:

```text
Developer
   ↓
Azure Artifacts Feed
   ↓
Development Teams
```

Benefits:

* Central Repository
* Version Control
* Security
* Dependency Management

---

# What is a Package?

A Package is a reusable software component.

Examples:

* Python Libraries
* NPM Packages
* Java Libraries
* .NET Packages
* Container Images

---

# Supported Package Types

Azure Artifacts supports:

| Package Type       | Technology    |
| ------------------ | ------------- |
| NuGet              | .NET          |
| npm                | Node.js       |
| Maven              | Java          |
| Python             | Python        |
| Universal Packages | Any File Type |

---

# Azure Artifacts Architecture

```text
Azure DevOps
     │
     ▼
Azure Artifacts
     │
 ┌───┼────┬────┬────┐
 │   │    │    │    │
NuGet npm Maven PyPI Universal
```

---

# What is a Feed?

A Feed is a logical container that stores packages.

Example:

```text
Company-Packages
```

Contains:

```text
Company-Packages
│
├── npm Packages
├── Python Packages
├── NuGet Packages
└── Universal Packages
```

---

# Benefits of Feeds

* Package Organization
* Access Control
* Version Management
* Team Collaboration

---

# Creating a Feed

Steps:

1. Azure DevOps Project
2. Artifacts
3. Create Feed
4. Enter Feed Name
5. Configure Visibility

Example:

```text
enterprise-packages
```

---

# Feed Visibility

## Private Feed

Accessible only within organization.

Recommended:

```text
Enterprise Production
```

---

## Public Feed

Accessible externally.

Used for:

* Open Source Projects
* Public Libraries

---

# Feed Permissions

Azure Artifacts provides role-based access.

| Role        | Permission       |
| ----------- | ---------------- |
| Owner       | Full Control     |
| Contributor | Publish Packages |
| Reader      | Consume Packages |

---

# Package Lifecycle

```text
Developer
   ↓
Build Package
   ↓
Publish Package
   ↓
Azure Artifacts Feed
   ↓
Consume Package
```

---

# Upstream Sources

## What are Upstream Sources?

Upstream Sources allow Azure Artifacts to connect to external repositories.

Examples:

* npm Registry
* Maven Central
* NuGet.org
* PyPI

---

# Upstream Source Architecture

```text
Developer
   ↓
Azure Artifacts
   ↓
External Registry
```

---

# Benefits of Upstream Sources

### Faster Package Access

Caches downloaded packages.

### Security

Approved package source.

### Reliability

Packages remain available even if external source is unavailable.

---

# Common Upstream Registries

### npm Registry

```text
https://registry.npmjs.org
```

---

### NuGet

```text
https://www.nuget.org
```

---

### Maven Central

```text
https://repo.maven.apache.org
```

---

### PyPI

```text
https://pypi.org
```

---

# Package Publishing

## Publish Package Workflow

```text
Source Code
     ↓
Build
     ↓
Package
     ↓
Publish
     ↓
Azure Artifacts
```

---

# Publishing NuGet Package

```bash
dotnet pack

dotnet nuget push
```

---

# Publishing npm Package

Authenticate:

```bash
npm login
```

Publish:

```bash
npm publish
```

---

# Publishing Python Package

Build Package:

```bash
python setup.py sdist
```

Publish:

```bash
twine upload
```

---

# Publishing Universal Package

Universal Packages support:

* ZIP Files
* Binaries
* Scripts
* Configuration Files

---

Example:

```bash
az artifacts universal publish
```

---

# Consuming Packages

Applications can consume packages from Azure Artifacts.

---

# Install npm Package

```bash
npm install company-library
```

---

# Install Python Package

```bash
pip install company-library
```

---

# Install Maven Package

```xml
<dependency>
    <groupId>com.company</groupId>
    <artifactId>library</artifactId>
</dependency>
```

---

# Install NuGet Package

```bash
dotnet add package Company.Library
```

---

# Semantic Versioning (SemVer)

## What is Semantic Versioning?

Industry-standard versioning format:

```text
MAJOR.MINOR.PATCH
```

Example:

```text
1.2.5
```

---

# Version Components

## Major Version

Breaking Changes

```text
1.x.x → 2.x.x
```

Example:

```text
1.0.0 → 2.0.0
```

---

## Minor Version

New Features

```text
1.1.0 → 1.2.0
```

---

## Patch Version

Bug Fixes

```text
1.1.1 → 1.1.2
```

---

# Semantic Version Examples

| Version | Meaning         |
| ------- | --------------- |
| 1.0.0   | Initial Release |
| 1.1.0   | New Feature     |
| 1.1.1   | Bug Fix         |
| 2.0.0   | Breaking Change |

---

# Package Retention Policies

Retention Policies automatically clean up old packages.

Benefits:

* Reduce Storage
* Simplify Management
* Improve Performance

Example:

```text
Keep Last 10 Versions
```

---

# Package Promotion Strategy

Enterprise environments often use:

```text
Development
     ↓
QA
     ↓
Production
```

Package progresses through environments.

---

# Azure Artifacts and CI/CD

Pipeline Workflow:

```text
Build
  ↓
Test
  ↓
Package
  ↓
Publish Artifact
  ↓
Deploy
```

---

# Publish Package in Azure Pipeline

Example:

```yaml
steps:

- script: npm install

- script: npm run build

- script: npm publish
```

---

# Download Package in Pipeline

```yaml
steps:

- task: DownloadPackage@1
```

---

# Universal Packages

## What are Universal Packages?

Azure DevOps package type that supports any file format.

Examples:

* ZIP
* ISO
* Configuration Files
* Binary Files

---

# Universal Package Workflow

```text
Application Build
       ↓
ZIP Package
       ↓
Azure Artifacts
       ↓
Deployment Pipeline
```

---

# Security Best Practices

## Access Control

Use least privilege principle.

---

## Feed Permissions

Restrict publishing rights.

---

## Package Validation

Validate packages before release.

---

## Vulnerability Scanning

Scan dependencies regularly.

---

## Approved Sources Only

Allow only trusted upstream sources.

---

# Real-World Scenario

A company develops:

```text
Customer Portal
```

Shared Libraries:

```text
Authentication Library

Logging Library

Notification Library
```

Instead of copying code between projects:

```text
Build Package
      ↓
Azure Artifacts
      ↓
Reuse Across Applications
```

Benefits:

* Reusability
* Consistency
* Faster Development

---

# Enterprise Architecture

```text
Developer
     ↓
Build Pipeline
     ↓
Azure Artifacts Feed
     ↓
Application Teams
     ↓
Deployment Pipeline
```

---

# Hands-On Lab 1

## Create Azure Artifacts Feed

Tasks:

1. Create Feed
2. Configure Permissions
3. Enable Upstream Sources

---

# Hands-On Lab 2

## Publish Package

Tasks:

1. Create Sample Package
2. Build Package
3. Publish to Feed
4. Verify Feed

---

# Hands-On Lab 3

## Consume Package

Tasks:

1. Connect Feed
2. Install Package
3. Test Application
4. Verify Dependency Resolution

---

# Hands-On Lab 4

## CI/CD Integration

Tasks:

1. Build Application
2. Create Package
3. Publish Artifact
4. Consume Artifact
5. Deploy Application

---

# Real-Time Project

## Enterprise Shared Library Management

Architecture:

```text
Developer
      ↓
Azure Repos
      ↓
Azure Pipeline
      ↓
Azure Artifacts
      ↓
Application Teams
      ↓
Production Deployment
```

Technologies:

* Azure Repos
* Azure Pipelines
* Azure Artifacts
* Azure App Service
* Azure Key Vault

---

# Interview Questions

### Q1. What is Azure Artifacts?

A package management service in Azure DevOps used to store, manage, and share packages.

---

### Q2. What is a Feed?

A logical container used to store packages.

---

### Q3. What are Upstream Sources?

External package repositories connected to Azure Artifacts.

Examples:

* npm
* Maven Central
* NuGet
* PyPI

---

### Q4. What package types are supported by Azure Artifacts?

* NuGet
* npm
* Maven
* Python
* Universal Packages

---

### Q5. What is Semantic Versioning?

Versioning standard using:

```text
MAJOR.MINOR.PATCH
```

---

### Q6. What is a Universal Package?

A package type that supports any file format.

---

### Q7. Why use Azure Artifacts?

* Centralized Package Storage
* Dependency Management
* Security
* Version Control

---

### Q8. What is the purpose of Package Retention Policies?

To automatically clean old package versions and reduce storage usage.

---

### Q9. What are the benefits of Upstream Sources?

* Faster Access
* Package Caching
* Security
* Reliability

---

### Q10. How does Azure Artifacts integrate with CI/CD?

Packages can be automatically published and consumed within Azure Pipelines.

---

# Points to Remember

* Azure Artifacts is Azure DevOps' package management solution.
* Feeds are used to organize packages.
* Supports NuGet, npm, Maven, Python, and Universal Packages.
* Upstream Sources provide secure access to external package repositories.
* Semantic Versioning follows MAJOR.MINOR.PATCH.
* Universal Packages support any file format.
* Azure Artifacts integrates directly with Azure Pipelines.
* Package reuse improves development speed and consistency.
* Feed permissions are critical for security.
* Artifact management is an important DevOps and AZ-400 certification topic. 

# Module 10: Security & Azure Key Vault

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers DevOps Security, Authentication, Authorization, Service Principals, Managed Identities, Personal Access Tokens (PAT), Service Connections, Azure Key Vault, DevSecOps, CodeQL, Dependabot, Secret Management, and Security Best Practices. 

---

# Introduction to DevSecOps

## What is DevSecOps?

DevSecOps means integrating Security into every phase of the DevOps lifecycle.

Traditional Model:

```text
Development
     ↓
Operations
     ↓
Security
```

Security is often added at the end.

---

DevSecOps Model:

```text
Plan
 ↓
Code
 ↓
Build
 ↓
Test
 ↓
Deploy
 ↓
Monitor
```

Security is integrated throughout the lifecycle.

---

# Benefits of DevSecOps

* Early Vulnerability Detection
* Reduced Security Risks
* Faster Compliance
* Automated Security Validation
* Secure CI/CD Pipelines

---

# Security in Azure DevOps

Security Areas:

```text
Identity Security
      ↓
Code Security
      ↓
Pipeline Security
      ↓
Infrastructure Security
      ↓
Application Security
```

---

# Authentication vs Authorization

These terms are commonly asked in interviews.

---

## Authentication

Authentication verifies identity.

Question:

```text
Who are you?
```

Examples:

* Username & Password
* MFA
* Certificates
* OAuth

---

## Authorization

Authorization determines permissions.

Question:

```text
What are you allowed to do?
```

Examples:

* Read
* Write
* Delete
* Deploy

---

# Authentication Flow

```text
User
  ↓
Login
  ↓
Authentication
  ↓
Authorization
  ↓
Access Granted
```

---

# Microsoft Entra ID

Formerly:

```text
Azure Active Directory
```

Provides:

* Authentication
* Authorization
* Identity Management
* Conditional Access
* MFA

---

# Service Principals

## What is a Service Principal?

A Service Principal is a non-human identity used for automation.

Examples:

* Azure Pipelines
* GitHub Actions
* Terraform
* Automation Scripts

---

# Service Principal Components

```text
Application ID (Client ID)

Tenant ID

Client Secret
```

---

# Create Service Principal

Azure CLI:

```bash
az ad sp create-for-rbac \
--name devops-sp
```

Output:

```json
{
  "appId": "xxxx",
  "password": "xxxx",
  "tenant": "xxxx"
}
```

---

# Service Principal Usage

```text
Azure Pipeline
       ↓
Service Principal
       ↓
Azure Resources
```

Used for:

* Deployments
* Resource Provisioning
* Automation

---

# Managed Identity

## What is Managed Identity?

Managed Identity is an Azure-managed identity for resources.

Azure automatically:

* Creates Identity
* Rotates Credentials
* Secures Authentication

---

# Managed Identity Architecture

```text
Azure VM
    ↓
Managed Identity
    ↓
Azure Key Vault
```

No passwords required.

---

# Benefits of Managed Identity

* No Secret Storage
* Automatic Credential Rotation
* Improved Security
* Native Azure Integration

---

# Types of Managed Identity

## System Assigned

Identity belongs to one resource.

Example:

```text
Virtual Machine
```

Delete VM:

```text
Identity Deleted
```

---

## User Assigned

Reusable identity.

Example:

```text
Identity
  ↓
VM1
VM2
App Service
```

---

# Service Principal vs Managed Identity

| Feature             | Service Principal | Managed Identity |
| ------------------- | ----------------- | ---------------- |
| Secret Required     | Yes               | No               |
| Credential Rotation | Manual            | Automatic        |
| Azure Native        | Yes               | Yes              |
| Security            | Good              | Better           |
| Maintenance         | Higher            | Lower            |

---

# Personal Access Tokens (PAT)

## What is PAT?

Personal Access Token is used instead of passwords.

Used For:

* Azure Repos
* API Access
* Automation

---

# Create PAT

Azure DevOps:

```text
User Settings
     ↓
Personal Access Tokens
     ↓
New Token
```

---

# PAT Best Practices

Use:

```text
Least Privilege
```

Example:

```text
Code Read

Code Write
```

Avoid:

```text
Full Access
```

---

# PAT Security Risks

Never:

```text
Store PAT in Git Repository
```

Never:

```text
Hardcode PAT in Pipeline
```

Store in:

* Azure Key Vault
* Secret Variables

---

# Service Connections

## What is Service Connection?

Service Connection allows Azure DevOps to securely connect to external systems.

Examples:

* Azure Subscription
* GitHub
* Docker Hub
* Kubernetes

---

# Service Connection Workflow

```text
Pipeline
   ↓
Service Connection
   ↓
Azure Resources
```

---

# Azure Resource Manager Connection

Most common connection type.

Used For:

* App Service Deployment
* AKS Deployment
* ARM/Bicep Deployment
* Terraform Deployment

---

# Azure Key Vault

## What is Azure Key Vault?

Azure Key Vault is a secure secret management service.

Stores:

* Secrets
* Keys
* Certificates

---

# Why Azure Key Vault?

Without Key Vault:

```text
Password Inside YAML File
```

Security Risk.

---

With Key Vault:

```text
Pipeline
   ↓
Key Vault
   ↓
Secret Retrieval
```

More Secure.

---

# Azure Key Vault Components

## Secrets

Store:

* Passwords
* API Keys
* Connection Strings

Example:

```text
DatabasePassword

StorageKey
```

---

## Keys

Used for:

* Encryption
* Signing

---

## Certificates

Used for:

* HTTPS
* SSL/TLS

---

# Create Azure Key Vault

Azure CLI:

```bash
az keyvault create \
--name my-keyvault \
--resource-group rg-devops \
--location eastus
```

---

# Create Secret

```bash
az keyvault secret set \
--vault-name my-keyvault \
--name db-password \
--value Admin@123
```

---

# View Secret

```bash
az keyvault secret show \
--vault-name my-keyvault \
--name db-password
```

---

# Azure Key Vault Integration with Azure DevOps

Workflow:

```text
Azure Pipeline
      ↓
Service Connection
      ↓
Azure Key Vault
      ↓
Retrieve Secrets
```

---

# Azure Pipeline Task

```yaml
- task: AzureKeyVault@2

  inputs:

    azureSubscription: 'Azure-Service-Connection'

    KeyVaultName: 'my-keyvault'

    SecretsFilter: '*'
```

---

# Key Vault Best Practices

* Enable RBAC
* Enable Soft Delete
* Enable Purge Protection
* Restrict Network Access
* Rotate Secrets Regularly

---

# DevSecOps Security Scanning

Security should be automated.

---

# Static Application Security Testing (SAST)

Scans source code.

Examples:

* CodeQL
* SonarQube
* Checkmarx

---

# Dynamic Application Security Testing (DAST)

Scans running applications.

Examples:

* OWASP ZAP
* Burp Suite

---

# Software Composition Analysis (SCA)

Checks dependencies.

Examples:

* Dependabot
* Snyk

---

# CodeQL

## What is CodeQL?

GitHub's code scanning solution.

Detects:

* SQL Injection
* Cross Site Scripting
* Hardcoded Credentials
* Command Injection

---

# CodeQL Workflow

```text
Source Code
      ↓
CodeQL Scan
      ↓
Security Report
```

---

# GitHub CodeQL Example

```yaml
- uses: github/codeql-action/init@v3
```

---

# Dependabot

## What is Dependabot?

Automatically identifies:

* Vulnerable Packages
* Outdated Dependencies

Example:

```text
Spring Boot 2.6 Vulnerable

Upgrade Recommended
```

---

# Dependabot Benefits

* Automatic Alerts
* Security Updates
* Pull Request Generation

---

# Microsoft Defender for DevOps

## What is Defender for DevOps?

Provides centralized security visibility across DevOps environments.

Supports:

* Azure DevOps
* GitHub
* Azure Resources

---

# Security Features

* Secret Detection
* Vulnerability Management
* IaC Scanning
* Container Security

---

# Secret Scanning

Detects:

```text
Passwords

API Keys

Connection Strings

Tokens
```

inside repositories.

---

# Example Secret Detection

```text
AWS_ACCESS_KEY

GitHub Token

PAT Token
```

Automatically flagged.

---

# Infrastructure Security

Infrastructure as Code security.

Examples:

* Terraform Security Scanning
* Bicep Validation
* ARM Template Validation

Tools:

* Checkov
* tfsec
* Defender for Cloud

---

# Secure Pipeline Design

```text
Repository
    ↓
Build
    ↓
Code Scan
    ↓
Dependency Scan
    ↓
Package
    ↓
Deploy
```

---

# Enterprise Security Pipeline

```text
Pull Request
      ↓
Build Validation
      ↓
CodeQL
      ↓
Dependency Scan
      ↓
Artifact
      ↓
Deploy DEV
      ↓
Approval
      ↓
Deploy PROD
```

---

# Real-World Scenario

Company Requirements:

* No passwords in code
* Automated security scanning
* Secure Azure deployment
* Compliance reporting

Solution:

```text
Azure Key Vault

Managed Identity

CodeQL

Dependabot

Defender for DevOps
```

---

# Hands-On Lab 1

## Create Service Principal

Tasks:

1. Create SPN
2. Assign Contributor Role
3. Test Azure Login

---

# Hands-On Lab 2

## Create Azure Key Vault

Tasks:

1. Create Vault
2. Create Secret
3. Retrieve Secret
4. Configure RBAC

---

# Hands-On Lab 3

## Azure DevOps Key Vault Integration

Tasks:

1. Create Service Connection
2. Connect Key Vault
3. Retrieve Secrets
4. Verify Pipeline

---

# Hands-On Lab 4

## GitHub Security

Tasks:

1. Enable CodeQL
2. Enable Dependabot
3. Run Security Scan
4. Review Findings

---

# Hands-On Lab 5

## Managed Identity

Tasks:

1. Create VM
2. Enable Managed Identity
3. Connect Key Vault
4. Retrieve Secret Securely

---

# Interview Questions

### Q1. Difference between Authentication and Authorization?

* Authentication = Verify identity.
* Authorization = Verify permissions.

---

### Q2. What is a Service Principal?

A non-human identity used for automation and Azure resource access.

---

### Q3. What is Managed Identity?

Azure-managed identity that eliminates the need for stored credentials.

---

### Q4. Difference between Service Principal and Managed Identity?

Managed Identity provides automatic credential management and is more secure for Azure-native workloads.

---

### Q5. What is Azure Key Vault?

Secure storage service for secrets, keys, and certificates.

---

### Q6. Why use Azure Key Vault in Azure Pipelines?

To securely retrieve secrets during pipeline execution.

---

### Q7. What is PAT?

Personal Access Token used for Azure DevOps authentication.

---

### Q8. What is CodeQL?

GitHub's Static Application Security Testing (SAST) solution.

---

### Q9. What is Dependabot?

Tool that identifies and updates vulnerable dependencies.

---

### Q10. What is DevSecOps?

Practice of integrating security throughout the DevOps lifecycle.

---

# AZ-400 Exam Tips

### Remember Security Hierarchy

```text
Identity
   ↓
Access
   ↓
Secrets
   ↓
Code
   ↓
Infrastructure
```

### Microsoft Recommendations

* Use Managed Identity whenever possible.
* Store secrets in Azure Key Vault.
* Avoid PATs unless required.
* Use OIDC for GitHub authentication.
* Enable CodeQL and Dependabot.
* Implement RBAC instead of Access Policies where possible.

---

# Points to Remember

* Security is a shared responsibility in DevOps.
* Authentication verifies identity; authorization grants permissions.
* Service Principals are commonly used for automation.
* Managed Identities eliminate credential management.
* Azure Key Vault is the preferred solution for secret management.
* PATs should be minimized and securely stored.
* CodeQL provides source code security scanning.
* Dependabot manages dependency vulnerabilities.
* Defender for DevOps centralizes DevSecOps security posture.
* Security, Key Vault, Managed Identity, and Service Principals are among the highest-weighted practical topics in AZ-400 certification. 

# Module 11: Continuous Delivery (CD)

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers Continuous Delivery (CD), Release Management, Deployment Automation, Environment Approvals, Deployment Gates, Release Governance, Azure App Service Deployments, Azure Virtual Machine Deployments, Azure Container Apps, Azure Kubernetes Service (AKS), and Enterprise Release Strategies. 

---

# Introduction to Continuous Delivery

## What is Continuous Delivery?

Continuous Delivery (CD) is the practice of automatically delivering validated application changes to deployment environments.

Workflow:

```text
Code
 ↓
Build
 ↓
Test
 ↓
Artifact
 ↓
Deploy
```

The application is always in a deployable state.

---

# Continuous Integration vs Continuous Delivery

| Continuous Integration | Continuous Delivery    |
| ---------------------- | ---------------------- |
| Build & Test Code      | Deploy Code            |
| Code Validation        | Release Automation     |
| Detect Issues Early    | Deliver Changes Faster |
| Developer Focused      | Operations Focused     |

---

# CI/CD Pipeline

```text
Developer
     ↓
Git Commit
     ↓
Build
     ↓
Unit Test
     ↓
Artifact
     ↓
Deploy DEV
     ↓
Deploy QA
     ↓
Deploy UAT
     ↓
Deploy PROD
```

---

# Benefits of Continuous Delivery

### Faster Releases

Multiple deployments per day.

### Reduced Risk

Small and frequent changes.

### Better Quality

Automated testing before deployment.

### Faster Feedback

Issues detected quickly.

### Consistency

Automated deployment process.

---

# Release Management

## What is Release Management?

Release Management controls how software moves from development to production.

Goals:

* Reliability
* Governance
* Traceability
* Compliance

---

# Release Lifecycle

```text
Build
  ↓
Package
  ↓
Release
  ↓
Approval
  ↓
Deployment
  ↓
Validation
```

---

# Release Components

### Source Code

Application code.

### Build Artifact

Deployable package.

### Environment

Deployment target.

### Approval

Manual or automated validation.

### Deployment

Release execution.

---

# Azure Release Architecture

```text
Azure Repos
      ↓
Azure Pipeline
      ↓
Build Artifact
      ↓
Development
      ↓
QA
      ↓
UAT
      ↓
Production
```

---

# Deployment Environments

## What is an Environment?

Logical deployment target.

Examples:

```text
Development

QA

UAT

Production
```

---

# Environment Purpose

| Environment | Purpose                 |
| ----------- | ----------------------- |
| Development | Developer Testing       |
| QA          | Functional Testing      |
| UAT         | User Acceptance Testing |
| Production  | Live Users              |

---

# Azure DevOps Environments

Create Environment:

```text
Pipelines
   ↓
Environments
   ↓
New Environment
```

Example:

```text
DEV

QA

PROD
```

---

# Deployment Jobs

## What is a Deployment Job?

A specialized Azure Pipeline job designed for deployments.

Example:

```yaml
jobs:

- deployment: DeployWeb
```

Benefits:

* Environment Tracking
* Deployment History
* Approval Support

---

# Environment Approvals

## What are Approvals?

Approvals ensure deployment governance before moving to the next environment.

Workflow:

```text
Build
 ↓
QA Approval
 ↓
UAT Deployment
```

---

# Approval Example

```text
Developer
   ↓
Deploy QA
   ↓
QA Approval
   ↓
Deploy UAT
```

---

# Production Approval Workflow

```text
Build
  ↓
Deploy UAT
  ↓
Manager Approval
  ↓
Deploy Production
```

---

# Benefits of Approvals

* Governance
* Change Control
* Compliance
* Audit Trail

---

# Deployment Gates

## What are Deployment Gates?

Automated checks before deployment.

Examples:

* REST API Check
* Azure Monitor Check
* Work Item Validation
* Security Validation

---

# Gate Workflow

```text
Deployment Request
        ↓
Gate Validation
        ↓
Deployment
```

---

# Example Gate Conditions

```text
No Critical Alerts

Application Healthy

Change Approved
```

---

# Release Governance

## What is Governance?

Controls and policies around deployments.

Objectives:

* Security
* Compliance
* Auditability
* Change Management

---

# Governance Controls

### Approval Checks

### RBAC

### Change Management

### Deployment Policies

### Audit Logs

---

# Deployment Strategies

## Recreate Deployment

Old version removed first.

```text
Old Version
    ↓
Delete
    ↓
Deploy New Version
```

Risk:

Downtime possible.

---

# Rolling Deployment

Gradually updates servers.

```text
Server 1 → Updated

Server 2 → Updated

Server 3 → Updated
```

Benefits:

* Reduced Downtime
* Controlled Deployment

---

# Blue-Green Deployment

Two identical environments.

```text
Blue Environment (Current)

Green Environment (New)
```

Traffic Switch:

```text
Blue
 ↓
Green
```

Benefits:

* Instant Rollback
* Minimal Downtime

---

# Canary Deployment

Deploy to small user percentage first.

```text
5%
 ↓
25%
 ↓
50%
 ↓
100%
```

Benefits:

* Reduced Risk
* Early Validation

---

# Feature Flags

## What are Feature Flags?

Enable or disable functionality without redeployment.

Example:

```text
New Payment Gateway
```

Enabled for:

```text
Internal Users Only
```

Benefits:

* Safer Releases
* Gradual Rollout

---

# Deploying to Azure App Service

## What is Azure App Service?

PaaS service for hosting web applications.

Supports:

* .NET
* Java
* Node.js
* Python
* PHP

---

# Deployment Flow

```text
Pipeline
   ↓
Artifact
   ↓
Azure App Service
```

---

# Azure App Service Deployment Task

```yaml
- task: AzureWebApp@1
  inputs:
    appName: 'webapp-prod'
```

---

# Deploying to Azure Virtual Machines

## VM Deployment

Used when:

* Full OS Control Required
* Legacy Applications
* Custom Middleware

---

# Deployment Flow

```text
Pipeline
   ↓
VM Agent
   ↓
Application Deployment
```

---

# Deploying to Azure Container Apps

## What is Azure Container Apps?

Serverless container platform.

Supports:

* Docker Containers
* Microservices
* APIs

Benefits:

* Auto Scaling
* Reduced Infrastructure Management

---

# Container Apps Deployment

```text
Pipeline
   ↓
Container Registry
   ↓
Container Apps
```

---

# Deploying to Azure Kubernetes Service (AKS)

## What is AKS?

Managed Kubernetes service on Azure.

Used for:

* Containers
* Microservices
* Cloud-Native Applications

---

# AKS Deployment Workflow

```text
Git
 ↓
Build Docker Image
 ↓
Push to ACR
 ↓
Deploy to AKS
```

---

# Kubernetes Deployment Example

```yaml
apiVersion: apps/v1
kind: Deployment

metadata:
  name: webapp
```

---

# Multi-Stage Deployment Pipeline

```text
Build
 ↓
Test
 ↓
Deploy DEV
 ↓
Deploy QA
 ↓
Approval
 ↓
Deploy PROD
```

---

# Enterprise Release Pipeline

```text
Developer
      ↓
Azure Repos
      ↓
Build Pipeline
      ↓
Security Scan
      ↓
Artifact
      ↓
Deploy DEV
      ↓
Automated Tests
      ↓
Deploy QA
      ↓
UAT Approval
      ↓
Deploy PROD
```

---

# Release Best Practices

## Separate Environments

Use:

```text
DEV

QA

UAT

PROD
```

---

## Use Approvals

Mandatory for:

```text
Production Deployments
```

---

## Enable Monitoring

After deployment:

* Azure Monitor
* Application Insights
* Log Analytics

---

## Infrastructure as Code

Use:

* Terraform
* Bicep
* ARM Templates

---

## Secure Secrets

Use:

* Azure Key Vault
* Managed Identity

---

# Hands-On Lab 1

## Create Environment

Tasks:

1. Create DEV Environment
2. Create QA Environment
3. Create PROD Environment

---

# Hands-On Lab 2

## Azure App Service Deployment

Tasks:

1. Create App Service
2. Configure Service Connection
3. Deploy Application
4. Validate Deployment

---

# Hands-On Lab 3

## Multi-Stage Pipeline

Tasks:

1. Build Stage
2. QA Stage
3. Approval Stage
4. Production Stage

---

# Hands-On Lab 4

## Azure Container Apps

Tasks:

1. Build Container Image
2. Push to Registry
3. Deploy Container App

---

# Hands-On Lab 5

## AKS Deployment

Tasks:

1. Create AKS Cluster
2. Push Image to ACR
3. Deploy Application
4. Verify Pods

---

# Real-Time Project

## Enterprise E-Commerce Deployment

Architecture:

```text
Azure Repos
      ↓
Azure Pipeline
      ↓
Build
      ↓
Unit Testing
      ↓
CodeQL Scan
      ↓
Artifact
      ↓
Deploy DEV
      ↓
Deploy QA
      ↓
Approval
      ↓
Deploy PROD
      ↓
Azure Monitor
```

Components:

* Azure Repos
* Azure Pipelines
* Azure Key Vault
* Azure App Service
* AKS
* Azure Monitor

---

# Interview Questions

### Q1. What is Continuous Delivery?

Practice of automatically preparing and deploying validated code changes to environments.

---

### Q2. Difference between Continuous Delivery and Continuous Deployment?

| Continuous Delivery        | Continuous Deployment    |
| -------------------------- | ------------------------ |
| Approval Required          | Fully Automated          |
| Human Validation Possible  | No Human Intervention    |
| More Common in Enterprises | Common in SaaS Companies |

---

### Q3. What are Azure DevOps Environments?

Logical deployment targets used to track deployments and approvals.

---

### Q4. What are Deployment Gates?

Automated validation checks executed before deployment.

---

### Q5. What are Environment Approvals?

Manual or automated approval processes before deployment progresses.

---

### Q6. What is Blue-Green Deployment?

Deployment strategy using two identical environments for near-zero downtime releases.

---

### Q7. What is Canary Deployment?

Gradual rollout strategy deploying changes to a small percentage of users first.

---

### Q8. What are Feature Flags?

Mechanism to enable or disable features without redeploying the application.

---

### Q9. Why use Azure App Service for deployments?

Managed PaaS platform with minimal infrastructure management.

---

### Q10. Why use AKS?

Managed Kubernetes platform for scalable containerized applications.

---

# AZ-400 Exam Tips

### Know Deployment Strategies

* Blue-Green
* Canary
* Rolling
* Recreate

These are frequently tested.

### Understand Approvals vs Gates

| Approvals    | Gates      |
| ------------ | ---------- |
| Manual/Human | Automated  |
| Governance   | Validation |

### Know Deployment Targets

* Azure App Service
* Azure Virtual Machines
* Azure Container Apps
* Azure Kubernetes Service (AKS)

---

# Points to Remember

* Continuous Delivery ensures software is always deployable.
* Azure DevOps Environments provide deployment tracking and governance.
* Approvals and Gates improve deployment safety.
* Blue-Green and Canary are preferred deployment strategies for production.
* Azure App Service is ideal for web applications.
* Azure Container Apps simplify container deployments.
* AKS is the preferred Azure platform for Kubernetes workloads.
* Release Governance is critical in enterprise DevOps.
* Monitoring should always follow deployment.
* Continuous Delivery and Deployment Strategies are high-priority AZ-400 certification topics. 

# Module 12: Deployment Strategies

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers modern deployment strategies including Blue-Green Deployments, Canary Releases, Rolling Deployments, Feature Flags, Rollback Strategies, Zero-Downtime Deployments, Risk Mitigation Techniques, and Enterprise Release Management Practices. 

---

# Introduction to Deployment Strategies

## What is a Deployment Strategy?

A Deployment Strategy defines how a new application version is released to users while minimizing:

* Downtime
* Risk
* Service Disruption
* Failed Releases

---

# Why Deployment Strategies Matter

Traditional Deployment:

```text
Version 1
    ↓
Stop Application
    ↓
Deploy Version 2
    ↓
Start Application
```

Problems:

* Downtime
* User Impact
* Difficult Rollback

---

Modern Deployment:

```text
Version 1
    ↓
Controlled Release
    ↓
Validation
    ↓
Version 2
```

Benefits:

* High Availability
* Reduced Risk
* Faster Recovery

---

# Deployment Strategy Selection

| Strategy   | Downtime | Risk     | Complexity |
| ---------- | -------- | -------- | ---------- |
| Recreate   | High     | High     | Low        |
| Rolling    | Low      | Medium   | Medium     |
| Blue-Green | Very Low | Low      | Medium     |
| Canary     | Very Low | Very Low | High       |

---

# Recreate Deployment

## What is Recreate Deployment?

The old application is stopped and replaced with a new version.

Workflow:

```text
Version 1
   ↓
Stop
   ↓
Deploy Version 2
   ↓
Start
```

---

# Advantages

* Simple
* Easy Implementation
* Low Cost

---

# Disadvantages

* Downtime
* No Gradual Validation
* Risky for Production

---

# Use Cases

* Development Environment
* Internal Applications
* Small Projects

---

# Rolling Deployment

## What is Rolling Deployment?

Servers are updated one at a time instead of all at once.

Workflow:

```text
Server1 → Updated

Server2 → Updated

Server3 → Updated

Server4 → Updated
```

---

# Rolling Deployment Architecture

```text
Load Balancer
      │
 ┌────┼────┐
 │    │    │
VM1  VM2  VM3
```

Update sequence:

```text
VM1 → VM2 → VM3
```

---

# Advantages

* Minimal Downtime
* Controlled Rollout
* Resource Efficient

---

# Disadvantages

* Multiple Versions Running
* Longer Deployment Time

---

# Kubernetes Rolling Update

Example:

```yaml
strategy:
  type: RollingUpdate
```

---

# Rolling Update Process

```text
Old Pod
   ↓
New Pod
   ↓
Health Check
   ↓
Next Pod
```

---

# Blue-Green Deployment

## What is Blue-Green Deployment?

Two identical environments exist.

### Blue

Current Production

### Green

New Version

---

# Blue-Green Architecture

```text
Users
   ↓
Load Balancer
   ↓
Blue Environment (Live)
Green Environment (Idle)
```

---

# Deployment Process

```text
Deploy Version 2
        ↓
Green Environment
        ↓
Testing
        ↓
Switch Traffic
```

---

# Traffic Switch

Before:

```text
Users
 ↓
Blue
```

After:

```text
Users
 ↓
Green
```

---

# Rollback

If issue occurs:

```text
Green
 ↓
Blue
```

Instant rollback.

---

# Advantages

* Near Zero Downtime
* Fast Rollback
* Safer Releases

---

# Disadvantages

* Double Infrastructure Cost
* Additional Complexity

---

# Azure Blue-Green Example

```text
AppService-Blue

AppService-Green
```

Traffic Routing:

```text
Azure Front Door

Application Gateway

Traffic Manager
```

---

# Canary Deployment

## What is Canary Deployment?

Deploy new version to a small percentage of users first.

---

# Canary Workflow

```text
Version 2
    ↓
5% Users
    ↓
25% Users
    ↓
50% Users
    ↓
100% Users
```

---

# Canary Architecture

```text
Users
   │
 ┌─┴──────┐
 │         │
95%      5%
Old      New
Version  Version
```

---

# Validation Process

Monitor:

* Error Rate
* Response Time
* CPU Usage
* User Feedback

---

# Advantages

* Lowest Risk
* Real User Validation
* Easy Rollback

---

# Disadvantages

* Complex Configuration
* Monitoring Required

---

# Azure Canary Deployment

Services:

* Azure Front Door
* Application Gateway
* AKS
* Azure Container Apps

---

# Kubernetes Canary Example

```yaml
replicas: 10

Old Version: 9 Pods

New Version: 1 Pod
```

Traffic:

```text
90% → Old Version

10% → New Version
```

---

# A/B Testing Deployment

## What is A/B Testing?

Different user groups receive different versions.

Example:

```text
Group A → Old UI

Group B → New UI
```

---

# Benefits

* User Behavior Analysis
* Feature Validation
* Product Optimization

---

# Feature Flags

## What are Feature Flags?

Feature Flags allow functionality to be enabled or disabled without redeployment.

---

# Traditional Deployment

```text
Code Change
     ↓
Build
     ↓
Deploy
```

---

# Feature Flag Deployment

```text
Deploy Code
      ↓
Enable Feature
```

---

# Example

```python
if feature_flag:
    enable_new_checkout()
```

---

# Feature Flag Benefits

* Safer Releases
* Instant Disable
* Gradual Rollout
* Reduced Risk

---

# Feature Flag Workflow

```text
Deploy Feature
      ↓
Hidden
      ↓
Enable for Internal Team
      ↓
Enable for Users
```

---

# Azure App Configuration

Feature flags can be managed through:

Azure App Configuration

Benefits:

* Centralized Configuration
* Dynamic Feature Control
* Integration with Azure Services

---

# Shadow Deployment

## What is Shadow Deployment?

Production traffic is duplicated to a new version.

Users still receive responses from old version.

---

# Shadow Workflow

```text
User Request
      ↓
Old Version
      ↓
Duplicate Traffic
      ↓
New Version
```

---

# Benefits

* Production Testing
* No User Impact
* Performance Validation

---

# Rollback Strategies

## What is Rollback?

Rollback restores previous stable application version.

---

# Manual Rollback

```text
Version 2 Failed
       ↓
Deploy Version 1
```

---

# Automated Rollback

Triggered by:

* Health Check Failure
* High Error Rate
* Failed Deployment

---

# Rollback Workflow

```text
Deploy
  ↓
Health Check
  ↓
Failure
  ↓
Rollback
```

---

# Rollback Triggers

Examples:

```text
Error Rate > 5%

CPU > 90%

Memory Leak

Application Crash
```

---

# Health Checks

Health Checks verify application availability.

Example:

```http
GET /health
```

Response:

```json
{
  "status": "healthy"
}
```

---

# Zero Downtime Deployment

## What is Zero Downtime?

Application remains available during deployment.

Methods:

* Blue-Green
* Canary
* Rolling Deployment

---

# Enterprise Deployment Pipeline

```text
Build
 ↓
Unit Test
 ↓
Security Scan
 ↓
Artifact
 ↓
Deploy DEV
 ↓
Integration Testing
 ↓
Deploy QA
 ↓
Approval
 ↓
Canary Release
 ↓
Production
```

---

# Azure Deployment Strategy Services

| Azure Service        | Strategy          |
| -------------------- | ----------------- |
| Azure App Service    | Blue-Green        |
| AKS                  | Rolling, Canary   |
| Azure Container Apps | Canary            |
| Azure Front Door     | Traffic Splitting |
| Application Gateway  | Blue-Green        |
| Traffic Manager      | Global Routing    |

---

# Monitoring During Deployment

Use:

* Azure Monitor
* Application Insights
* Log Analytics

Monitor:

* Availability
* Response Time
* Exceptions
* User Activity

---

# Deployment Decision Matrix

| Requirement           | Recommended Strategy |
| --------------------- | -------------------- |
| Small Application     | Recreate             |
| Web Application       | Blue-Green           |
| Enterprise Production | Canary               |
| Kubernetes Workload   | Rolling              |
| Feature Validation    | A/B Testing          |
| Zero Downtime         | Blue-Green / Canary  |

---

# Hands-On Lab 1

## Blue-Green Deployment

Tasks:

1. Create Blue Environment
2. Create Green Environment
3. Deploy New Version
4. Switch Traffic
5. Validate Application

---

# Hands-On Lab 2

## Canary Deployment

Tasks:

1. Deploy New Version
2. Route 10% Traffic
3. Monitor Metrics
4. Increase Traffic
5. Complete Rollout

---

# Hands-On Lab 3

## Feature Flags

Tasks:

1. Create Feature Flag
2. Deploy Application
3. Enable Feature
4. Disable Feature
5. Validate Behavior

---

# Hands-On Lab 4

## Rolling Deployment in AKS

Tasks:

1. Create AKS Deployment
2. Update Container Image
3. Observe Rolling Update
4. Validate Pods

---

# Hands-On Lab 5

## Rollback Testing

Tasks:

1. Deploy Faulty Version
2. Trigger Health Check Failure
3. Execute Rollback
4. Verify Recovery

---

# Real-Time Project

## E-Commerce Platform Deployment

Architecture:

```text
Azure Repos
      ↓
Azure Pipeline
      ↓
Build
      ↓
Security Scan
      ↓
Artifact
      ↓
Blue-Green Deployment
      ↓
Azure Front Door
      ↓
Production Users
      ↓
Azure Monitor
```

Features:

* Zero Downtime
* Automated Rollback
* Health Checks
* Traffic Routing

---

# Interview Questions

### Q1. What is Blue-Green Deployment?

A deployment strategy using two identical environments where traffic is switched from the old version to the new version.

---

### Q2. What is Canary Deployment?

A deployment strategy where a new version is released to a small percentage of users before full rollout.

---

### Q3. Difference between Rolling and Blue-Green Deployment?

| Rolling                  | Blue-Green                  |
| ------------------------ | --------------------------- |
| Update Servers Gradually | Switch Between Environments |
| Lower Cost               | Higher Cost                 |
| Slower Rollback          | Instant Rollback            |

---

### Q4. What are Feature Flags?

Mechanism to enable or disable functionality without redeploying the application.

---

### Q5. What is Zero Downtime Deployment?

Deployment approach where users experience no service interruption.

---

### Q6. What is a Rollback Strategy?

Process of restoring a previous stable application version after deployment failure.

---

### Q7. What is Shadow Deployment?

Production traffic is copied to a new version without affecting users.

---

### Q8. Which deployment strategy is best for enterprise production?

Canary Deployment because it minimizes risk through gradual rollout and validation.

---

### Q9. Which Azure services support traffic routing?

* Azure Front Door
* Azure Application Gateway
* Azure Traffic Manager

---

### Q10. Why are health checks important?

They validate application health and enable automated rollback decisions.

---

# AZ-400 Exam Tips

### Know These Deployment Strategies

* Recreate
* Rolling
* Blue-Green
* Canary
* A/B Testing
* Shadow Deployment

### Frequently Tested Scenario

**Requirement:** Zero downtime and quick rollback.

**Answer:** Blue-Green Deployment.

### Frequently Tested Scenario

**Requirement:** Gradually validate a new release with real users.

**Answer:** Canary Deployment.

---

# Points to Remember

* Blue-Green provides near-zero downtime and instant rollback.
* Canary minimizes risk through gradual traffic exposure.
* Rolling Deployments are common in Kubernetes environments.
* Feature Flags separate deployment from feature release.
* Health Checks and Monitoring are critical during deployments.
* Rollback plans should exist for every production deployment.
* Azure Front Door and Application Gateway support advanced deployment strategies.
* Canary and Blue-Green are the most commonly used enterprise deployment models.
* Deployment Strategies are one of the most important real-world and AZ-400 certification topics. 


# Module 13: Infrastructure as Code (IaC)

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers Infrastructure as Code (IaC), Azure CLI, Bicep, Terraform, State Management, Modules, Remote Backends, and CI/CD integration using Azure Pipelines and GitHub Actions. 

---

# Introduction to Infrastructure as Code (IaC)

## What is Infrastructure as Code?

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure through code instead of manual processes.

Traditional Approach:

```text id="6w1m91"
Portal
 ↓
Create VM
 ↓
Create Network
 ↓
Create Storage
```

Problems:

* Time Consuming
* Human Errors
* No Version Control
* Difficult Reproducibility

---

IaC Approach:

```text id="d0qowm"
Code
 ↓
Automation
 ↓
Infrastructure
```

Benefits:

* Automation
* Consistency
* Repeatability
* Version Control

---

# Why Use IaC?

Benefits:

### Automation

Infrastructure creation without manual effort.

### Consistency

Same deployment every time.

### Version Control

Infrastructure stored in Git.

### Faster Deployments

Provision infrastructure within minutes.

### Disaster Recovery

Rebuild infrastructure quickly.

---

# Infrastructure Provisioning Methods

| Method          | Example               |
| --------------- | --------------------- |
| Manual          | Azure Portal          |
| Script Based    | Azure CLI, PowerShell |
| Declarative IaC | Bicep, ARM            |
| Multi-Cloud IaC | Terraform             |

---

# Azure CLI

## What is Azure CLI?

Azure CLI is a command-line tool used to manage Azure resources.

Install:

### Windows

```powershell id="wmw4jv"
winget install Microsoft.AzureCLI
```

---

### macOS

```bash id="8lztm2"
brew update

brew install azure-cli
```

---

### Linux

```bash id="zgrq8f"
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```

---

# Azure Login

```bash id="vtxc59"
az login
```

Verify Subscription:

```bash id="rj6j50"
az account show
```

---

# Create Resource Group

```bash id="vb08cw"
az group create \
--name rg-devops \
--location eastus
```

---

# Create Virtual Machine

```bash id="1iutuh"
az vm create \
--resource-group rg-devops \
--name vm-dev \
--image Ubuntu2204
```

---

# Create Storage Account

```bash id="g1u50a"
az storage account create \
--name devopsstorage01 \
--resource-group rg-devops
```

---

# Advantages of Azure CLI

* Automation Friendly
* Scriptable
* Pipeline Integration
* Cross Platform

---

# Azure CLI in Pipelines

Example:

```yaml id="nl6ggq"
- task: AzureCLI@2
```

Used for:

* Resource Creation
* Configuration Changes
* Deployment Automation

---

# Bicep

## What is Bicep?

Bicep is Microsoft's Infrastructure as Code language for Azure.

Built on top of ARM.

Advantages:

* Simpler Syntax
* Easier Maintenance
* Native Azure Support

---

# Bicep Architecture

```text id="6o0c79"
Bicep File
    ↓
ARM Template
    ↓
Azure Resource Manager
    ↓
Azure Resources
```

---

# Bicep File Extension

```text id="6dwdfo"
.bicep
```

Example:

```text id="0e4q59"
main.bicep
```

---

# First Bicep Template

```bicep id="08xxqv"
resource storage 'Microsoft.Storage/storageAccounts@2023-01-01' = {
  name: 'devopsstorage01'
  location: resourceGroup().location
  sku: {
    name: 'Standard_LRS'
  }
  kind: 'StorageV2'
}
```

---

# Deploy Bicep Template

```bash id="hcc49o"
az deployment group create \
--resource-group rg-devops \
--template-file main.bicep
```

---

# Parameters in Bicep

```bicep id="1rzlm8"
param storageName string
```

Usage:

```bicep id="i2u3ea"
name: storageName
```

---

# Variables in Bicep

```bicep id="26uj6t"
var location = 'eastus'
```

Benefits:

* Reusability
* Consistency

---

# Bicep Modules

## What are Modules?

Reusable infrastructure components.

Example:

```text id="mn5rd5"
network.bicep

storage.bicep

vm.bicep
```

---

# Module Example

```bicep id="u6h5ws"
module storage './storage.bicep' = {
  name: 'storageDeployment'
}
```

---

# Bicep Best Practices

* Use Parameters
* Use Modules
* Avoid Hardcoding
* Store Templates in Git
* Use RBAC

---

# Terraform

## What is Terraform?

Terraform is an open-source Infrastructure as Code tool created by:

HashiCorp

Supports:

* Azure
* AWS
* GCP
* Kubernetes
* VMware

---

# Terraform Architecture

```text id="3ftl06"
Terraform Code
       ↓
Provider
       ↓
Cloud Platform
       ↓
Resources
```

---

# Terraform Workflow

```text id="q0tp7h"
Write Code
    ↓
terraform init
    ↓
terraform plan
    ↓
terraform apply
```

---

# Terraform Files

```text id="1v2x4c"
main.tf

variables.tf

outputs.tf

terraform.tfvars
```

---

# Terraform Configuration Example

```hcl id="6gc1jm"
provider "azurerm" {
  features {}
}

resource "azurerm_resource_group" "rg" {
  name     = "rg-devops"
  location = "East US"
}
```

---

# Terraform Commands

## Initialize

```bash id="uhs9cr"
terraform init
```

Downloads:

* Providers
* Plugins

---

## Validate

```bash id="6yg9ud"
terraform validate
```

Checks syntax.

---

## Plan

```bash id="ks13ut"
terraform plan
```

Shows proposed changes.

---

## Apply

```bash id="es44b9"
terraform apply
```

Creates resources.

---

## Destroy

```bash id="4l34c7"
terraform destroy
```

Deletes resources.

---

# Terraform State

## What is State?

Terraform maintains infrastructure information in:

```text id="gd4e3i"
terraform.tfstate
```

State tracks:

* Resources
* IDs
* Dependencies

---

# Why State is Important?

Terraform compares:

```text id="yho7uw"
Current State

Desired State
```

to determine changes.

---

# Local State

Stored locally.

Example:

```text id="zk4hsh"
terraform.tfstate
```

Problem:

* Team Collaboration Issues

---

# Remote Backend

Stores state remotely.

Recommended for teams.

---

# Azure Storage Backend

Example:

```hcl id="g6kr2w"
backend "azurerm" {
  resource_group_name  = "rg-tfstate"
  storage_account_name = "tfstate001"
  container_name       = "tfstate"
  key                  = "prod.tfstate"
}
```

Benefits:

* Shared State
* State Locking
* Security

---

# Terraform Variables

## Variables

```hcl id="1af8uk"
variable "location" {
  default = "East US"
}
```

Usage:

```hcl id="s4bvvf"
location = var.location
```

---

# Outputs

```hcl id="f8p8t9"
output "vm_ip" {
  value = azurerm_linux_virtual_machine.vm.public_ip_address
}
```

---

# Terraform Modules

## What are Modules?

Reusable Terraform code.

Example:

```text id="iv5n3j"
modules

├── network

├── vm

└── storage
```

---

# Module Usage

```hcl id="vwg9uz"
module "network" {
  source = "./modules/network"
}
```

Benefits:

* Reusability
* Standardization
* Reduced Duplication

---

# Terraform Best Practices

* Use Remote Backend
* Use Modules
* Protect State Files
* Store Code in Git
* Use Variables
* Enable State Locking

---

# Terraform vs Bicep

| Feature          | Terraform | Bicep        |
| ---------------- | --------- | ------------ |
| Vendor           | HashiCorp | Microsoft    |
| Multi-Cloud      | Yes       | No           |
| Azure Native     | No        | Yes          |
| Learning Curve   | Moderate  | Easy         |
| State Management | Required  | Not Required |

---

# IaC Security Best Practices

## Store Code in Git

Version control all infrastructure.

---

## Use Azure Key Vault

Store:

* Passwords
* Secrets
* API Keys

---

## RBAC

Use least privilege principle.

---

## Enable Scanning

Tools:

* Checkov
* tfsec
* Defender for Cloud

---

# Terraform Pipeline Integration

## Azure DevOps Pipeline

```text id="bb6je5"
Git Commit
      ↓
Pipeline
      ↓
Terraform Init
      ↓
Terraform Plan
      ↓
Approval
      ↓
Terraform Apply
```

---

# Terraform Pipeline Example

```yaml id="fzd9u8"
steps:

- script: terraform init

- script: terraform plan

- script: terraform apply -auto-approve
```

---

# Bicep Pipeline Integration

```text id="jxf90k"
Git Commit
      ↓
Pipeline
      ↓
Validate Bicep
      ↓
Deploy Resources
```

---

# Bicep Pipeline Example

```yaml id="vzg3oe"
- task: AzureCLI@2

  inputs:

    scriptType: bash

    inlineScript: |
      az deployment group create \
      --resource-group rg-devops \
      --template-file main.bicep
```

---

# Enterprise IaC Workflow

```text id="qug5r5"
Developer
      ↓
Git Repository
      ↓
Pull Request
      ↓
Code Review
      ↓
Terraform Plan
      ↓
Approval
      ↓
Terraform Apply
      ↓
Azure Infrastructure
```

---

# Hands-On Lab 1

## Azure CLI

Tasks:

1. Install Azure CLI
2. Login to Azure
3. Create Resource Group
4. Create VM

---

# Hands-On Lab 2

## Bicep

Tasks:

1. Create Bicep Template
2. Add Parameters
3. Deploy Storage Account
4. Validate Deployment

---

# Hands-On Lab 3

## Terraform

Tasks:

1. Install Terraform
2. Create Resource Group
3. Run Init
4. Run Plan
5. Run Apply

---

# Hands-On Lab 4

## Remote Backend

Tasks:

1. Create Storage Account
2. Configure Backend
3. Migrate State
4. Verify Remote State

---

# Hands-On Lab 5

## Pipeline Integration

Tasks:

1. Create Azure DevOps Pipeline
2. Execute Terraform Plan
3. Add Approval
4. Execute Apply

---

# Real-Time Project

## Azure Infrastructure Deployment Platform

Components:

```text id="rfavsy"
Azure Repos
      ↓
Azure Pipeline
      ↓
Terraform
      ↓
Resource Groups
      ↓
VNet
      ↓
VMs
      ↓
Storage
      ↓
Key Vault
```

---

# Interview Questions

### Q1. What is Infrastructure as Code?

Managing and provisioning infrastructure using code instead of manual processes.

---

### Q2. What is Azure CLI?

Command-line tool used to manage Azure resources.

---

### Q3. What is Bicep?

Microsoft's Infrastructure as Code language for Azure.

---

### Q4. What is Terraform?

Open-source multi-cloud Infrastructure as Code tool from HashiCorp.

---

### Q5. What is Terraform State?

File that tracks deployed infrastructure resources.

---

### Q6. Why use Remote Backend?

To securely share Terraform state across teams.

---

### Q7. What are Terraform Modules?

Reusable infrastructure components.

---

### Q8. Difference between Bicep and Terraform?

* Bicep = Azure Native
* Terraform = Multi-Cloud

---

### Q9. Why use Terraform Plan?

To preview infrastructure changes before applying them.

---

### Q10. What is State Locking?

Mechanism preventing multiple users from modifying Terraform state simultaneously.

---

# AZ-400 Exam Tips

### Choose Bicep When:

* Azure-only environment
* Native Azure integration
* Simpler syntax required

### Choose Terraform When:

* Multi-cloud environment
* Standardized infrastructure across providers
* Enterprise automation platform

### Remember Terraform Workflow

```text id="wt3mgb"
Init
 ↓
Validate
 ↓
Plan
 ↓
Apply
```

---

# Points to Remember

* IaC enables automated, repeatable infrastructure deployments.
* Azure CLI is useful for scripting and automation.
* Bicep is Microsoft's preferred Azure-native IaC language.
* Terraform is the most widely used multi-cloud IaC tool.
* Remote Backends are mandatory for team-based Terraform projects.
* Modules improve reusability and maintainability.
* Store all infrastructure code in Git repositories.
* Use Key Vault for secrets and credentials.
* Implement approvals before production infrastructure changes.
* IaC, Terraform, Bicep, State Management, and Pipeline Integration are among the most important practical and AZ-400 certification topics. 


# Module 14: Testing & Quality Management

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers Azure Test Plans, Software Testing Fundamentals, Quality Assurance, Test Automation, Quality Gates, Code Coverage, Build Validation, Release Gates, and Enterprise Testing Practices. 

---

# Introduction to Testing

## What is Software Testing?

Software Testing is the process of verifying and validating that an application works as expected and meets business requirements.

Objectives:

* Detect Defects
* Improve Quality
* Verify Functionality
* Reduce Production Issues
* Improve Customer Satisfaction

---

# Why Testing is Important

Without Testing:

```text id="2tx3rb"
Code
 ↓
Production
 ↓
Failure
```

Problems:

* Bugs
* Downtime
* Customer Impact
* Revenue Loss

---

With Testing:

```text id="cv3x64"
Code
 ↓
Testing
 ↓
Validation
 ↓
Production
```

Benefits:

* Improved Reliability
* Better User Experience
* Reduced Risk

---

# Quality Assurance (QA)

## What is QA?

Quality Assurance focuses on preventing defects by improving development processes.

QA Activities:

* Requirement Reviews
* Test Planning
* Process Improvement
* Quality Standards

---

# Quality Control (QC)

## What is QC?

Quality Control focuses on identifying defects in the product.

Examples:

* Testing
* Code Review
* Validation

---

# QA vs QC

| QA               | QC               |
| ---------------- | ---------------- |
| Process Oriented | Product Oriented |
| Prevent Defects  | Detect Defects   |
| Proactive        | Reactive         |

---

# Testing Lifecycle

```text id="l9v8ga"
Requirements
      ↓
Test Planning
      ↓
Test Design
      ↓
Test Execution
      ↓
Defect Reporting
      ↓
Retesting
      ↓
Closure
```

---

# Azure Test Plans

## What is Azure Test Plans?

Azure Test Plans is a testing management service within Azure DevOps.

Used For:

* Test Case Management
* Manual Testing
* Exploratory Testing
* User Acceptance Testing (UAT)

---

# Azure Test Plans Components

```text id="p9wz1u"
Test Plan
    ↓
Test Suite
    ↓
Test Cases
```

---

# Test Plan

A Test Plan is a collection of testing activities.

Example:

```text id="h4dw7u"
E-Commerce Testing Plan
```

Contains:

* Functional Tests
* Regression Tests
* UAT Tests

---

# Test Suite

Logical grouping of test cases.

Examples:

```text id="cf3w7m"
Login Module

Payment Module

Order Module
```

---

# Test Case

A specific validation scenario.

Example:

```text id="w9ik6c"
Verify user login with valid credentials
```

---

# Creating a Test Plan

Steps:

1. Azure DevOps
2. Test Plans
3. New Test Plan
4. Create Test Suites
5. Add Test Cases

---

# Test Case Example

## Test Case ID: TC-001

### Scenario

Login Functionality

### Preconditions

User Account Exists

### Test Steps

```text id="o76w0m"
1. Open Login Page

2. Enter Username

3. Enter Password

4. Click Login
```

### Expected Result

```text id="g06j9f"
User successfully logged in
```

---

# Manual Testing

## What is Manual Testing?

Testing performed manually by testers.

Examples:

* UI Testing
* Exploratory Testing
* UAT

---

# Advantages

* Human Observation
* Better User Experience Validation

---

# Limitations

* Time Consuming
* Repetitive
* Not Scalable

---

# Exploratory Testing

## What is Exploratory Testing?

Testing without predefined scripts.

Purpose:

* Discover Hidden Issues
* Validate User Experience

---

# Automated Testing

## What is Automated Testing?

Testing executed automatically using tools and scripts.

Examples:

* Unit Tests
* API Tests
* Integration Tests

---

# Automated Testing Workflow

```text id="g33jtv"
Code
 ↓
Build
 ↓
Automated Tests
 ↓
Results
```

---

# Types of Testing

---

# Unit Testing

## What is Unit Testing?

Testing individual components or functions.

Example:

```python id="txr2yb"
def add(a,b):
    return a+b
```

Unit Test:

```python id="q4l9xy"
assert add(2,3) == 5
```

---

# Unit Testing Characteristics

* Fast
* Developer Owned
* Runs During Build

---

# Integration Testing

## What is Integration Testing?

Validates interaction between components.

Example:

```text id="z8fywo"
Application
      ↓
Database
```

Tests communication.

---

# Functional Testing

## What is Functional Testing?

Verifies business requirements.

Example:

```text id="v15o8t"
Login Functionality

Checkout Process

Order Placement
```

---

# Regression Testing

## What is Regression Testing?

Ensures new changes do not break existing functionality.

Example:

```text id="qsv2lq"
New Payment Feature Added
```

Verify:

```text id="bn7h5t"
Login Still Works

Checkout Still Works
```

---

# User Acceptance Testing (UAT)

## What is UAT?

Testing performed by business users.

Goal:

```text id="u2z4tv"
Validate Business Requirements
```

---

# Performance Testing

## What is Performance Testing?

Measures application behavior under load.

Metrics:

* Response Time
* Throughput
* Scalability

Tools:

* JMeter
* LoadRunner

---

# Security Testing

## What is Security Testing?

Identifies vulnerabilities.

Checks:

* Authentication
* Authorization
* Data Protection

Tools:

* OWASP ZAP
* Burp Suite
* CodeQL

---

# Test Automation in CI/CD

Testing should be integrated into pipelines.

Workflow:

```text id="lg5y9t"
Commit
 ↓
Build
 ↓
Unit Tests
 ↓
Integration Tests
 ↓
Package
```

---

# Example Azure Pipeline

```yaml id="kq1cme"
steps:

- script: pytest

- script: npm test
```

---

# Build Validation

## What is Build Validation?

Ensures code passes quality checks before merge.

Workflow:

```text id="gkr57m"
Pull Request
      ↓
Build
      ↓
Tests
      ↓
Success
      ↓
Merge
```

---

# Benefits

* Prevents Broken Code
* Improves Quality
* Reduces Production Issues

---

# Code Coverage

## What is Code Coverage?

Measures how much code is tested.

Formula:

Code\ Coverage=\frac{Lines\ Tested}{Total\ Lines}\times100

Example:

```text id="4iz0sa"
80%
```

coverage means:

```text id="7wz1yb"
80% of code tested
```

---

# Code Coverage Targets

| Project Type           | Recommended Coverage |
| ---------------------- | -------------------- |
| Small Project          | 60%                  |
| Enterprise Application | 80%+                 |
| Critical Systems       | 90%+                 |

---

# Quality Gates

## What are Quality Gates?

Quality Gates are conditions that must pass before deployment.

Examples:

```text id="jpbxhj"
Code Coverage > 80%

No Critical Vulnerabilities

All Tests Passed
```

---

# Quality Gate Workflow

```text id="3fz55f"
Build
 ↓
Quality Gate
 ↓
Deploy
```

---

# Common Quality Gates

### Build Success

```text id="y0k0pk"
Build = Successful
```

### Unit Tests

```text id="yivg2l"
All Tests Passed
```

### Code Coverage

```text id="6a07ns"
Coverage > 80%
```

### Security Scan

```text id="cyquzv"
No Critical Issues
```

---

# Release Gates

## What are Release Gates?

Checks performed before deployment to production.

Examples:

* Azure Monitor Validation
* Work Item Validation
* Security Checks
* REST API Validation

---

# Release Gate Workflow

```text id="ck4ezz"
Deployment Request
       ↓
Gate Validation
       ↓
Production Deployment
```

---

# Test Metrics

Important Metrics:

### Test Pass Rate

Formula:

Pass\ Rate=\frac{Passed\ Tests}{Total\ Tests}\times100

---

### Defect Density

Measures defects per module.

---

### Defect Leakage

Defects found after production release.

---

# Enterprise Testing Strategy

```text id="n7e8bg"
Developer
     ↓
Unit Testing
     ↓
CI Pipeline
     ↓
Integration Testing
     ↓
QA Testing
     ↓
UAT
     ↓
Production
```

---

# Real-World Scenario

## E-Commerce Application

Testing Layers:

```text id="e2m2u0"
Unit Tests
      ↓
API Tests
      ↓
UI Tests
      ↓
Security Tests
      ↓
UAT
```

Tools:

* Azure Test Plans
* Selenium
* JUnit
* PyTest
* CodeQL

---

# Hands-On Lab 1

## Azure Test Plans

Tasks:

1. Create Test Plan
2. Create Test Suite
3. Create Test Cases
4. Execute Tests

---

# Hands-On Lab 2

## Manual Testing

Tasks:

1. Login Testing
2. Checkout Testing
3. Defect Reporting

---

# Hands-On Lab 3

## Automated Testing

Tasks:

1. Create Unit Tests
2. Run Tests in Pipeline
3. Generate Reports

---

# Hands-On Lab 4

## Code Coverage

Tasks:

1. Enable Coverage
2. Execute Tests
3. Review Coverage Report

---

# Hands-On Lab 5

## Quality Gates

Tasks:

1. Configure Coverage Threshold
2. Configure Build Validation
3. Configure Security Validation

---

# Interview Questions

### Q1. What is Azure Test Plans?

A testing management service within Azure DevOps used for manual and exploratory testing.

---

### Q2. Difference between QA and QC?

* QA = Prevent Defects
* QC = Detect Defects

---

### Q3. What is Unit Testing?

Testing individual functions or components.

---

### Q4. What is Regression Testing?

Testing existing functionality after new changes.

---

### Q5. What is UAT?

User Acceptance Testing performed by business users.

---

### Q6. What is Code Coverage?

Metric that measures how much code is tested.

---

### Q7. What are Quality Gates?

Conditions that must pass before deployment.

---

### Q8. What is Build Validation?

Automated verification before code merge.

---

### Q9. Difference between Quality Gates and Release Gates?

| Quality Gates | Release Gates          |
| ------------- | ---------------------- |
| Build Level   | Deployment Level       |
| Code Quality  | Environment Validation |

---

### Q10. Why integrate testing into CI/CD?

To detect issues early and improve release quality.

---

# AZ-400 Exam Tips

### Testing Pyramid

```text id="w7ybpr"
UI Tests
   ↑
Integration Tests
   ↑
Unit Tests
```

Most tests should be Unit Tests.

### Remember Quality Gate Examples

* Code Coverage
* Build Success
* Security Scan
* Test Pass Rate

### Testing Order

```text id="ocryvk"
Unit
 ↓
Integration
 ↓
Functional
 ↓
UAT
```

---

# Points to Remember

* Azure Test Plans supports manual and exploratory testing.
* QA prevents defects; QC identifies defects.
* Unit Testing is the foundation of automated testing.
* Regression Testing protects existing functionality.
* Code Coverage measures testing effectiveness.
* Quality Gates prevent low-quality code from progressing.
* Release Gates validate deployment readiness.
* Testing should be integrated into CI/CD pipelines.
* Automated testing reduces release risk and improves reliability.
* Testing, Quality Gates, Code Coverage, and Build Validation are important AZ-400 certification topics. 

# Module 15: Monitoring & Observability

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module covers Azure Monitor, Log Analytics, Application Insights, Kusto Query Language (KQL), Alerting, Observability, Performance Monitoring, Distributed Tracing, and Enterprise Monitoring Strategies. 

---

# Introduction to Monitoring & Observability

## What is Monitoring?

Monitoring is the process of collecting and analyzing system data to understand the health and performance of applications and infrastructure.

Examples:

* CPU Utilization
* Memory Usage
* Disk Usage
* Application Response Time
* Network Traffic

---

# What is Observability?

Observability goes beyond monitoring.

It helps answer:

```text id="j3p0mz"
Why did the issue occur?
```

instead of only:

```text id="3t0czr"
What failed?
```

---

# Monitoring vs Observability

| Monitoring      | Observability           |
| --------------- | ----------------------- |
| Detect Problems | Explain Problems        |
| Metrics Focused | Metrics + Logs + Traces |
| Reactive        | Proactive               |
| Alerting        | Root Cause Analysis     |

---

# Three Pillars of Observability

```text id="uy40b4"
Metrics
   ↓
Logs
   ↓
Traces
```

---

# Metrics

Numerical measurements collected over time.

Examples:

* CPU %
* Memory %
* Request Count
* Response Time

---

# Logs

Detailed records of events.

Example:

```text id="0ep2si"
Application Started

User Login Successful

Database Connection Failed
```

---

# Traces

Track requests across multiple services.

Example:

```text id="1u3zh2"
Frontend
   ↓
API
   ↓
Database
```

---

# Azure Monitor

## What is Azure Monitor?

Azure Monitor is Azure's centralized monitoring service.

Used for:

* Infrastructure Monitoring
* Application Monitoring
* Alerting
* Analytics

---

# Azure Monitor Architecture

```text id="9g3l6k"
Azure Resources
       ↓
Azure Monitor
       ↓
Metrics
Logs
Alerts
Dashboards
```

---

# Azure Monitor Components

### Metrics

Performance data.

### Logs

Detailed operational data.

### Alerts

Notifications.

### Dashboards

Visualization.

### Workbooks

Interactive reports.

---

# Azure Monitor Metrics

## What are Metrics?

Performance measurements collected automatically.

Examples:

| Metric                 | Description         |
| ---------------------- | ------------------- |
| Percentage CPU         | CPU Utilization     |
| Available Memory Bytes | Free Memory         |
| Network In Total       | Incoming Traffic    |
| Network Out Total      | Outgoing Traffic    |
| Disk Read Bytes        | Storage Performance |

---

# Metric Collection

```text id="5vhr3u"
Virtual Machine
      ↓
Metrics
      ↓
Azure Monitor
```

---

# Common VM Metrics

### CPU Utilization

Monitor server load.

### Memory Usage

Monitor resource consumption.

### Disk Usage

Monitor storage availability.

### Network Usage

Monitor traffic patterns.

---

# Azure Monitor Alerts

## What are Alerts?

Alerts notify teams when specific conditions occur.

Example:

```text id="8f3qby"
CPU > 80%
```

---

# Alert Workflow

```text id="38uh2h"
Metric
   ↓
Threshold
   ↓
Alert
   ↓
Notification
```

---

# Alert Types

### Metric Alerts

Based on metrics.

Example:

```text id="jqup3w"
CPU > 80%
```

---

### Log Alerts

Based on KQL queries.

Example:

```text id="yng3f6"
Failed Login Attempts > 5
```

---

### Activity Log Alerts

Monitor Azure events.

Examples:

```text id="98ldg0"
VM Deleted

Role Assigned

Resource Created
```

---

# Action Groups

## What is an Action Group?

Action Groups define what happens when an alert fires.

Examples:

* Email
* SMS
* Push Notification
* Webhook
* Azure Function

---

# Alert Architecture

```text id="gaxey3"
Metric
  ↓
Alert Rule
  ↓
Action Group
  ↓
Email / SMS
```

---

# Create Alert

Steps:

1. Azure Monitor
2. Alerts
3. Create Alert Rule
4. Select Resource
5. Configure Threshold
6. Assign Action Group

---

# Log Analytics Workspace

## What is Log Analytics?

Log Analytics stores and analyzes log data.

Used For:

* Troubleshooting
* Security Analysis
* Operational Monitoring

---

# Log Analytics Architecture

```text id="zibzbt"
Azure Resources
       ↓
Log Analytics Workspace
       ↓
KQL Queries
```

---

# Data Sources

Examples:

* Virtual Machines
* Azure App Service
* AKS
* Azure Firewall
* Azure Monitor Agent

---

# Log Collection

```text id="z5gx6j"
Application
      ↓
Logs
      ↓
Log Analytics
```

---

# Common Log Types

### Security Logs

Authentication events.

### Application Logs

Application activities.

### System Logs

Operating system events.

### Audit Logs

Administrative actions.

---

# Kusto Query Language (KQL)

## What is KQL?

Kusto Query Language is used to query Azure logs.

Example:

```kusto id="8qhhho"
Heartbeat
| take 10
```

Shows 10 records.

---

# View Virtual Machines

```kusto id="wb2wsi"
Heartbeat
| summarize count() by Computer
```

---

# Error Logs

```kusto id="93hkzj"
AppTraces
| where SeverityLevel >= 3
```

---

# Sort Results

```kusto id="tux5v6"
Heartbeat
| order by TimeGenerated desc
```

---

# Filter Data

```kusto id="e2hjw8"
Heartbeat
| where Computer == "webserver01"
```

---

# Summarize Data

```kusto id="7gw0d4"
Heartbeat
| summarize count() by Computer
```

---

# Application Insights

## What is Application Insights?

Application Insights is Azure's Application Performance Monitoring (APM) solution.

Used For:

* Application Monitoring
* Performance Analysis
* Error Tracking
* Distributed Tracing

---

# Application Insights Architecture

```text id="ks8eje"
Application
      ↓
Application Insights SDK
      ↓
Telemetry
      ↓
Azure Monitor
```

---

# Telemetry Data

Collected Automatically:

* Requests
* Exceptions
* Dependencies
* Performance Counters

---

# Request Monitoring

Example:

```text id="m2m3my"
GET /login

Response Time: 150ms
```

---

# Exception Monitoring

Tracks:

```text id="30kg3x"
Application Errors

Unhandled Exceptions
```

---

# Dependency Tracking

Tracks external services.

Example:

```text id="jyjlwm"
Web App
   ↓
SQL Database
   ↓
Storage Account
```

---

# Live Metrics

Real-time monitoring.

Shows:

* Request Rate
* CPU Usage
* Failed Requests
* Response Time

---

# Distributed Tracing

## What is Distributed Tracing?

Tracks requests across microservices.

Example:

```text id="zyz5x3"
Frontend
    ↓
API Gateway
    ↓
Service A
    ↓
Database
```

---

# Trace Example

```text id="44uwba"
Request ID: 123

Frontend: 20ms

API: 50ms

Database: 200ms
```

Root cause identified quickly.

---

# Monitoring AKS

Monitor:

* Nodes
* Pods
* Containers

Metrics:

```text id="q2o27u"
CPU

Memory

Restart Count

Pod Status
```

---

# Monitoring App Services

Monitor:

* Requests
* Errors
* Response Time
* Availability

---

# Workbooks

## What are Workbooks?

Interactive dashboards used for visualization.

Benefits:

* Rich Reporting
* Custom Monitoring Views
* Troubleshooting

---

# Dashboard Example

```text id="z0krt3"
CPU Usage

Memory Usage

Response Time

Error Rate
```

---

# Enterprise Monitoring Strategy

```text id="d09tq8"
Infrastructure
       ↓
Azure Monitor
       ↓
Log Analytics
       ↓
Application Insights
       ↓
Alerts
       ↓
Operations Team
```

---

# Monitoring Best Practices

## Enable Alerts

Monitor:

* CPU
* Memory
* Availability

---

## Centralize Logs

Store logs in Log Analytics.

---

## Use Application Insights

Monitor application performance.

---

## Monitor Business Metrics

Examples:

* Orders Per Minute
* Login Success Rate
* Revenue Metrics

---

## Configure Dashboards

Create operational visibility.

---

# Real-Time Scenario

## E-Commerce Application

Monitor:

```text id="w0ml5x"
Web Application

API

Database

AKS Cluster
```

Metrics:

```text id="wb0c6r"
CPU

Memory

Request Rate

Response Time

Error Rate
```

Alerts:

```text id="0b5jlwm"
CPU > 80%

Availability < 99%

Response Time > 2 Seconds
```

---

# Hands-On Lab 1

## Azure Monitor

Tasks:

1. Create VM
2. Enable Monitoring
3. View Metrics
4. Create Dashboard

---

# Hands-On Lab 2

## Alert Configuration

Tasks:

1. Create CPU Alert
2. Create Action Group
3. Trigger Alert
4. Verify Notification

---

# Hands-On Lab 3

## Log Analytics

Tasks:

1. Create Workspace
2. Connect VM
3. Generate Logs
4. Run KQL Queries

---

# Hands-On Lab 4

## Application Insights

Tasks:

1. Create Web Application
2. Enable Application Insights
3. Generate Traffic
4. Analyze Telemetry

---

# Hands-On Lab 5

## KQL Queries

Tasks:

1. Query Heartbeat Logs
2. Query Errors
3. Create Alert Rule
4. Create Workbook

---

# Real-Time Project

## Enterprise Monitoring Platform

Architecture:

```text id="xw6r9y"
Azure Resources
       ↓
Azure Monitor
       ↓
Log Analytics
       ↓
Application Insights
       ↓
KQL
       ↓
Alerts
       ↓
Dashboard
```

Services:

* Azure Virtual Machines
* Azure App Services
* AKS
* Azure SQL Database

---

# Interview Questions

### Q1. What is Azure Monitor?

Azure's centralized monitoring and observability platform.

---

### Q2. What are the three pillars of observability?

* Metrics
* Logs
* Traces

---

### Q3. What is Log Analytics?

Service used to store and query Azure log data.

---

### Q4. What is KQL?

Kusto Query Language used to query logs in Azure Monitor and Log Analytics.

---

### Q5. What is Application Insights?

Application Performance Monitoring (APM) service for monitoring applications.

---

### Q6. What is an Action Group?

Collection of notification actions executed when alerts trigger.

---

### Q7. What is Distributed Tracing?

Tracking requests across multiple services to identify bottlenecks and failures.

---

### Q8. Difference between Metrics and Logs?

| Metrics             | Logs                    |
| ------------------- | ----------------------- |
| Numerical Data      | Detailed Events         |
| Lightweight         | Detailed Analysis       |
| Performance Focused | Troubleshooting Focused |

---

### Q9. What is Live Metrics?

Real-time monitoring view provided by Application Insights.

---

### Q10. Why is observability important?

It helps identify, troubleshoot, and resolve issues quickly in complex distributed systems.

---

# AZ-400 Exam Tips

### Remember Azure Monitoring Stack

```text id="4o0vsl"
Azure Monitor
     ↓
Log Analytics
     ↓
Application Insights
```

### Most Common Metrics

* Percentage CPU
* Available Memory Bytes
* Network In Total
* Network Out Total
* Disk Usage

### Common KQL Commands

```kusto
where
summarize
project
order by
take
```

### Frequently Tested Topics

* Azure Monitor
* Log Analytics
* Application Insights
* Alerts
* Action Groups
* KQL Queries
* Distributed Tracing

---

# Points to Remember

* Monitoring tells you what happened; observability helps explain why.
* Azure Monitor is the central monitoring platform.
* Log Analytics stores and analyzes logs using KQL.
* Application Insights provides application-level monitoring and APM.
* Alerts proactively notify operations teams.
* Action Groups define alert responses.
* Distributed Tracing is critical for microservices and AKS environments.
* Metrics, Logs, and Traces form the foundation of observability.
* Monitoring should be integrated into every production deployment.
* Azure Monitor, Log Analytics, Application Insights, and KQL are key AZ-400 certification and real-world DevOps topics. 


# Module 16: Capstone Project – Enterprise Azure DevOps CI/CD Platform

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This capstone project combines all concepts learned throughout the course including Azure Boards, Azure Repos, GitHub, Azure Pipelines, GitHub Actions, Azure Artifacts, Azure Key Vault, Terraform, Bicep, Azure Monitor, Application Insights, and DevSecOps practices. 

---

# Project Overview

## Project Title

**Enterprise Azure DevOps CI/CD Platform**

---

## Project Objective

Design and implement an end-to-end DevOps platform capable of:

* Planning Agile Work
* Managing Source Code
* Building Applications
* Running Automated Tests
* Managing Artifacts
* Deploying Infrastructure
* Deploying Applications
* Implementing Security
* Monitoring Production Workloads

---

# Business Scenario

A company wants to modernize application delivery using Azure DevOps and GitHub.

Current Problems:

* Manual Deployments
* No CI/CD
* No Source Control Governance
* No Centralized Secrets Management
* Limited Monitoring
* Slow Release Cycles

Required Solution:

```text
Automated CI/CD Platform
        ↓
Infrastructure as Code
        ↓
Secure Deployments
        ↓
Continuous Monitoring
```

---

# Project Architecture

```text
Azure Boards
      ↓
Azure Repos / GitHub
      ↓
Pull Request
      ↓
Azure Pipelines
      ↓
Code Quality Checks
      ↓
Azure Artifacts
      ↓
Terraform / Bicep
      ↓
Azure Infrastructure
      ↓
Application Deployment
      ↓
Azure Monitor
      ↓
Application Insights
```

---

# Project Components

## Component 1 – Agile Planning

Using Azure Boards:

### Create

* Epic
* Features
* User Stories
* Tasks

Example:

```text
Epic
 └─ Cloud Native E-Commerce Platform

Feature
 └─ User Authentication

User Story
 └─ User Login

Task
 └─ Build Login API
```

---

# Component 2 – Source Control

Using:

* Azure Repos
* GitHub

Repository Structure:

```text
project
│
├── src
├── tests
├── terraform
├── bicep
├── pipelines
└── docs
```

---

# Branching Strategy

```text
main
│
develop
│
├── feature-login
├── feature-payment
└── feature-cart
```

---

# Component 3 – Pull Request Workflow

Requirements:

* Minimum 2 Reviewers
* Build Validation
* Linked Work Item
* Branch Protection

Workflow:

```text
Feature Branch
      ↓
Pull Request
      ↓
Review
      ↓
Build Validation
      ↓
Merge
```

---

# Component 4 – Continuous Integration

Azure Pipeline:

```text
Code Commit
      ↓
Build
      ↓
Unit Test
      ↓
Code Quality Scan
      ↓
Artifact
```

---

# YAML Pipeline Structure

```yaml
trigger:
- main

stages:
- Build

- Test

- Publish
```

---

# Component 5 – Package Management

Using Azure Artifacts.

Create:

```text
Enterprise Feed
```

Store:

* npm Packages
* Python Packages
* Universal Packages

---

# Component 6 – DevSecOps

Security Controls:

### Azure Key Vault

Store:

* Database Passwords
* API Keys
* Connection Strings

---

### CodeQL

Perform:

* SAST Scanning
* Security Analysis

---

### Dependabot

Perform:

* Dependency Analysis
* Vulnerability Detection

---

# Component 7 – Infrastructure as Code

Infrastructure deployed using:

* Terraform
* Bicep

---

# Terraform Resources

Create:

```text
Resource Group

Virtual Network

Subnet

Virtual Machine

Storage Account

Key Vault
```

---

# Terraform Workflow

```text
terraform init
      ↓
terraform plan
      ↓
Approval
      ↓
terraform apply
```

---

# Bicep Resources

Create:

```text
App Service

Storage Account

Key Vault
```

---

# Component 8 – Continuous Delivery

Deployment Targets:

### Azure App Service

Deploy Web Application.

---

### Azure Container Apps

Deploy Containerized Workloads.

---

### Azure Kubernetes Service (AKS)

Deploy Microservices.

---

# Multi-Stage Pipeline

```text
Build
 ↓
DEV
 ↓
QA
 ↓
UAT
 ↓
PROD
```

---

# Environment Approvals

```text
DEV → Automatic

QA → Automatic

UAT → Manual

PROD → Management Approval
```

---

# Component 9 – Deployment Strategy

Implement:

### Blue-Green Deployment

```text
Blue → Current

Green → New
```

---

### Canary Deployment

```text
10%
 ↓
50%
 ↓
100%
```

---

# Rollback Strategy

Automatic rollback when:

```text
Application Unhealthy

Deployment Failure

High Error Rate
```

---

# Component 10 – Monitoring

Enable:

### Azure Monitor

Collect:

* CPU
* Memory
* Disk
* Network

---

### Application Insights

Monitor:

* Response Time
* Exceptions
* User Activity

---

### Log Analytics

Store:

* Application Logs
* System Logs
* Security Logs

---

# Alerting Strategy

Create Alerts:

```text
CPU > 80%

Availability < 99%

Response Time > 2 Seconds

Disk Usage > 85%
```

---

# KQL Dashboard Queries

Example:

```kusto
Heartbeat
| summarize count() by Computer
```

---

# Project Deliverables

Students must submit:

## Azure DevOps

* Organization
* Project
* Boards
* Pipelines

---

## GitHub

* Repository
* Branch Protection
* Pull Requests

---

## Infrastructure

* Terraform Code
* Bicep Templates

---

## Security

* Key Vault Integration
* Service Connection
* CodeQL Report

---

## Deployment

* Working CI/CD Pipeline
* Multi-Stage Deployment
* Blue-Green Deployment

---

## Monitoring

* Azure Monitor Dashboard
* Application Insights
* Alert Rules

---

# Success Criteria

The project is considered successful if:

✅ Code stored in GitHub/Azure Repos

✅ Pull Requests implemented

✅ CI Pipeline working

✅ Artifacts generated

✅ Terraform deployment successful

✅ Application deployed automatically

✅ Key Vault integrated

✅ Monitoring configured

✅ Alerts configured

✅ Documentation completed

---

# Real-World Enterprise Architecture

```text
Developers
      ↓
GitHub
      ↓
Azure Pipelines
      ↓
CodeQL
      ↓
Azure Artifacts
      ↓
Terraform
      ↓
Azure Infrastructure
      ↓
App Service / AKS
      ↓
Azure Monitor
      ↓
Application Insights
```

---

# Interview Questions

### Q1. Why is Infrastructure as Code important?

Provides repeatable, automated, and version-controlled infrastructure deployments.

---

### Q2. Why use Azure Key Vault?

To securely manage secrets, keys, and certificates.

---

### Q3. What are the benefits of CI/CD?

* Faster Releases
* Improved Quality
* Reduced Manual Effort
* Better Reliability

---

### Q4. What is the purpose of Azure Artifacts?

Centralized package and dependency management.

---

### Q5. Why use Blue-Green Deployment?

Near-zero downtime and quick rollback.

---

### Q6. What is the role of Azure Monitor?

Monitoring infrastructure and application health.

---

### Q7. What are the benefits of Terraform?

Multi-cloud Infrastructure as Code automation.

---

### Q8. Why use Pull Requests?

Code review, governance, and quality control.

---

### Q9. What is DevSecOps?

Integrating security throughout the software delivery lifecycle.

---

### Q10. What are the three pillars of observability?

* Metrics
* Logs
* Traces

---

# Final AZ-400 Course Outcome

After completing all modules and this capstone project, participants will be able to:

* Design Enterprise DevOps Solutions
* Implement CI/CD Pipelines
* Manage GitHub and Azure Repos
* Implement DevSecOps Practices
* Deploy Infrastructure using Terraform and Bicep
* Manage Azure Key Vault and Secrets
* Deploy Applications to Azure
* Implement Monitoring and Observability
* Design Blue-Green and Canary Deployments
* Successfully prepare for the AZ-400 Certification Exam. 

# Module 17: AZ-400 Certification Preparation & Exam Readiness

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module is designed to help learners prepare for the AZ-400 certification exam through exam-focused concepts, scenario-based learning, mock questions, architecture discussions, troubleshooting exercises, and certification strategies. 

---

# AZ-400 Certification Overview

## Certification Name

**AZ-400: Designing and Implementing Microsoft DevOps Solutions**

Certification Earned:

**Microsoft Certified: DevOps Engineer Expert**

---

# Certification Path

```text
AZ-900 (Optional)
      ↓
AZ-104 or AZ-204
      ↓
AZ-400
      ↓
DevOps Engineer Expert
```

---

# Target Audience

* DevOps Engineers
* Cloud Engineers
* Platform Engineers
* Site Reliability Engineers (SRE)
* Azure Administrators
* Software Engineers
* Release Engineers
* Automation Engineers

---

# Skills Measured

The AZ-400 exam typically focuses on the following domains:

| Domain                                         | Approx Weight |
| ---------------------------------------------- | ------------- |
| Configure Processes and Communications         | 10-15%        |
| Design and Implement Source Control            | 15-20%        |
| Design and Implement Build & Release Pipelines | 40-45%        |
| Develop Security and Compliance Plan           | 10-15%        |
| Implement Instrumentation Strategy             | 10-15%        |

---

# Exam Format

| Item          | Details              |
| ------------- | -------------------- |
| Exam Code     | AZ-400               |
| Level         | Expert               |
| Questions     | 40–60                |
| Duration      | ~100–120 Minutes     |
| Passing Score | 700/1000             |
| Exam Type     | Scenario Based       |
| Delivery      | Online / Test Center |

---

# AZ-400 Exam Mindset

The exam tests:

❌ Command Memorization

✅ Architecture Decisions

✅ Best Practices

✅ DevOps Design

✅ Security Implementation

✅ CI/CD Scenarios

---

# Exam Blueprint Summary

```text
Azure Boards
      ↓
GitHub / Azure Repos
      ↓
Azure Pipelines
      ↓
Azure Artifacts
      ↓
Azure Key Vault
      ↓
Terraform / Bicep
      ↓
Deployment Strategies
      ↓
Azure Monitor
```

---

# Domain 1: Configure Processes & Communications

Topics:

### Agile Planning

* Epics
* Features
* User Stories
* Sprint Planning

### Azure Boards

* Queries
* Dashboards
* Analytics Views

### Collaboration

* Wiki
* Notifications
* Work Item Linking

---

# Exam Scenario

Requirement:

```text
Track work from requirement to deployment.
```

Answer:

```text
Azure Boards + Work Item Traceability
```

---

# Domain 2: Design & Implement Source Control

Topics:

### Git

* Branches
* Merge
* Rebase
* Cherry Pick

### Pull Requests

* Reviews
* Policies

### Branch Protection

* Build Validation
* Required Reviewers

---

# Exam Scenario

Requirement:

```text
Prevent direct commits to production branch.
```

Answer:

```text
Branch Policies
+
Pull Requests
```

---

# Domain 3: Build & Release Pipelines

Highest-weighted domain.

---

# Azure Pipelines

Topics:

* YAML Pipelines
* Multi-Stage Pipelines
* Templates
* Variables
* Artifacts

---

# GitHub Actions

Topics:

* Workflows
* Secrets
* OIDC
* Runners

---

# Azure Artifacts

Topics:

* Feeds
* Packages
* Upstream Sources

---

# Deployment Targets

* Azure App Service
* AKS
* Container Apps
* Virtual Machines

---

# Exam Scenario

Requirement:

```text
Deploy to QA automatically
but Production after approval.
```

Answer:

```text
Environment Approvals
```

---

# Domain 4: Security & Compliance

Topics:

### Azure Key Vault

* Secrets
* Certificates
* Keys

### Managed Identity

### Service Principal

### PAT

### CodeQL

### Dependabot

### Defender for DevOps

---

# Exam Scenario

Requirement:

```text
Remove passwords from pipeline.
```

Answer:

```text
Azure Key Vault
+
Managed Identity
```

---

# Domain 5: Monitoring & Observability

Topics:

### Azure Monitor

### Log Analytics

### Application Insights

### KQL

### Alerts

### Action Groups

---

# Exam Scenario

Requirement:

```text
Monitor request latency
across multiple microservices.
```

Answer:

```text
Application Insights
+
Distributed Tracing
```

---

# Most Important Services for AZ-400

| Service              | Importance |
| -------------------- | ---------- |
| Azure Pipelines      | ⭐⭐⭐⭐⭐      |
| GitHub Actions       | ⭐⭐⭐⭐⭐      |
| Azure Repos          | ⭐⭐⭐⭐⭐      |
| Azure Boards         | ⭐⭐⭐⭐       |
| Azure Key Vault      | ⭐⭐⭐⭐⭐      |
| Azure Monitor        | ⭐⭐⭐⭐⭐      |
| Application Insights | ⭐⭐⭐⭐⭐      |
| Terraform            | ⭐⭐⭐⭐⭐      |
| Bicep                | ⭐⭐⭐⭐       |
| Azure Artifacts      | ⭐⭐⭐⭐       |

---

# High-Frequency Exam Topics

## CI/CD

* YAML Pipelines
* Multi-Stage Pipelines
* Build Validation
* Release Gates

---

## Security

* Managed Identity
* Service Principal
* Azure Key Vault
* OIDC Authentication

---

## Source Control

* GitFlow
* Trunk-Based Development
* Branch Policies
* Pull Requests

---

## Deployment Strategies

* Blue-Green
* Canary
* Rolling Deployment
* Feature Flags

---

## Monitoring

* Azure Monitor
* Application Insights
* KQL
* Alerts

---

# Architecture Decision Questions

Example:

### Scenario

Application deployed on AKS.

Requirement:

```text
Zero downtime deployment
with quick rollback.
```

Answer:

```text
Blue-Green Deployment
```

---

### Scenario

Requirement:

```text
Gradually release
new feature to users.
```

Answer:

```text
Canary Deployment
```

---

### Scenario

Requirement:

```text
Store database passwords securely.
```

Answer:

```text
Azure Key Vault
```

---

# Troubleshooting Scenarios

## Pipeline Failure

Check:

```text
Agent Logs

Pipeline Logs

Service Connection

Permissions
```

---

## Deployment Failure

Check:

```text
Application Logs

App Service Logs

AKS Events

Kubernetes Pods
```

---

## Terraform Failure

Check:

```text
terraform validate

terraform plan

State File

Provider Version
```

---

## Key Vault Access Failure

Check:

```text
RBAC

Managed Identity

Service Principal

Access Permissions
```

---

# Mock Questions

### Question 1

Requirement:

```text
Store secrets securely for Azure Pipeline.
```

Options:

A. Variable

B. Git Repository

C. Azure Key Vault

D. Wiki

✅ Answer:

```text
Azure Key Vault
```

---

### Question 2

Requirement:

```text
Deploy to production
after manager approval.
```

✅ Answer:

```text
Environment Approval
```

---

### Question 3

Requirement:

```text
Protect main branch from direct commits.
```

✅ Answer:

```text
Branch Policies
```

---

### Question 4

Requirement:

```text
Monitor distributed microservices.
```

✅ Answer:

```text
Application Insights
```

---

### Question 5

Requirement:

```text
Reuse infrastructure code across projects.
```

✅ Answer:

```text
Terraform Modules
```

---

# Practical Lab Revision Checklist

## Azure Boards

* Create Epic
* Create Sprint
* Create Dashboard

---

## Azure Repos

* Create Branch
* Create Pull Request
* Configure Branch Policy

---

## Azure Pipelines

* Create YAML Pipeline
* Publish Artifact
* Multi-Stage Deployment

---

## GitHub Actions

* Workflow Creation
* Secrets
* OIDC

---

## Azure Key Vault

* Create Vault
* Create Secret
* Pipeline Integration

---

## Terraform

* Init
* Plan
* Apply
* Remote Backend

---

## Monitoring

* Azure Monitor
* KQL
* Alerts
* Application Insights

---

# AZ-400 Interview Questions

### Q1. Difference between CI and CD?

CI validates code changes; CD automates deployments.

---

### Q2. Why use Azure Key Vault?

To securely manage secrets and credentials.

---

### Q3. Difference between Managed Identity and Service Principal?

Managed Identity automatically manages credentials; Service Principal requires manual credential management.

---

### Q4. What are Azure DevOps Environments?

Logical deployment targets supporting approvals and deployment tracking.

---

### Q5. Difference between Blue-Green and Canary Deployment?

Blue-Green switches entire traffic; Canary gradually shifts traffic.

---

### Q6. Why use Terraform Remote Backend?

To securely store and share state files.

---

### Q7. What are Quality Gates?

Conditions that must pass before code progresses.

---

### Q8. What are Release Gates?

Deployment validation checks before release.

---

### Q9. What is Distributed Tracing?

Tracking requests across multiple services.

---

### Q10. Why use GitHub Actions OIDC?

Provides secure passwordless authentication.

---

# AZ-400 Exam Strategy

## First Pass

Answer:

* Easy Questions
* Direct Knowledge Questions

---

## Second Pass

Answer:

* Scenario-Based Questions

---

## Final Pass

Review:

* Marked Questions
* Architecture Decisions

---

# Last Week Revision Plan

| Day   | Topics                     |
| ----- | -------------------------- |
| Day 1 | Azure Boards + Repos       |
| Day 2 | Git + GitHub               |
| Day 3 | Azure Pipelines            |
| Day 4 | GitHub Actions             |
| Day 5 | Azure Key Vault + Security |
| Day 6 | Terraform + Bicep          |
| Day 7 | Azure Monitor + Mock Exam  |

---

# Final AZ-400 Success Checklist

✅ Azure Boards

✅ Git & GitHub

✅ Azure Repos

✅ Azure Pipelines

✅ GitHub Actions

✅ Azure Artifacts

✅ Azure Key Vault

✅ Service Connections

✅ Managed Identity

✅ Terraform

✅ Bicep

✅ Blue-Green Deployment

✅ Canary Deployment

✅ Azure Monitor

✅ Application Insights

✅ KQL Queries

✅ Capstone Project Completed

---

# Course Completion Outcome

After completing all 17 modules, hands-on labs, and the capstone project, participants will be able to:

* Design Enterprise DevOps Architectures
* Implement End-to-End CI/CD Pipelines
* Manage GitHub and Azure DevOps Repositories
* Implement DevSecOps Controls
* Deploy Infrastructure using Terraform and Bicep
* Secure Pipelines using Key Vault and Managed Identities
* Implement Monitoring and Observability
* Troubleshoot DevOps Platforms
* Successfully clear the AZ-400 Certification Exam
* Work as an Azure DevOps Engineer, Platform Engineer, SRE, or Cloud DevOps Architect. 

---

## Complete Course Summary

```text
Module 1  - Cloud, Azure & DevOps Fundamentals
Module 2  - Linux & Git Fundamentals
Module 3  - Azure DevOps Fundamentals
Module 4  - Azure Boards
Module 5  - Git & Branching Strategies
Module 6  - Azure Repos & GitHub
Module 7  - Azure Pipelines
Module 8  - GitHub Actions
Module 9  - Azure Artifacts
Module 10 - Security & Azure Key Vault
Module 11 - Continuous Delivery
Module 12 - Deployment Strategies
Module 13 - Infrastructure as Code
Module 14 - Testing & Quality Management
Module 15 - Monitoring & Observability
Module 16 - Enterprise Capstone Project
Module 17 - AZ-400 Certification Preparation
```

This completes the full AZ-400 (50 Hours / 3 Months Weekend Batch) course curriculum. 



# Module 18: Real-World DevOps Scenarios, Troubleshooting & Mock Interviews

Part of AZ-400: Designing and Implementing Microsoft DevOps Solutions. This module focuses on real-world enterprise DevOps scenarios, troubleshooting techniques, production support, incident management, root cause analysis (RCA), architecture discussions, and mock interview preparation.

---

# Module Objective

By the end of this module, learners will be able to:

* Troubleshoot Azure DevOps Pipelines
* Debug CI/CD Failures
* Resolve Git Issues
* Troubleshoot Terraform Deployments
* Resolve Azure Key Vault Access Problems
* Troubleshoot AKS Deployments
* Analyze Production Incidents
* Perform Root Cause Analysis (RCA)
* Handle Real-Time DevOps Scenarios
* Crack Azure DevOps Interviews

---

# Real-World DevOps Lifecycle

```text
Requirement
     ↓
Development
     ↓
Git Commit
     ↓
CI Pipeline
     ↓
Testing
     ↓
Artifact
     ↓
Deployment
     ↓
Monitoring
     ↓
Incident Management
```

---

# Scenario 1: Azure Pipeline Failed

## Problem

Pipeline suddenly fails during deployment.

Error:

```text
Deployment Failed
Unauthorized Access
```

---

## Investigation

Check:

```text
Pipeline Logs
Service Connection
Agent Logs
Azure Activity Logs
```

---

## Possible Causes

* Expired Service Principal Secret
* Missing RBAC Permission
* Deleted Resource Group
* Invalid Subscription

---

## Resolution

```text
Validate Service Connection

Validate Azure Subscription

Validate RBAC Roles

Re-run Pipeline
```

---

# Scenario 2: Azure Key Vault Access Denied

## Error

```text
Caller is not authorized
```

---

## Investigation

Check:

```text
RBAC Assignment

Managed Identity

Service Principal

Key Vault Permissions
```

---

## Solution

Assign:

```text
Key Vault Secrets User

Key Vault Secrets Officer
```

Verify:

```bash
az role assignment list
```

---

# Scenario 3: Terraform Apply Failure

## Error

```text
Resource Already Exists
```

---

## Investigation

```bash
terraform state list
```

Check:

```text
State File

Azure Resources

Provider Configuration
```

---

## Resolution

Import Existing Resource:

```bash
terraform import
```

---

# Scenario 4: Terraform State Corruption

## Symptoms

```text
Infrastructure Exists

Terraform Doesn't Know
```

---

## Resolution

Use Remote Backend.

Store State In:

```text
Azure Storage Account
```

Enable:

```text
State Locking
Versioning
Backup
```

---

# Scenario 5: AKS Deployment Failure

## Error

```text
CrashLoopBackOff
```

---

## Investigation

Check Pods:

```bash
kubectl get pods
```

Describe Pod:

```bash
kubectl describe pod pod-name
```

Logs:

```bash
kubectl logs pod-name
```

---

## Common Causes

* Application Crash
* Missing Environment Variable
* Invalid Image
* Database Connectivity Issue

---

# Scenario 6: ImagePullBackOff

## Error

```text
Failed to pull image
```

---

## Investigation

Check:

```bash
kubectl describe pod
```

---

## Common Causes

```text
Wrong Image Name

Missing Registry Credentials

Deleted Container Image
```

---

# Scenario 7: Azure App Service Down

## Symptoms

```text
502 Error

503 Error
```

---

## Investigation

Check:

```text
App Service Logs

Application Insights

Availability Metrics
```

---

## Resolution

```text
Restart Application

Scale Instance

Review Deployment Changes
```

---

# Scenario 8: Production Outage

## Situation

Application unavailable.

---

# Incident Process

```text
Alert
 ↓
Incident
 ↓
Investigation
 ↓
Mitigation
 ↓
RCA
 ↓
Prevention
```

---

# Priority Matrix

| Priority | Description                |
| -------- | -------------------------- |
| P1       | Production Down            |
| P2       | Major Functionality Impact |
| P3       | Minor Issue                |
| P4       | Enhancement                |

---

# Root Cause Analysis (RCA)

## What is RCA?

Root Cause Analysis identifies the actual cause of a problem.

---

# RCA Structure

```text
Issue

Impact

Timeline

Root Cause

Resolution

Preventive Action
```

---

# Example RCA

## Issue

Website unavailable.

---

## Root Cause

```text
Certificate Expired
```

---

## Resolution

```text
Renew SSL Certificate
```

---

## Prevention

```text
Certificate Expiry Alert
```

---

# Scenario 9: Git Merge Conflict

## Problem

```text
Merge Conflict
```

---

## Investigation

```bash
git status
```

Files:

```text
<<<<<<< HEAD
=======
>>>>>>> branch
```

---

## Resolution

```bash
git add .

git commit
```

---

# Scenario 10: Pull Request Blocked

## Error

```text
Build Validation Failed
```

---

## Investigation

Check:

```text
Unit Tests

SonarQube

Code Coverage
```

---

## Resolution

Fix Build Failure and Re-submit PR.

---

# Scenario 11: High CPU Usage

## Alert

```text
CPU > 90%
```

---

## Investigation

Azure VM:

```bash
top

htop
```

---

Azure Monitor:

```text
CPU Metrics
```

---

## Resolution

```text
Scale Up

Scale Out

Optimize Application
```

---

# Scenario 12: High Memory Usage

## Investigation

Linux:

```bash
free -m

top
```

---

Application:

```text
Memory Leak

Cache Issue
```

---

## Resolution

```text
Restart Service

Optimize Application
```

---

# Scenario 13: Slow Application

## Investigation

Use:

* Application Insights
* Azure Monitor
* KQL Queries

---

## Check

```text
Database Queries

API Response Time

External Dependencies
```

---

# Scenario 14: Kubernetes Node Not Ready

Check:

```bash
kubectl get nodes
```

---

Describe Node:

```bash
kubectl describe node node-name
```

---

Common Causes:

* Disk Full
* Memory Exhausted
* Network Failure

---

# Scenario 15: Service Connection Failure

## Error

```text
Failed to obtain access token
```

---

## Resolution

Check:

```text
Client ID

Tenant ID

Client Secret

Subscription Access
```

---

# Monitoring Troubleshooting Flow

```text
Alert
 ↓
Azure Monitor
 ↓
Log Analytics
 ↓
KQL
 ↓
Root Cause
```

---

# Important KQL Queries

## VM Availability

```kusto
Heartbeat
| summarize count() by Computer
```

---

## Errors

```kusto
AppExceptions
| take 20
```

---

## Failed Requests

```kusto
requests
| where success == false
```

---

# Production Deployment Checklist

Before Deployment:

✅ Backup Available

✅ Rollback Plan Ready

✅ Approval Completed

✅ Monitoring Enabled

✅ Key Vault Verified

---

After Deployment:

✅ Smoke Testing

✅ Health Check

✅ Metrics Validation

✅ Error Monitoring

---

# Azure DevOps Mock Interview

### Q1. Difference between CI and CD?

CI validates code changes while CD automates deployments.

---

### Q2. Why use Azure Key Vault?

To securely store secrets, keys, and certificates.

---

### Q3. Difference between Managed Identity and Service Principal?

Managed Identity automatically manages credentials, while Service Principal requires manual management.

---

### Q4. What is Blue-Green Deployment?

Two identical environments where traffic switches from old to new version.

---

### Q5. What is Canary Deployment?

Gradual rollout to a subset of users before full deployment.

---

### Q6. How do you troubleshoot a failed pipeline?

Check:

* Pipeline Logs
* Service Connections
* Agent Logs
* Resource Permissions

---

### Q7. How do you secure Terraform State?

Store remotely in Azure Storage Account with RBAC and state locking.

---

### Q8. What is Application Insights?

Azure APM solution for monitoring application performance and failures.

---

### Q9. What is KQL?

Kusto Query Language used to query Azure Monitor and Log Analytics data.

---

### Q10. What is the difference between Monitoring and Observability?

Monitoring tells what happened; Observability helps determine why it happened.

---

# Hands-On Troubleshooting Lab

## Lab 1: Pipeline Failure

Tasks:

1. Break Pipeline
2. Analyze Logs
3. Fix Issue
4. Re-run Pipeline

---

## Lab 2: Terraform Failure

Tasks:

1. Create Terraform Error
2. Run Plan
3. Troubleshoot
4. Deploy Successfully

---

## Lab 3: AKS Failure

Tasks:

1. Deploy Broken Application
2. Check Pod Status
3. Review Logs
4. Fix Deployment

---

## Lab 4: Key Vault Access Issue

Tasks:

1. Remove Permission
2. Trigger Pipeline Failure
3. Assign RBAC
4. Validate Success

---

## Lab 5: Monitoring & RCA

Tasks:

1. Generate Alert
2. Investigate Logs
3. Perform RCA
4. Create Prevention Plan

---

# Enterprise DevOps Engineer Checklist

A successful Azure DevOps Engineer should be able to:

✅ Design CI/CD Pipelines

✅ Implement Git Branching Strategies

✅ Manage Azure DevOps & GitHub

✅ Deploy Infrastructure with Terraform

✅ Implement DevSecOps Controls

✅ Configure Azure Key Vault

✅ Deploy to App Service & AKS

✅ Implement Monitoring & Alerting

✅ Troubleshoot Production Issues

✅ Lead Incident Response & RCA

---

# Course Completion Outcome

After completing Modules 1–18, learners will have:

* End-to-End Azure DevOps Knowledge
* Real Production Troubleshooting Experience
* Enterprise CI/CD Implementation Skills
* Infrastructure Automation Expertise
* DevSecOps Knowledge
* Monitoring & Observability Skills
* AZ-400 Certification Readiness
* Azure DevOps Interview Readiness

---

# Final Project Presentation

Each learner should present:

```text
Azure Boards
     ↓
Azure Repos/GitHub
     ↓
Azure Pipelines
     ↓
Terraform/Bicep
     ↓
Azure Key Vault
     ↓
Deployment Strategy
     ↓
Azure Monitor
     ↓
Incident Response
```

This module serves as the bridge between certification knowledge and real-world Azure DevOps Engineer responsibilities in enterprise environments.




