# Cloud-Based Penetration Testing Toolkit

> **SIT737 Task 6.1P** – Kubernetes Deployment of a Containerized Application

This project demonstrates the deployment of a cloud-native penetration testing toolkit using Kubernetes. It consists of:
- A **Node.js backend** exposing a `/scan` API
- A **React frontend** built with MUI for user interaction

---

## 🧾 Project Structure
```
.
├── backend/                  # Node.js backend microservice
├── frontend/                 # React frontend
├── k8s/                      # Kubernetes YAML manifests
│   ├── backend-deployment.yaml
│   ├── backend-service.yaml
│   ├── frontend-deployment.yaml
│   ├── frontend-service.yaml
└── README.md
```

---

## 🚀 Deployment Steps

### 1. ✅ Prerequisites
Make sure you have:
- Docker
- Node.js (v18+)
- Kubernetes (Minikube or Docker Desktop)
- kubectl
- Docker Hub account

---

### 2. 🐳 Build & Push Docker Images

#### Backend
```bash
cd backend
docker build -t <your-dockerhub-username>/backend:latest .
docker push <your-dockerhub-username>/backend:latest
```

#### Frontend
```bash
cd frontend

# Build and push
docker build -t <your-dockerhub-username>/frontend:latest .
docker push <your-dockerhub-username>/frontend:latest
```

---

### 3. ☸️ Deploy to Kubernetes

```bash
kubectl apply -f k8s/
```

Check if everything is running:
```bash
kubectl get all
```

---

### 4. 🌐 Access the App

```bash
kubectl get svc frontend-service
```

Open the app in a browser:
```
http://localhost:<node-port>
```

---

## 📦 Tech Stack
- Node.js (Backend)
- React + MUI (Frontend)
- Docker
- Kubernetes

---



