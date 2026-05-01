# SafeHer — Women Safety Analytics Platform
### SIH Problem Statement: Women Safety Analytics

A full frontend prototype for the Smart India Hackathon "Women Safety Analytics" problem statement.

---

## Features
- **Live Dashboard** — Real-time stats, incident feed, hourly pattern chart
- **Safety Heatmap** — Geospatial heatmap with risk zones (powered by Leaflet + heatmap.js)
- **Incident Reporting** — Anonymous report form with evidence upload, severity picker, geolocation
- **Analytics** — Incident type breakdown, day-of-week patterns, silence index, confidence scores
- **Safe Route Finder** — Route scoring against heatmap data
- **Alerts & SOS** — SOS modal with step-by-step status, alert feed
- **Confidence-weighted zones** — Grey hatched "uncertain" zones (low data ≠ safe)

---

## Run locally (VS Code / any browser)

### Option 1 — Live Server (recommended)
1. Open folder in VS Code
2. Install the **Live Server** extension (ritwickdey.LiveServer)
3. Right-click `index.html` → **Open with Live Server**

### Option 2 — Python
```bash
cd women-safety-app
python -m http.server 8080
# Open http://localhost:8080
```

### Option 3 — Node.js
```bash
npx serve .
```

> **No build step needed.** Pure HTML + CSS + JS.

---

## Project Structure
```
women-safety-app/
├── index.html          # Main HTML shell + all pages
├── src/
│   ├── styles.css      # All styles (dark theme, responsive)
│   ├── app.js          # Navigation, maps, charts, form logic
│   └── data.js         # Mock incident data (Mumbai coordinates)
└── README.md
```

---

## Tech Stack
| Library | Purpose |
|---|---|
| Leaflet.js | Interactive maps |
| Leaflet.heat | Heatmap overlay |
| Chart.js | Analytics charts |
| CartoDB tiles | Dark map tiles |
| Google Fonts (Syne + DM Sans) | Typography |

All loaded via CDN — no npm install needed.

---

## Key Design Decisions (for SIH presentation)

1. **Silence Index** — Zones with high footfall but low reports are flagged as high under-reporting risk, not "safe"
2. **Uncertain zones** — Grey hatched overlay instead of green (absence of reports ≠ safety)
3. **Anonymous reporting** — No login required, no identity stored
4. **Confidence-weighted scoring** — Each zone has a data confidence score factored into the risk display
5. **Multi-source signals** — Incident reports + lighting data + footfall index combined for route scoring

---

## Screenshots
Run locally to see the full interactive prototype.

---

*Built for Smart India Hackathon | College Project*
