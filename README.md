# 🚀 HealthChecks - Production Deployment with Docker & Kubernetes

## 📌 Overview

This project demonstrates the **containerization and production-grade deployment** of the open-source **HealthChecks** application — a cron job monitoring system.

I transformed the application into a **scalable, cloud-ready system** using modern DevOps practices including Docker and Kubernetes.

---

## 🧠 DevOps Highlights

✅ Containerized Django application using Docker
✅ Production-ready Gunicorn setup
✅ Kubernetes deployments for app + database
✅ Persistent storage using PVC
✅ Service-based architecture (internal networking)
✅ Environment-based configuration management
✅ Infrastructure as Code using Kubernetes YAML

---

## 🏗️ Architecture

```id="arch1"
        ┌──────────────────────┐
        │   HealthChecks App   │
        │  (Django + Gunicorn)│
        └─────────┬────────────┘
                  │
                  ▼
        ┌──────────────────────┐
        │     PostgreSQL DB    │
        └──────────────────────┘
```

---

## ⚙️ Tech Stack

### 🖥️ Application

* Python 3.12
* Django
* Gunicorn (Production WSGI server)

### ⚙️ DevOps

* Docker
* Kubernetes (K8s)
* PostgreSQL
* Persistent Volume Claims (PVC)

---

## 🐳 Docker Implementation

### 🔹 Dockerfile Overview

* Base Image: `python:3.12-slim`
* Installed system dependencies (gcc, libpq, ssl libs)
* Installed Python dependencies via `requirements.txt`
* Production server using **Gunicorn**

### 🔹 Run Locally

```bash id="run1"
docker build -t healthchecks .
docker run -p 8000:8000 healthchecks
```

Application will be available at:
👉 http://localhost:8000

---

## ☸️ Kubernetes Deployment

All Kubernetes manifests are available in the `k8s/` directory.

### 🔹 Resources Created

* Namespace
* Deployment (HealthChecks App)
* Deployment (PostgreSQL)
* Services (App + DB)
* Persistent Volume Claim (Database storage)
* ConfigMap (Environment configuration)

---

### 🔹 Apply Deployment

```bash id="run2"
kubectl apply -f k8s/
```

---

### 🔹 Verify Deployment

```bash id="run3"
kubectl get pods
kubectl get services
```

---

## 🔐 Configuration

Application is configured using environment variables:

* Database connection settings
* Django settings (DEBUG, ALLOWED_HOSTS)
* Email/alert configurations

Config is managed via:

* Kubernetes ConfigMap
* Environment variables

---

## 📦 Project Structure

```id="struct1"
healthchecks/
├── Dockerfile
├── docker-compose.yaml
├── k8s/
│   ├── namespace.yaml
│   ├── healthchecks-deployment.yaml
│   ├── healthchecks-service.yaml
│   ├── postgres-deployment.yaml
│   ├── postgres-service.yaml
│   └── postgre-pvc.yaml
├── requirements.txt
└── manage.py
```

---

## 🌐 Features

* ⏱️ Cron job monitoring
* 🔔 Alerting system
* 📊 Dashboard for job status
* 🔐 Secure authentication
* 📡 API + Web interface

---

## 🚀 Deployment Strategy

1. Containerize application using Docker
2. Push image to container registry
3. Deploy using Kubernetes manifests
4. Expose service internally
5. Attach persistent storage for database

---

## 💼 What This Project Demonstrates

This project proves my ability to:

* Deploy real-world production applications
* Work with Django in containerized environments
* Manage stateful applications in Kubernetes
* Configure persistent storage (PVC)
* Design scalable microservice architectures

---

## 🚀 Future Improvements

* Helm charts for easier deployment
* CI/CD pipeline integration (GitHub Actions / Jenkins)
* Monitoring (Prometheus + Grafana)
* Logging (ELK Stack)
* Ingress + HTTPS (Nginx / Cert-Manager)

---

## 👨‍💻 Author

**Shazil Ali**

* GitHub: https://github.com/Shazil91

---

## ⭐ Final Note

This project is part of my DevOps learning journey, focusing on:

* Containerization
* Kubernetes orchestration
* Production deployment practices

If you found this useful, feel free to ⭐ the repository!
