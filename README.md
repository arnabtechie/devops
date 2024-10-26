# CI/CD with Jenkins and ArgoCD

This repository demonstrates how to implement a Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins and ArgoCD. The first step is to install the NGINX Ingress Controller (to access Jenkins and ArgoCD on the web) on your Kubernetes cluster.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Docker Account and Hub Access](#docker)
- [Install NGINX Ingress Controller on K8s cluster](#install-nginx-ingress-controller)
- [Set Up Jenkins](#set-up-jenkins)
- [Install and Configure ArgoCD](#install-and-configure-argocd)
- [Configure Jenkins for CI](#configure-jenkins-for-ci)
- [Deploy Applications with ArgoCD](#deploy-applications-with-argocd)
- [Conclusion](#conclusion)

## Prerequisites

Before you begin, ensure you have the following:

- A running Kubernetes cluster (e.g., GKE, EKS, AKS, or a local Minikube setup)
- `kubectl` installed and configured to interact with your Kubernetes cluster
- `Helm` installed for managing Kubernetes applications
- Jenkins installed (can be run locally or on a cloud service)
- Basic knowledge of Kubernetes, Jenkins, and ArgoCD

## Install NGINX Ingress Controller

To install the NGINX Ingress Controller, follow the official installation guide using Helm:

1. Open your terminal.
2. Run the following command to add the NGINX Ingress Controller Helm repository:

   ```bash
   helm repo add ingress-nginx https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/helm-chart/ingress-nginx
