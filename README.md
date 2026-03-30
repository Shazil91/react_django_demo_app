# 🚀 React + Django Full Stack App (Dockerized & Kubernetes Deployed)

## 📌 Overview

This project is a **full-stack web application** built using:

* **Frontend**: React
* **Backend**: Django REST Framework
* **Database**: SQLite (for development)

I transformed this application into a **production-ready DevOps project** by implementing:

* Docker containerization
* Multi-service orchestration using Docker Compose
* Kubernetes-based deployment

---

## 🧠 DevOps Highlights

✅ Containerized frontend & backend using Docker
✅ Multi-container setup using Docker Compose
✅ Kubernetes deployment for both services
✅ Service-based communication between frontend & backend
✅ Infrastructure as Code using Kubernetes YAML
✅ Separation of concerns (frontend vs backend services)

---

## 🏗️ Architecture

```
        ┌──────────────┐
        │   Frontend   │  (React)
        └──────┬───────┘
               │ API Calls
               ▼
        ┌──────────────┐
        │   Backend    │  (Django API)
        └──────────────┘
```

---

## ⚙️ Tech Stack

### 🖥️ Application

* React (Frontend)
* Django REST Framework (Backend)
* SQLite (Database)

### ⚙️ DevOps

* Docker
* Docker Compose
* Kubernetes (K8s)

---

## 🐳 Docker Implementation

### 🔹 Services

* **Frontend Container**

  * Builds React app
  * Serves static files

* **Backend Container**

  * Django API server
  * Handles business logic & API requests

---

### 🔹 Run Locally (Docker Compose)

```bash
docker-compose down
docker-compose up -d --build
```

### 🔹 Access Application

* Frontend → http://localhost
* Backend API → http://localhost:8000

---

## ☸️ Kubernetes Deployment

Kubernetes manifests are available in the `k8s/` directory.

### 🔹 Resources Created

* Namespace
* Backend Deployment & Service
* Frontend Deployment & Service

---

### 🔹 Deploy to Kubernetes

```bash
kubectl apply -f k8s/
```

---

### 🔹 Verify Deployment

```bash
kubectl get pods
kubectl get services
```

---

## 📦 Project Structure

```
react_django_demo_app/
├── frontend/                # React App
│   ├── Dockerfile
│   └── src/
├── api/                     # Django APIs
├── Dockerfile               # Backend Dockerfile
├── docker-compose.yaml      # Multi-container setup
├── k8s/                     # Kubernetes manifests
│   ├── backend-deployment.yaml
│   ├── backend-service.yaml
│   ├── frontend-deployment.yaml
│   ├── frontend-service.yaml
│   └── namespace.yaml
├── manage.py
└── requirements.txt
```

---

## 🌐 Features

* 📋 Task management (Todo app)
* 🔄 REST API integration
* ⚡ Fast frontend-backend communication
* 📱 Responsive UI

---

## 🚀 Deployment Strategy

1. Build Docker images for frontend & backend
2. Run locally using Docker Compose
3. Deploy services on Kubernetes
4. Expose services via K8s networking


---

## 💼 What This Project Demonstrates

This project highlights my ability to:

* Build and deploy full-stack applications
* Containerize multi-service architectures
* Use Docker Compose for local orchestration
* Deploy applications using Kubernetes
* Manage frontend-backend communication

---

## 🚀 Future Improvements

* Replace SQLite with PostgreSQL
* Add CI/CD pipeline (GitHub Actions / Jenkins)
* Add Ingress controller for routing
* Add monitoring (Prometheus + Grafana)
* Implement authentication (JWT)

---

## 👨‍💻 Author

**Shazil Ali**

* GitHub: https://github.com/Shazil91

---

## ⭐ Final Note

This project is part of my DevOps journey, focusing on:

* Containerization
* Kubernetes orchestration
* Full-stack deployment

If you like this project, feel free to ⭐ the repository!

