# Analytics Overview

A sample product/marketing analytics dashboard, built as a single
self-contained `index.html` (no build step, no dependencies).

One view with a persistent time-range filter (7d / 30d / 90d / 1y), all
client-side with mock data generated from a seeded RNG (so numbers stay
consistent across reloads):

- **KPI row** — Revenue, Active Users, Conversion Rate, and Average Order
  Value, each with a period-over-period delta and an inline sparkline.
- **Revenue & Active Users** — a dual-line daily trend chart over the
  selected time range.
- **Revenue by Channel** — a bar chart showing each acquisition channel's
  share of total revenue.
- **Channel Breakdown** — a sortable table of channel performance (revenue,
  users, CVR, AOV, change vs. prior period, share of total) across Organic
  Search, Paid Search, Direct, Email, Social, and Referral.

All charts (sparklines, line chart, bar chart) are hand-rolled inline SVG —
no charting library. Includes a light/dark theme toggle.

## Running locally

It's a static file — open `index.html` directly, or serve it:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## Stack

Plain HTML/CSS/JS, no framework or build tooling, system font stack. All
data (revenue, users, conversion, channels) is mocked in `index.html` for
demonstration purposes only.
