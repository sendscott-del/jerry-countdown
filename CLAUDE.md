# Jerry Countdown — current state

> Read before touching. Update the moment an infra fact changes. Append to docs/SESSIONS.md each session. Lane: Personal/Family.

## What this is

Single-page joke/fan site counting down to **Jan 1, 2029** — the first day Jerry Reinsdorf can sell his controlling interest in the Chicago White Sox to Justin Ishbia. Rotating cards of 10 real, sourced quotes about the Reinsdorf ownership (Defector, Sun-Times, Tribune, The Athletic) with clickable attributions. Timeline toggle: "He goes willingly" (2029) vs "Ishbia drags him out" (Nov 1, 2034), persisted in localStorage. v1.2.1.

## Infrastructure

- **Pure static: one `index.html`. No build step, no dependencies, no framework, no database.**
- GitHub: `sendscott-del/jerry-countdown`. Deploy: drag folder into Vercel or import the repo — no build settings.

## Architecture snapshot

- Everything lives in `index.html`: `TARGET_DATE` const + `roasts` array at the top of the `<script>` block; countdown (D/H/M/S), 6s crossfade rotation, mobile 2x2 layout, reduced-motion support, endgame swap at zero.

## Rules for this repo

1. Keep it dependency-free — resist the urge to add a build step.
2. Config changes = edit the consts in `index.html` (README documents this).
3. Changelog lives in `README.md` — append a dated version entry per change.
4. Session docs: append a dated entry to `docs/SESSIONS.md` each session.

## Gotchas

- Quotes are real and attributed — don't swap in invented ones (v1.2.0 deliberately replaced fictional roasts with sourced quotes).
- Timeline choice persists in localStorage — test both scenarios after date logic changes.
