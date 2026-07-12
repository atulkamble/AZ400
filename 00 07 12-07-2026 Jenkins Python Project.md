# DevOps CI/CD Pipeline and Azure Backup Notes

## 1. Introduction

A **pipeline** is an automated sequence of steps used to build, test, package, release, and deploy an application.

In DevOps, a pipeline helps teams:

- Detect code changes automatically
- Compile or validate application code
- Install dependencies
- Run tests
- Build artifacts or Docker images
- Push images to a container registry
- Deploy applications
- Perform health checks
- Notify teams about success or failure

---

## 2. Common CI/CD Platforms

| Platform | Pipeline File | Main Use |
|---|---|---|
| Jenkins | `Jenkinsfile` | Open-source, self-managed CI/CD automation |
| Azure DevOps | `azure-pipelines.yml` | Microsoft Azure-based CI/CD and project management |
| GitHub Actions | `.github/workflows/<name>.yml` | GitHub-native workflow automation |
| GitLab CI/CD | `.gitlab-ci.yml` | GitLab-native CI/CD automation |

---

## 3. CI and CD

### Continuous Integration — CI

Continuous Integration automatically validates code whenever developers push or merge changes.

Typical CI stages:

```text
Code Push
   ↓
Checkout
   ↓
Install Dependencies
   ↓
Code Validation
   ↓
Unit Testing
   ↓
Docker Build
   ↓
Docker Image Test
```

### Continuous Delivery

Continuous Delivery ensures the application is always ready for deployment, but production deployment may require manual approval.

### Continuous Deployment

Continuous Deployment automatically deploys every successfully tested change to the target environment.

```text
Continuous Integration
        ↓
Publish Artifact/Image
        ↓
Deploy to Development
        ↓
Deploy to Testing
        ↓
Approval
        ↓
Deploy to Production
```

---

## 4. Pipeline Trigger

A **trigger** starts the pipeline when a specified event occurs.

Common triggers:

- Code push
- Pull request
- Merge request
- Scheduled time
- Manual execution
- Webhook event
- Tag creation
- Release creation
- Completion of another pipeline

---

## 5. Jenkins Pipeline

Jenkins is an open-source automation server commonly used for CI/CD.

### Jenkins Pipeline File

The Jenkins pipeline is defined in:

```text
Jenkinsfile
```

### Jenkins Declarative Pipeline Structure

```groovy
pipeline {
    agent any

    environment {
        APP_NAME = 'flask-app'
    }

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing application...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }

        failure {
            echo 'Pipeline failed.'
        }
    }
}
```

### Important Jenkins Pipeline Components

| Component | Purpose |
|---|---|
| `pipeline` | Defines the complete pipeline |
| `agent` | Defines where the pipeline runs |
| `environment` | Stores pipeline environment variables |
| `options` | Configures timeout, timestamps, concurrency, and retention |
| `triggers` | Defines automatic pipeline execution |
| `stages` | Groups pipeline activities |
| `stage` | Represents one logical pipeline phase |
| `steps` | Contains commands executed in a stage |
| `post` | Runs actions after success, failure, or completion |

---

## 6. Jenkins Pipeline Project

### Repository

```text
https://github.com/atulkamble/jenkins-git-python-pipeline
```

### Clone Repository

```bash
git clone https://github.com/atulkamble/jenkins-git-python-pipeline.git
cd jenkins-git-python-pipeline
```

### Main Jenkins Pipeline Flow

```text
GitHub Push
    ↓
Jenkins Trigger
    ↓
Checkout Source Code
    ↓
Check Python Version
    ↓
Create Virtual Environment
    ↓
Install Dependencies
    ↓
Run Tests
    ↓
Validate Python Code
    ↓
Build Docker Image
    ↓
Run Docker Smoke Test
    ↓
Push Image to Docker Hub
    ↓
Deploy Docker Container
    ↓
Application Health Check
    ↓
Network Validation
```

### Important Environment Variables

```groovy
environment {
    APP_NAME        = 'flask-app'
    VENV_DIR        = 'venv'
    APP_PORT        = '5000'

    DOCKER_IMAGE    = 'atuljkamble/flask-pipeline-app'
    DOCKER_TAG      = "build-${BUILD_NUMBER}"
    DOCKER_LATEST   = 'latest'
    DOCKER_CREDS_ID = 'docker-creds'
    CONTAINER_NAME  = 'flask-pipeline-app'
}
```

### Docker Image Tagging Strategy

Each Jenkins build creates two image tags:

```text
atuljkamble/flask-pipeline-app:build-85
atuljkamble/flask-pipeline-app:latest
```

Benefits:

