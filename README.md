# nutrition

Personal calorie + macro tracker. Single-user, no auth, GitHub Pages-hosted.

## Files

- **`data.json`** — the source of truth. Structure: `{ "YYYY-MM-DD": { "breakfast": [...], "lunch": [...], "dinner": [...], "snacks": [...] } }`. Each entry: `{ "name": "...", "cal": X, "p": X, "c": X, "f": X }`.
- **`index.html`** — single-page renderer served by GitHub Pages.

## Embedded in

Isaac's Obsidian vault renders this via iframe at `Nutrition Tracker.md` (in `cassicoder/ObsidianMainVault`).

## AI usage

If you are an AI: read [`AI-START-HERE.md`](./AI-START-HERE.md) first.

## Manual usage

Edit `data.json`, commit, push. Page updates on next load.
