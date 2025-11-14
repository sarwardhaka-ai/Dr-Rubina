![Firebase Deploy](https://github.com/sarwardhaka-ai/Dr-Rubina/actions/workflows/firebase-hosting.yml/badge.svg)

# 🩺 Dr. Mosammat Rubina Sultana — Patient-Friendly Homepage

This repository contains the deploy-ready homepage for **Dr. Mosammat Rubina Sultana**, a dedicated cancer specialist and radiation oncologist in Dhaka, Bangladesh.  
The project is optimized for ethical outreach, secure hosting, and search engine visibility across Google and Bing.

---

## 🔍 Purpose

- Democratize access to verified medical profiles  
- Benchmark patient-friendly healthcare services in Bangladesh  
- Enable ethical, inclusive digital outreach for medical professionals  
- Strengthen Bengali-language visibility and culturally sensitive communication  

---

## 🚀 Deployment Strategy

This project is hosted using **Firebase Hosting** with advanced security headers and optimized caching rules.

### Key Deployment Features (From `firebase.json`)
- **Hosting Target:** `drrubinasultanasite2025`
- **Public Directory:** `/public`
- **Automatic clean URLs:** Enabled  
- **Trailing slash removal:** Enabled  
- **301 Redirects:**  
  - `/bn.html` → `/bn`  
  - All non-matching routes → `https://drrubinasultana.com/:splat`
- **Rewrite:**  
  - `/bn` → `/bn.html`

### 🔒 Security Headers Included
Your hosting configuration includes enterprise-grade security:

- `Strict-Transport-Security`
- `X-Frame-Options`
- `X-Content-Type-Options`
- `X-XSS-Protection`
- `Referrer-Policy`
- `Permissions-Policy`
- `Cross-Origin-Resource-Policy`
- `Cross-Origin-Opener-Policy`
- Full **Content-Security-Policy (CSP)** support

### ⚡ Performance Optimization

- Long-term immutable caching for images & font files  
- Controlled caching for HTML, JS, and CSS  
- Optimized content delivery for Firebase global CDN  

---

## 📁 Key Files

| File | Description |
|------|-------------|
| `firebase.json` | Main config: hosting, headers, redirects, rewrites |
| `public/index.html` | English homepage |
| `public/bn.html` | Bengali homepage |
| `public/404.html` | Custom 404 page |
| `googleb7e3002053d12986.html` | Google Search Console verification |

---

## 🌐 Outreach & SEO Goals

- Embed Google Maps for chamber locations  
- Showcase verified patient testimonials  
- Maintain version history for medical recognition benchmarking  
- Optimize for Google, Bing, AI search, and Bengali audiences  
- Enable high-performance distribution across Facebook, WhatsApp, and medical directories  

---

## 🤝 Maintained By

**Md. Golam Sarwar**  
ICT Professional • Ethical Outreach Strategist  
Focused on inclusive benchmarking across healthcare, travel, and wellness sectors.