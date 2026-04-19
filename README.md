# Jerry Countdown

A single-page site that counts down to **January 1, 2029** — the first day Jerry Reinsdorf can sell his controlling interest in the Chicago White Sox to Justin Ishbia. Pure HTML/CSS/JS, no build step, no dependencies.

## Deploy

Drag the folder into the Vercel dashboard, or push to GitHub and import the repo. No build settings needed — it's a static `index.html`.

## Configure

To swap the target date (e.g. to the pessimistic 2034 fallback), edit the `TARGET_DATE` const at the top of the `<script>` block in `index.html`. To add roasts, append strings to the `roasts` array — no other code changes needed.

## Changelog

### v1.2.0 — 2026-04-18
- Replaced the writer's-room roasts with **10 verified real-world quotes** about Reinsdorf's ownership, pulled from Defector, the Chicago Sun-Times, the Chicago Tribune, and The Athletic. Each rotating card now shows the quote plus a clickable attribution (author, outlet, date) linking back to the source article.

### v1.1.0 — 2026-04-18
- Added on-page timeline toggle: **He goes willingly** (Jan 1, 2029) vs **Ishbia drags him out** (Nov 1, 2034). Choice is persisted in `localStorage`. Subhead updates to match the active scenario, and a small footnote explains why both dates exist.

### v1.0.0 — 2026-04-18
- Initial build: countdown timer (D/H/M/S), 10 rotating roasts on a 6s crossfade, mobile 2x2 layout, reduced-motion support, endgame swap when the timer hits zero.
