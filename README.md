# 🚀 3-Tier DevSecOps Project

This repository contains a **Node.js API** (backend) and a **React client** (frontend) for a simple user management demo.  
It is designed as a **3-tier DevSecOps project** with modern practices for development and deployment.

---

## 📋 Table of Contents
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Run Locally](#run-locally)
- [Access the App](#access-the-app)
- [Features](#features)
- [Deployment to EKS with Jenkins](#deployment-to-eks-with-jenkins)

---

## 🔧 Prerequisites
- [Node.js](https://nodejs.org/) **v18 or later**
- npm (comes with Node.js)

---

## ⚙️ Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```

2. Install dependencies for both API and client:
   ```bash
   cd api && npm install
   cd ../client && npm install
   ```

---

## ▶️ Run Locally

### Start the API server
```bash
cd api
npm start
```

### Start the React client
In a separate terminal:
```bash
cd client
npm start
```

---

## 🌐 Access the App
Open your browser and go to:
```
http://localhost:3000
```

The client will display an **animated banner** welcoming you to **DevOps Shack** 🎉.

---

## ✨ Features
- Simple 3-tier architecture
- Node.js backend (API)
- React frontend (client)
- Animated welcome banner: *"Welcome to DevOps Shack"*

---

## ☸️ Deployment to EKS with Jenkins

This project includes a **Jenkins pipeline** to automate CI/CD deployment to **Amazon EKS**.

### Steps:
1. **Build & Push Docker Images**  
   Backend and frontend images are built, scanned with Trivy, and pushed to Docker Hub.

2. **Apply Kubernetes Manifests**  
   Jenkins uses `kubectl` with kubeconfig credentials to apply manifests (`mysql`, `backend`, `frontend`, `ingress`) to the `prod` namespace.

3. **Verification Stage**  
   Jenkins checks the pods and ingress to confirm deployment success.

4. **Manual Approval**  
   Before deploying to production, Jenkins prompts for manual approval.

---

### References
https://medium.com/@khushboo.sah067/devsecops-megaproject-series-three-tier-project-deployment-application-66816ae1e2f5 