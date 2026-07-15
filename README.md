# GymBro Workout Tracker

A fast, offline-capable workout tracker for a 6-day push/pull/legs split, built to run as a real installable app on iPhone (no App Store required).

- **Today** — see your scheduled workout, start a session, log weight/reps per set, auto rest timer (90s / 45s for core), PR detection.
- **Schedule** — the full weekly split, expandable per day.
- **Progress** — streak, weekly volume chart, and personal records.

All data (logged sets, streak, PRs) is saved on-device with `localStorage` — nothing is sent to a server, and it works fully offline once loaded.

## Install it on your iPhone

1. Host these files somewhere reachable over HTTPS — the easiest way is **GitHub Pages**:
   - Repo → Settings → Pages → Deploy from branch → pick this branch → `/ (root)`.
   - GitHub gives you a URL like `https://<user>.github.io/<repo>/`.
2. Open that URL in **Safari** on your iPhone (must be Safari, not Chrome — only Safari supports "Add to Home Screen" as a standalone app on iOS).
3. Tap the **Share** button → **Add to Home Screen** → **Add**.
4. Launch GymBro from your Home Screen. It opens full-screen, with no Safari address bar, and works offline after the first load.

No Mac, Xcode, or Apple Developer account needed — this is a Progressive Web App (PWA), which is the only path to a real installable iPhone app without going through the App Store.

## Files

- `index.html` — the app (vanilla HTML/CSS/JS, no build step, no external dependencies).
- `manifest.webmanifest` — app name/icons/theme for "Add to Home Screen".
- `sw.js` — service worker that caches the app for offline use.
- `icons/` — home-screen icons.

## Local development

```
python3 -m http.server 8000
```

Then open `http://localhost:8000` in a browser (use responsive/device mode to preview at iPhone dimensions).
