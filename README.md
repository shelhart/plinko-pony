# 🐴 Plinko Pony — PWA Deployment Guide

## What's in the zip

```
plinko-pony-pwa/
├── index.html          ← The game (everything in one file)
├── manifest.json       ← PWA config (name, icon, fullscreen)
├── sw.js               ← Service worker (enables offline play)
└── icons/
    ├── icon-192x192.png
    └── icon-512x512.png
```

---

## Option A: GitHub Pages (recommended, free)

### One-time setup (~5 minutes)

1. Create a GitHub account at github.com (if you don't have one)
2. Click **New Repository** → name it `plinko-pony` → make it **Public** → Create
3. Click **"uploading an existing file"** link
4. Unzip the download and drag ALL 5 files (keeping the icons folder) into the upload area
   - Make sure `index.html` is at the root, NOT inside a subfolder
5. Click **Commit changes**
6. Go to **Settings** → **Pages** (left sidebar)
7. Under "Source" pick **Deploy from a branch**
8. Branch: **main**, folder: **/ (root)** → **Save**
9. Wait ~1 minute. Your game is live at:

```
https://YOUR-USERNAME.github.io/plinko-pony/
```

### To update the game later
Just upload the changed files again — GitHub Pages redeploys automatically.

---

## Option B: Netlify (drag & drop, free)

1. Go to app.netlify.com and sign up (free)
2. On the dashboard, find the drag & drop area
3. Unzip and drag the entire `plinko-pony-pwa` folder onto it
4. Done! You get a URL like `random-name.netlify.app`
5. You can customize the subdomain in Site settings

---

## Installing on Android

1. Open your game URL in **Chrome** on your phone
2. Play for a moment — Chrome will show a banner: **"Add Plinko Pony to Home screen"**
3. If no banner appears: tap the **⋮ menu** → **"Install app"** or **"Add to Home screen"**
4. It now launches fullscreen with its own icon — no browser bar!
5. It works offline too (service worker caches everything)

---

## Installing on Fire TV

1. Open **Silk Browser** (or Firefox) on your Fire TV
2. Navigate to your game URL
3. Bookmark it for easy access
4. For Silk: tap the **⋮ menu** → **Add to Favorites** or **Add shortcut**

### Fire TV tips
- The game works with the **Fire TV remote** — the center button acts as a tap
- For better control, pair a **Bluetooth mouse** or use the **Fire TV app** on your phone as a touchpad
- Silk Browser supports fullscreen: tap the ⋮ menu → "Full screen"

---

## Updating your game

When you make changes:
1. Edit `index.html` locally
2. Re-upload to GitHub/Netlify
3. In `sw.js`, change the cache name (e.g., `plinko-pony-v4`) so the service worker fetches the new version
4. On devices, close and reopen the app — it auto-updates

---

## Total cost: $0 forever
GitHub Pages and Netlify free tiers have no limits that matter for a game like this.
