# Helm Flask App

Deploying a Flask application to Kubernetes using a custom Helm chart.

## What I learned
- Creating Helm charts from scratch
- Writing templated Kubernetes manifests
- Using values.yaml for environment configuration
- Deploying and managing releases with Helm

## Project Structure
```
helm-flask-app/
├── flask-chart/
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
│       ├── deployment.yaml
│       └── service.yaml
```

## How to run

### Prerequisites
- minikube installed and running
- Helm installed
- kubectl installed
- Docker Desktop running

### Steps
```bash
minikube start --driver=docker
helm install flask-app flask-chart
kubectl get pods
minikube service flask-app-service
```

### Upgrade the release
```bash
helm upgrade flask-app flask-chart
```

### Uninstall
```bash
helm uninstall flask-app
```

## Tech Stack
- Helm
- Kubernetes
- minikube
- Python / Flask
- Docker
