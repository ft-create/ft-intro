# FT 3D Intro — fareedtareen.com

A standalone intro/landing page for [fareedtareen.com](https://fareedtareen.com).

Your `ft_logo_centered.stl` is loaded and rendered in WebGL (three.js): the solid
splits into a light-gray base slab and a white letterform, which assemble in a
short machining-style animation and then orbit slowly. An **Enter Portfolio →**
button links through to the live site. Nothing here touches the existing
portfolio — it links to it.

## What's inside

| Path | Purpose |
|---|---|
| `index.html` | The intro page (markup + styles + module script) |
| `assets/ft_logo_centered.stl` | Your 3D monogram mesh (served to the page) |
| `assets/ft-logo.png` | Favicon / header mark |
| `vendor/three/` | Vendored three.js r160 (no CDN, no build step) |

## Preview locally

Any static file server works — no build step:

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

(It must be served over HTTP — `file://` won't load the STL or modules.)

## Deploy to GitHub Pages

1. Push these files to the `main` branch of this repo.
2. Repo → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save.
3. The site goes live at `https://ft-create.github.io/ft-intro/`.

## Use it as your real intro

Two options, neither touches your portfolio code:

- **Standalone intro URL** — share/point to the Pages URL above.
- **On your own domain** — upload these files to your hosting (same structure).
  If your portfolio moves, update the one link in `index.html`:

  ```html
  <a class="cta" href="https://fareedtareen.com">Enter Portfolio →</a>
  ```

## URL parameters

- `?spin=0` — start with the turntable paused
- `?theme=white` — start on the light plate (default is dark)
