# Panchangam

Panchāṅgam — Deployment Guide
================================

This folder contains a complete, self-contained Panchāṅgam web app.


OPTION A — WINDOWS (quickest)
-----------------------------
1. Copy this entire "panchanga-deploy" folder anywhere on your PC.
2. Double-click  launch-edge.bat
   → The app opens in Microsoft Edge.

That's it. The HTML file runs entirely offline except for the weather
widget (which calls Open-Meteo).


OPTION B — ANDROID "INSTALL AS APP" (Progressive Web App)
---------------------------------------------------------
To get an app-like experience on Android (home-screen icon, no browser
chrome, works offline), you need to serve these files over HTTPS.

The easiest free host is GitHub Pages:

1. Create a new GitHub repository (e.g. "panchanga").
2. Upload these four files to the repository:
      index.html
      manifest.json
      sw.js
      README.txt   (optional)
3. Go to  Settings → Pages → Source → "Deploy from a branch"
   Pick the main branch, root folder (/), and Save.
4. After a minute or so your site will be live at:
      https://<your-username>.github.io/panchanga/
5. Open that URL in Chrome on your Android phone.
6. Chrome will show a banner: "Add Panchāṅgam to Home screen"
   (or tap the ⋮ menu → "Install app" / "Add to Home screen").
7. The app now lives on your home screen, launches full-screen,
   and works offline (except weather).

Other free HTTPS hosts that work: Netlify, Cloudflare Pages, Vercel.


FILES IN THIS PACKAGE
---------------------
  index.html      The complete app (HTML + CSS + JS, all-in-one)
  manifest.json   PWA manifest (icon, name, display mode)
  sw.js           Service worker (offline caching)
  launch-edge.bat Windows launcher (opens index.html in Edge)
  README.txt      This file