# 🚀 AWS Portfolio CI/CD
A simple **CI/CD pipeline** that automatically deploys a static portfolio website to **Amazon S3** using **GitHub Actions**.

Instead of manually uploading files to S3, every `git push` can automatically trigger the deployment.
---
## 🔥 How It Works

```text
        👨‍💻 Developer
             │
             │ git push
             ▼
      📦 GitHub Repository
             │
             │ Trigger
             ▼
      ⚙️ GitHub Actions
             │
             │ Deploy
             ▼
        ☁️ Amazon S3
             │
             ▼
       🌐 Portfolio
```

### Simple Flow

**Code → GitHub → GitHub Actions → AWS S3 → Website**

---

## 🛠️ Technologies

* 🐙 Git & GitHub
* ⚙️ GitHub Actions
* ☁️ Amazon S3
* 🔐 AWS IAM
* 💻 HTML / CSS / JavaScript
* 🖥️ AWS CLI

---

## 📁 Project Structure

```text
CI-CD-pipeline/
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── AWS-Portfolio-cicd-main/
│   ├── index.html
│   ├── css/
│   ├── js/
│   └── images/
│
└── README.md
```

---

## ⚙️ CI/CD Pipeline

When code is pushed to GitHub:

```text
1️⃣ Developer pushes code
          ↓
2️⃣ GitHub receives code
          ↓
3️⃣ GitHub Actions starts
          ↓
4️⃣ AWS credentials configured
          ↓
5️⃣ Website files deployed
          ↓
6️⃣ S3 website updated 🚀
```

---

## 🔐 Security

AWS credentials are stored in **GitHub Secrets** instead of putting them directly inside the code.

```text
GitHub
  │
  └── Settings
       └── Secrets and variables
            └── Actions
```

Example:

```text
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_REGION
S3_BUCKET_NAME
```

> ⚠️ Never upload AWS secret keys directly to GitHub.

---

## 📦 Main AWS Service

### ☁️ Amazon S3

S3 is used to:

* Store website files
* Host the static website
* Serve HTML, CSS and JavaScript files

---

## 🎯 Why CI/CD?

### Without CI/CD ❌

```text
Change Code
    ↓
Build
    ↓
Manually Upload
    ↓
Update Website
```

### With CI/CD ✅

```text
Change Code
    ↓
git push
    ↓
GitHub Actions
    ↓
S3
    ↓
Website Updated 🚀
```

**Result:** Less manual work + faster deployment + repeatable process.

---

## 🚀 Setup

### 1. Clone Repository

```bash
git clone https://github.com/GS01-wyatt/CI-CD-pipeline.git
```

### 2. Create S3 Bucket

Create an Amazon S3 bucket for the portfolio website.

### 3. Configure IAM

Create appropriate AWS permissions for deployment.

### 4. Add GitHub Secrets

Add your AWS credentials and S3 bucket information to GitHub Secrets.

### 5. Push Code

```bash
git add .
git commit -m "Update portfolio"
git push origin main
```

GitHub Actions will automatically run the deployment workflow.

---

## 📊 Architecture

```text
                         🌐 USER
                           │
                           ▼
                    ☁️ Amazon S3
                           ▲
                           │
                    🚀 Deployment
                           │
                           │
                  ⚙️ GitHub Actions
                           ▲
                           │
                      git push
                           │
                           │
                    👨‍💻 Developer
```

---

## 💡 What I Learned

* Git & GitHub
* GitHub Actions
* CI/CD pipeline
* AWS S3
* AWS IAM
* AWS CLI
* Static website deployment
* Automation

---

## 🔮 Future Improvements

* 🌐 CloudFront CDN
* 🔒 HTTPS
* 🌍 Custom Domain
* 📊 CloudWatch Monitoring
* 🧪 Automated Testing
* 🔄 Deployment Rollback

---

## 👨‍💻 Author

**Golu Kumar**

🎯 Cloud & DevOps | Full-Stack Development

⭐ If you find this project useful, consider giving it a star!
