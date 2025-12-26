# Grafana Observability Stack

A production-style **Grafana observability stack** built with Docker Compose, designed to simulate and monitor **AGV / factory systems** using MQTT-based telemetry.

This project demonstrates how real-time machine data flows from MQTT → time-series storage → dashboards, following patterns commonly used in manufacturing, logistics, and industrial IoT platforms.

---

## 🚀 What This Stack Provides

- Real-time **MQTT telemetry ingestion**
- Time-series storage for metrics and events
- Live dashboards for speed, counts, and alarms
- Clean separation of concerns (ingestion, storage, visualization)
- Environment-variable–driven configuration (production-ready)

---

## 🧱 Components

| Component | Purpose |
|---------|--------|
| **Mosquitto (MQTT)** | Message broker for AGV / factory signals |
| **Telegraf** | Ingests MQTT data and writes to InfluxDB |
| **InfluxDB** | Time-series database for telemetry & alarms |
| **Grafana** | Dashboards, visualization, alerting |
| **PostgreSQL** | Configuration, metadata, historical records |
| **pgAdmin** | Database administration UI (optional) |

---

## 🧠 Architecture Overview



## ⚙️ Configuration

### Environment variables

This project uses a `.env` file (not committed) for secrets and environment-specific configuration.

Create your local file:



▶️ Running the Stack

Start everything:

docker compose up -d


Verify:

docker ps

🌐 Service Access
Service	URL
Grafana	http://localhost:3000

InfluxDB	http://localhost:8086

pgAdmin (container)	http://localhost:5050

PostgreSQL	localhost:5432
MQTT	localhost:1883

Grafana default login:

user: admin

password: admin (change on first login)
