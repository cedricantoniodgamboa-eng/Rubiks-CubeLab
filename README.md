# Cube Lab

A single-file puzzle-cube playground that runs in any browser and installs as an app. No build step, no dependencies.

## Features
- 2×2 to 5×5 cubes plus Pyraminx, Skewb, Megaminx, Square-1 and a Circle 3×3
- Drag-to-turn 3D cube, keyboard notation, solver, scrambler, pattern lab, sticker painting, tutorials
- Speedcube timer with ao5/ao12, inspection and +2/DNF
- Play: race bots, time attack, par puzzles, daily scramble, missions, badges, daily gift streak and a shop
- Camera: scan your real 3×3 into the app, or race a bot with your real cube and show all six faces to prove the solve
- Cube Creator for building your own connected 3D parts, themes, music and sound effects

## Run locally
Open `index.html` in a browser. For the camera and install features, serve it over http:

```
python3 -m http.server 8000
```
then visit `http://localhost:8000`.

## Publish on GitHub Pages
1. Create a new repository on GitHub and upload every file from this folder to the root.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
4. After a minute your app is live at `https://<your-username>.github.io/<repo-name>/`.

GitHub Pages uses HTTPS, which the camera requires.

## Install as an app
Open the live link on your phone and choose **Add to Home screen** (Chrome) or **Share → Add to Home Screen** (Safari). The service worker keeps the app working offline after the first visit.

## Android WebView
If you wrap the page in your own Android app, the camera needs the `CAMERA` permission in the manifest and a `WebChromeClient.onPermissionRequest` handler that grants it.

## Known limits
The built-in solver searches about 8 moves deep, so hints and solutions work for lightly scrambled cubes. A full two-phase solver is not included.

## License
MIT. See `LICENSE`.
