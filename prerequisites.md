# Prerequisites to Learn Azure DevOps

You do **not need to be an expert developer**, but having the following knowledge will make Azure DevOps much easier to learn.

## 1. Operating System Basics (Mandatory)

* Linux fundamentals

  * File management
  * Permissions (`chmod`, `chown`)
  * Process management
  * Systemd services
  * Package management (`apt`, `yum`)
* Basic Windows Server administration

### Practice Commands

```bash
ls
cd
pwd
mkdir
rm
cp
mv
chmod
chown
ps
top
systemctl
```

---

## 2. Git & Version Control (Mandatory)

Azure DevOps heavily relies on Git.

### Topics

* Git repositories
* Commit
* Push
* Pull
* Clone
* Branching
* Merge
* Pull Requests

### Practice Commands

```bash
git init
git clone
git add .
git commit -m "Initial Commit"
git push
git pull
git checkout -b dev
git merge
```

---

## 3. Basic Networking (Important)

### Topics

* IP Address
* CIDR
* DNS
* HTTP/HTTPS
* Load Balancer
* Firewall
* Ports

### Common Ports

| Service | Port |
| ------- | ---- |
| SSH     | 22   |
| HTTP    | 80   |
| HTTPS   | 443  |
| RDP     | 3389 |
| MySQL   | 3306 |

---

## 4. Cloud Fundamentals (Mandatory)

Learn Azure basics before Azure DevOps.

### Azure Services

* Microsoft Azure Resource Groups
* Virtual Machines
* Storage Accounts
* Virtual Networks
* Azure Monitor
* Azure App Services
* Azure Key Vault

### Certification

* AZ-900 (Recommended)

---

## 5. Scripting Knowledge (Important)

### PowerShell

```powershell
Get-Process
Get-Service
New-Item
```

### Bash

```bash
for i in {1..5}
do
echo $i
done
```

---

## 6. Programming Basics (Recommended)

You should understand:

* Variables
* Loops
* Functions
* Conditions

### Languages

* Python (Recommended)
* PowerShell
* C#
* JavaScript (Optional)

Example:

```python
for i in range(5):
    print(i)
```

---

## 7. CI/CD Concepts (Very Important)

### Understand:

* Continuous Integration (CI)
* Continuous Delivery (CD)
* Continuous Deployment
* Build Pipeline
* Release Pipeline
* Artifact Repository

### Flow

```text
Developer
   ↓
Git Repository
   ↓
Build Pipeline
   ↓
Testing
   ↓
Artifact
   ↓
Deployment
   ↓
Production
```

---

## 8. Containers (Recommended)

### Learn Docker

* Images
* Containers
* Dockerfile
* Docker Hub
* Volumes
* Networks

Commands:

```bash
docker build
docker run
docker ps
docker logs
docker exec
```

---

## 9. Infrastructure as Code (Recommended)

### Tools

* Terraform
* Bicep
* ARM Templates

Example:

```hcl
resource "azurerm_resource_group" "rg" {
  name     = "dev-rg"
  location = "Central India"
}
```

---

## 10. Azure DevOps Services (Core Learning)

Learn:

* Azure DevOps Organizations
* Projects
* Azure Repos
* Azure Pipelines
* Azure Boards
* Azure Artifacts
* Azure Test Plans
* Service Connections
* Agent Pools
* Self-Hosted Agents

---

## 11. Kubernetes (Advanced)

After Azure DevOps basics:

### Topics

* Pods
* Deployments
* Services
* Ingress
* ConfigMaps
* Secrets

### Azure Service

* Azure Kubernetes Service (AKS)

---

# Recommended Learning Path (30 Days)

### Week 1

* Linux Basics
* Git & GitHub
* Networking Basics

### Week 2

* Azure Fundamentals (AZ-900)
* PowerShell & Bash
* Python Basics

### Week 3

* Docker
* CI/CD Concepts
* Azure DevOps Repos & Pipelines

### Week 4

* Terraform
* Azure DevOps YAML Pipelines
* AKS Basics
* End-to-End Azure DevOps Project

# Ideal Profile Before Starting Azure DevOps

✅ Linux Basics
✅ Git & GitHub
✅ Networking Basics
✅ Azure Fundamentals (AZ-900)
✅ Bash/PowerShell Scripting
✅ Basic Python
✅ Docker Basics

Once you are comfortable with these topics, you can move directly to **AZ-400 Azure DevOps Engineer Expert** preparation and real-world DevOps projects.
