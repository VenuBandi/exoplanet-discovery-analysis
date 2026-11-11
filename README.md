# Exoplanet Discovery Analysis

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://python.org)
[![Stars](https://img.shields.io/github/stars/VenuBandi/exoplanet-discovery-analysis?style=social)](https://github.com/VenuBandi/exoplanet-discovery-analysis)

Data story analyzing the explosive growth of exoplanet discoveries — from rare detections to **6,147 confirmed worlds** — using the NASA Exoplanet Archive TAP API.

---

## Story

For centuries, humanity knew only the planets in our solar system. After the 1990s, discoveries accelerated — and after Kepler launched in 2009, they exploded. This project asks: **what changed, and why?**

## Key Findings

| Insight | Number |
|---|---|
| Total confirmed exoplanets (Mar 2026) | **6,147** |
| Discoveries since 2009 | **~95%** |
| Transit method share | **~73%** |
| Kepler + TESS + K2 combined share | **~65%** |

## Data Source

**NASA Exoplanet Archive** via TAP API — `pscomppars` table  
Live query at: `https://exoplanetarchive.ipac.caltech.edu/TAP/sync`

Fields used: `pl_name`, `disc_year`, `discoverymethod`, `disc_facility`, `pl_rade`, `pl_orbper`

## Analysis

The notebook walks through four charts that build the narrative:

1. **Discovery curve** — annual count + cumulative, showing the exponential-like growth after 2009
2. **Method breakdown** — transit detections dominate; radial velocity mattered early but doesn't explain the boom
3. **Top facilities** — Kepler, TESS, K2 account for two-thirds of all confirmed planets
4. **Radius vs orbital period** — most planets cluster at short periods with modest radii, unlike our solar system

## Repo Structure

```
exoplanet-discovery-analysis/
├── notebooks/
│   └── exoplanet_analysis.ipynb
├── docs/
│   ├── exoplanet_data_story_presentation_with_sources.pptx
│   └── exoplanet_reflection.docx
└── data/                   # output charts saved here
```

## Setup

```bash
git clone https://github.com/VenuBandi/exoplanet-discovery-analysis
cd exoplanet-discovery-analysis
pip install -r requirements.txt
jupyter lab notebooks/exoplanet_analysis.ipynb
```

The notebook queries the NASA TAP API live — no data download needed.

## Stack

`Python` · `Pandas` · `Matplotlib` · `Seaborn` · `requests` · NASA TAP API
