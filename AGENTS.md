# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **static HTML website** (Akaki Kuumeri's personal homepage) hosted on GitHub Pages (see `CNAME` → `akakikuumeri.com`). There is **no build step, no package manager, no backend, and no dependencies** — it is plain HTML pages plus JPEG image assets.

### Layout
- `index.html` — frameset shell: left `menu.htm` (sidebar nav) + right `top.htm` (content).
- `top.htm` — landing/content page. `puzzles/puzzles.htm` and `gaming/gaming.htm` are placeholder sections (intentionally near-empty tables — a blank content area below their headers is expected, not a bug).
- `image/bg.jpg`, `akaki-top.jpg` — image assets.

### Run locally (development)
Serve the repo root over HTTP (framesets and relative paths do not work over `file://`):

```
python3 -m http.server 8080
```

Then open `http://localhost:8080/index.html`. Any static file server works (`npx serve`, `php -S`, etc.).

### Lint / test / build
There is no lint, test, or build tooling in this repo. Verification is manual: load the site and confirm the sidebar links update the right content frame.
