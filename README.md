# Cursor Usage Dashboard

Open `index.html`, drop a Cursor usage CSV, and chart it in the browser. Nothing is uploaded.

## Charts

- **KPIs** — requests, tokens, on-demand spend, and a no-plan estimate
- **Activity calendar** — click a day for model × kind × tokens
- **Token trend** — daily, weekly, or monthly
- **Hourly heatmap** — weekday × hour
- **Within month** — average tokens per day from the 1st to that month’s real last day (28–31)
- **Model breakdown** — donut by model name
- **Cost estimate** — input, cache write, cache read, and output at [Cursor list rates](https://cursor.com/docs/models-and-pricing) (2026-09-25). Models without a list price use their own on-demand rows

Time range is 7D–All or custom dates. The last file stays in localStorage. Layout is for a desktop window at least 1440px wide.

## Use

Export CSV from Cursor **Settings → Usage**, then open `index.html` and select or drop the file.

## Deploy

GitHub Pages: branch `main`, folder `/ (root)`. Any static host works. One HTML file, hand-written SVG, no build.
