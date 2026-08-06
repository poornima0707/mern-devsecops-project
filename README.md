# 🚀 End-to-End Kubernetes Three-Tier DevSecOps MERN Stack Project

## 📌 Project Overview

This project demonstrates a complete **End-to-End DevSecOps pipeline** for deploying a **Three-Tier MERN Stack Application** on **Amazon EKS (Elastic Kubernetes Service)** using modern DevOps and GitOps practices.

The application consists of:

- 🎨 ReactJS Frontend
- ⚙️ Node.js + Express Backend
- 🗄 MongoDB Database

The complete deployment is automated using **GitHub Actions**, **Terraform**, **Docker**, **Amazon ECR**, **Kubernetes**, **Helm**, **ArgoCD**, **Prometheus**, and **Grafana**.

---

# 🏗 Architecture

```
                   Developer
                       │
                       ▼
                 GitHub Repository
                       │
                       ▼
             GitHub Actions Pipeline
                       │
        ┌──────────────┼────────────────┐
        │              │                │
        ▼              ▼                ▼
   SonarQube      OWASP Dependency     Trivy
 Code Analysis         Check        Security Scan
        │
        ▼
    Docker Build
        │
        ▼
     Amazon ECR
        │
        ▼
 Terraform Infrastructure
        │
        ▼
     Amazon EKS Cluster
        │
        ▼
 Kubernetes Deployments
        │
 ┌──────┼───────────┐
 │      │           │
 ▼      ▼           ▼
Frontend Backend MongoDB
        │
        ▼
      ArgoCD
        │
        ▼
 Prometheus + Grafana
```

---

# 🎯 Problem Statement

Organizations require a scalable, secure, and automated deployment solution for modern web applications.

Traditional deployments often suffer from:

- Manual deployment errors
- Slow release cycles
- Lack of monitoring
- Poor scalability
- Security vulnerabilities
- Difficult infrastructure management

This project solves these challenges by implementing a complete DevSecOps pipeline with Infrastructure as Code, GitOps, Kubernetes, Continuous Integration, Continuous Deployment, and Monitoring.

---

# 🛠 Tech Stack

## Frontend

- ReactJS

## Backend

- Node.js
- Express.js

## Database

- MongoDB

## Cloud

- AWS
- Amazon EKS
- Amazon ECR
- EC2
- IAM
- VPC

## Infrastructure

- Terraform

## Containerization

- Docker

## Orchestration

- Kubernetes

## Package Management

- Helm

## GitOps

- ArgoCD

## CI/CD

- GitHub Actions

## Monitoring

- Prometheus
- Grafana

## Security

- SonarQube
- Trivy
- OWASP Dependency Check

---

# 📂 Project Structure

```
End-to-End-Kubernetes-Three-Tier-DevSecOps-MERN-Stack-Project

│
├── frontend/
│
├── backend/
│
├── kubernetes/
│
├── terraform/
│
├── mern-app/
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
│
├── argocd/
│
├── .github/
│   └── workflows/
│
└── README.md
```

---

# ⚙ Infrastructure Provisioning

Terraform is used to provision:

- AWS VPC
- Public Subnets
- Internet Gateway
- Route Tables
- IAM Roles
- Security Groups
- Amazon EKS Cluster
- Node Groups

---

# 🐳 Docker

Each component is containerized.

Docker Images:

- Frontend
- Backend
- MongoDB

Images are pushed to **Amazon ECR**.

---

# ☸ Kubernetes Deployment

The application is deployed on **Amazon EKS**.

Resources used:

- Deployment
- Service
- PersistentVolumeClaim
- ReplicaSet
- Pods

Current Deployment

| Component | Replicas |
|------------|----------|
| Frontend | 2 |
| Backend | 2 |
| MongoDB | 1 |

---

# 💾 Persistent Storage

MongoDB uses

- Persistent Volume
- Persistent Volume Claim
- Amazon EBS CSI Driver

This ensures data persistence even if the MongoDB pod is restarted.

---

# 🚀 GitHub Actions CI/CD Pipeline

Pipeline Stages

```
GitHub Push
      │
      ▼
Checkout Repository
      │
      ▼
Install Dependencies
      │
      ▼
Run Tests
      │
      ▼
SonarQube Scan
      │
      ▼
OWASP Dependency Check
      │
      ▼
Trivy Scan
      │
      ▼
Docker Build
      │
      ▼
Push Images to Amazon ECR
      │
      ▼
Update Kubernetes Manifest
      │
      ▼
ArgoCD Sync
      │
      ▼
Deploy on Amazon EKS
```

---

# 🔄 GitOps using ArgoCD

ArgoCD continuously monitors the GitHub repository.

Whenever a change is pushed,

- GitHub updates manifests
- ArgoCD detects the change
- Kubernetes automatically syncs
- Application is updated

Application Status

```
Application

mern-app

Sync Status

Synced

Health Status

Healthy
```

---

# 📊 Monitoring

Monitoring Stack

- Prometheus
- Grafana
- kube-state-metrics
- Node Exporter
- AlertManager

Grafana dashboards monitor:

- CPU Utilization
- Memory Usage
- Pod Status
- Node Health
- Network Traffic
- Storage
- Kubernetes Resources

---

# 🔐 Security

Security implementation includes:

- SonarQube Code Quality
- Trivy Image Scanning
- OWASP Dependency Check
- IAM Roles
- Kubernetes Secrets
- ClusterIP for MongoDB
- EBS Persistent Storage

---

# 📷 Project Verification

Verified Components

✅ Amazon EKS Cluster

✅ Terraform Infrastructure

✅ Docker Containers

✅ Amazon ECR

✅ GitHub Actions

✅ Kubernetes

✅ Helm Charts

✅ ArgoCD

✅ MongoDB PVC

✅ Prometheus

✅ Grafana

✅ Node Exporter

✅ kube-state-metrics

---

# 📸 Screenshots

Include screenshots of:

- AWS EKS Cluster
- Worker Nodes
- Terraform Apply
- GitHub Actions Pipeline
- Amazon ECR
- Kubernetes Pods
- Kubernetes Services
- ArgoCD Dashboard
- Prometheus Dashboard
- Grafana Dashboard
- MERN Application

---

# 📈 Future Enhancements

- HTTPS using AWS ACM
- Ingress Controller
- ExternalDNS
- Horizontal Pod Autoscaler
- Cluster Autoscaler
- AWS Load Balancer Controller
- Loki Logging
- ELK Stack
- Slack Notifications

---

# 🎯 Learning Outcomes

This project demonstrates practical experience in:

- Infrastructure as Code
- Kubernetes
- Docker
- AWS Cloud
- GitOps
- CI/CD
- Monitoring
- Security
- DevSecOps
- Terraform
- Helm
- ArgoCD
- Prometheus
- Grafana

---

# 👨‍💻 Author

**Poornima Umesh Kamatar**

- GitHub: https://github.com/poornima0707
- LinkedIn: https://linkedin.com/in/poornima-kamatar

---

# ⭐ If you found this project useful, please give it a Star!
