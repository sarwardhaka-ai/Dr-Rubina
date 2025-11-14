![Firebase Deploy](https://github.com/sarwardhaka-ai/Dr-Rubina/actions/workflows/firebase-hosting.yml/badge.svg)

# 🩺 Dr. Mosammat Rubina Sultana — Patient-Friendly Homepage

This repository contains the deploy-ready homepage for **Dr. Mosammat Rubina Sultana**, a leading cancer specialist and radiation oncologist in Dhaka, Bangladesh.  
The project is optimized for ethical outreach, secure hosting, fast performance, and strong visibility on Google, Bing, and AI-powered search platforms.

---

## 🌟 Features

- Fully static, fast-loading website  
- Bengali + English language support  
- SEO-optimized for healthcare queries in Bangladesh  
- Modern security headers (CSP, HSTS, XFO, XSS Protection)  
- Firebase Hosting + GitHub Actions automatic deployments  
- Responsive UI focused on patient readability  
- Privacy-respecting analytics (Google Analytics + Clarity)

---

## 🔍 Purpose

- Democratize access to verified medical profiles  
- Benchmark patient-friendly cancer-care communication  
- Support ethical outreach for healthcare professionals  
- Strengthen Bengali-language visibility in search engines  
- Provide a transparent, research-backed medical homepage  

---

## 🚀 Deployment Strategy

This project is deployed using **Firebase Hosting**, with automated GitHub Actions for continuous delivery.

### 🔧 Firebase Hosting Configuration (from `firebase.json`)
- **Site:** `drrubinasultanasite2025`  
- **Public Directory:** `public/`  
- **Clean URLs:** Enabled  
- **Trailing Slash:** Disabled  
- **301 Redirects:**  
  - `/bn.html` → `/bn`  
  - All unmatched routes → `https://drrubinasultana.com/:splat`  
- **Rewrite:**  
  - `/bn` → `/bn.html`  

### 🔒 Security Headers
This project enforces enterprise-grade security:

- `Strict-Transport-Security` (HSTS)  
- `X-Frame-Options: SAMEORIGIN`  
- `X-Content-Type-Options: nosniff`  
- `X-XSS-Protection: 1; mode=block`  
- `Content-Security-Policy` with strict rules  
- `Permissions-Policy` (restricted access to sensors/camera/microphone)  
- `Referrer-Policy: strict-origin-when-cross-origin`  

### ⚡ Performance Optimization

- Long-term caching for images/fonts (`max-age=31536000`)  
- Controlled caching for HTML, JS, CSS  
- Delivered via Firebase's global CDN  

---

## 📁 Project Structure

```txt
/
├─ public/
│  ├─ index.html              # English homepage
│  ├─ bn.html                 # Bengali homepage
│  ├─ 404.html                # Custom 404 page
│  └─ assets/                 # Images, icons, CSS, JS
├─ firebase.json              # Hosting + security configuration
└─ .github/
   └─ workflows/
      ├─ firebase-hosting.yml     # Deploy on push to main
      └─ firebase-hosting-PR.yml  # Deploy previews on PR
```

---

## 🔄 Continuous Deployment (GitHub Actions)

### **Push to main branch → Automatic deployment**
Triggered by:

```
.github/workflows/firebase-hosting.yml
```

### **Pull Requests → Preview deployment**
Triggered by:

```
.github/workflows/firebase-hosting-PR.yml
```

### 🔐 GitHub Secrets Required

| Secret Name | Purpose |
|-------------|---------|
| `FIREBASE_SERVICE_ACCOUNT_DRRUBINASULTANASITE2025` | Authenticates GitHub → Firebase |
| `GITHUB_TOKEN` | Default GitHub token for actions |

---

## 🛠 Developer Guide

### Install Firebase Tools (optional)
```bash
npm install -g firebase-tools
```

### Preview the site locally
```bash
firebase serve
```

### Deploy manually (optional)
```bash
firebase deploy --only hosting:drrubinasultanasite2025
```

---

## 🤝 Maintainer

**Md. Golam Sarwar**  
ICT Professional • Ethical Outreach Strategist  
Focused on inclusive benchmarking across healthcare, travel, and wellness sectors. 

---

## 📜 License

This project is maintained privately and should not be redistributed without permission.
