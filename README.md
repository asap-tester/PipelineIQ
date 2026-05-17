# PipelineIQ 
> Your job search has a score. Time to see it.

## The Problem
Most job seekers manage 10–30 active applications across notes, emails, and memory. There is no tool that tells you which applications are going cold, which need a follow-up today, or whether your overall pipeline is healthy or stalling.

## Who It's For
- Final-year student managing 15 applications across different stages
- Recent graduate who sent applications 3 weeks ago and hasn't tracked since
- Anyone who has ever missed a follow-up window because they forgot

## What It Does
- Scores your entire pipeline 0–100 based on activity, stage distribution, and recency
- Flags applications that are cooling or likely ghosted before you lose them
- Surfaces a "Do Today" action queue so you always know the next right move

## How to Use
1. Download `index.html` or copy the raw file
2. Open in any browser — no install, no login, no internet required after first load
3. Log your applications — pipeline score and action queue update instantly

> First-time visitors see demo data so the interface is never empty. Clear it and add your own applications.

## Auto-Status Intelligence

| Days Since Applied (No Update) | Flag |
|---|---|
| 0–6 days | Active |
| 7–13 days | Warm — follow up soon |
| 14–20 days | Cooling — follow up now |
| 21+ days | Cold — likely ghosted |
| Stage = Rejected / Ghosted | Closed |
| Stage = Offer | Won |

## Pipeline Health Score Formula

```
base     = (active / total) × 40
recency  = (active apps updated last 7 days / active) × 30
stage    = (interviews + finals + offers) / active × 30
score    = base + recency + stage  (capped at 100)
```

| Score | Band |
|---|---|
| 75–100 | Healthy |
| 50–74 | Needs Attention |
| 25–49 | Stalling |
| 0–24 | Critical |

## Deploy to GitHub Pages
1. Create a new GitHub repo (e.g. `pipelineiq`)
2. Upload `index.html` as the only file in the repo root
3. Go to **Settings → Pages → Source: main branch → / (root)**
4. Your app is live at `https://[username].github.io/pipelineiq`

## Tech Stack
- Vanilla HTML / CSS / JS — zero dependencies
- `localStorage` for persistence — data never leaves the browser
- Fully offline after first load (fonts cached by browser)
- Single file — copy anywhere, run anywhere

## Roadmap
- [ ] Weekly pipeline digest (copy / export to clipboard)
- [ ] Response rate trend over time (7-day rolling chart)
- [ ] Stage change timestamps for accurate activity tracking
- [ ] PWA manifest for home screen install

## License
MIT — use, modify, distribute freely.
