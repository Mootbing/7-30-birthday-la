# 7/30 Birthday LA Day Plan

Interactive OpenStreetMap itinerary for **Thursday, July 30, 2026**:

**Santa Monica → Beverly Hills → Hollywood → Griffith Observatory → Uchi West Hollywood**

[Open the GitHub Pages site](https://mootbing.github.io/7-30-birthday-la/)

## Features

- Interactive OpenStreetMap map rendered with Leaflet
- OSM/OSRM driving and walking routes calculated in the browser
- Scheduled time versus routing baseline, estimated traffic padding, gaps, and arrival slack
- Exact itinerary for Oceana, Greystone, Beverly Hills, Avra, Rodeo Drive, Hollywood, Griffith, and Uchi
- Confirmed Avra and Uchi reservations
- Downloadable calendar itinerary embedded directly in the site
- Responsive desktop and mobile layout

## How it is packaged

The full static planner is gzip-compressed and divided into `p0.txt` through `p7.txt`. `index.html` assembles and decompresses those chunks in the browser. This keeps every repository file small while preserving the complete interactive site.

## Run locally

No build step is required:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## GitHub Pages

`.github/workflows/pages.yml` publishes the static files with GitHub's official Pages actions whenever `main` changes.

## Routing note

Driving durations are OSM routing baselines plus planning buffers. They are not live Uber or live-traffic ETAs.
