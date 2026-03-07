# ServeCyber Website

A professional cybersecurity volunteer hub built with pure HTML/CSS/JS — fast, secure, and deployable to GitHub Pages for free.

---

## 📁 File Structure

```
servecyber/
├── index.html          → Homepage
├── volunteer.html      → Volunteer hub (choose virtual or in-person)
├── virtual.html        → Virtual opportunities listings
├── inperson.html       → In-person opportunities listings
├── connect.html        → Submit an opportunity (Google Form)
├── newsletter.html     → Newsletter signup (Google Form)
├── css/
│   └── style.css       → All shared styles
├── js/
│   └── main.js         → Shared JavaScript
└── assets/
    └── favicon.svg     → Site favicon/icon
```

---

## 🔗 Plugging In Your Google Forms

In `connect.html` and `newsletter.html`, find the `<iframe>` tags and replace:

```
REPLACE_WITH_YOUR_CONNECT_FORM_ID
REPLACE_WITH_YOUR_NEWSLETTER_FORM_ID
```

With your actual Google Form embed URL. To get it:
1. Open your Google Form
2. Click **Send** → **< >** (Embed tab)
3. Copy the URL from inside the `src="..."` attribute

---

## 🚀 Deploying to GitHub Pages

### Step 1 — Create a GitHub repo
1. Go to github.com → New repository
2. Name it exactly: `servecyber.org` (or any name)
3. Set to **Public**
4. Click Create

### Step 2 — Upload your files
Option A (drag & drop): GitHub repo → "uploading an existing file" → drag all files
Option B (Git): `git init`, `git add .`, `git commit -m "launch"`, `git push`

### Step 3 — Enable GitHub Pages
1. Repo → Settings → Pages
2. Source: **Deploy from a branch**
3. Branch: `main` → `/ (root)` → Save
4. Your site will be live at `https://yourusername.github.io/reponame`

---

## 🌐 Connecting Your Namecheap Domain

### In GitHub — add a CNAME file
Create a file called `CNAME` (no extension) in the root of your repo with just:
```
servecyber.org
```

### In Namecheap DNS Settings
Go to your domain → Advanced DNS → Add these records:

| Type  | Host | Value              | TTL  |
|-------|------|--------------------|------|
| A     | @    | 185.199.108.153    | Auto |
| A     | @    | 185.199.109.153    | Auto |
| A     | @    | 185.199.110.153    | Auto |
| A     | @    | 185.199.111.153    | Auto |
| CNAME | www  | yourusername.github.io | Auto |

Wait 5–30 minutes for DNS to propagate.

### In GitHub Pages settings
- Custom domain: enter `servecyber.org`
- ✅ Enforce HTTPS (check this box — this is your SSL certificate, free)

---

## ✏️ Adding Volunteer Opportunities

In `virtual.html` and `inperson.html`, copy an `.opp-card` div and replace:
- The emoji in `.opp-card-img-placeholder` with an actual `<img>` tag if you have a logo
- The `.opp-card-title` text
- The location and date in `.opp-card-meta`

---

## 🎨 Colors
- Primary blue: `#00aff3`
- Dark blue text: `#0d1f3c`
- Navy: `#0a1628`
- Muted text: `#6b7a8d`
