# Kundali Open — Vedic Birth Chart Calculator

Free, open-source, client-side Vedic Kundali calculator. **No backend. No API keys. No data collection.**

## Live Demo
👉 `https://<your-username>.github.io/kundali-open`

---

## Features
- **North Indian chart** (SVG, drawn in browser)
- **12 planetary positions** with sidereal longitudes (Lahiri Ayanamsha)
- **Nakshatra + Pada** for every planet
- **Planetary dignity** (exaltation, debilitation, own sign)
- **12 houses** with sign assignments and planet placements
- **Vimshottari Dasha** timeline with current period interpretation
- **Yoga detection** (Gajakesari, Budha-Aditya, Pancha Mahapurusha, Mangal Dosha, Kaal Sarp)
- **Career, relationships, health** analysis per house lords
- **Remedies** — gemstones, mantras, donations per planet
- **Print / Save as PDF** support
- Fully responsive, mobile-first

---

## Calculation Methodology

| Element | Method |
|---------|--------|
| Ayanamsha | Lahiri (default), KP, Raman |
| Sun | Full VSOP87 truncated series |
| Moon | IAU 1980 truncated series (accurate ±0.3°) |
| Lagna | LST + obliquity formula (requires birth time) |
| Mars/Jupiter/Saturn | Mean elements + major perturbations (±1–2°) |
| Mercury/Venus | Mean elements + primary perturbation (±1°) |
| Rahu | Mean node (retrograde) |
| Ketu | Rahu + 180° |
| Dasha | Vimshottari (120yr cycle) from Moon Nakshatra |
| Houses | Equal house system from Lagna |

**Accuracy note:** Sun is highly accurate. Moon ±0.3°. Lagna requires correct birth time and timezone. Mars/outer planets ±1–2° — sufficient for sign-level readings but not degree-precise. For exact degrees, use Jagannatha Hora with Swiss Ephemeris.

---

## Deploy to GitHub Pages (5 minutes)

### Option A — Automatic (GitHub Actions)
1. Fork this repo
2. Go to **Settings → Pages → Source → GitHub Actions**
3. Push to `main` — auto-deploys

### Option B — Manual
1. Fork this repo
2. Go to **Settings → Pages → Source → Deploy from branch**
3. Select `main` branch, `/ (root)` folder
4. Save — live in ~60 seconds

---

## Repository Structure
```
kundali-open/
├── index.html              # Entire app (single file)
├── .github/
│   └── workflows/
│       └── deploy.yml      # Auto-deploy workflow
├── README.md
└── LICENSE
```

---

## Privacy & Ethics

- ✅ **Zero data transmission** — all calculations in browser JS
- ✅ **No cookies, no analytics, no localStorage**
- ✅ **No API keys required**
- ✅ **Educational purpose** — not a substitute for a qualified Jyotishi
- ✅ **Open source** — audit the code yourself

---

## Roadmap (future milestones)

- [ ] Swiss Ephemeris WASM port for degree-precise planets
- [ ] Navamsa (D9) chart
- [ ] Divisional charts (D2, D10)
- [ ] Hindi language toggle
- [ ] Antardasha (sub-period) breakdown
- [ ] Chart comparison / synastry
- [ ] PDF export with full chart image

---

## License
MIT — free to use, modify, distribute. Attribution appreciated.
