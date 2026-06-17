# Deployment Guide – Crystal Wellness Website

This guide covers the **easiest and best ways** to deploy your new Crystal Wellness website.

**Recommended Order:**
1. **Netlify** ← **Best choice** (Easiest + Fastest + Free)
2. GitHub Pages
3. Traditional Hosting (A2 Hosting, etc.)

---

## 1. Netlify (Recommended – Easiest)

Netlify is the simplest and most professional way to host this site.

### Steps:
1. Go to [https://netlify.com](https://netlify.com) and sign up for a free account.
2. Once logged in, click **"Add new site"** → **"Deploy manually"**.
3. Drag and drop the entire `crystal-wellness-new` folder (or just the `index.html` file) into the upload area.
4. Netlify will deploy your site instantly and give you a free URL like:
   `https://crystal-wellness-abc123.netlify.app`

### Connecting a Custom Domain (crystalwellness-sf.com)
1. In Netlify, go to **Site settings → Domain management → Add custom domain**.
2. Enter `crystalwellness-sf.com` and follow the DNS instructions (usually just add a CNAME record at your domain registrar).

### Contact Form on Netlify (Easiest Option)
Netlify has built-in form handling — no extra services needed.

**How to activate:**
1. In your `index.html` file, change the form tag to:
   ```html
   <form name="consultation" method="POST" data-netlify="true">
   ```
2. Add this hidden field inside the form:
   ```html
   <input type="hidden" name="form-name" value="consultation" />
   ```
3. Redeploy the site on Netlify.
4. All submissions will appear in your Netlify dashboard under **Forms**.

This is the simplest method.

### Advantages of Netlify
- Free SSL certificate (https)
- Extremely fast worldwide
- Automatic deployments if you connect GitHub later
- Built-in forms
- Free custom domain support

---

## 2. GitHub Pages (Good Free Alternative)

If you prefer using GitHub:

### Steps:
1. Create a new repository on GitHub (name it `crystalwellness-sf` or similar).
2. Upload the `index.html`, `robots.txt`, and `sitemap.xml` files to the repository.
3. Go to **Settings → Pages**.
4. Under "Source", select **Deploy from a branch** → `main` branch → `/ (root)` folder.
5. Click **Save**. GitHub will publish your site at:
   `https://yourusername.github.io/crystalwellness-sf`

### Custom Domain on GitHub Pages
You can also connect `crystalwellness-sf.com` in the repository settings.

**Note on Forms:** GitHub Pages does **not** support forms natively. You will need to use Formspree or another service.

---

## 3. Traditional Hosting (A2 Hosting, Bluehost, SiteGround, etc.)

You can host this site on almost any web hosting provider.

### Steps:
1. Upload the `index.html` file (and optionally `robots.txt` + `sitemap.xml`) to the `public_html` or `www` folder via FTP or File Manager.
2. Make sure the file is named `index.html`.
3. Point your domain `crystalwellness-sf.com` to the hosting account.

### Contact Form on Traditional Hosting
You have two main options:
- Use **Formspree** (easiest – see instructions below)
- Use a PHP contact form (requires more setup)

**Using Formspree (Recommended for Traditional Hosting):**
1. Go to [https://formspree.io](https://formspree.io) and create a free account.
2. Create a new form and copy the endpoint URL.
3. In `index.html`, replace the form `action` with your Formspree URL.
4. Upload the updated file.

---

## Formspree Setup (Works Everywhere)

If you're not using Netlify Forms, use Formspree:

1. Visit [https://formspree.io](https://formspree.io)
2. Sign up (free tier is sufficient)
3. Create a new form
4. Copy the form endpoint (example: `https://formspree.io/f/abc123xyz`)
5. Open `index.html` and replace:
   ```html
   action="https://formspree.io/f/YOUR_FORMSPREE_ID_HERE"
   ```
   with your real endpoint.
6. Re-upload the file (or redeploy on Netlify).

All submissions will be sent to your email.

---

## Final Checklist After Deployment

- [ ] Test the website on mobile and desktop
- [ ] Test the contact form
- [ ] Submit your sitemap to Google Search Console: `https://crystalwellness-sf.com/sitemap.xml`
- [ ] Add your real photos (replace picsum placeholders)
- [ ] Update phone, address, and hours if needed
- [ ] Set up Google Analytics (optional but recommended)

---

## Need Help?

This site was built to be as simple as possible while still looking professional and compliant.

If you run into any issues during deployment, feel free to reach out.

**Recommended Path:** Netlify + Netlify Forms (fastest and cleanest).

Good luck with the new site!