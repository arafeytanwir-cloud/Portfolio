# Portfolio Deployment Guide

## Step 1 — Push to GitHub

```bash
cd portfolio
git init
git add .
git commit -m "init: portfolio"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

## Step 2 — Enable GitHub Pages

1. Go to your repo → **Settings → Pages**
2. Under **Source**, select **GitHub Actions**
3. The workflow runs automatically on every push to `main`

## Step 3 — Set your custom domain (Namecheap)

### In the CNAME file
Replace `yourdomain.com` with your actual domain (e.g. `rafey.dev`).

### In Namecheap DNS settings
Go to Namecheap → Domain List → Manage → Advanced DNS and add:

| Type  | Host | Value                   | TTL  |
|-------|------|-------------------------|------|
| A     | @    | 185.199.108.153         | Auto |
| A     | @    | 185.199.109.153         | Auto |
| A     | @    | 185.199.110.153         | Auto |
| A     | @    | 185.199.111.153         | Auto |
| CNAME | www  | YOUR_USERNAME.github.io | Auto |

### In GitHub Pages settings
- Set **Custom domain** to your domain (e.g. `rafey.dev`)
- Check **Enforce HTTPS** (after DNS propagates — can take up to 24h)

## Done!

Your site will be live at `https://yourdomain.com` 🎉
