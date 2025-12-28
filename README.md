# 📦 Kubernetes Databases

A collection of Kubernetes manifests and configurations for deploying stateful database components such as MongoDB, MySQL, Redis, RabbitMQ, and more on a Kubernetes cluster.
This repository provides examples and templates to run production-like databases as Kubernetes workloads with persistent storage. 
GitHub

# 🧠 About

Deploying databases on Kubernetes requires handling stateful applications, persistent volumes, and stable network identities. This repository simplifies that by providing ready-to-use YAMLs for common database systems, enabling hands-on learning, rapid prototyping, and reference architecture for Kubernetes-based data services. 
Medium

Each database is structured using Kubernetes best practices such as PersistentVolumeClaims (PVCs), StatefulSets, Services, and configuration tailored to each database type.

> *Each folder (e.g., `mongodb`, `mysql`, `redis`, etc.) contains Kubernetes manifests for deploying that specific database/service.* :contentReference[oaicite:3]{index=3}

## 🚀 What’s Included

This repository includes database configurations for:

✔ **MongoDB** – NoSQL document database  
✔ **MySQL** – Relational database  
✔ **Redis** – In-memory key-value store  
✔ **RabbitMQ** – Message broker  
✔ **PersistentVolume / StorageClass configurations** – For persistent storage  
✔ **Namespace scoping** – Isolated environments via namespace manifests :contentReference[oaicite:4]{index=4}

## 🧠 Usage

You can apply these manifests to any working Kubernetes cluster (e.g., Minikube, Kind, GKE, EKS, AKS):

### 1. **Create the namespace for databases:**


kubectl apply -f 01-namespace.yaml


Apply a specific database manifest:

kubectl apply -f mongodb/


Verify the deployment:

kubectl get pods -n <namespace>
kubectl get svc -n <namespace>


Replace <namespace> with the namespace defined in 01-namespace.yaml. 
GitHub

# 📌 Best Practices for DB on Kubernetes

Running stateful databases on Kubernetes involves key considerations:

✔ Use PersistentVolumes (PVs) and StorageClasses to ensure data durability. 
Medium

✔ Prefer StatefulSets for stable network IDs and persistent volumes. 
Medium

✔ Monitor and back up databases regularly.
✔ Choose database operators or Helm charts for production-grade installations.

# 📈 Learning and Reference

Deploying and managing databases on Kubernetes is a valuable skill for cloud-native engineers. Kubernetes supports stateful workloads using stable storage and identity patterns, though running production databases on K8s requires careful planning around persistence, backup, and scaling strategies. 
Medium

# 🤝 Contributions

Contributions are welcome! You can help by:

Adding Helm charts or Operators for these databases

Improving persistence and backup configurations

Adding documentation and usage examples

Including monitoring and logging manifests

Fork the repo

Create a feature branch

Open a pull request
