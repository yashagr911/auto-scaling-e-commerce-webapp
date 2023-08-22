# Auto-scaling E-commerce Web Application

This repository contains the code and configuration for an automated infrastructure provisioning system that scales a Django-based e-commerce web application using Azure, Ansible, Docker, Jenkins, and Git.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Project Structure](#project-structure)
- [Deployment Workflow](#deployment-workflow)
- [Scaling and Auto-Scaling](#scaling-and-auto-scaling)
- [Continuous Integration and Deployment](#continuous-integration-and-deployment)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project aims to create an auto-scaling infrastructure for a Django e-commerce web application using Azure resources. The system utilizes Ansible for provisioning VMs, Docker for containerization, Jenkins for continuous integration and deployment, and Azure Monitor with Autoscale for managing scaling based on metrics.

## Features

- Auto-scaling of VM instances based on performance metrics.
- Automated provisioning of VMs using Ansible.
- Docker-based containerization for the Django e-commerce app.
- Continuous integration and deployment through Jenkins pipelines.
- Efficient use of Azure resources for dynamic scaling.

## Prerequisites

Before starting, make sure you have the following set up:

- Azure account and subscription.
- Docker Hub account for storing Docker images.
- Ansible installed on your local machine.
- Jenkins server configured and running.
- Azure DevOps project for managing code and pipelines.
- Django e-commerce application code stored in a Git repository.

## Setup Instructions

1. Clone this repository to your local machine.
2. Install necessary tools: Azure CLI, Docker, Ansible, Jenkins.
3. Set up Azure credentials and configure Azure CLI.
4. Create and configure Docker Hub credentials.
5. Set up Ansible inventory and dynamic inventory script.
6. Configure Jenkins with appropriate plugins and credentials.
7. Create Jenkins pipelines for build and deployment stages.
8. Define scaling rules and profiles using Azure Monitor and Autoscale.
9. Configure Azure DevOps for repository management.

## Project Structure

The project directory is organized as follows:

- `ansible/`: Contains Ansible playbooks and roles.
- `jenkins/`: Includes Jenkins pipeline scripts.
- `docker/`: Docker related files (Dockerfile, docker-compose, etc.).
- `src/`: Django e-commerce application source code.
- `azure_rm.py`: Azure Resource Manager dynamic inventory script.
- `README.md`: Project documentation (you're here!).

## Deployment Workflow

1. Azure Monitor detects metric threshold crossings.
2. Azure Autoscale triggers scaling actions.
3. Azure VM instances are added or removed.
4. Azure RM dynamic inventory script updates inventory.
5. Jenkins pipeline triggers Ansible playbooks.
6. Ansible provisions VMs and deploys app using Docker.

## Scaling and Auto-Scaling

- Define metrics and thresholds in Azure Monitor.
- Configure autoscale rules in Azure Autoscale.
- Azure RM dynamic inventory script updates VM inventory.
- Jenkins pipelines use dynamic inventory for deployment.

## Continuous Integration and Deployment

- Jenkins pipelines define stages for build and deployment.
- Build stage: Build Docker image and push to Docker Hub.
- Deployment stage: Run Ansible playbook for app deployment.

