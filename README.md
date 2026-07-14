# Fontastic Find

A fast, self-service browser for the entire Google Fonts catalog, built to make finding the right typeface actually quick. Filter the whole catalog by category, weight, and style. Preview faces in your own words. Audition pairings in your own layout. All the things the official directory makes slow.

Everything runs client-side. No build step, no API key, no server required.

## What it does

**Find**
- Search by name, filter by category (serif / display / sans / script / mono).
- **Has-italic** and **variable** toggles, plus a minimum-weights filter.
- **Hide overused** — drops the ~50 most ubiquitous families so you're browsing the distinctive end on purpose.
- Sort by popularity, **rarest-first**, or A–Z.

**Judge — on your own content**
- **Project Profiles:** define your own stack of specimen lines — each with its own text, size, weight, italic, ALL-CAPS, and an optional "render in the paired body font" flag. Add, remove, and reorder lines. Every card re-renders in *your* layout.
- Real weights only: fonts load with their actual weight set and `font-synthesis: none`, so you never see a browser-faked bold. Want to compare weights? Add two header lines at different weights.
- **Pairing mode:** lock any face as the body font and audition display faces above it.
- Zoom, and a light/dark toggle to judge on either ground.

**Keep**
- **★ Favorites** — global, across every project.
- **⚑ Shortlist** — per-project candidate pools (separate from favorites).
- **Blocklist** — banish a face forever (Fraunces ships pre-blocked; unblock any time).
- **Copy code** — grab the `<link>` + `font-family` for any face.
- Profiles **export / import** as JSON. Favorites, shortlists, blocklist, and profiles all persist in your browser.

## Running it

- **Locally:** double-click `index.html`. (It loads `fonts-data.js` as a sibling; keep them together.) If your browser blocks the local data file, serve the folder instead — e.g. `python -m http.server` — and open `http://localhost:8000`.
- **Hosting:** it's fully static. Drop the folder on GitHub Pages, Netlify, or any static host.

## Data & attribution

- Font families and their metadata come from **[Google Fonts](https://fonts.google.com)**. The fonts are licensed under the **SIL Open Font License** or **Apache 2.0**; the tool loads them from Google's CDN at runtime.
- `fonts-data.js` is a dated snapshot of the public Google Fonts metadata (family, category, weights, italic availability, popularity rank). Refresh it any time by re-pulling the metadata and regenerating the file.
- Tool code is MIT licensed (see `LICENSE`).

Built by [Courtney Caldwell](https://courtneyccaldwell.com).
