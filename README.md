# 🌐 Personal Portfolio Website using AWS S3 & CloudFront

A production-ready **static portfolio website** hosted on **Amazon S3** and delivered globally using **Amazon CloudFront CDN**.  
This project demonstrates real-world **Cloud & DevOps fundamentals** including static hosting, CDN configuration, public access control, and performance optimization.

---

## 🚀 Live Demo
🔗 **Portfolio URL:**  
https://d1oubma31p0z6e.cloudfront.net

---

## 🛠️ Tech Stack
- **AWS S3** – Static website hosting
- **AWS CloudFront** – CDN for low latency & global delivery
- **HTML / CSS / JavaScript** – Frontend
- **AWS IAM** – Access control
- **AWS Console** – Infrastructure setup

---

## 📐 Architecture Overview
```
User Browser
     |
     v
CloudFront (CDN)
     |
     v
S3 Bucket (Static Website Hosting)
```

---

## ⚙️ Key Features
- 📦 Static website hosting using Amazon S3
- 🌍 Global content delivery with CloudFront
- ⚡ Low latency & caching via edge locations
- 🔐 Secure and controlled public access
- 🧩 Proper CloudFront origin configuration (HTTP-only for S3 website)
- 🏠 Default root object configuration (`index.html`)
- 🔄 Cache invalidation support

---

## 🧑‍💻 Implementation Steps

### 1️⃣ Create S3 Bucket
- Created an S3 bucket for static website hosting
- Uploaded `index.html`, CSS, JS, and assets
- Enabled **Static Website Hosting**
- Configured **Bucket Policy** for public read access

### 2️⃣ Configure Permissions
- Disabled **Block Public Access**
- Added bucket policy to allow `s3:GetObject` on `bucket/*`

### 3️⃣ Create CloudFront Distribution
- Origin: **S3 Website Endpoint**
- Origin Protocol Policy: **HTTP Only**
- Enabled global edge locations
- Set **Default Root Object = `index.html`**

### 4️⃣ Fix & Optimize
- Resolved `403 Access Denied` using correct bucket policy
- Resolved `504 Gateway Timeout` by:
  - Setting correct origin protocol
  - Adding default root object
- Performed cache invalidation (`/*`)

---

## ❗ Common Issues Solved
| Issue | Solution |
|-----|--------|
| 403 Access Denied | Correct S3 bucket policy & public access |
| 504 Gateway Timeout | HTTP-only origin + default root object |
| Blank homepage | Set `index.html` as root object |
| Cached errors | CloudFront invalidation |

---

## 💡 What I Learned
- Difference between **S3 REST endpoint vs S3 Website endpoint**
- How CloudFront interacts with S3 website origins
- Importance of **Default Root Object**
- Debugging real AWS production errors (403 / 504)
- CDN caching & invalidation concepts

---

## 📈 Future Enhancements
- 🔐 HTTPS with custom domain (Route 53 + ACM)
- 🧱 Infrastructure as Code (Terraform)
- 🚀 CI/CD pipeline for auto-deploy
- 🛡️ AWS WAF integration
- 📊 CloudFront access logging

---

## 📬 Contact
**Pranit Potsure**  
🔗 LinkedIn: https://www.linkedin.com/in/pranit-potsure  
📂 GitHub: https://github.com/your-github-username

---

⭐ If you like this project, feel free to star the repository!
