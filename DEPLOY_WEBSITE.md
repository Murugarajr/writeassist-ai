# How to Deploy Your WriteBetter AI Website

This guide will help you deploy your single-page website to GitHub Pages (free hosting).

---

## Files in This Folder

```
website/
├── index.html          # Main website with landing page + privacy policy
├── icon48.png          # Copy from parent folder (needed for logo)
├── DEPLOY_WEBSITE.md   # This guide
```

---

## Step 1: Prepare the Files

Before deploying, copy the icon file to this folder:

```bash
# From the writebetter-extension folder:
cp icon48.png website/
```

---

## Step 2: Update Placeholder Content

Open `index.html` and replace these placeholders:

| Find | Replace With |
|------|--------------|
| `YOUR-EXTENSION-ID` | Your actual Chrome Web Store extension ID |
| `your-email@example.com` | Your actual contact email |
| `© 2025 WriteBetter AI` | Your company/name if different |

---

## Step 3: Deploy to GitHub Pages

### Option A: New Repository (Recommended)

1. **Create a new GitHub repository**
   - Go to https://github.com/new
   - Name: `writebetter` or `writebetter-ai`
   - Make it **Public**
   - Don't initialize with README

2. **Upload files**
   ```bash
   cd website
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/writebetter.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` / `/ (root)`
   - Click Save

4. **Your website URL:**
   ```
   https://YOUR-USERNAME.github.io/writebetter/
   ```

### Option B: Add to Existing Repository

If you want to add the website to your extension repository:

1. Create a `docs` folder in your repo root
2. Move `index.html` and `icon48.png` to `docs/`
3. Enable GitHub Pages with source: `main` / `/docs`

---

## Step 4: Verify Deployment

1. Wait 1-2 minutes for GitHub to build
2. Visit your URL: `https://YOUR-USERNAME.github.io/writebetter/`
3. Test all sections:
   - [ ] Hero section loads
   - [ ] Features section displays
   - [ ] Supported sites section shows
   - [ ] How it works section visible
   - [ ] Privacy policy section complete
   - [ ] Navigation links work
   - [ ] "Add to Chrome" button links correctly

---

## Step 5: Use in Chrome Web Store

Once deployed, use these URLs:

| Field | URL |
|-------|-----|
| **Privacy Policy URL** | `https://YOUR-USERNAME.github.io/writebetter/#privacy` |
| **Homepage URL** | `https://YOUR-USERNAME.github.io/writebetter/` |
| **Support URL** | `https://YOUR-USERNAME.github.io/writebetter/#privacy` (or create separate contact page) |

---

## Custom Domain (Optional)

If you have your own domain:

1. Create a `CNAME` file in the website folder:
   ```
   writebetter.yourdomain.com
   ```

2. Add DNS records at your domain registrar:
   - Type: CNAME
   - Name: writebetter (or www)
   - Value: YOUR-USERNAME.github.io

3. Enable HTTPS in GitHub Pages settings

---

## Updating the Website

To make changes after deployment:

1. Edit `index.html` locally
2. Commit and push:
   ```bash
   git add .
   git commit -m "Update website"
   git push
   ```
3. Changes go live in 1-2 minutes

---

## Alternative Hosting Options

### Netlify (Drag & Drop)
1. Go to https://app.netlify.com/drop
2. Drag the `website` folder
3. Get instant URL

### Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run: `vercel` in the website folder
3. Follow prompts

### Cloudflare Pages
1. Connect GitHub repo
2. Build command: (leave empty)
3. Output directory: `/`

---

## Troubleshooting

**Website not loading?**
- Check GitHub Pages is enabled in Settings
- Verify the branch and folder are correct
- Wait a few minutes for deployment

**Icon not showing?**
- Make sure `icon48.png` is in the same folder as `index.html`
- Check the file name matches exactly (case-sensitive)

**Privacy policy link not working?**
- The privacy section uses anchor `#privacy`
- Full URL: `https://your-site.github.io/writebetter/#privacy`

---

## Quick Checklist

- [ ] Copied `icon48.png` to website folder
- [ ] Updated `YOUR-EXTENSION-ID` placeholder
- [ ] Updated `your-email@example.com` placeholder
- [ ] Created GitHub repository
- [ ] Pushed files to repository
- [ ] Enabled GitHub Pages
- [ ] Verified website loads correctly
- [ ] Added URLs to Chrome Web Store listing

---

*Your website is now ready to use as your extension's official homepage and privacy policy!*
