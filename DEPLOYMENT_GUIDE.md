# 🚀 Portfolio Deployment Guide
## Domain: buildmewithkartikey.site

### Option 1: Netlify (Easiest & Recommended) ⭐

**Steps:**
1. Go to [netlify.com](https://netlify.com) and sign up (free)
2. Drag and drop your `kartikey-portfolio-v2 (2).html` file
3. Netlify will give you a URL like `random-name.netlify.app`
4. Go to **Domain settings** → **Add custom domain**
5. Enter `buildmewithkartikey.site`
6. Follow DNS instructions:
   - Add CNAME record: `www` → `random-name.netlify.app`
   - Add A record: `@` → Netlify's IP (they'll provide)
7. Wait 5-10 minutes for DNS propagation
8. **Done!** Your site is live at `buildmewithkartikey.site`

**For Auto-Deploy (Future Changes):**
- Create a GitHub repo
- Push your HTML file
- Connect Netlify to GitHub repo
- Every time you push changes → Auto-deploy in 30 seconds!

---

### Option 2: GitHub Pages (Free)

**Steps:**
1. Create GitHub account (if you don't have)
2. Create new repository: `portfolio` (public)
3. Upload your HTML file (rename to `index.html`)
4. Go to Settings → Pages
5. Select branch: `main` → Save
6. Your site: `username.github.io/portfolio`
7. For custom domain:
   - Add `CNAME` file with content: `buildmewithkartikey.site`
   - Update DNS: CNAME `www` → `username.github.io`
   - Add A records (GitHub provides IPs)

**Auto-Deploy:** Every push to GitHub = Auto-update!

---

### Option 3: Vercel (Fast & Modern)

**Steps:**
1. Go to [vercel.com](https://vercel.com) and sign up
2. Click "Add New Project"
3. Import from GitHub (or drag-drop)
4. Add custom domain: `buildmewithkartikey.site`
5. Update DNS as instructed
6. **Done!**

**Auto-Deploy:** Every Git push = Instant deploy!

---

### Quick Setup (Right Now - 5 Minutes)

**For immediate deployment:**

1. **Rename file:**
   - `kartikey-portfolio-v2 (2).html` → `index.html`

2. **Go to Netlify:**
   - Visit: https://app.netlify.com/drop
   - Drag `index.html` file
   - Copy the URL they give you

3. **Add Domain:**
   - Click on site → Domain settings
   - Add `buildmewithkartikey.site`
   - Follow DNS setup

4. **Update DNS (in your domain provider):**
   ```
   Type: CNAME
   Name: www
   Value: your-site.netlify.app
   
   Type: A
   Name: @
   Value: 75.2.60.5 (Netlify's IP)
   ```

5. **Wait 5-10 minutes** → Your site is LIVE! 🎉

---

### For Future Changes (Auto-Deploy Setup)

**Best Practice:**
1. Create GitHub repo
2. Push your `index.html`
3. Connect Netlify/Vercel to GitHub
4. Every time you edit → Push to GitHub → Auto-deploy in 30 seconds!

**Commands:**
```bash
git init
git add index.html
git commit -m "Initial portfolio"
git remote add origin https://github.com/yourusername/portfolio.git
git push -u origin main
```

---

### Important Notes:

✅ **Rename file to `index.html`** (required for hosting)
✅ **All images should be in `./images/` folder** (relative paths work)
✅ **Test locally first** - Open `index.html` in browser
✅ **DNS propagation takes 5-60 minutes** (be patient)
✅ **HTTPS is automatic** (free SSL certificate)

---

### Need Help?

- Netlify Docs: https://docs.netlify.com
- GitHub Pages: https://pages.github.com
- Vercel Docs: https://vercel.com/docs

**Your site will be live at:** `https://buildmewithkartikey.site` 🚀