- `build-85` provides traceability and rollback.
- `latest` points to the most recently published version.
- Jenkins `BUILD_NUMBER` creates a unique version for every build.

---

## 7. Jenkins Trigger Using GitHub Webhook

### Jenkins Job Setting

Enable:

```text
GitHub hook trigger for GITScm polling
```

### GitHub Webhook URL

```text
http://<JENKINS-PUBLIC-IP>:8080/github-webhook/
```

### GitHub Configuration

Go to:

```text
GitHub Repository
→ Settings
→ Webhooks
→ Add webhook
```

Configure:

| Field | Value |
|---|---|
| Payload URL | `http://<JENKINS-IP>:8080/github-webhook/` |
| Content type | `application/json` |
| Event | Push events |
| Active | Enabled |

### Trigger Flow

```text
Developer
   ↓ git push
GitHub Repository
   ↓ webhook
Jenkins
   ↓
Pipeline Execution
```

---

## 8. Jenkins Docker Hub Credentials

Create Docker Hub credentials in Jenkins:

```text
Manage Jenkins
→ Credentials
→ System
→ Global credentials
→ Add Credentials
```

Use:

| Field | Value |
|---|---|
| Kind | Username with password |
| Username | Docker Hub username |
| Password | Docker Hub password or access token |
| ID | `docker-creds` |

The Jenkinsfile accesses the credentials using:

```groovy
withCredentials([usernamePassword(
    credentialsId: "${DOCKER_CREDS_ID}",
    usernameVariable: 'DOCKER_USER',
    passwordVariable: 'DOCKER_PASS'
)]) {
    sh '''
        echo "$DOCKER_PASS" | docker login \
          --username "$DOCKER_USER" \
          --password-stdin

        docker push "$DOCKER_IMAGE:$DOCKER_TAG"
        docker push "$DOCKER_IMAGE:$DOCKER_LATEST"
    '''
}
```

Never write the Docker Hub password directly inside the Jenkinsfile.

---

## 9. Pull and Run the Docker Image

### Pull a Specific Build

```bash
docker pull atuljkamble/flask-pipeline-app:build-85
```

### Run the Container

```bash
docker run -d \
  --name flask-pipeline-app \
  -p 5000:5000 \
  --restart unless-stopped \
  atuljkamble/flask-pipeline-app:build-85
```

### Verify Running Container

```bash
docker ps
```

### Test the Application

```bash
curl http://127.0.0.1:5000
curl http://127.0.0.1:5000/health
```

Open in a browser:

```text
http://<SERVER-PUBLIC-IP>:5000
```

### View Container Logs

```bash
docker logs flask-pipeline-app
```

### Follow Logs Continuously

```bash
docker logs -f flask-pipeline-app
```

### Stop and Remove the Container

```bash
docker stop flask-pipeline-app
docker rm flask-pipeline-app
```

### Pull and Run the Latest Image

```bash
docker pull atuljkamble/flask-pipeline-app:latest

docker run -d \
  --name flask-pipeline-app \
  -p 5000:5000 \
  --restart unless-stopped \
  atuljkamble/flask-pipeline-app:latest
```

---

## 10. Allow Port 5000

### Ubuntu UFW

```bash
sudo ufw allow 5000/tcp
sudo ufw status
```

When SSH is being used, allow SSH before enabling UFW:

```bash
sudo ufw allow OpenSSH
sudo ufw allow 5000/tcp
sudo ufw enable
```

### Azure Network Security Group

```bash
az network nsg rule create \
  --resource-group <RESOURCE_GROUP> \
  --nsg-name <NSG_NAME> \
  --name Allow-Flask-5000 \
  --priority 1001 \
  --direction Inbound \
  --access Allow \
  --protocol Tcp \
  --source-address-prefixes Internet \
  --destination-port-ranges 5000
```

For better security, replace `Internet` with the required trusted source IP or CIDR range whenever public access is not necessary.

---

## 11. Azure DevOps Pipeline

Azure DevOps pipeline configuration is normally stored in:

```text
azure-pipelines.yml
```

### Basic Azure Pipeline Example

