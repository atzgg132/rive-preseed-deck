# Rive — Preseed · $350K

Investor deck for [rive.work](https://rive.work) *(not rive.app)*. Single self-contained HTML file. 12 slides, Michael Seibel / YC seed structure.

Open `index.html`. That is the deck.

## Open locally

Double-click `index.html`, or from this folder:

```bash
python3 -m http.server 8080
```

Then visit [http://localhost:8080](http://localhost:8080).

A static server is optional — Chrome/Safari/Firefox can open the file directly. Google Fonts (Outfit) need a network connection for the intended type; system sans is the fallback.

## Navigate

| Input | Action |
| --- | --- |
| `←` `→` `↑` `↓` Space, click, swipe | Previous / next |
| Click left ~28% of the slide | Previous |
| `O` | Slide overview (Esc to close) |
| `P` | Print / Save as PDF |
| `Home` / `End` | First / last |
| `#3` in the URL | Deep-link to slide 3 (hash updates as you move) |

## Print to PDF

1. Press `P`, or `Cmd-P` / `Ctrl-P`.
2. Destination: **Save as PDF**.
3. Paper: **Landscape**. Chrome should pick **13.333 × 7.5 in** (16:9). If not, choose a widescreen landscape size and **zero margins**.
4. Turn **Background graphics** on so cream and navy print.
5. Headers/footers off.

You should get 12 pages, one slide each. On-screen chrome (progress, arrows, hint, overview) is hidden.

Headless Chrome (optional):

```bash
google-chrome --headless --disable-gpu --no-pdf-header-footer --print-to-pdf=rive-preseed.pdf index.html
```

## Deploy

The site is static. `index.html` lives at the repo root.

**GitHub Pages** — Settings → Pages → Deploy from a branch → `main` → `/ (root)`.

**Vercel** — Import the repo. Framework preset: Other. Output directory empty / `.`. The root `index.html` is the app.

No build step, no env vars, no backend.

## Content lock

Locked copy lives in the deck. Do not invent ARR, paid users, Remit-as-live, Calendar, take rates, or tiers. Traction is **deck-proposed / Arnav audits**: lead with **~25 deeply activated** and the definition on the same slide. Market math that is not a census is labeled **ASSUMPTION**. Ask is **$350K** runway to prove one loop.

## Files

- `index.html` — the deck (HTML + CSS + JS, no bundler)
- `README.md` — this file
