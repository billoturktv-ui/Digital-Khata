# DigiKhata — PWA (installable web app)

This is a standalone, self-contained version of the DigiKhata ledger app —
no build step needed. It runs entirely in the browser and stores data on
the device via `localStorage`, so it keeps working offline once loaded.

## Try it locally right now

Just double-click `index.html` to open it in your browser. Everything works,
though "Add to Home Screen" / offline caching needs it to be served over
http(s) (see below) rather than opened as a raw file.

## Install it like an app on your phone

Static hosting is the easiest path (all free):
1. Upload this whole folder to any static host — e.g. **Netlify Drop**
   (netlify.com/drop), **GitHub Pages**, **Vercel**, or **Cloudflare Pages**.
2. Open the resulting URL on your phone.
3. **Android (Chrome):** tap the menu (⋮) → **"Add to Home screen" / "Install app"**.
4. **iPhone (Safari):** tap the Share icon → **"Add to Home Screen"**.

It will then open full-screen with its own icon, like a real app — this is
a Progressive Web App (PWA), which is the closest thing to a native app that
doesn't require the Play Store / App Store.

## Files

- `index.html` — the entire app (React, loaded from a CDN, runs in-browser)
- `manifest.json` — app name/icon/theme metadata used by "Add to Home Screen"
- `sw.js` — service worker that caches the app shell for offline use
- `icons/` — app icons (192px, 512px, maskable)

## Want an actual APK / IPA instead?

See the sibling `digikhata-capacitor` package — it wraps this same app with
Capacitor so you can build a real installable Android/iOS binary.