```yaml
trigger:
  branches:
    include:
      - main

pr:
  branches:
    include:
      - main

pool:
  vmImage: ubuntu-latest

variables:
  imageName: atuljkamble/flask-pipeline-app

stages:
  - stage: CI
    displayName: Build and Test

    jobs:
      - job: Build
        steps:
          - checkout: self

          - task: UsePythonVersion@0
            inputs:
              versionSpec: '3.12'

          - script: |
              python -m pip install --upgrade pip
              pip install -r requirements.txt
            displayName: Install dependencies

          - script: |
              python -m compileall .
              if [ -d tests ]; then
                pytest tests/ -v
              fi
            displayName: Validate and test

          - script: |
              docker build \
                -t $(imageName):$(Build.BuildId) \
                -t $(imageName):latest .
            displayName: Build Docker image

  - stage: CD
    displayName: Deploy
    dependsOn: CI
    condition: succeeded()

    jobs:
      - deployment: DeployApplication
        environment: production

        strategy:
          runOnce:
            deploy:
              steps:
                - script: |
                    docker pull $(imageName):$(Build.BuildId)
                    docker rm -f flask-pipeline-app || true
                    docker run -d \
                      --name flask-pipeline-app \
                      -p 5000:5000 \
                      --restart unless-stopped \
                      $(imageName):$(Build.BuildId)
                  displayName: Deploy application
```

### Azure DevOps Trigger Examples

Push trigger:

```yaml
trigger:
  branches:
    include:
      - main
```

Disable automatic push trigger:

```yaml
trigger: none
```

Pull request trigger:

```yaml
pr:
  branches:
    include:
      - main
```

Path-based trigger:

```yaml
trigger:
  branches:
    include:
      - main

  paths:
    include:
      - app/**
      - Dockerfile
    exclude:
      - docs/**
```

Scheduled trigger:

```yaml
schedules:
  - cron: "0 2 * * *"
    displayName: Daily Build
    branches:
      include:
        - main
    always: true
```

---

## 12. GitHub Actions

GitHub Actions workflow files are stored under:

```text
.github/workflows/
```

Example:

```text
.github/workflows/docker-pipeline.yml
```

### GitHub Actions CI/CD Example

```yaml
name: Flask Docker CI/CD

on:
  push:
    branches:
      - main

  pull_request:
    branches:
      - main

  workflow_dispatch:

jobs:
  build-test-push:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout source code
        uses: actions/checkout@v4

      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: '3.12'

      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt
          pip install pytest

      - name: Validate Python code
        run: python -m compileall .

      - name: Run tests
        run: |
          if [ -d tests ]; then
            pytest tests/ -v
          else
            echo "No tests directory found."
          fi

      - name: Log in to Docker Hub
        uses: docker/login-action@v3
        with:
          username: ${{ secrets.DOCKERHUB_USERNAME }}
          password: ${{ secrets.DOCKERHUB_TOKEN }}

      - name: Build and push Docker image
        uses: docker/build-push-action@v6
        with:
          context: .
          push: true
          tags: |
            atuljkamble/flask-pipeline-app:build-${{ github.run_number }}
            atuljkamble/flask-pipeline-app:latest
```

### GitHub Actions Trigger Types

```yaml
on:
  push:
  pull_request:
  workflow_dispatch:
  schedule:
```

Manual trigger:

```yaml
on:
  workflow_dispatch:
```

Scheduled trigger:

```yaml
on:
  schedule:
    - cron: '0 2 * * *'
```

---

## 13. GitLab CI/CD

GitLab pipeline configuration is stored in:

```text
.gitlab-ci.yml
```

### GitLab Pipeline Example

```yaml
stages:
  - validate
  - test
  - build
  - deploy

variables:
  IMAGE_NAME: atuljkamble/flask-pipeline-app
  IMAGE_TAG: build-$CI_PIPELINE_IID

validate:
  stage: validate
  image: python:3.12

  script:
    - python -m pip install --upgrade pip
    - pip install -r requirements.txt
    - python -m compileall .

test:
  stage: test
  image: python:3.12

  script:
    - pip install -r requirements.txt
    - pip install pytest
    - |
      if [ -d tests ]; then
        pytest tests/ -v
      else
        echo "No tests directory found."
      fi

docker-build:
  stage: build
  image: docker:latest
  services:
    - docker:dind

  before_script:
    - echo "$DOCKER_PASSWORD" | docker login
      -u "$DOCKER_USERNAME"
      --password-stdin

  script:
    - docker build
      -t "$IMAGE_NAME:$IMAGE_TAG"
      -t "$IMAGE_NAME:latest" .
    - docker push "$IMAGE_NAME:$IMAGE_TAG"
    - docker push "$IMAGE_NAME:latest"

  rules:
    - if: '$CI_COMMIT_BRANCH == "main"'

deploy:
  stage: deploy

  script:
    - docker pull "$IMAGE_NAME:$IMAGE_TAG"
    - docker rm -f flask-pipeline-app || true
    - docker run -d
      --name flask-pipeline-app
      -p 5000:5000
      --restart unless-stopped
      "$IMAGE_NAME:$IMAGE_TAG"

  rules:
    - if: '$CI_COMMIT_BRANCH == "main"'
```

