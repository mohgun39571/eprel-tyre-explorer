# EPREL Tyre Explorer

A lightweight internal web tool for searching and exporting tyre energy label data from the [EU EPREL registry](https://eprel.ec.europa.eu) (European Product Registry for Energy Labelling).

## What it does

- **Search** tyres by brand or model name
- **Filter** by EU energy label class — fuel efficiency and wet grip
- **View** colour-coded EU label data: fuel efficiency, wet grip, and external rolling noise
- **Export** filtered results to CSV for offline analysis

## Why we built it

The EPREL public website is designed for individual product lookups. This tool is built for small teams that need to query, compare, and export tyre label data in bulk — for example, when benchmarking supplier ranges or auditing product compliance across a catalogue.

## Screenshots

> *(Add a screenshot of the app here once deployed)*

## Usage

The app runs entirely in the browser — no backend or installation required. Just open `index.html`.

### With the EPREL API (recommended)

1. Request a free public API key at:  
   `https://eprel.ec.europa.eu/screen/requestpublicapikey`
2. Open `index.html` and add your key to the script section:
   ```javascript
   const API_KEY = 'YOUR_API_KEY_HERE';
   ```
3. Uncomment the `fetchFromEPREL()` function and swap it in for the mock data block in `doSearch()`.

### Without an API key (demo mode)

The app ships with a built-in sample dataset of 30 tyres from major brands so you can explore the interface immediately without any setup.

## Data fields

| Field | Description |
|---|---|
| EPREL ID | Registry registration number |
| Supplier | Brand / manufacturer name |
| Model | Commercial product name |
| Tyre Size | Size designation (e.g. 225/45R17) |
| Load / Speed | Load capacity index and speed category symbol |
| Fuel Efficiency | EU label class A–G (A = most efficient) |
| Wet Grip | EU label class A–G (A = shortest stopping distance) |
| Noise (dB) | External rolling noise value in decibels |
| Noise Class | EU noise class A, B, or C |

## Tech stack

- Plain HTML, CSS, and vanilla JavaScript
- No frameworks, no build step, no dependencies
- Deployable as a single static file

## Deployment

Hosted via [GitHub Pages](https://pages.github.com/) at:  
`https://<your-username>.github.io/eprel-tyre-explorer`

## Data source

All tyre energy label data is sourced from the [EPREL public registry](https://eprel.ec.europa.eu), maintained by the European Commission under EU Regulation 2020/740 on tyre labelling.

## License

MIT
