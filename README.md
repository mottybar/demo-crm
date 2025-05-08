# 📘 Portfolio Project Overview

This portfolio project is designed to demonstrate your capabilities in modern DevOps practices including SaaS application development, CI/CD, cloud infrastructure, and microservices deployment.

---

## ✅ Project Requirements

The project should demonstrate the following aspects:

- ✅ A SaaS application
- ✅ A CI/CD workflow
- ✅ Public cloud-based infrastructure
- ✅ Microservices-based deployment/architecture

---

## 🛠 Tools & Technologies

| Category                  | Tools / Technologies                                |
|---------------------------|-----------------------------------------------------|
| Source Code Management    | GitHub                                              |
| Development               | Python Flask with REST API                          |
| Containerization          | Docker                                              |
| CI/CD                     | GitHub Actions                                      |
| Scripting                 | Bash                                                |
| Database                  | MongoDB                                             |
| Docker Image Registry     | Amazon ECR                                          |
| Infrastructure as Code    | Terraform                                           |
| Cloud Provider            | AWS                                                 |

---

## 📁 Git Repository Structure

Implement your project using **multiple Git repositories** (private):

1. **Application Repository**
   - Purpose: Manage source code and CI/CD workflows
2. **Infrastructure Repository**
   - Purpose: Manage Terraform code for AWS infrastructure
3. **Cluster Resources Repository**
   - Purpose: Manage Kubernetes YAMLs and Helm Charts  
   - (Later include your own Helm chart for the application)

---

## 🧭 Architecture Diagrams

Create **two primary diagrams**:

### 🧱 1. 2-Tier Application Architecture

- Frontend/Backend
- Database (MongoDB)

### 🔄 2. Complete Workflow Architecture

Include:
- Git repositories
- GitHub Actions (CI)
- AWS infrastructure components
- Kubernetes deployment: Application + supporting services

---

## 👨‍💻 Application Development

You may choose one of the following application approaches:

### Option 1: DemoCRM (MongoDB)
- Based on the provided `demo-crm-main.zip`
- Perform minor refactoring from the original repo

### Option 2: Fork WorkProfile (MySQL)

### Option 3: Build Your Own Application
Use a simple REST API service that interacts with a database.  
**Example Endpoints**:
- `GET /person`: Return list of people (JSON)
- `POST /person/{id}`: Add a new person to the database

> 🔹 _Note: The application is **not** the main focus of the project._

---

## 🐳 Docker Implementation

- Create a **Dockerfile** for efficient runtime image
- Write a `docker-compose.yaml` for:
  - Local development (app + database)
  - End-to-end testing environment (mimicked in CI)

---

## 🔁 CI/CD Workflow with GitHub Actions

Target only the `main` branch (production).

### 🎯 Workflow Stages:

1. Clone/Pull code
2. Build the application
3. Unit tests (mocked)
4. Package Docker image
5. End-to-end testing (mocked)
6. Deploy testing environment (`docker compose up`)
7. Run API endpoint tests (GET, POST, DELETE)
8. Tear down test environment
9. Push image to ECR
10. Deploy new version to your environment

> ⚠️ Production environments are delicate—start with single-branch (`main`) workflows only.

---

## ☸️ Kubernetes Setup

- Use **Terraform** to deploy an **EKS cluster on AWS**
- Node type: `t3a.medium` (1 node)
- Deploy application and microservices manually
- Expose the Deployment with a Kubernetes Service to allow public access

---

## 🗂 Project Management Tips

- Use **Trello** to track tasks and define priorities
- Focus on mandatory requirements first
- Start with diagrams for better planning
- The application itself is a means to demonstrate the platform—keep it simple
- Reach out to mentors if using additional tools/resources

