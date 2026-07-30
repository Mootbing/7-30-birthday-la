# 7/30 Birthday LA Day Plan

Interactive OpenStreetMap itinerary for **Thursday, July 30, 2026**:

**Santa Monica → Beverly Hills → Hollywood → Griffith Observatory → Uchi West Hollywood**

[Open the GitHub Pages site](https://mootbing.github.io/7-30-birthday-la/)

![Trip planner preview](assets/preview.webp)

## What is included

- OpenStreetMap tiles rendered with Leaflet
- OSM/OSRM driving and walking routes calculated in the browser
- Planned time versus routing baseline, distance, traffic scenarios, and schedule slack
- Exact calendar sequence with Uber, walking, reservation, and gap blocks
- Confirmed Avra and Uchi reservations
- Downloadable `.ics` itinerary

## Run locally

No build step is required. Serve the repository root with any static HTTP server:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish the prepared repository

After authenticating GitHub CLI as `Mootbing`, run one of these from the repository folder:

```bash
./scripts/publish.sh
```

```powershell
.\scripts\publish.ps1
```

The helper creates the public `Mootbing/7-30-birthday-la` repository, pushes `main`, enables GitHub Actions as the Pages source, and dispatches the deployment workflow.

## GitHub Pages

The workflow in `.github/workflows/pages.yml` builds a minimal `_site` directory and deploys it through the official GitHub Pages actions.

## Routing note

Driving durations are OSM routing baselines plus selectable planning multipliers. They are not live Uber or live-traffic ETAs.
