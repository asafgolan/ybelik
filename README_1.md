# 🌿 Yael Luna Feder — Landing Page Setup Guide

## Quick Start

This is a single-file landing page — no build tools, no framework, no backend.
Just HTML + CSS + a tiny bit of vanilla JS.

---

## 📋 Setup Checklist

### Step 1: Kit (ConvertKit) Form Setup
1. Go to [kit.com](https://kit.com) → create free account
2. Navigate to **Grow → Landing Pages & Forms**
3. Click **Create New → Form → Inline**
4. Pick any template (we override the styling anyway)
5. Add a "First Name" field
6. Click **Publish → HTML**
7. From the embed code, copy:
   - `FORM_ID` — the number in the action URL
   - `data-uid` — the unique string
8. In `index.html`, search for `YOUR_FORM_ID` and `YOUR_UID` and replace them

### Step 2: WhatsApp Link
1. Search for `972XXXXXXXXX` in `index.html` (appears 3 times)
2. Replace with Yael's actual phone number in international format
   - Example: `972501234567` (no + sign, no dashes)
3. You can customize the pre-filled message in the `?text=` parameter

### Step 3: Images
Replace the placeholder `<div class="image-placeholder">` blocks with actual `<img>` tags:
- **Hero image**: ~800×1000px portrait of Yael
- **About image**: ~600×800px candid/professional photo
- Design the images in Canva, export as JPG/WebP
- Place image files in the same folder as `index.html`

### Step 4: Content
Search for `✏️ EDIT` comments in the HTML — these mark all content you need to customize:
- Hero tagline and description
- About bio text and personal quote
- Service card titles and descriptions
- Testimonial texts, names, and details
- Social media links (replace `#` with real URLs)

### Step 5: Social Links
In the footer, replace `href="#"` with Yael's actual social profiles:
- Instagram
- Facebook
- TikTok
- WhatsApp (already configured in Step 2)

---

## 🚀 Deploy to Cloudflare Pages (Free)

### Option A: Direct Upload
1. Go to [dash.cloudflare.com](https://dash.cloudflare.com)
2. Navigate to **Workers & Pages → Create → Pages → Upload assets**
3. Drag your folder (with `index.html` + images) into the upload area
4. Done — you'll get a `*.pages.dev` URL

### Option B: Git Deploy
1. Push the folder to a GitHub repo
2. In Cloudflare dashboard → **Pages → Connect to Git**
3. Select the repo → deploy
4. Every push auto-deploys

### Custom Domain
1. Buy domain on Cloudflare Registrar (~$10/year for .com)
2. In Pages project settings → **Custom domains → Add**
3. DNS configures automatically

---

## 📁 File Structure

```
landing-page/
├── index.html          ← The entire landing page (single file)
├── yael-hero.jpg       ← Hero section photo (you add this)
├── yael-about.jpg      ← About section photo (you add this)
└── README.md           ← This file
```

---

## 🎨 Customizing Colors

All colors are CSS variables at the top of the `<style>` block.
Change the palette by editing these values:

```css
--color-cream: #FBF7F0;         /* Background */
--color-terracotta: #C4734F;     /* Primary accent */
--color-olive: #7A8B6F;          /* Secondary accent */
--color-charcoal: #3A3530;       /* Text */
```

---

## 💰 Total Cost

| Item | Cost |
|------|------|
| Landing page hosting (Cloudflare Pages) | Free |
| Email form + subscribers (Kit free plan) | Free |
| WhatsApp Business App | Free |
| Domain (Cloudflare Registrar) | ~$10/year |
| Canva Pro (already have) | Already paid |
| **Total new cost** | **~$10/year** |
