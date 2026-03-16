## Graded Assignment on Container Orchestration

## Project overview 
This project demonstrates the deployment of a MERN (MongoDB, Express.js, React.js, Node.js) application using:

- Docker for containerization
- Kubernetes for container orchestration
- Helm for package management
- Jenkins for CI/CD automation

The application consists of:
- Frontend (React)
- Backend (Node.js + Express)
- MongoDB Database
  
## Project Architecture

Jenkins
   ↓
Docker Build (FE & BE)
   ↓
Docker Push (DockerHub / ECR)
   ↓
Helm Deploy
   ↓
Kubernetes Cluster
   ├── Frontend (React + Nginx)
   ├── Backend (Node.js + Express)
   └── MongoDB

   ## Step 1: Clone the Repository
   ![Git Repo clone snapshot](https://github.com/user-attachments/assets/2440b7ff-f73b-420a-a712-3ca532c751ec)
   ![Kubernetrs-shopnow mohan git repo forked snapshot](https://github.com/user-attachments/assets/fcf876fb-76df-464e-b99b-31c6838a516e)

   ## Step 2: Dockerization
   Frontend Dockerfile shopNow/frontend/Dockerfile
      Node image for build
      Nginx image for serving static files
  ![Shopnow-Frontend deployment snapshot](https://github.com/user-attachments/assets/b7c8a991-cccc-4425-89e2-49eacb47b403)

Backend Dockerfile shopNow/backend/Dockerfile
         Uses Node.js 18 base image

![Shop-now Backend deployment snapshot](https://github.com/user-attachments/assets/cb678888-2005-47bd-83c4-342f74448566)

## Kubernetes Deployment

Kubernetes YAML files are located in the k8s/ directory.
Files include:
mongo-deployment.yaml
mongo-service.yaml
backend-deployment.yaml
backend-service.yaml
frontend-deployment.yaml
frontend-service.yaml

 ## K8s Deployment
 kubectl apply -f k8s/
 kubectl get pods
kubectl get services

## Helm Chart Deployment

 helm install shopnow ./shopnow
 helm upgrade shopnow ./shopnow

 ## Jenkins CI/CD Pipeline

  ## Pipeline Stages:
Clone repository
Build frontend Docker image
Build backend Docker image
Push images to DockerHub
Deploy application using Helm
![NPM Installed snapshot](https://github.com/user-attachments/assets/27c5c39a-3e6a-47dd-a830-62b2148b25c9)
![NPM start snapshot](https://github.com/user-attachments/assets/9ae4d680-e3a5-40e7-b3bd-88fa3ab29f4d)
![shopnow-assignment services details](https://github.com/user-attachments/assets/b78b544c-4aee-4982-a710-6a125f192ec3)

## “Frontend running on localhost:3000”
![“Frontend running on localhost3000”](https://github.com/user-attachments/assets/f733447b-6f37-46e4-a5aa-dbd845b79ece)

## Solutions Implemented

Used Kubernetes Services for internal communication.
Configured MongoDB connection using environment variables.
Implemented Helm templating with values.yaml for dynamic configuration.
Automated CI/CD using Jenkins pipeline.

## Outcome
Successfully containerized MERN application.
Deployed application using Kubernetes.
Managed deployment using Helm chart.
Automated CI/CD pipeline using Jenkins.

## conclusion

This assignment demonstrates practical implementation of container orchestration and CI/CD automation for a MERN stack application using modern DevOps tools.







         


   


