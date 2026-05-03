# Nexus Site — Deploy to Cloudflare Pages

## Files in this folder
```
nexus-site/
├── index.html      ← Home page
├── about.html      ← About page
├── scripts.html    ← Scripts page
├── getkey.html     ← Get Key page
├── style.css       ← All styles (easy to customize)
└── main.js         ← Interactions
```

---

## How to deploy on Cloudflare Pages

### Option A — Direct upload (easiest, no GitHub needed)

1. Go to https://pages.cloudflare.com and sign in (free account)
2. Click **"Create a project"** → **"Direct Upload"**
3. Give your project a name (e.g. `nexus-community`)
4. Click **"Upload assets"** and upload ALL files in this folder
5. Click **"Deploy site"**
6. Your site will be live at `nexus-community.pages.dev`!

### Option B — GitHub (recommended for updates)

1. Create a free GitHub account and a new repository
2. Upload all files to the repository
3. In Cloudflare Pages → Create project → Connect to Git → select your repo
4. Build settings: leave blank (no build command needed — it's plain HTML)
5. Deploy! Every time you push to GitHub, the site auto-updates.

---

## Customizing the site

### 1. Change your links
Open each HTML file and replace these placeholders:
- `https://discord.gg/YOURLINK` → your actual Discord invite link
- `https://lootlabs.gg/YOURLINK` → your actual LootLabs page link

### 2. Change colors
Open `style.css` and edit the `:root` block at the top:
```css
:root {
  --accent: #a855f7;       /* Main purple — change this hex */
  --bg: #0a0a0f;           /* Dark background */
  --text: #f1f0ff;         /* Text color */
}
```

### 3. Change member/game counts
In `index.html`, search for "500+" and "50+" and update to your real numbers.

### 4. Change the Discord button color
In `style.css`, find `.nav-links .btn-discord` and change the `background:` value.

### 5. Add your community name / branding
- Replace "NXS" logo in all HTML files with your preferred abbreviation
- Update page `<title>` tags to match

---

## Adding a custom domain (optional)
1. In Cloudflare Pages → your project → Custom Domains
2. Add your domain (e.g. `nexus.gg`)
3. If your domain is already on Cloudflare, it activates instantly
4. If not, update your domain's nameservers to Cloudflare's

---

## Tips
- The site is fully static — no server needed
- Mobile responsive out of the box
- No dependencies to install, no build step required