---

## 14. Pipeline Platform Comparison

| Feature | Jenkins | Azure DevOps | GitHub Actions | GitLab CI/CD |
|---|---|---|---|---|
| Configuration | `Jenkinsfile` | `azure-pipelines.yml` | Workflow YAML | `.gitlab-ci.yml` |
| Hosting | Usually self-managed | Microsoft-hosted or self-hosted | GitHub-hosted or self-hosted | GitLab-hosted or self-hosted |
| Source Integration | Any Git platform | Azure Repos, GitHub, others | GitHub | GitLab |
| Plugin Ecosystem | Very large | Azure Marketplace | GitHub Marketplace | GitLab integrations |
| Maintenance | User-managed | Mostly managed | Mostly managed | Managed or self-managed |
| Best Fit | Highly customized enterprise pipelines | Microsoft/Azure environments | GitHub repositories | GitLab end-to-end platform |
| Secret Storage | Jenkins Credentials | Variable groups / Key Vault | GitHub Secrets | CI/CD Variables |

---

## 15. Azure Backup

Azure Backup protects workloads and data by creating recovery points that can be restored after accidental deletion, corruption, hardware failure, or ransomware incidents.

### Azure Backup Can Protect

- Azure virtual machines
- Managed disks
- Azure Files
- SQL Server in Azure VM
- SAP HANA in Azure VM
- On-premises files and folders
- Selected other Azure workloads

### Important Azure Backup Components

| Component | Purpose |
|---|---|
| Recovery Services vault | Stores backup management data for supported workloads |
| Backup vault | Used for newer Azure Backup workloads such as Azure Disk Backup |
| Backup policy | Defines schedule and retention |
| Recovery point | Restorable version of protected data |
| Soft delete | Protects deleted backup data for a retention period |
| Resource lock | Helps prevent accidental deletion of the vault |

---

## 16. Azure VM Backup

Azure VM Backup creates application-consistent or file-system-consistent recovery points for an Azure VM.

### VM Backup Flow

```text
Azure VM
   ↓
Backup Policy
   ↓
Recovery Services Vault
   ↓
Recovery Point
   ↓
Restore VM / Disk / Files
```

### VM Backup Steps

1. Create or select a Recovery Services vault.
2. Open the vault.
3. Select **Backup**.
4. Choose **Azure Virtual Machine**.
5. Select or create a backup policy.
6. Select the VM.
7. Enable backup.
8. Run **Backup now** for an immediate recovery point.

### VM Restore Options

- Create a new virtual machine
- Restore disks
- Replace existing disks
- Perform file recovery

---

## 17. Azure Files Backup

Azure Files backup protects Azure file shares stored in a storage account.

### Important Points

- The source is an Azure file share.
- Backup is managed through a Recovery Services vault.
- Backup policy defines schedule and retention.
- Individual files or folders can be restored.
- The entire file share can also be restored.

### Azure Files Backup Flow

```text
Storage Account
   ↓
Azure File Share
   ↓
Recovery Services Vault
   ↓
Backup Policy
   ↓
Recovery Point
```

---

## 18. Azure Disk Backup

Azure Disk Backup protects managed disks independently of the VM.

### Main Features

- Snapshot-based backup
- Incremental recovery points
- Agentless backup
- Backup without shutting down the VM
- Disk-level recovery
- Useful when only selected managed disks require protection

### Azure Disk Backup Flow

```text
Managed Disk
   ↓
Backup Vault
   ↓
Backup Policy
   ↓
Incremental Snapshot
   ↓
Restore to New Managed Disk
```

### VM Backup vs Disk Backup

| Feature | Azure VM Backup | Azure Disk Backup |
|---|---|---|
| Protection Scope | Complete VM | Individual managed disk |
| Vault | Recovery Services vault | Backup vault |
| Restore | VM, disks, files | Managed disk |
| Application Awareness | Supported for VM workloads | Primarily crash-consistent disk protection |
| Common Use | Full VM recovery | Disk-specific protection |

---

## 19. Azure Site Recovery

Azure Site Recovery is a **disaster recovery** service. It replicates workloads from a primary location to a secondary location and orchestrates failover.

Azure Site Recovery is different from Azure Backup.

### Site Recovery Flow

```text
Primary Region
   ↓ continuous replication
Secondary Region
   ↓
Failover
   ↓
Application Runs in Secondary Region
   ↓
Failback When Primary Region Is Available
```

### Important Site Recovery Concepts

