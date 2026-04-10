# Cursor Usage Dashboard

A **single-file** dashboard you open in the browser: upload Cursor’s usage CSV, parse and chart it **locally**—no backend or build step.

## Features

| Area | What it does |
|------|----------------|
| **KPIs** | Request count, total tokens, actual overage cost, no-subscription cost estimate, etc. |
| **Activity calendar** | GitHub-style contribution heatmap; **click a day** for a modal with that day’s **`model × kind × tokens`** roll-up |
| **Token trend** | Auto **daily / weekly / monthly** buckets by span |
| **Hourly heatmap** | Weekday × hour token distribution |
| **Included vs Overage** | Included vs on-demand token trends |
| **Model breakdown** | Donut chart by **real model names** (not a coarse premium/standard split) |
| **Cost estimate** | Infers unit rates from on-demand rows; compares actual overage vs a “no plan” estimate |

Also: **range chips** (7D–All + custom dates), **change file**, global CSV drag-and-drop. After a successful load, data is saved to **localStorage** so the next visit in the same browser opens straight to the dashboard (you can always upload a new CSV to replace it).

> Layout is desktop-oriented; a window **≥ 1440px** wide is recommended.

## How to use

1. Open `index.html` from the repo root in a browser (or your deployed URL).
2. **Select or drop** a `.csv` file (drag-and-drop works on the dashboard too).
3. Use the top chips for the time range; **Custom** uses the date inputs.

All processing stays on your machine—nothing is uploaded to a server.

## Where the CSV comes from

In Cursor: **Settings → Usage → Export CSV** (wording may vary slightly by version).

## Deploy (e.g. GitHub)

Push the repo to GitHub, then enable **GitHub Pages** (Settings → Pages → branch `main`, folder `/ (root)`). The site serves `index.html` at the root.

Any static host (Vercel, Netlify, etc.) works as well—**no** framework or build command required.

## Tech

- One file: `index.html` (HTML + CSS + vanilla JS)
- Charts: hand-written **SVG**, **no npm** dependencies
