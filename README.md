# AI Is Not Special — GFMI Boston

Web version of the talk. Single self-contained HTML deck. No build step.

## Files

```
gfmi-talk/
├── index.html              ← the deck (open this)
├── viz/
│   ├── epicycles.html      ← interactive geocentric/heliocentric (iframe on slide 4)
│   └── risk-surface.html   ← interactive 3D risk surface (iframe on slide 10)
├── .nojekyll               ← tells GitHub Pages to serve files as-is
└── README.md
```

## Run locally

Just open `index.html` in any modern browser. No server required for static viewing.

If you want the iframes to load properly (some browsers restrict `file://`), serve the folder over HTTP:

```bash
cd gfmi-talk
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy to GitHub Pages

1. Push this folder to a repo (it can be at the root, or under `/docs`, or any subfolder).
2. In **Settings → Pages**, set the source to your branch and folder.
3. Wait a minute for Pages to build, then visit:
   - `https://<user>.github.io/<repo>/` if `index.html` is at the repo root
   - `https://<user>.github.io/<repo>/gfmi-talk/` if it's in the `gfmi-talk/` subfolder

The included `.nojekyll` file disables Jekyll preprocessing so nothing in the HTML or JS gets mangled.

## Navigation

| Key                | Action              |
| ------------------ | ------------------- |
| `→` / `Space`      | Next slide          |
| `←`                | Previous slide      |
| `Home` / `End`     | First / last slide  |
| `F`                | Toggle fullscreen   |
| `?`                | Show/hide help      |
| `#5` in URL        | Jump to slide 5     |
| Click on slide     | Next slide          |

## Customization

All styling lives in the `<style>` block at the top of `index.html`. The Domino dark palette is defined via CSS custom properties:

```css
:root {
  --bg:        #0A0B0D;
  --mint:      #2DE2A0;   /* primary accent      */
  --cyan:      #4DD0E1;   /* ML / typed accent   */
  --pink:      #F87171;   /* risk / warning      */
  --yellow:    #F4D03F;   /* alt accent          */
  --pink-grad: #EC4899;   /* signature gradient  */
  /* ... */
}
```

Slides are 1920×1080 pixel canvases that scale to fit the viewport, so type and layout are pixel-perfect on any screen.
