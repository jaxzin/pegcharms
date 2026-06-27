# Through-Hole Band Clasp — CAD Viewer

An interactive **3D CAD viewer + dimensioned engineering drawing sheets** for four
adjustable "through-hole silicone band clasp" concepts, all sized to a real Ø20 mm
bead-chain exercise band.

**Live site:** https://jaxzin.github.io/pegcharms/ &nbsp;*(once GitHub Pages is enabled — see below)*

## The four designs

| | Design | Mechanism |
|---|---|---|
| **A** | Hex Drop-Pin Buckle | Captive knurled hex pin drops through both layers of the doubled band; hex flats lock rotation |
| **B** | Twin-Prong Snap Plate | Two hex prongs snap through into a catch plate with real through-holes |
| **C** | Threaded Hex Clamp | Hex stud with a real helical M5 thread; knurled cap screws down to clamp |
| **D** | One-Piece Press-Stud | A single solid hex stud with a mushroom head — press the silicone over it and it snaps captive |

## Features

- Orbit / zoom 3D view, with **Explode**, **Wire**, and **Band** toggles
- Four metal finishes (incl. Antique Bronze), cycled with **Finish**
- A per-design spec strip and a per-design **dimensioned SVG drawing sheet** (title blocks BC-001…BC-004),
  plus a shared, dimensioned band detail

## Tech

Single self-contained `index.html`, no build step — vanilla JS plus
[Three.js 0.160.0](https://threejs.org/) loaded at runtime via an import map pointing at
`https://esm.sh`, with fonts from Google Fonts. It needs an internet connection on open to
fetch Three.js and the fonts; everything else is inline. If the 3D engine is ever blocked, the
viewer degrades gracefully — the UI and the dimensioned drawing sheets still render.

## Viewing locally

Because it uses an ES-module import map, open it through a local web server rather than `file://`:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000/
```

## Publishing on GitHub Pages

The whole site is just `index.html` at the repo root. To go live:

1. Merge this to the `main` branch.
2. **Settings → Pages → Build and deployment → Deploy from a branch**, choose `main` and `/ (root)`.
3. The site publishes at https://jaxzin.github.io/pegcharms/.
