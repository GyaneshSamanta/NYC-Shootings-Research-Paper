<div align="center">
  <img src="docs/ydh.png" height="80" />

# Bullets Over Broadway

**A data-driven research paper on NYC shootings — built for Youth Data Hack by Team ByteBridgers.**

[![Hackathon](https://img.shields.io/badge/Built%20at-Youth%20Data%20Hack-purple.svg)](https://youth-data-hack.devpost.com/)
[![Live Site](https://img.shields.io/badge/Live-bullets--over--broadway.vercel.app-black.svg)](https://bullets-over-broadway.vercel.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<img src="docs/preview1.png" width="85%" />

</div>

---

## About

|        |                                                                                                  |
| ------ | ------------------------------------------------------------------------------------------------ |
| Who    | Team **ByteBridgers** — [Gyanesh Samanta](https://github.com/GyaneshSamanta) and [Priyadarsh S S](https://github.com/priyadarshss). |
| What   | A research paper + interactive Next.js site analyzing NYPD historic shooting incident data.       |
| When   | October 2023 — submitted to **Youth Data Hack**.                                                  |
| Where  | Hosted at [bullets-over-broadway.vercel.app](https://bullets-over-broadway.vercel.app/).          |
| Why    | Public datasets contain stories that policy debates ignore. We wanted ours to be unignorable.     |

## The Story

The prompt was open-ended: "Analyze a public dataset to gain insight into a social issue." We picked the **NYPD Shooting Incident Data (Historic)** because it's enormous, granular, and politically loaded. Every row is a shooting. Every column is a question — borough, precinct, time of day, perpetrator demographics, victim demographics, whether the incident ended in murder.

We started in a Jupyter notebook. Pandas to clean it, Matplotlib and Seaborn for distributions, Folium for a heatmap that made geography feel like fate. The patterns showed up fast: shootings concentrate in specific precincts, evening hours dominate, and the cross-tabulation of perpetrator vs. victim demographics tells a story the headlines flatten.

Then we layered analysis: K-Means clustering to find recurring "incident types" by precinct + time + day-of-week, and a separate notebook (`Analysis_Disparities_Suspect_Identification.ipynb`) probing disparities in suspect identification across groups.

The Next.js site at [bullets-over-broadway.vercel.app](https://bullets-over-broadway.vercel.app/) is the research paper made interactive — Leaflet maps for the geospatial layer, scrollable charts, and the conclusion served as a story rather than a PDF.

## Gallery

<div align="center">
  <img src="docs/preview2.png" width="80%" />
  <img src="docs/preview3.png" width="80%" />
  <img src="docs/preview4.png" width="80%" />
  <img src="docs/preview5.png" width="80%" />
</div>

---

## Tech Stack

**Analysis:** Python · Pandas · NumPy · Matplotlib · Seaborn · Folium · scikit-learn (K-Means)
**Web:** Next.js 13 · React · Chakra UI · Framer Motion · Leaflet / react-leaflet
**Data:** NYPD Shooting Incident Data (Historic) + NYC Police Precincts GeoJSON

## Repo Structure

```
Youth-Data-Hack/
├── Dataset/                                       # Raw NYPD CSV
├── JupyterNotebook/
│   ├── notebook.ipynb                             # Main EDA + clustering
│   ├── Analysis_Disparities_Suspect_Identification.ipynb
│   └── nyc-police-precincts.geojson
├── src/app/                                       # Next.js (App Router) site
├── public/images/                                 # Generated charts + map exports
└── docs/                                          # README assets
```

## Getting Started

**Run the notebooks:**

```bash
pip install pandas numpy matplotlib seaborn folium scikit-learn jupyter
jupyter notebook JupyterNotebook/notebook.ipynb
```

**Run the site:**

```bash
git clone https://github.com/GyaneshSamanta/Youth-Data-Hack.git
cd Youth-Data-Hack
yarn install   # or npm install
yarn dev       # http://localhost:3000
```

## Contributing

Open an issue first if you're proposing a methodology change — we want the analysis to stay defensible. UI/UX PRs welcome any time.

## License

[MIT](LICENSE).

## Credits

- **Team ByteBridgers:** [Gyanesh Samanta](https://github.com/GyaneshSamanta), [Priyadarsh S S](https://github.com/priyadarshss).
- **Data:** NYC Open Data — NYPD Shooting Incident Data (Historic).
- **Event:** [Youth Data Hack](https://youth-data-hack.devpost.com/).

<div align="center">
  <a href="https://github.com/GyaneshSamanta/Youth-Data-Hack/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=GyaneshSamanta/Youth-Data-Hack" />
  </a>
</div>
