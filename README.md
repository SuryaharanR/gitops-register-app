
🚀 DevOps CI/CD Pipeline – Jenkins | Docker | SonarQube | Trivy | ArgoCD | AWS EKS
📖 Overview

This project implements a real-world DevOps CI/CD pipeline for a Java application. It automates building, testing, scanning, and deploying to an AWS EKS Kubernetes cluster using GitOps with ArgoCD.

🛠️ Tech Stack

CI/CD: Jenkins

Build Tool: Maven

Code Quality: SonarQube

Security Scan: Trivy

Containerization: Docker

GitOps: ArgoCD

Cloud: AWS EKS

Notifications: Slack

🔄 Workflow

Developer pushes code → GitHub.

Jenkins pipeline builds & tests using Maven.

SonarQube analyzes code quality.

Docker builds and pushes image to Docker Hub.

Trivy scans for vulnerabilities.

Jenkins updates Kubernetes manifests in GitOps repo.

ArgoCD syncs manifests → deploys to EKS cluster.

Slack notifies build & deploy status.

⚙️ Setup Instructions
1. Infrastructure

AWS EC2 for Jenkins, SonarQube, and bootstrap server.

AWS EKS cluster created using eksctl:

   eksctl create cluster --name devops-cluster --region us-east-1 --nodes 2


2. Tools Installation

Jenkins + Plugins (Git, Docker, SonarQube, Slack, Pipeline).

SonarQube server (with PostgreSQL).

ArgoCD installed in Kubernetes cluster:

 kubectl create namespace argocd  
 kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml  


✅ Key Benefits

End-to-end automation from code commit → production.

Code quality & security gates before deployment.

GitOps ensures version-controlled deployments.

Scalable with AWS EKS.

📌 Next Improvements

Add monitoring with Prometheus & Grafana.

Implement blue/green or canary deployments.

Automate rollback on failures.


For know each and every commnads : check command file
