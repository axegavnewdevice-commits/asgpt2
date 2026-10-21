# Arabic Scrabble — responsive PWA

This package preserves the original game logic, on-screen wording, palette, Arabic font choices, board, tiles, and controls. It adds responsive portrait/landscape layout behavior and PWA installation/offline-shell files.

## Put it on GitHub

1. Extract this ZIP.
2. Upload **the contents** of the extracted folder to the root of your GitHub repository (so `index.html`, `manifest.webmanifest`, `sw.js`, and `vercel.json` are at the repository root).
3. Commit and push.

## Deploy on Vercel

Import the GitHub repository into Vercel. Select **Other** as the Framework Preset. Leave the Build Command empty and set the Output Directory to `.` (the repository root). Deploy over HTTPS.

## Install on devices

- **Android / desktop Chromium browsers:** open the deployed HTTPS site and use the browser's Install app or Add to Home screen option.
- **iPhone / iPad:** open the deployed HTTPS site in Safari, tap Share, then Add to Home Screen.
- The manifest allows either portrait or landscape; the page adapts the layout instead of forcing an orientation.

## Offline behavior

The HTML shell and icons are precached by the service worker. External Tailwind, Firebase, and Google Fonts assets are cached after they have loaded online once. Because those existing dependencies remain external and the game originally relied on them, first launch and full functionality are not guaranteed offline until the dependencies have been cached.

## Vercel configuration

`vercel.json` sets useful cache headers for the service worker, manifest, and icons. This is a static site; no build step is required.
