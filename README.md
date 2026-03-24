# GameDay ⚾ — Baseball PWA

A Progressive Web App that tracks your baseball team's schedule, shows game times and TV channels, and marks games where you have season tickets.

## Features
- Pick any MLB team
- Live schedule from the official MLB Stats API
- Countdown timer to the next game
- Import season ticket dates via CSV
- Push notifications before game time
- Add to home screen on iPhone & Android (works like a native app)
- Works offline after first load

## How to deploy (free, 5 minutes)

### Option 1: Netlify Drop (easiest — no account needed)
1. Go to https://app.netlify.com/drop
2. Drag the entire `baseball-pwa` folder onto the page
3. You get a live URL instantly — open it on your phone!

### Option 2: Vercel (free account)
1. Install: `npm install -g vercel`
2. From this folder run: `vercel`
3. Follow the prompts — you'll get a URL in ~30 seconds

### Option 3: GitHub Pages (free)
1. Push this folder to a GitHub repo
2. Go to Settings → Pages → Deploy from branch (main/root)
3. Your site will be at `https://yourusername.github.io/repo-name`

## Add to home screen

**iPhone (Safari):**
1. Open your app URL in Safari
2. Tap the Share button (box with arrow)
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add" — it now appears like a native app!

**Android (Chrome):**
1. Open your app URL in Chrome
2. Tap the three-dot menu
3. Tap "Add to Home Screen" or "Install App"
4. Tap "Add"

## Season ticket CSV format

Create a file called `tickets.csv` with this format:
```
date
2025-04-11
2025-04-13
2025-05-02
```

The only required column is `date` in YYYY-MM-DD format.
Import it from the Settings screen inside the app.

## Adding app icons (optional)

Replace `icon-192.png` and `icon-512.png` with your own baseball/team icons.
Free icon generators: https://favicon.io or https://realfavicongenerator.net

## Notifications

Notifications work when:
- The app is open in the browser, OR
- The app is installed as a PWA on Android (background push)
- On iPhone, notifications work when the PWA is installed to the home screen (iOS 16.4+)

## Tech stack
- Pure HTML/CSS/JavaScript — no build tools needed
- MLB Stats API (free, no API key required)
- Web Notifications API
- PWA manifest + service worker for offline/install support
