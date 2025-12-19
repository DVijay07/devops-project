# 🚀 Automated CI/CD Web Deployment Pipeline

## 📝 Project Overview
This project demonstrates a fully automated **Continuous Integration and Continuous Deployment (CI/CD)** workflow. It takes a web application from a GitHub repository and automatically deploys it as a Docker container on a Linux server using Jenkins.



---

## 🛠️ Tech Stack
* **Source Control:** GitHub
* **Automation:** Jenkins
* **Containerization:** Docker
* **IDE:** VS Code
* **Environment:** Ubuntu (VirtualBox)

---

## 🏗️ How It Works (The Pipeline)
1. **Developer:** Pushes code changes to the `main` branch on GitHub.
2. **Jenkins:** Automatically detects changes via **SCM Polling**.
3. **Build Stage:** Jenkins uses the `Dockerfile` to build a fresh Nginx image.
4. **Deploy Stage:** Jenkins stops the old container and starts the new one on port `8081`.

---

## 📂 Key Files
* `index.html`: The website content.
* `Dockerfile`: Instructions to build the Nginx container.
* `Jenkinsfile`: The "Pipeline as Code" script that manages the automation.

---

## 🔥 Challenges Solved
* **Git Conflict Resolution:** Fixed merge issues between local and remote repositories.
* **Security:** Implemented **Personal Access Tokens (PAT)** for secure GitHub access.
* **Permissions:** Configured Jenkins user access to the Docker daemon.

---

## ✅ Success Indicators
* Jenkins Build Status: **SUCCESS**
* Live URL: `http://localhost:8081`
