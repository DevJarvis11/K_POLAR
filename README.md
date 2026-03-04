# 🚀 K_POLAR — Kubernetes Pod Observability, Logging, Alerting & Reporting System

> A production-grade, cloud-native observability platform engineered to monitor Kubernetes workloads, aggregate logs, detect failures, and deliver real-time intelligent alerts.

---

## 📖 Overview

Modern distributed systems demand robust observability to detect failures fast and maintain reliability at scale. **K_POLAR** addresses this challenge head-on — providing comprehensive pod lifecycle monitoring, intelligent log analysis, and automated alerting within a Kubernetes environment.

Whether you're tracking a pod going from `Running` → `CrashLoopBackOff` → `Terminated`, or visualizing log spikes during rolling deployments, K_POLAR gives you the visibility your cluster deserves.

---

## ✨ Core Features

### 🔍 Pod Observability
Continuously monitors Kubernetes pods and detects lifecycle state changes — including creation, termination, restarts, and failure events — the moment they happen.

### 📦 Centralized Log Aggregation
Container logs are automatically collected and aggregated through **Loki** and **Promtail**, making them available for real-time analysis and visualization.

### 📊 Real-Time Monitoring Dashboard
An interactive dashboard built with Flask and Grafana displays live system logs, activity spikes, and workload behaviour at a glance.

### 🚨 Automated Alerting System
Sends instant **CRITICAL** and **RECOVERY** alerts via Telegram Bot for pod crashes, unexpected restarts, and abnormal log patterns — before they become outages.

### 📑 Reporting & Visibility
Provides actionable operational insights into pod health and overall cluster behaviour, enabling faster root cause analysis and informed decision-making.

---

## 🏗️ Architecture Stack

| Layer | Technology |
|---|---|
| Containerization | 🐳 Docker |
| Orchestration | ☸️ Kubernetes |
| Backend / Monitoring | 🐍 Python (Flask) |
| Visualization | 📊 Grafana |
| Log Aggregation | 📦 Loki |
| Log Shipping | 🚚 Promtail |
| Cluster Access Control | 🔐 RBAC |
| Alerting | 📢 Telegram Bot |
| Frontend Dashboard | 🖥️ HTML + CSS |

---

## 🔍 What K_POLAR Does

- ✅ Detects pod state changes (`Running` → `CrashLoopBackOff` → `Terminated`)
- ✅ Sends real-time **CRITICAL** & **RECOVERY** alerts via Telegram
- ✅ Visualizes logs and metrics in Grafana dashboards
- ✅ Tracks log spikes during pod deletion and recreation events
- ✅ Interfaces with the Kubernetes API securely via RBAC
- ✅ Fully containerized and deployable via YAML manifests

---

## ⚙️ Technical Highlights

- **Custom pod-state monitoring logic** — purpose-built state machine tracking pod lifecycle transitions
- **Log spike analysis** — observes and correlates log volume changes during pod deletion and container restart sequences
- **Modular Python microservices** — each component is independently deployable and maintainable
- **Animated interactive dashboard** — built from scratch with a clean, responsive UI
- **Scalable architecture** — designed with production adaptation in mind from day one

---

## 🚀 Getting Started

### Prerequisites

- Kubernetes cluster (local via `minikube` or cloud-hosted)
- `kubectl` configured
- Docker installed
- Telegram Bot token (for alerting)

### Deployment

```bash
# Clone the repository
git clone https://github.com/your-username/k-polar.git
cd k-polar

# Apply Kubernetes manifests
kubectl apply -f k8s/

# Verify pods are running
kubectl get pods -n monitoring
```

> Detailed setup instructions for Grafana, Loki, and Promtail configuration coming soon.

---

## 📁 Project Structure

```
k-polar/
├── k8s/                  # Kubernetes YAML manifests
├── monitoring/           # Python Flask monitoring service
├── dashboard/            # HTML + CSS frontend
├── alerts/               # Telegram alerting module
└── README.md
```



<div align="center">
  Built with ☸️ Kubernetes, 🐍 Python, and a passion for observability.
</div>
