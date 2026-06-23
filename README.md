# 🌀 Hurricane Dorian — Power Outage Progression (2019)

An interactive map visualizing the progression of power outages across the southeastern US during Hurricane Dorian (August 30 – September 10, 2019) and the subsequent restoration efforts, broken down by county.

**Live site:** https://\<your-username\>.github.io/hurricane-dorian-outages/

---

## Features

- **Animated time-lapse** of hourly power outages across 373 counties in FL, GA, SC, NC, and VA
- **Dark OpenStreetMap** base layer via CARTO
- **County-level circles** scaled and colored by outage severity
- **Heat overlay** showing intensity hotspots
- **Real substation locations** (41 substations across the five states) with voltage class info
- **Feeder backbone** (115–500 kV transmission lines) and **distribution laterals** (12.47 kV)
- **Storm phase indicator** tracking Dorian's progression
- **Live statistics panel**: customers out, counties affected, hardest-hit county, % restoration vs. peak
- **Playback controls**: play/pause, step forward/back, 5 speed settings
- **Top-30 county list** with bar charts, clickable to fly-to on map

---

## Data Sources

| Dataset | Source |
|---|---|
| Power outage counts | EIA Power Outage Monitor (Aug–Sep 2019) |
| County FIPS / centroids | US Census TIGER |
| Map tiles | OpenStreetMap / CARTO Dark Matter |
| Substation locations | EIA Form 860, OpenStreetMap |
| Transmission lines | EIA, utility annual reports |

---

## Setup — GitHub Pages

1. **Fork or clone** this repository
2. In your repo, go to **Settings → Pages**
3. Set Source to **Deploy from a branch**, branch `main`, folder `/` (root)
4. Click **Save** — your site will be live at `https://<username>.github.io/<repo-name>/`

No build step required — this is pure HTML/CSS/JS.

---

## Project Structure

```
hurricane-dorian-outages/
├── index.html          # Main interactive page
├── README.md
└── data/
    ├── outages.json    # Hourly outage records (4,890 rows, 157 hours)
    ├── counties.json   # County centroids (374 counties, 5 states)
    ├── substations.json # 41 real substation locations
    └── grid.json       # 17 backbone feeders + 16 laterals
```

---

## Hurricane Dorian Timeline

| Date | Event |
|---|---|
| Aug 24 | Dorian forms as tropical storm |
| Aug 28 | Reaches hurricane strength |
| Aug 30 | First outages recorded in Florida |
| Sep 1–2 | Cat 4/5 over Bahamas; grazes FL coast |
| Sep 4–5 | Moves along GA/SC coast |
| Sep 6 | Makes landfall near Cape Hatteras, NC (Cat 1) |
| Sep 6–7 | Peak outages: ~250k customers across NC, SC, VA |
| Sep 8–10 | Restoration underway; tracked dataset ends |

---

## License

Data sourced from US government open data. Map tiles © OpenStreetMap contributors, © CARTO.
