# 🚀 Cloud & DevOps Engineering Portfolio

**Author:** Yashas Nagaraj  
**Focus:** AWS, Kubernetes (EKS), Terraform, CI/CD, Observability  

Welcome to my portfolio! This repository serves as a central index for my DevOps journey. Below you will find links to specific projects:

### 🏗️ Project Index

| Project Name | Tech Stack | Key Achievement |
| :--- | :--- | :--- |
| **[Project Lazarus](https://github.com/yashas-nagaraj/stranger-things-app)** | Jenkins, Docker, AWS EC2 | Automated Zero-Downtime Deployment |
| **[Project Humangasaurus](https://github.com/yashas-nagaraj/humangasaurus-k8s)** | AWS EKS, Kubernetes, Helm | Scalable Microservices Migration |
| **[Project Terra-Saurus](https://github.com/yashas-nagaraj/terra-saurus)** | Terraform, AWS S3, DynamoDB | Infrastructure as Code (IaC) |
| **[Project Eye-Saurus](https://github.com/yashas-nagaraj/eyesaurus-app)** | Prometheus, Grafana, cAdvisor | Full-Stack Observability |
| **[Project Allsaurus](https://github.com/yashas-nagaraj/allsaurus)** | Terraform, Jenkins, AWS EKS, RDS, Helm | End-to-End 3-Tier Cloud Architecture |

---

### 📂 Brief Project Breakdown

#### 1. [Project Lazarus: CI/CD Pipeline Automation]
* **Repository:** `stranger-things-app` 
* **Goal:** Eliminate manual "SSH-and-patch" deployments by building a robust CI/CD pipeline.
* **Architecture:**
  * **Source:** GitHub Webhooks trigger the pipeline on commit.
  * **CI (Jenkins):** Builds Docker images for Frontend/Backend and pushes to Docker Hub.
  * **CD (Shell):** SSHs into the Production EC2, pulls new images, and seamlessly restarts containers.
* **Key Challenge Solved:** Implemented automated testing gates to prevent broken code from reaching production.

#### 2. [Project Humangasaurus: Kubernetes Migration]
* **Repository:** `humangasaurus-k8s` 
* **Goal:** Migrate the Dockerized app to **AWS EKS** for high availability and self-healing.
* **Key Features:**
  * **Security:** Decoupled database credentials using Kubernetes Secrets (etcd encryption).
  * **Networking:** Configured Ingress Controllers and Load Balancers to route traffic.
* **The "Nginx Crash" Fix:** Re-engineered the frontend architecture from Server-Side Proxying to **Client-Side Rendering** to resolve Nginx `CrashLoopBackOff` issues caused by upstream DNS dependencies during startup.

#### 3. [Project Terra-Saurus: Infrastructure as Code]
* **Repository:** `terra-saurus`
* **Goal:** Provision the entire AWS infrastructure (VPC, EKS, RDS) using code to eliminate manual console errors.
* **Key Features:**
  * **Modules:** Utilized `terraform-aws-modules` for VPC and EKS to ensure best practices.
  * **State Management:** Implemented **Remote State** using AWS S3 (encrypted) and **State Locking** using DynamoDB to enable safe team collaboration and prevent state corruption.

#### 4. [Project Eye-Saurus: Observability Stack]
* **Repository:** `eyesaurus-app` 
* **Goal:** Gain visibility into the application performance and resource usage.
* **Architecture:**
  * **Spy:** `cAdvisor` collects container-level metrics (CPU, Memory).
  * **Brain:** `Prometheus` scrapes metrics every 15 seconds.
  * **Face:** `Grafana` dashboards visualize the health of the Microservices.

#### 5. [Project Allsaurus: End-to-End 3-Tier Architecture]
* **Repository:** `allsaurus` 
* **Goal:** Architect and automate a complete, production-grade 3-tier application (Stranger Things Q&A app) integrating IaC, CI/CD, Kubernetes orchestration, and observability.
* **Architecture:**
  * **IaC:** Terraform provisioned a custom VPC, EKS cluster (`t3.small` nodes), and a private, secure RDS MySQL database.
  * **CI/CD:** Declarative Jenkins pipeline automating Docker image builds, dynamic LoadBalancer URL injection (`sed`), and Kubernetes zero-touch deployments.
  * **Observability:** Deployed `kube-prometheus-stack` via Helm for real-time cluster and pod monitoring.
* **Key Challenge Solved:** Engineered dynamic environment variable injection for secure K8s-to-RDS authentication and bypassed aggressive Docker layer caching to ensure seamless, real-time frontend-to-backend API routing.

---

### 🛠️ Core Competencies Demonstrated

* **Cloud:** AWS (EC2, EKS, RDS, S3, IAM, ELB).
* **Containerization:** Docker, Kubernetes (Manifests, Services, Deployments).
* **Automation:** Jenkins (Groovy Pipelines), Terraform (HCL), Helm.
* **Scripting:** Bash, Python.
* **Database:** MySQL (Schema management, Connectivity).
