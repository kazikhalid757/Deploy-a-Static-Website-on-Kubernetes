# 🚀 Deploying a Static Website on Kubernetes

This project demonstrates how to deploy a simple static website using **Docker**, **Nginx**, and **Kubernetes**. The goal is to help beginners get hands-on experience with containerization and Kubernetes deployment basics.

## 📦 Tech Stack

- **HTML + CSS (Inline)** — Simple static webpage
- **Nginx (Alpine)** — Web server
- **Docker** — Containerization
- **Kubernetes** — Orchestration
- **kubectl (Single Node EC2)**

## 📁 Project Structure

```
Deploy-a-Static-Website-on-Kubernetes/
├── static-site/
│   ├── Dockerfile
│   ├── html/
│   │   └── index.html
│   └── k8s/
│       ├── nginx-deployment.yaml
│       └── nginx-service.yaml
```

## 🛠️ Steps to Deploy

### 1. Clone the Project

```bash
git clone https://github.com/your-username/Deploy-a-Static-Website-on-Kubernetes.git
cd Deploy-a-Static-Website-on-Kubernetes/static-site
```

### 2. Build and Push Docker Image

```bash
sudo docker build -t dockerhub_username/nginx-static-site:latest .

sudo docker login

sudo docker push dockerhub_username/nginx-static-site:latest
```


### 3. Apply Kubernetes Manifests

```bash
kubectl apply -f k8s/
```

> 🔁 Restart the deployment if needed:
```bash
kubectl rollout restart deployment nginx-deployment
```

### 4. Access the Website

  #### Use EC2 the external IP of the LoadBalancer.
  ![image](https://github.com/user-attachments/assets/0d7ef084-d87a-429d-99fc-90a562766477)



## ConfigMap for Nginx Configuration

You can use a ConfigMap to dynamically configure Nginx, such as custom error pages, rewrite rules, etc.


## ✍️ Author

**Kazi Tamim**  
Follow me on [GitHub](https://github.com/kazitamim757)

---

## 📜 License

This project is licensed under the MIT License. Feel free to use and modify it!
```
