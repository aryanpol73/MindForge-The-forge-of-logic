# MindForge 🧠

> Train your logical thinking with daily challenges, brain games and cognitive puzzles.

A **Progressive Web App (PWA)** — installable on mobile & desktop, works fully offline.

## 🎮 Games

| Game | Type | Skill Trained |
|------|------|---------------|
| 🔢 Pattern Sculptor | Sequences | Dual-rule recognition |
| ⛓️ Causal Chain | Logic | Causation vs correlation |
| 🕵️ Lying Grid | Grids | Inconsistency detection |
| 🪞 Mirror Logic | Inversion | Metacognition |
| ⚗️ Word Alchemy | Language | Grammatical transformation |
| 🔐 Number Vault | Arithmetic | Working memory |
| 🌉 Logic Bridge | Deduction | Formal reasoning |
| 🔏 Cipher Room | Decoding | Abstract pattern recognition |
| 🌀 Mind Maze | Multi-clue | Fluid intelligence |

## 🚀 Deploy on Netlify

### Option 1 — Drag & Drop (fastest)
1. Go to [netlify.com](https://netlify.com) → **Add new site → Deploy manually**
2. Drag the entire project folder into the upload area
3. Done — live in seconds!

### Option 2 — GitHub + Netlify (recommended)
1. Push this repo to GitHub
2. Go to Netlify → **Add new site → Import from Git**
3. Select your repo
4. Build settings:
   - **Build command**: *(leave empty)*
   - **Publish directory**: `.`
5. Click **Deploy site**

## 📁 File Structure

```
mindforge/
├── index.html       ← Main app (all-in-one)
├── manifest.json    ← PWA manifest
├── sw.js            ← Service worker (offline)
├── icon-192.png     ← PWA icon (small)
├── icon-512.png     ← PWA icon (large)
├── _redirects       ← Netlify SPA routing
├── netlify.toml     ← Netlify headers & config
└── README.md        ← This file
```

## ✨ Features

- 🔐 **Google Sign-In** (simulated OAuth — swap for real GIS SDK in production)
- ☁️ **Guest mode** — play without signing in
- 📊 **Brain Score** — tracks cognitive improvement over time
- ⚡ **Daily Challenge** — curated 8-question mix each day
- 🌙 **Dark / Light theme**
- 📳 Haptic feedback, timer control, shuffle mode
- 🔔 Push notification permission support
- 📦 **Full offline support** via Service Worker

## 🔑 Adding Real Google OAuth

Replace the `loginGoogle()` function in `index.html` with the [Google Identity Services SDK](https://developers.google.com/identity/gsi/web):

```html
<script src="https://accounts.google.com/gsi/client" async defer></script>
```

```javascript
google.accounts.id.initialize({
  client_id: 'YOUR_GOOGLE_CLIENT_ID',
  callback: handleCredentialResponse
});
```

Get a Client ID at [console.cloud.google.com](https://console.cloud.google.com) → APIs & Services → Credentials.

## 📄 License

MIT — free to use, modify and deploy.