| Concept | Meaning |
|---|---|
| Replication | Copies workload changes to the secondary location |
| Recovery Services vault | Manages replication and recovery |
| Recovery plan | Defines ordered failover of multiple machines |
| Test failover | Tests disaster recovery without affecting production |
| Planned failover | Used when the primary environment is available |
| Unplanned failover | Used during an outage |
| Commit | Confirms the selected recovery point after failover |
| Re-protect | Reverses replication after failover |
| Failback | Returns workload operation to the primary location |

---

## 20. Azure Backup vs Azure Site Recovery

| Area | Azure Backup | Azure Site Recovery |
|---|---|---|
| Purpose | Data protection and restoration | Business continuity and disaster recovery |
| Mechanism | Scheduled recovery points | Continuous or frequent replication |
| Main Use | Restore deleted or corrupted data | Run workloads in another region/site |
| Recovery Target | File, disk, VM, database, share | Secondary environment |
| RPO | Based on backup schedule | Usually lower due to replication |
| RTO | Restore may take longer | Designed for faster failover |
| Historical Retention | Strong retention capability | Not intended as long-term backup |
| Replacement for Other Service | Does not replace ASR | Does not replace backups |

Best practice:

```text
Azure Backup + Azure Site Recovery
```

Use both where the workload requires data protection and disaster recovery.

---

## 21. Backup and Disaster Recovery Strategy

A complete resilience strategy should include:

```text
Application Source Code
    → GitHub / Azure Repos / GitLab

Build Artifacts
    → Artifact Repository / Container Registry

Docker Images
    → Docker Hub / Azure Container Registry

Virtual Machine Data
    → Azure VM Backup

File Shares
    → Azure Files Backup

Managed Disks
    → Azure Disk Backup

Regional Disaster Recovery
    → Azure Site Recovery
```

---

## 22. Recommended CI/CD Best Practices

1. Keep the pipeline file in source control.
2. Use separate CI and CD stages.
3. Run tests before building and deploying.
4. Use immutable image tags such as build number or commit SHA.
5. Do not deploy only with the `latest` tag.
6. Store secrets in credential stores.
7. Never place passwords inside YAML or Jenkinsfiles.
8. Scan dependencies and Docker images.
9. Add application health checks.
10. Use approval gates for production.
11. Maintain separate development, testing, staging, and production environments.
12. Configure pipeline timeouts.
13. Prevent overlapping deployments where necessary.
14. Archive logs and test results.
15. Implement rollback using previous image tags.
16. Restrict public inbound ports to trusted sources.
17. Use HTTPS and a reverse proxy for production.
18. Back up important application and infrastructure data.
19. Regularly test backup restoration.
20. Regularly conduct Site Recovery test failovers.

---

## 23. Important Commands

### Git

```bash
git clone https://github.com/atulkamble/jenkins-git-python-pipeline.git
git status
git add .
git commit -m "Update pipeline"
git push origin main
```

### Docker

```bash
docker build -t atuljkamble/flask-pipeline-app:build-85 .
docker images
docker pull atuljkamble/flask-pipeline-app:build-85
docker run -d -p 5000:5000 atuljkamble/flask-pipeline-app:build-85
docker ps
docker logs <CONTAINER_ID>
docker stop <CONTAINER_ID>
docker rm <CONTAINER_ID>
```

### Application Test

```bash
curl http://127.0.0.1:5000
curl http://127.0.0.1:5000/health
```

### Network Test

```bash
ss -tulnp | grep 5000
sudo ufw allow 5000/tcp
sudo ufw status
```

---

## 24. End-to-End DevOps Flow

```text
Developer Writes Code
        ↓
Git Commit
        ↓
Push to GitHub
        ↓
Webhook Trigger
        ↓
Jenkins Pipeline
        ↓
Python Validation and Tests
        ↓
Docker Image Build
        ↓
Container Smoke Test
        ↓
Docker Hub Push
        ↓
Docker Deployment
        ↓
Health Check
        ↓
Application Available on Port 5000
```

---

## 25. Points to Remember

- Jenkins uses a `Jenkinsfile`.
- Azure DevOps uses `azure-pipelines.yml`.
- GitHub Actions uses workflow YAML files under `.github/workflows/`.
- GitLab uses `.gitlab-ci.yml`.
- A trigger starts a pipeline.
- CI validates and packages code.
- CD releases and deploys code.
- Jenkins credentials should store Docker Hub secrets.
- A build-number Docker tag supports rollback and traceability.
- UFW and the Azure NSG must both allow the application port when public access is required.
- Azure Backup protects data and recovery points.
- Azure Site Recovery provides replication and failover.
- Backup and disaster recovery are complementary, not interchangeable.
