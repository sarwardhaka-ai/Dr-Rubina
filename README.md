![Firebase Deploy](https://github.com/sarwardhaka-ai/Dr-Rubina/actions/workflows/firebase-hosting.yml/badge.svg)
![IndexNow Automation](https://github.com/sarwardhaka-ai/Dr-Rubina/actions/workflows/indexnow.yml/badge.svg)

# 🩺 Dr. Mosammat Rubina Sultana — Patient-Friendly Homepage

This repository contains the production-ready homepage for  
**Dr. Mosammat Rubina Sultana**, a leading cancer specialist and Associate Professor of Radiation Oncology, Bangladesh.

The project is built with a priority on **patient accessibility**, **fast performance**,  
**search visibility**, and **secure medical communication**.

---

## 🌟 Features

- High-performance static website (HTML + CSS + JS)
- Bengali + English language support  
- Correct hreflang tags for bilingual SEO  
- Strict security headers (CSP, HSTS, Permissions-Policy)  
- Rich structured data: Person, WebPage, FAQ, VideoObject  
- Firebase Hosting + GitHub Actions deployment  
- IndexNow auto-recrawl submission every 6 hours  
- Privacy-preserving analytics (GA4 + Clarity)

---

## 🔍 Purpose

- Strengthen visibility of credible cancer-care information  
- Support ethical medical outreach in Bangladesh  
- Enhance Bengali-language presence in Google & Bing  
- Deliver fast, secure, accessible patient communication  
- Provide a benchmark example for healthcare websites

---

## 🚀 Deployment Architecture

This project is deployed on **Firebase Hosting**, powered by **GitHub Actions CI/CD**.

---

## 🔧 Firebase Hosting Configuration

- **Site:** `drrubinasultanasite2025`  
- **Public Directory:** `public/`  
- **Clean URLs:** Enabled (removes `.html`)  
- **Trailing Slash:** Disabled (`/bn`, not `/bn/`)  
- **Redirects:** None (bn.html completely removed)  
- **Rewrites:** None (static site, not SPA)

### 🔒 Security Headers (from `firebase.json`)
- `Strict-Transport-Security: max-age=63072000; includeSubDomains; preload`
- `X-Frame-Options: SAMEORIGIN`
- `X-Content-Type-Options: nosniff`
- `X-XSS-Protection: 1; mode=block`
- `Permissions-Policy` (cameras/microphones/sensors blocked)
- `Referrer-Policy: strict-origin-when-cross-origin`
- `Content-Security-Policy` allowing only required domains (YouTube, GA4, Clarity, Facebook)

### ⚡ Performance
- CDN-cached assets (`max-age=31536000`, immutable)  
- Controlled caching for HTML, JS, CSS  
- Fast global delivery using Firebase CDN

---

## 📁 Project Structure

```txt
/
├─ public/
│  ├─ index.html              # English homepage
│  ├─ bn/
│  │   └─ index.html          # Bengali homepage
│  ├─ assets/                 # Images, CSS, JS
│  ├─ sitemap.xml
│  └─ robots.txt
├─ firebase.json              # Hosting, security, CSP configuration
└─ .github/
   └─ workflows/
      ├─ firebase-hosting.yml     # Auto deploy on push to main
      ├─ firebase-hosting-PR.yml  # PR preview deploy
      └─ indexnow.yml             # Auto IndexNow recrawl submission
