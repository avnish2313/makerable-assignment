# Ruby on Rails CI/CD Pipeline with Docker, Kubernetes, ArgoCD, and Tekton

This project demonstrates a complete CI/CD pipeline for a Ruby on Rails application using Docker, Kubernetes, ArgoCD, and Tekton. The pipeline includes building a Docker image, deploying to Kubernetes, managing deployments with ArgoCD, and setting up Tekton pipelines for automation.

## Table of Contents

- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Steps Completed](#steps-completed)
- [Getting Started](#getting-started)
  - [Clone the Repository](#clone-the-repository)
  - [Build Docker Image](#build-docker-image)
  - [Deploy to Kubernetes](#deploy-to-kubernetes)
  - [ArgoCD Deployment](#argocd-deployment)
  - [Set Up Tekton Pipelines](#set-up-tekton-pipelines)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project demonstrates the following steps in a CI/CD pipeline:

1. **Step 1: Docker**
   - Built a Dockerfile for deploying a simple Ruby on Rails application with PostgreSQL DB enabled. Application and DB run on different containers.

2. **Step 2: Kubernetes**
   - Built a YAML file to deploy the Ruby on Rails application and PostgreSQL DB on Kubernetes.
   - Used a Kubernetes StatefulSet for the standalone PostgreSQL pod.
   - Used an Ingress Controller for routing external traffic to the application.

3. **Step 3: ArgoCD**
   - Deployed ArgoCD to manage the deployment of the application using GitOps.
   - Created a private GitHub repository to manage the YAML files for GitOps.
   - Configured ArgoCD with application.yaml, ArgoCD config maps, and Kubernetes manifest files.

4. **Step 4: Tekton**
   - Set up Tekton pipelines and the Tekton dashboard.
   - Created a Task to download source code, build Docker images, and push them to Docker Hub.
   - Created a TaskRun to trigger the Task with specified parameters.

## Prerequisites

Before running this project, ensure you have the following installed:

- Docker
- Kubernetes (Minikube, K3d, or any local cluster)
- ArgoCD
- Tekton Pipelines

## Steps Completed

- Step 1: Dockerfile for Rails app and PostgreSQL DB
- Step 2: Kubernetes YAML for deployment
- Step 3: ArgoCD setup for GitOps deployment management
- Step 4: Tekton pipelines for automated building and deployment


