# Google Cloud Compute Engine & Kubernetes Microservice (Go)

[![Language](https://img.shields.io/badge/Language-Go-00ADD8.svg?logo=go&logoColor=white)](https://golang.org/)
[![GCP](https://img.shields.io/badge/Google%20Cloud-GCE%20%2F%20GKE-4285F4.svg?logo=googlecloud&logoColor=white)](https://cloud.google.com/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-Manifests-326CE5.svg?logo=kubernetes&logoColor=white)](https://kubernetes.io/)

A lightweight Go HTTP service and Kubernetes deployment manifest demonstration designed for Google Cloud Compute Engine metadata discovery, load balancing, and containerized GKE orchestration.

---

## Architecture Overview
- **Compute Engine Metadata Ingestion:** Queries the Google Cloud metadata server (`metadata.google.internal`) to resolve runtime instance IDs, zones, internal IPs, and machine hostnames.
- **Dual Runtime Modes:** Supports execution as a standalone frontend proxy or as an upstream backend service.
- **Health Probing:** Provides `/healthz` and `/version` endpoints for Cloud Load Balancer and Kubernetes readiness/liveness probes.

---

## Local Run

```bash
# Run locally in backend mode
go run main.go -port=8080

# Build Docker image
docker build -t gcp-go-demo:latest .
```
