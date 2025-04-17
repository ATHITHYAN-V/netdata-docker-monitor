# Netdata Docker Monitor

This project demonstrates how to monitor system and container-level performance metrics using **Netdata**, a lightweight, open-source monitoring tool running inside a Docker container.

## 📌 Objective

Install and run Netdata using Docker to monitor real-time performance metrics like:
- CPU usage
- Memory consumption
- Disk I/O
- Network traffic
- Docker containers (per-container stats)

---

## 🛠 Tools Used

- [Netdata](https://www.netdata.cloud/) – Open-source monitoring dashboard
- Docker – For containerizing and running Netdata

---

## 🚀 Getting Started

### 1. Pull and Run Netdata in Docker

```bash
docker run -d \
  --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  -v netdataconfig:/etc/netdata \
  -v netdatalib:/var/lib/netdata \
  -v netdatacache:/var/cache/netdata \
  -v /etc/passwd:/host/etc/passwd:ro \
  -v /etc/group:/host/etc/group:ro \
  -v /proc:/host/proc:ro \
  -v /sys:/host/sys:ro \
  -v /etc/os-release:/host/etc/os-release:ro \
  netdata/netdata
```
## 2. Access the Dashboard
Open your browser and visit:
- 👉 http://localhost:19999

## 3. What You Can Monitor
## 🔧 System Metrics:

-  CPU, Memory, Disk I/O, Network

## 🐳 Docker Containers:

- Per-container CPU, RAM, Net I/O, Block I/O

⚠️ Alerts & Warnings

📊 Live updating charts

## 📂 Exploring Logs

- docker exec -it netdata bash
- cd /var/log/netdata
- ls

## ✅ Deliverables

 - Netdata running in Docker
 - Access to http://localhost:19999
 - Screenshot showing dashboard with metrics and Docker monitoring
 - Explored alerts and logs

## 📸 Screenshot Example


