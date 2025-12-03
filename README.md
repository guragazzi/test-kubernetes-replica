# Kubernetes HPA Autoscaling Demo (MicroK8s)

This project demonstrates how to configure a Horizontal Pod Autoscaler (HPA) in Kubernetes using a simple deployment with a single initial replica. The cluster automatically increases the number of pods as load grows.

---

## 📦 Project Goals

- Create a Deployment with 1 replica.
- Expose the Deployment using a Service.
- Configure an HPA to scale between 1 and 5 replicas.
- Generate load to observe autoscaling behavior.
- Clean up all created resources afterward.

---

## 📁 File Structure

This repository contains the following Kubernetes manifests:

- **deploy-nginx.yaml** — Creates the initial Deployment.
- **svc-nginx.yaml** — Creates an internal ClusterIP Service.
- **hpa-nginx.yaml** — Defines the Horizontal Pod Autoscaler configuration.

---

## 🛠 Prerequisites

- A functional Kubernetes cluster (MicroK8s, Minikube, K3s, AKS, etc.)
- `kubectl` installed and configured
- `metrics-server` enabled in the cluster

---

## ▶️ How to Run

### 1. Apply the Kubernetes Manifests

Apply the files in the following order:

1. `deploy-nginx.yaml`
2. `svc-nginx.yaml`
3. `hpa-nginx.yaml`

After applying, the Deployment will be running and monitored by the HPA.

---

## ⚙️ Testing Autoscaling

To test HPA behavior:

- Generate continuous load against the service.
- Monitor the number of running pods.
- Watch the HPA scale pods automatically as CPU usage increases.

---

## 🧹 Cleanup

When finished, remove:

- The Deployment  
- The Service  
- The HPA  
- Any load generator pod created for testing  

---

## 🎯 Purpose

This repository serves to:

- Demonstrate basic Kubernetes autoscaling using HPA.
- Support studies, labs, and proof-of-concepts.
- Provide a simple and reusable example of autoscaling behavior.

---

## 📚 References

- Kubernetes Official Documentation — Horizontal Pod Autoscaler  
- MicroK8s Documentation — Metrics and Add-ons  


