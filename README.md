# Ironman 70.3 Belgrade — Training Plan

Personal 21-week periodized training plan for Ironman 70.3 Belgrade, 13 September 2026.

Single-page web app, zero dependencies, all state stored locally in the browser. Synthesised from Matt Fitzgerald (Triathlete), Joe Friel, the official IRONMAN 16-week plan, MyProCoach, Triathlon Magazine Canada and 80/20 Endurance — adapted for a strong runner, ok cyclist, developing swimmer, with CFA and engineering exam windows, Peru travel, and a full-time job start baked into the periodization.

## Features

- 21 weeks × 7 days × multiple workouts per day
- Tap circle to mark sessions done, with satisfying animations
- Drag and drop workouts between days of the same week (press-and-hold on mobile)
- Progress tracked across total hours, by discipline, and per week
- Phase view for quick macro navigation
- Guide with intensity zones and periodization principles

## Running it

It's a single `index.html` — open it in any modern browser. No build, no server, no install.

## Hosting

Deployed via GitHub Pages from the `main` branch root. All files served statically.

## Changelog

### v2 — stable IDs, localStorage, icon, delete workout

- Drag-and-drop uses stable workout IDs instead of position-based keys. Moving a workout between days no longer duplicates cards or orphans completion state.
- Progress persists across browser sessions via `localStorage` (storage key bumped to `ironman_belgrade_v3`).
- Custom dark / red-glow home-screen icon with `apple-touch-icon` and PWA meta tags. Mini logo in the header, hero logo in the PHASES view.
- Workouts can be removed from the plan: expand a workout and tap **REMOVE FROM PLAN**. Empty days show a drop-target hint.

### v1

- Initial release: 21-week periodized plan, tap-to-complete, drag-to-reorder, phase / guide views.

## Race

- **Event:** Ironman 70.3 Belgrade
- **Date:** 13 September 2026
- **Distances:** 1.9 km swim / 90 km bike / 21.1 km run
