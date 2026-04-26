# 🚀 Flask CI/CD Pipeline on AWS ECS (Fargate)

A production-style cloud project demonstrating a complete **CI/CD pipeline** using **GitHub Actions, Docker, Amazon ECR, and AWS ECS (Fargate)** to deploy a Flask web application.

## 🌐 Live Application
👉 Access the app via Load Balancer:
** http://flask-alb-1307443051.us-east-1.elb.amazonaws.com/

## 🏗️ Architecture
<img width="1400" height="933" alt="cicd architecture" src="https://github.com/user-attachments/assets/35463143-5f61-46a8-8032-9ca55925e59e" />

## 📸 Screenshots

### 🖥️ Application Running
<img width="1920" height="942" alt="application running" src="https://github.com/user-attachments/assets/89181f96-2df1-48c2-8c04-1d7ad29e4d73" />

### ⚙️ ECS Service (Running Tasks)
<img width="1920" height="945" alt="ecs task running" src="https://github.com/user-attachments/assets/5d0872bc-2b9f-4b63-a457-236d86239a60" />

### ❤️ Target Group Health
<img width="1908" height="949" alt="load balancer target group health" src="https://github.com/user-attachments/assets/16b60e64-6048-4021-ad8c-bcfc0f79d675" />

### 🔄 CI/CD Pipeline (GitHub Actions)
<img width="1920" height="942" alt="github actions run" src="https://github.com/user-attachments/assets/d2a65bdd-3180-4fcf-b167-84ecd5824592" />

### 📦 ECR Repository (Docker Image)
<img width="1920" height="945" alt="ECR image push" src="https://github.com/user-attachments/assets/0312e786-b56f-4b0f-a8db-7fb27f1512f0" />

## 🔄 CI/CD Workflow
Developer pushes code → GitHub
        ↓
GitHub Actions Workflow triggers
        ↓
Build Docker Image
        ↓
Push Image → Amazon ECR
        ↓
Update ECS Service
        ↓
New Task Deployment (Fargate)
        ↓
Application Load Balancer routes traffic
        ↓
Users access updated application

## 🛠️ Tech Stack
Backend: Flask (Python)
Containerization: Docker
CI/CD: GitHub Actions
Container Registry: Amazon ECR
Compute: AWS ECS (Fargate)
Load Balancing: Application Load Balancer (ALB)
Cloud Platform: AWS

## ✨ Key Features
Automated CI/CD pipeline using GitHub Actions
Dockerized Flask application
Image storage and versioning with Amazon ECR
Serverless container deployment using ECS Fargate
Load-balanced production-style architecture
Zero manual deployment after initial setup

## 📂 Project Structure
flask-cicd-app/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── .github/
│   └── workflows/
│       └── deploy.yml


## ⚙️ How It Works
1.Developer pushes code to GitHub
2.GitHub Actions workflow is triggered
3.Docker image is built and pushed to Amazon ECR
4.ECS service pulls the latest image
5.New container task is deployed
6.Application is updated automatically

