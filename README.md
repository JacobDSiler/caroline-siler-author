# Caroline Siler — Author Website
> Sweet Southern Romance · Direct Sales Site

A fully custom author website for Caroline Siler, designed for direct ebook and audiobook sales. Clean, professional, and optimized for romance readers.

---

## 🗂️ File Structure

```
caroline-siler-site/
├── index.html          ← Main site (everything is here — single-file)
├── README.md           ← This file
└── (future)
    ├── /books/         ← Individual book pages
    ├── /assets/        ← Book cover images, author photo
    └── CNAME           ← Custom domain (e.g. carolinesiler.com)
```

---

## 🚀 Deploying to GitHub Pages (Step by Step)

### Step 1 — Create a GitHub Account
If you don't have one: go to [github.com](https://github.com) and sign up. Free.

### Step 2 — Create a New Repository
1. Click the **+** button (top right) → "New repository"
2. Name it: `caroline-siler-site` (or `carolinesiler.com` if using a custom domain)
3. Set it to **Public**
4. Check "Add a README file"
5. Click **Create repository**

### Step 3 — Upload Your Files
1. Open your new repository
2. Click **"Add file"** → **"Upload files"**
3. Drag `index.html` into the upload area
4. Scroll down → click **"Commit changes"**

### Step 4 — Enable GitHub Pages
1. Go to your repository → click **"Settings"** tab
2. Scroll to **"Pages"** in the left sidebar
3. Under "Source" → select **"Deploy from a branch"**
4. Choose **"main"** branch, **"/ (root)"** folder
5. Click **Save**

Your site will be live at:
```
https://[your-github-username].github.io/caroline-siler-site/
```
(Takes 1–2 minutes to go live)

### Step 5 — Custom Domain (Optional but Recommended)
To use `carolinesiler.com` instead:

1. Buy a domain from Namecheap, GoDaddy, or Google Domains (~$12/year)
2. In GitHub Pages settings → type your domain in "Custom domain"
3. In your domain registrar, add these DNS records:
   ```
   A     @    185.199.108.153
   A     @    185.199.109.153
   A     @    185.199.110.153
   A     @    185.199.111.153
   CNAME www  [username].github.io
   ```
4. Check "Enforce HTTPS" in GitHub Pages settings

---

## 💳 Connecting Real Payments (Required for Live Sales)

The site's "Buy Now" buttons are wired up with JavaScript — you need to connect a payment processor. The best options for direct ebook/audiobook sales:

### Option A — Lemon Squeezy (Recommended ⭐)
**Best for:** Digital downloads, built-in file delivery, VAT handling
- Free to start · 5% + 50¢ per transaction
- They host your files and deliver them automatically
- Steps:
  1. Sign up at [lemonsqueezy.com](https://lemonsqueezy.com)
  2. Create a "Product" for each book
  3. Upload your EPUB, MOBI, or MP3 files
  4. Set your price
  5. Copy the "Buy Link" for each product
  6. In `index.html`, replace the `openModal()` calls with links to those URLs

### Option B — Gumroad
**Best for:** Simple setup, existing reader community
- Free plan available · 10% fee
- Similar process to Lemon Squeezy
- Visit [gumroad.com](https://gumroad.com)

### Option C — Payhip
**Best for:** Lowest fees for UK/EU audiences
- Free plan · 5% fee
- [payhip.com](https://payhip.com)

### Option D — Stripe (Advanced)
**Best for:** Most control, lowest fees (2.9% + 30¢)
- Requires more technical setup or a developer
- You'd need to add Stripe Checkout to the site

---

## 📧 Email List / Newsletter

In `index.html`, the newsletter form needs connecting to an email service:

### Recommended: Kit (formerly ConvertKit)
- Free up to 10,000 subscribers
- [kit.com](https://kit.com)
- Create a "Form" → get the form embed code
- Replace the `<form>` in `index.html` with Kit's embed code

### Also good: Mailchimp, MailerLite, Flodesk

---

## 🖼️ Replacing Placeholder Content

### Author Photo
Replace the CSS placeholder in the "About" section with a real `<img>` tag:
```html
<!-- Find this in #about section and replace the .portrait-frame div with: -->
<img src="./assets/caroline-photo.jpg" 
     alt="Caroline Siler" 
     style="width:100%; border-radius:3px; object-fit:cover; aspect-ratio:3/4" />
```

### Book Covers
For each `.book-card-cover` div, add a background image:
```html
<div class="book-card-cover" style="background-image: url('./assets/magnolia-lane-cover.jpg'); background-size: cover; background-position: center;">
```

### Book Titles & Descriptions
Replace the placeholder book titles/descriptions with Caroline's real books directly in the HTML.

---

## 🎨 Customizing Colors

All colors are CSS variables at the top of the `<style>` tag:
```css
:root {
  --burgundy: #7a3030;    /* Main accent — change to match cover palette */
  --rose: #c9846e;        /* Secondary accent */
  --cream: #fdf8f2;       /* Page background */
  --sage: #8a9e87;        /* Green accent */
  --gold: #c9a84c;        /* Badges & highlights */
}
```

---

## 📱 Mobile

The site is fully responsive. It collapses gracefully to a single column on mobile. Test at [responsivedesignchecker.com](https://responsivedesignchecker.com).

---

## 🔒 HTTPS & Security

GitHub Pages includes free HTTPS/SSL. Once live, enable it in:
Settings → Pages → "Enforce HTTPS" ✓

---

## 📊 Analytics (Optional)

Add Google Analytics or Plausible to track visitors:
```html
<!-- Add just before </head> -->
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🆘 Need Help?

- GitHub Pages docs: [docs.github.com/pages](https://docs.github.com/pages)
- Lemon Squeezy docs: [docs.lemonsqueezy.com](https://docs.lemonsqueezy.com)
- For site edits: open `index.html` in any text editor (Notepad works!)

---

*Built with love for Caroline Siler · Clean & Wholesome Romance*
