# garrettidler.com

Static apps published by GitHub Pages from `main` at the repository root.
`CNAME` preserves the canonical domain `www.garrettidler.com`.

- `/`: app links; old `?g=...` Push Fight links redirect to `/pushfight/`, preserving query parameters and fragments.
- `/pushfight/`: generated Vite build. In `../pushfight`, run `npm run test` and `npm run deploy` to build, replace only this app, commit it, and push this repository.
- `/sphere_hunter.html`: copied from `../alex_game/sphere_hunter_speed.html`. Its graphics and audio are generated in-browser; Three.js 0.185.1 loads from jsDelivr (including its relative core module). Internet access to that CDN is required.

- `/nfl_elimination/`: NFL Quick Pick, copied from `../nfl_elimination/index_8bit.html` to `nfl_elimination/index.html`. Self-contained, including its pixel font. Update by copying that file again, checking locally, then committing and pushing.

To update Sphere Hunter, copy the source HTML to `sphere_hunter.html`, test it via a local HTTP server (`python3 -m http.server 8000`), then commit only the intended files and push `main`. If new external assets are introduced, place app-specific local assets in a dedicated directory and update their references.

Keep generated app updates inside their own paths; do not replace the root homepage or other apps.
