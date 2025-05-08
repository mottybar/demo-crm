Overview
The portfolio project should contain/demonstrate several aspects:

A SaaS application
A CI/CD workflow
Public cloud based infrastructure
Micro-service based deployment/architecture


Tools & Technologies
Source Code Management: GitHub
Development: Python Flask with REST API
Containerization: Docker
CI/CD: GitHub Actions
Scripting: Bash
Database: MongoDB
Docker image registry: ECR
Provision Infrastructure as Code with Terraform:
AWS as cloud provider


Git Repository Structure
Implement your work in multiple private Git repositories:

'Application' repository to manage source code, CI/CD workflows
'Infrastructure' repository to manage Terraform files
'Cluster Resources' repository to manage your Kubernetes resources yaml files and Helm Charts (in the future you will create this to your application Helm Chart)


Create Architecture Diagrams
Create two main diagrams:

2-tier application architecture (application + database)
Complete workflow architecture including:
Git repositories
GitHub Actions as a CI tool
Infrastructure components
Kubernetes deployment - application and supporting services


Application Development
For this project you may use one of the following application options:

1. DemoCRM(MongoDB) from the following file:



Demo CRM source code
A slight re-write from the original repo
demo-crm-main.zip


2. Fork from WorkProfile(MySQL) repository.

3. Develop your own by the following instructions.

Use a simple REST API service with database interaction:

Example endpoints:

GET /person: Return an array of people and their details (JSON) by ID
POST /person/{id}: Adds a person with their details (JSON) to the database
Keep in mind - the application is not the focus of the project

Docker Implementation
Create a Dockerfile for efficient runtime image
Develop docker-compose.yaml for:
Local development - verify your application works with a database in a simple, local environment
Mimic end to end testing environment in CI workflow


CI/CD Workflow
Implement a GitHub Actions workflow only for branch main (production environment) with multiple stages:

Notice: Production environments are delicate and usually won't include fully automated CD workflow.
As a first step we work with only one branch 'main'. Later as a bonus additional branches may be added.  
Clone/Pull
Build the application
Unit tests (Mimic)
Package (Docker image)
End-to-end testing (Mimic)
Deploy the testing environment (docker compose up)
API endpoint testing (GET, POST, DELETE)
Remove testing environment
Publish to ECR
Deploy the new version in your running environment


Kubernetes Setup
With Terraform, deploy an EKS cluster in AWS using 1 node of t3a.medium (if you need more please consult with your mentor)
Manually connect to your cluster and deploy your application and additional micro-services
Expose your application Deployment with the proper Service to allow end-users access



Project Management Tips
Organize your tasks and define clear priorities (Use Trello)
Complete mandatory requirements before bonuses (see next lesson)
The application is not the focus of the project
It's recommended to start with diagrams to provide the full scale of the project
Consult a mentor for using additional tools and resources

Next Lesson
