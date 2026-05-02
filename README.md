# OpenCode Go — Model Comparison

A fast, interactive single-page app for comparing request limits across all models available to [OpenCode Go](https://opencode.ai/go) subscribers.

**Live site:** [https://preginald.github.io/opencode-go/](https://preginald.github.io/opencode-go/)

## What it does

- **Filterable table** — Search by model or provider, filter by category, and toggle models with/without published limits.
- **Multiplier preview** — Instantly see how limits scale at 1×, 5×, 10×, 25×, 50×, and 100×.
- **Bar chart** — Visual comparison of requests per 5-hour window across all known models.
- **Doughnut chart** — Relative share of total request budget by model.
- **Summary stats** — Highest limit, best value (requests per dollar), and free-tier baseline at a glance.

## Data source

All limits are sourced directly from the [OpenCode Go pricing page](https://opencode.ai/go). Models that are included in Go but do not have individually published limits on that page are noted as such.

## Tech stack

- React 18 (via CDN, no build step)
- Chart.js for visualisations
- Pure CSS with CSS variables for theming
- Hosted on GitHub Pages

## Running locally

Since there is no build step, you can open the file directly:

```bash
git clone https://github.com/preginald/opencode-go.git
cd opencode-go
open index.html
```

Or serve it with any static file server:

```bash
cd opencode-go
python3 -m http.server 8080
# open http://localhost:8080
```

## License

MIT
