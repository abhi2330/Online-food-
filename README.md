# 🍔 Online Food Ordering Website – DevOps CI/CD Project

## 📌 Project Overview

This project showcases an **end-to-end DevOps CI/CD pipeline** implemented for a **static Online Food Ordering Website**.  
The application is **containerized using Docker** and **automatically built and deployed on an AWS EC2 instance** using **Jenkins CI/CD**, triggered by **GitHub Webhooks**.

This repository is created for **DevOps hands-on practice**, **interview preparation**, and **portfolio demonstration**.

---

## 🧰 Tech Stack Used

- **Frontend**: HTML, CSS, JavaScript  
- **Version Control**: Git & GitHub  
- **CI/CD Tool**: Jenkins  
- **Containerization**: Docker  
- **Web Server**: Nginx  
- **Cloud Platform**: AWS EC2  
- **Automation Trigger**: GitHub Webhooks  

---

## 📁 Project Structure

```
Online-food-
│
├── index.html        # Food ordering website UI
├── Dockerfile        # Docker image configuration
├── Jenkinsfile       # Jenkins CI/CD pipeline
└── README.md         # Project documentation
```

---

## 🎯 Application Features

- Colorful and responsive food website UI  
- Food items displayed with images and pricing  
- Add to Cart functionality  
- Cart total price calculation  
- Order placement simulation  
- Ready for Docker-based deployment  

---

## 🏗️ Step-by-Step DevOps Implementation

### 🔹 Step 1: Create Food Ordering Website

- Designed a static food ordering website using **HTML, CSS, and JavaScript**  
- Implemented menu display, cart section, and basic UI interactions

📸 **Website UI Screenshot**

<img width="1920" height="878" alt="Website UI" src="https://github.com/user-attachments/assets/db2e0bf2-d7b7-4719-8f5d-7e06222262b8" />

---

### 🔹 Step 2: Push Code to GitHub

- Created a GitHub repository to manage source code  
- Pushed `index.html`, `Dockerfile`, and `Jenkinsfile` to GitHub

📸 **GitHub Repository Screenshot**

<img width="1917" height="883" alt="GitHub Repo" src="https://github.com/user-attachments/assets/abcbe9b3-c998-4e69-9d96-1bf00f450dc1" />

---

### 🔹 Step 3: Dockerize the Application

- Created a `Dockerfile` using **Nginx Alpine** base image  
- Copied website files into Nginx web root directory  
- Exposed port **80** for web access

📸 **Docker Build & Container Screenshot**

<img width="1915" height="1018" alt="Docker Build" src="https://github.com/user-attachments/assets/c89bd754-f950-4afe-a822-cf71ccb0ddd2" />

---

### 🔹 Step 4: Setup Jenkins on AWS EC2

- Launched an **AWS EC2 instance**  
- Installed required tools:
  - Jenkins  
  - Docker  
  - Git  
- Configured Jenkins to execute Docker commands

📸 **Jenkins Dashboard Screenshot**

<img width="1920" height="961" alt="Jenkins Dashboard" src="https://github.com/user-attachments/assets/dfe806be-460e-45fb-8b56-c3af7e9aa98e" />

---

### 🔹 Step 5: Create Jenkins CI/CD Pipeline

- Created a Jenkins **Pipeline Job**  
- Configured:
  - Pipeline script from SCM  
  - GitHub repository URL  
  - Branch: `main`

**Pipeline Stages:**
- Checkout source code  
- Build Docker image  
- Stop and remove old container  
- Deploy new container

---

### 🔹 Step 6: Configure GitHub Webhook

- Added a webhook in the GitHub repository  
- Configured Jenkins webhook endpoint  
- Enabled automatic pipeline trigger on every `git push`

📸 **GitHub Webhook Screenshot**

<img width="1902" height="896" alt="GitHub Webhook" src="https://github.com/user-attachments/assets/3d6a951e-dd2c-4fa4-a7d3-5281c5612863" />

---

### 🔹 Step 7: Continuous Deployment

On every code push:

- Jenkins pipeline is automatically triggered  
- Docker image is rebuilt  
- Old container is stopped and removed  
- Updated application is deployed on EC2

📸 **Live Deployment Screenshot**

<img width="1920" height="963" alt="Live Website" src="https://github.com/user-attachments/assets/58e6f7ab-ee85-4dad-90b6-be102eb318fe" />

---

## 🌐 Live Application Access

🔗 **Application URL:**  
[http://3.230.158.5](http://3.230.158.5)

---

## 🧠 Key Learnings

- Practical implementation of CI/CD using Jenkins  
- Docker image creation and container lifecycle management  
- GitHub webhook-based automation  
- Real-world DevOps deployment workflow on AWS EC2  

