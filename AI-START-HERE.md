# AI START HERE — Nutrition Tracker

> **You are an AI with zero context. Read this first.** Total read time: ~60 seconds.

---

## What this repo is

A minimal calorie/macro tracker for Isaac. Data lives in `data.json`. Frontend renders via GitHub Pages at the repo's pages URL. The tracker is **embedded into Isaac's Obsidian vault** via iframe at `Nutrition Tracker.md`.

Two files, that's it:
- **`data.json`** — the source of truth. All meals, all dates, all macros.
- **`index.html`** — the single-page renderer (GitHub Pages serves it).

---

## Who Isaac is (short)

18, Doral Miami, solo entrepreneur (TikTok Shop). Currently on a cut: ~2,100–2,200 cal/day, 180–200g protein target. Trains 3–4x/wk hypertrophy (machines + dumbbells, no bodyweight).

---

## How to log a meal (the canonical AI task here)

When Isaac mentions eating, **log it without asking for confirmation.**

1. Clone with PAT (from his server `.env`, never from chat)
2. Edit `data.json`:
   ```json
   {
     "2026-05-12": {
       "breakfast": [
         {"name": "Food Name", "cal": X, "p": X, "c": X, "f": X}
       ],
       "lunch": [...],
       "dinner": [...],
       "snacks": [...]
     }
   }
   ```
3. `git add . && git commit -m "Log [food] — [meal type]" && git pull --rebase origin main && git push`

Date key = `YYYY-MM-DD` (today). Meal type by time of day or Isaac's wording. Macros: `cal` calories, `p` protein g, `c` carbs g, `f` fat g.

**Add to the array. Don't overwrite existing entries.**

---

## Voice and style

Direct, no filler. When confirming a log, one line: `Logged: [food] — Xc / Yp / Zc / Wf`.

---

## NEVER

- ❌ Paste the PAT in chat or commit messages
- ❌ Ask "should I log this?" — just log it
- ❌ Edit `index.html` without explicit instruction — it's load-bearing
- ❌ Overwrite past dates — always append to existing entries

---

## Cross-repo

This repo is one of 8. See the parent vault (`cassicoder/ObsidianMainVault`) `REPO-MAP.md` for the full ecosystem.
