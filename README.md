# 🎨 PaletteSnap

Extract stunning color palettes from any image — right in your browser.

**🚀 Live demo:** https://alikali68.github.io/palettesnap/

## Features

- 🖼️ Drag & drop or browse to upload (PNG, JPG, WEBP, AVIF, SVG)
- ✨ One-click sample image — generated in-canvas, zero external assets
- 🎯 Dominant-color extraction via Canvas API (quantization + distinctness filtering)
- 📋 Click any swatch to copy HEX · hover reveals RGB
- 🔢 Adjustable palette size (4 / 6 / 8 / 10 colors)
- 💾 Export as CSS variables or download a 1200×630 PNG palette card
- 🌙 Dark, modern, fully responsive UI

## How it works

A single self-contained `index.html` — no build step, no dependencies beyond CDN
(Tailwind CSS, Google Fonts). The extraction pipeline:

1. Image is downscaled to ≤100px on an offscreen canvas for speed
2. Pixels are quantized to 4 bits per channel and counted by frequency
3. A Euclidean-distance filter keeps the final colors visually distinct

## Run locally

Just open `index.html` in a browser. That's it.
