# Astro Commander

A child-friendly space-exploration game packaged as an installable Progressive Web App (PWA).

## Run the game

Serve this folder from a local web server or HTTPS website; opening `index.html` directly as a `file://` URL will not enable PWA installation or offline caching.

For a quick local preview, run this command from the folder:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`. On a hosted website, publish the folder contents to the site root and use HTTPS. After the first visit, the service worker caches the game shell, game engine, manifest and icon assets for offline reopening.

## Install on a device

Use the browser's **Install app** or **Add to Home Screen** command. The Astro Commander logo is used for the tab favicon, Android/PWA icons and Apple home-screen icon.

## Progress and controls

Progress is saved automatically in this browser on this device. **Continue Game** resumes the saved setup or expedition. **New Game** asks before clearing the saved game and score history. Browser storage is local to this device and is not account-synced.

The language button switches between Arabic and English in the menu, setup/settings and NASA mission panel. Existing in-game science narration and minigame instructions remain primarily in Arabic.

## Tutorial

On a player's first trip (no saved game and no finished tutorial) an interactive training starts right after landing: move, jump, scan, mini-map, collect a sample, probe, enter a lab, rover, control center, survival resources and the Mission · NASA panel. Each step waits for the real action, can be skipped, and finishing it gives a one-time reward. Replay it any time with the **🎓 Tutorial** button in the game HUD or from Settings. State is stored in `localStorage` key `ac_tut`.

## Files

- `index.html` — game and interface
- `manifest.webmanifest` — install name, display mode and app icons
- `sw.js` — offline app-shell caching
- `assets/` — custom logo, icon sizes and locally bundled Phaser engine
- `LICENSE-PHASER.txt` — license notice for the bundled Phaser engine
