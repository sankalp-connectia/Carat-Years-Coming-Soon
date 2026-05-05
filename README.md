# Carat Years – Coming Soon Page

A minimal, responsive "Sparkling Soon" holding page for **caratyears.in**, deployable on Vercel in ~2 minutes.

---

## 📁 Project Structure

```
carat-years/
├── index.html          ← The page
├── vercel.json         ← Vercel config (redirect + headers)
├── public/
│   └── Coming_Soon.jpeg
└── README.md
```

---

## 🚀 Deploy to Vercel

### Option A — Vercel CLI (fastest)
```bash
npm i -g vercel
cd carat-years
vercel
```
Follow the prompts. Done.

### Option B — Vercel Dashboard (no CLI)
1. Push this folder to a GitHub repo
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your repo → click **Deploy**

---

## 🌐 Domain Setup (caratyears.in + caratyears.com)

### Add caratyears.in (main domain)
1. Vercel Dashboard → your project → **Settings → Domains**
2. Add `caratyears.in` and `www.caratyears.in`
3. Point your domain's DNS to Vercel:
   - **A record**: `76.76.21.21`
   - **CNAME** (www): `cname.vercel-dns.com`

### Add caratyears.com (redirect to .in)
1. Add `caratyears.com` and `www.caratyears.com` in the same Domains section
2. The `vercel.json` already has redirect rules: `.com` → `.in` (301 permanent)

---

## 🖼️ Using S3 Image Instead of Local File

If you have an S3 URL for the image, open `index.html` and replace:
```html
src="./Coming_Soon.jpeg"
```
with:
```html
src="https://your-bucket.s3.amazonaws.com/Coming_Soon.jpeg"
```
You can then remove the `public/` folder entirely.

---

## ✅ What's Included

- ✅ Responsive — looks great on mobile, tablet, desktop
- ✅ Image aspect ratio preserved on all screen sizes
- ✅ caratyears.com → caratyears.in 301 redirect via vercel.json
- ✅ Security headers included
- ✅ Fast load — no JS, no frameworks
