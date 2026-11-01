# Worven

**The world's most trusted creative talent network.**

> Geography should not determine income.

---

## What is Worven?

Worven is a human-curated creative talent marketplace connecting verified South Asian creative professionals with global clients. We accept the top 5% of applicants, match clients with 3 verified talents within 24 hours, and guarantee every hire — personally.

**Not the biggest. Not the cheapest. The most trusted.**

---

## Tech Stack

- Pure HTML + CSS + Vanilla JS — zero dependencies, zero frameworks
- Hosted on Cloudflare Pages (free tier)
- Forms powered by Formspree (free tier)
- Fonts: DM Serif Display + DM Sans via Google Fonts

---

## File Structure

```
worven/
├── index.html        ← Main landing page (everything)
├── _redirects        ← Cloudflare Pages routing
├── robots.txt        ← Search engine instructions
├── sitemap.xml       ← SEO sitemap (update domain when live)
├── .gitignore        ← Git ignore rules
└── README.md         ← This file
```

---

## Deploy to Cloudflare Pages

### Step 1 — GitHub setup
1. Create a new GitHub repo called `worven`
2. Upload all files (index.html, _redirects, robots.txt, sitemap.xml, .gitignore, README.md)
3. Make sure `index.html` is in the ROOT of the repo — not inside a folder

### Step 2 — Cloudflare Pages
1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Click **"Create a project"**
3. Click **"Connect to Git"**
4. Authorize GitHub and select the `worven` repo
5. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave blank)*
   - **Build output directory:** *(leave blank or `/`)*
6. Click **"Save and Deploy"**
7. Wait ~60 seconds — your site is live on a `.pages.dev` URL

### Step 3 — Connect your domain
1. In Cloudflare Pages → your project → **Custom domains**
2. Add `worven.io` (or `worven.com`)
3. Follow the DNS instructions — usually takes 5–10 minutes

---

## Connect the Forms (Formspree — Free)

The forms currently show a success message after 1 second (demo mode).
To receive real submissions in your email inbox:

1. Go to [formspree.io](https://formspree.io) → Sign up free
2. Click **"New Form"** → name it "Worven Hire Brief"
3. Copy your Form ID (looks like `xpwzabcd`)
4. Open `index.html` in VS Code
5. Find this comment inside the JS section:

```js
/*
  TO CONNECT A REAL BACKEND:
  Replace the setTimeout below with a fetch() call.

  Example using Formspree (free tier available):
  -----------------------------------------------
  fetch('https://formspree.io/f/YOUR_FORM_ID', {
```

6. Replace `YOUR_FORM_ID` with your actual ID from Formspree
7. Repeat for the talent form (create a second Formspree form)
8. Push to GitHub — Cloudflare auto-deploys in 60 seconds

**Free Formspree tier:** 50 submissions/month. Upgrade to paid ($8/mo) when you grow.

---

## Update sitemap.xml

Once your domain is live, open `sitemap.xml` and replace all instances of:
```
https://worven.io/
```
with your actual live domain, then push to GitHub.

---

## SEO Checklist (do these before launch)

- [ ] Update `sitemap.xml` with live domain
- [ ] Add Google Analytics or Cloudflare Web Analytics (free)
- [ ] Submit sitemap to Google Search Console
- [ ] Add Open Graph image (1200×630 PNG) and update `<meta>` tags in index.html
- [ ] Test on mobile (Chrome DevTools → Toggle device toolbar)
- [ ] Run Lighthouse audit (Chrome DevTools → Lighthouse tab) — aim for 90+ score

---

## Built by

**Souvik Saha** — Kolkata, India  
Founder, Worven  
[linkedin.com/in/souviksaha](https://linkedin.com)

---

*Geography should not determine income.*
