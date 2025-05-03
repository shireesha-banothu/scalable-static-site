# 🚀 Scalable Static Website with S3 + Cloudflare + GitHub Actions

This project demonstrates how to host a **static HTML website** on **AWS S3**, automate deployment with **GitHub Actions**, and configure **Cloudflare** for CDN, custom domain, and free HTTPS — all using free tiers.

---

## 📁 Project Structure
scalable-static-site/
├── index.html
└── .github/
└── workflows/
└── deploy.yml

---

## 🌐 Live Demo

> http://scalable-static-site-siri1419.s3-website-us-east-1.amazonaws.com

---

## 🔧 Tools Used

- **AWS S3** – Static website hosting
- **GitHub Actions** – CI/CD pipeline for automatic deployment
- **Cloudflare** – CDN, custom domain, free SSL
- **HTML** – Static content

---

## ✅ Prerequisites

- AWS account (free tier)
- GitHub account
- Cloudflare account (free plan)
- Basic HTML knowledge

---

## 🧱 Steps to Reproduce

### 1. 📂 Create Project Files

In your GitHub repo (e.g., `scalable-static-site`):

```bash
echo "<h1>Hello from S3 + GitHub Actions!</h1>" > index.html
mkdir -p .github/workflows
 Add GitHub Secrets
Go to your GitHub repo → Settings → Secrets and Variables → Actions → New repository secret and add:

Secret Name	Value
AWS_ACCESS_KEY_ID	Your IAM Access Key ID
AWS_SECRET_ACCESS_KEY	Your IAM Secret Access Key
AWS_S3_BUCKET	Your S3 bucket name (e.g., scalable-static-site-siri1419)


 Create S3 Bucket
Go to AWS S3 → Create bucket

Name: scalable-static-site-siri1419

Region: us-east-1

Disable block public access (uncheck all)

Enable Static website hosting

Index document: index.html

git init
git remote add origin https://github.com/yourusername/scalable-static-site.git
git add .
git commit -m "Initial commit"
git push -u origin main
