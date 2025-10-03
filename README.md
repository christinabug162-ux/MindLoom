
# MindLoom – PWA (no build setup)

This folder is a ready-to-upload **Progressive Web App**. It uses React from a CDN and runs your JSX using Babel in the browser so you don't need Node or a bundler. It's perfect for GitHub Pages and quick testing.

## Files
- `index.html` — loads React, your app code, and registers the service worker.
- `manifest.webmanifest` — PWA metadata (name, icons, colors).
- `service-worker.js` — enables install + offline.
- `assets/icon-192.png`, `assets/icon-512.png`, `assets/maskable-512.png` — app icons (replace later if you have brand assets).

## How to publish on GitHub Pages
1. Create a **new public repo** on GitHub (for example `mindloom-pwa`).
2. Upload all files in this folder to the repo root.
3. In GitHub → **Settings** → **Pages**:
   - Set **Source** to `Deploy from a branch`.
   - Select the `main` branch and `/ (root)` folder. Save.
4. Wait ~30–60 seconds; your site will appear at `https://<username>.github.io/<repo-name>/`.
5. Open the site on your phone → **Add to Home Screen** to install as an app.

## How to package for Google Play
1. Visit **https://www.pwabuilder.com/** and paste your GitHub Pages URL.
2. Run the checks and click **Build my PWA** → **Android**.
3. Download the generated `.aab` and follow PWABuilder's steps to submit to the **Google Play Console**.
4. Tip: To pass PWA checks, keep HTTPS (GitHub Pages is HTTPS), include a manifest (done), and a working service worker (done).

## Customization
- Replace icons in `assets/` with your own artwork (keep the same sizes/filenames).
- Change colors/text in `manifest.webmanifest` and `<meta name="theme-color">` in `index.html`.
- For performance later, you can migrate to a bundler (Vite/Parcel) and move the JSX out of `index.html`.
