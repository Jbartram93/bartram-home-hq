# Bartram Home HQ

Kitchen dashboard for the family — the layout inspired by
[joelgaff/home-hq](https://github.com/joelgaff/home-hq) (Rails), rebuilt as a
zero-maintenance static page. Data lives in `data.py`; the page is generated
by `dashboard.py` and deployed to GitHub Pages automatically.

## Edit anything

- **Events** → `EVENTS` in `data.py` (`d(0)` = today, `d(1)` = tomorrow)
- **Chores** → `TODOS` — checked circles reset at midnight, tap on the frame
- **Dinner** → `DINNER_MENU`
- **Countdowns** → `COUNTDOWNS`
- **People** → `PEOPLE_COLORS` (one line per person)

Or just **text Hermes**: "Jessie hair apt tomorrow 6pm" and it edits for you.

## Deploy

Push to `main` → GitHub Actions rebuilds + publishes in ~1 min, then every
30 min on a schedule. Live at: https://jbartram93.github.io/bartram-home-hq/

## Frame compatibility

Everything is 2015-safe on purpose: **no CSS variables, no CSS grid, no
`gap`** — the Frameo/AEEZO WebView 44 (Android 6) drops those silently and
the page renders unstyled. Hardcoded hex colors + flexbox only.
