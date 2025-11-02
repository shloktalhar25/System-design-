# 🛍️ GoShop – Observable REST API

**GoShop** is a conceptual **System Design and Architecture** project built around a RESTful e-commerce API written in **Golang**, enhanced with a complete **Observability Stack** — including **Prometheus**, **Grafana**, and **Jaeger**.

This repository focuses on **system design, architecture diagrams, request flow, and observability integration**, serving as a blueprint for developers interested in building scalable and monitorable APIs.

---

## 🧠 About the Project

The goal of **GoShop** is to design a **traceable, measurable, and observable API system** that can handle CRUD operations for products while providing deep insights into its internal behavior.

### 🧩 Core Objectives:
- Design a **Go REST API architecture** following modern microservice principles.
- Integrate an **observability layer** using metrics, logs, and traces.
- Demonstrate how **Prometheus**, **Grafana**, and **Jaeger** interact with a Go service.
- Provide a **Docker-based architecture** for easy deployment and visualization.

---

## ⚙️ System Design Overview

### 🧱 Components:
1. **GoShop API** – REST API written in Golang using Gin/Echo.
2. **PostgreSQL** – For storing product and user data.
3. **Prometheus** – For collecting real-time metrics.
4. **Grafana** – For dashboard visualization and alerting.
5. **Jaeger** – For distributed tracing.
6. **Docker Compose** – For running all services together.

---
## Why Docker?

Docker helps by:
Running GoShop, Prometheus, Grafana, and Jaeger in isolated containers.
Avoids setup issues (works on any system).
Simplifies deployment and scaling.

---

## 🛠️ Planned Endpoints (REST API Design)

| Method | Endpoint | Description |
|---------|-----------|-------------|
| **GET** | `/api/v1/products` | Fetch all products |
| **GET** | `/api/v1/products/:id` | Fetch a single product |
| **POST** | `/api/v1/products` | Create a new product |
| **PUT** | `/api/v1/products/:id` | Update a product |
| **DELETE** | `/api/v1/products/:id` | Delete a product |
| **GET** | `/metrics` | Prometheus metrics endpoint |
| **GET** | `/healthz` | Health check endpoint |
| **GET** | `/readyz` | Readiness probe for deployment |

---

## 🔍 Observability Features

| Feature | Tool | Purpose |
|----------|------|----------|
| **Metrics** | Prometheus | Request rate, latency, and error monitoring |
| **Dashboards** | Grafana | Visualize metrics in real time |
| **Tracing** | Jaeger | Track request flow across system components |
| **Logging** | Go’s native log + middleware | Request/response and error logging |

---

## Project Structure
```
goshop/
├── main.go
├── go.mod
├── internal/
│ ├── handlers/
│ │ ├── product_handler.go
│ │ └── user_handler.go
│ ├── models/
│ │ ├── product.go
│ │ └── user.go
│ ├── db/
│ │ └── connection.go
│ └── observability/
│ ├── metrics.go
│ ├── tracing.go
│ └── logger.go
├── configs/
│ ├── prometheus.yml
│ └── docker-compose.yml
└── README.md
```

### Services:
- `goshop-api` → Exposes REST endpoints  
- `prometheus` → Collects metrics  
- `grafana` → Displays dashboards  
- `jaeger` → Visualizes traces  
- `postgres` → Stores data  

