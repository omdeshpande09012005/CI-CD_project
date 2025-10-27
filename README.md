# 🚀 CI-CD Project

This project demonstrates a simple **CI/CD pipeline** using **GitHub** and **Jenkins**.  
It automates testing and deployment whenever changes are pushed to the repository — ensuring **faster development cycles** and **reliable delivery**.

---

## 📋 Overview

The pipeline automatically:
- Runs tests on every GitHub push.
- Integrates Jenkins for continuous integration.
- Enables easy future extension for deployment or build steps.

---

## ✨ Features
- 🔁 Automated pipeline triggered by **GitHub push events**  
- ⚙️ Integration with **Jenkins** for CI  
- 🧪 Automated testing with **pytest**  
- 🌐 **Ngrok** support to expose local Jenkins to GitHub  
- 🧩 Extensible for custom deployment or build stages  

---

## 🧰 Technologies Used
| Technology | Purpose |
|-------------|----------|
| **Python** | Main project language |
| **Jenkins** | Continuous Integration server |
| **GitHub Webhooks** | Trigger Jenkins pipeline on push |
| **Ngrok** | Tunnel for exposing local Jenkins to GitHub |

---

## ⚙️ Getting Started

### ✅ Prerequisites
Before running this project, ensure you have:
- Python **3.x**
- Jenkins installed and running
- Ngrok (for public tunneling)
- Git

---

### 🪜 Setup Instructions

#### 1. Clone the repository
```bash
git clone https://github.com/omdeshpande09012005/CI-CD_project.git
cd CI-CD_project
```

#### 2. Install dependencies
```bash
pip install -r requirements.txt
```

#### 3. Run tests locally
```bash
pytest
```

---

### 🧩 Jenkins Setup

1. **Install Jenkins Plugins**
   - GitHub Integration Plugin  
   - Pipeline Plugin  

2. **Expose Jenkins using Ngrok (optional for local setup)**
   ```bash
   ngrok http 8080
   ```
   Copy the generated HTTPS URL (e.g., `https://<ngrok-id>.ngrok-free.app`).

3. **Create a Jenkins Pipeline Job**
   - Select **Pipeline** in “New Item”.
   - Check ✅ *GitHub hook trigger for GITScm polling*.
   - Use your repository’s URL in the Git configuration.

4. **Configure GitHub Webhook**
   - Go to **Repository → Settings → Webhooks → Add webhook**
   - **Payload URL:**  
     `https://<ngrok-id>.ngrok-free.app/github-webhook/`
   - **Content type:** `application/json`
   - **Trigger:** Push events

5. **Push changes**
   - Each new commit to `main` will trigger the Jenkins pipeline.

---

## 🧠 Pipeline Workflow

1. GitHub push → triggers Jenkins via webhook  
2. Jenkins pulls the latest code  
3. Automated tests run using `pytest`  
4. Build or deployment steps (optional) execute  

---

## 🤝 Contributing

Contributions are always welcome!

1. **Fork** the repository  
2. Create a **feature branch**  
   ```bash
   git checkout -b feature-branch
   ```
3. **Commit** and **push** your changes  
   ```bash
   git push origin feature-branch
   ```
4. Open a **Pull Request**

---

## 📄 License

This project is **open-source**.  
No specific license is currently included.

---

## 👨‍💻 Author

**Om Deshpande**  
📦 GitHub: [@omdeshpande09012005](https://github.com/omdeshpande09012005)  
💡 Built for learning and demonstrating CI/CD automation.

---
