# Website with MySQL on Kubernetes using Helm

This project shows how to deploy a **Website** along with a **MySQL database** on a Kubernetes cluster using **Helm**.

The goal is to automate everything needed to get a working WordPress site up and running inside Kubernetes using the best practices (like Helm charts, PVCs, Services, and Secrets).

---

## 🧱 Project Structure

```
kubernetes/
└── website/
    ├── templates/           # All YAML templates like Deployments, Services, PVCs, etc.
    ├── values.yaml          # All configurable values like image, ports, passwords, etc.
    └── Chart.yaml           # Basic Helm chart metadata
```

---

## 🚀 Features

- Website and MySQL are deployed using **Helm templates**
- Data is stored using **Persistent Volumes (PV + PVC)**
- Database credentials are securely managed using **Kubernetes Secrets**
- MySQL container waits for readiness before WordPress connects
- WordPress pod waits until MySQL is fully ready using **initContainers**
- Exposes WordPress via **NodePort**, accessible in the browser

---

## 🛠️ Requirements

- Kubernetes cluster (tested with Minikube and kubeadm)
- Helm (v3 or above)
- kubectl
- Internet access to pull container images

---


