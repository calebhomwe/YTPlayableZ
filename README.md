# YT Playable Z - Mini Life Sim

A touch-first life-sim playable: one character, a four-room house, six needs (hunger, bladder,
energy, hygiene, fun, social) and objects to click. Includes autonomy, 1x-60x speed and
save/load. A single HTML file drawn with Canvas 2D, no build step, no network
(`three.min.js` sits next to it but the game does not load it).

## Play / Test

- **Play online:** https://calebhomwe.github.io/YTPlayableZ/ (deployed by
  `.github/workflows/pages.yml` on every push to `master`, once Pages is enabled in
  Settings → Pages → Source: GitHub Actions).
- **Play locally:** `python3 -m http.server 8000` in this folder, then open http://localhost:8000
  (the root page redirects to `3D browser games/`).
- **Test:** `npm install --no-save playwright@1.56.1 && npx playwright install chromium && node .github/smoke.mjs index.html "3D browser games/index.html"`
  loads both pages in headless Chromium and fails on page errors or missing files. CI runs the
  same check in `.github/workflows/smoke.yml`.
