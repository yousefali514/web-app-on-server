# Scalable Microservices Deployment with CI/CD Pipeline

A complete DevOps project demonstrating the deployment of a
containerized microservices application using **Docker**,
**Kubernetes**, and **GitHub Actions**. The project focuses on
automation, scalability, and high availability.

## Project Overview

This project showcases a production-style DevOps workflow for deploying
a multi-service application consisting of:

-   Frontend
-   Backend API
-   Database

The deployment process is automated using GitHub Actions while
Kubernetes manages orchestration and scaling.

## Architecture

``` text
GitHub Repository
        │
        ▼
 GitHub Actions
        │
        ▼
 Build Docker Images
        │
        ▼
 Push Images to Docker Hub
        │
        ▼
 Kubernetes Cluster (Minikube)
        │
 ┌──────┴─────────────┐
 │                    │
 ▼                    ▼
Frontend          Backend
                       │
                       ▼
                   Database
```

## Features

-   Dockerized microservices architecture
-   Kubernetes Deployments, Services, ConfigMaps, and Secrets
-   Automated CI/CD with GitHub Actions
-   Docker Hub image publishing
-   Rolling updates and self-healing
-   Basic monitoring and logging with kubectl

## Technologies

-   Docker
-   Kubernetes (Minikube)
-   GitHub Actions
-   Docker Hub
-   YAML
-   Git
-   Linux

## Project Structure

``` text
.
├── frontend/
├── backend/
├── database/
├── kubernetes/
│   ├── frontend-deployment.yaml
│   ├── backend-deployment.yaml
│   ├── database-deployment.yaml
│   ├── services.yaml
│   ├── configmap.yaml
│   └── secret.yaml
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── docker-compose.yml
└── README.md
```

## CI/CD Pipeline

1.  Checkout source code
2.  Build Docker images
3.  Run tests
4.  Push images to Docker Hub
5.  Deploy to Kubernetes
6.  Verify deployment

## Getting Started

``` bash
git clone https://github.com/yousef-ali54554/scalable-microservices-devops.git
cd scalable-microservices-devops
minikube start
kubectl apply -f kubernetes/
kubectl get all
```

## Future Improvements

-   Deploy to Amazon EKS
-   Helm Charts
-   Argo CD
-   Prometheus & Grafana
-   Horizontal Pod Autoscaler

## Author

**Yousef Ali**

GitHub: https://github.com/yousef-ali54554
