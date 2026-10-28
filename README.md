

https://github.com/user-attachments/assets/cf3b9d93-eec4-4e7b-a936-c9e1f137609e

# U.S. CMIP6 Temperature Map

An interactive web dashboard that visualizes average annual near-surface temperature (TAS) by U.S. state across multiple CMIP6 climate scenarios and years from 2015 to 2100.

This project combines a choropleth map of the continental United States with a state-level comparison chart, allowing users to compare a selected state against the national average for a chosen model and year.

## Project Overview

The visualization is designed to help users explore how projected temperatures change over time across the U.S. and how individual states differ from the national mean under a given climate model.

Key interactions include:

- Model selection from available CMIP6-style projections
- Year slider for exploring annual temperature patterns
- Hover tooltips for state-level temperature values
- Click-to-select a state and compare it against the U.S. average
- Animated, threshold-based legend for temperature ranges
- Downloadable project writeup in PDF form

## Features

- Interactive choropleth map of the U.S.
- State-by-state temperature values for each model and year
- Dynamic line chart comparing a selected state with the U.S. mean
- Temperature trend summary for the selected state
- Flexible legend and map highlighting
- Lightweight browser-based deployment without a build step

## Tech Stack

- HTML
- CSS
- JavaScript
- D3.js
- GeoJSON for U.S. state boundaries
- CSV-based climate dataset

## Data Source

The map uses a derived dataset in CSV format:

- `new_avg_states_model.csv`

The data includes state-level annual temperature values for multiple models and years. A geographic boundary dataset is loaded from a public mapping API and joined to the climate data for rendering.

## File Structure

```text
Project-3/
├── README.md
├── index.html
├── plot.css
├── plot.js
├── new_avg_states_model.csv
├── assets/
│   └── Project 3 Writeup.pdf
└── .git/ and .vscode/ (workspace/editor metadata)
```

## How to Run

Because this project loads D3.js from a CDN and reads local CSV/GeoJSON resources in the browser, there is no package installation or build process required.

1. Open the project folder in a browser.
2. Open `index.html` directly, or serve it with a simple local web server if preferred.
3. Use the model dropdown and year slider to explore the map.
4. Click a state to inspect its time-series trend compared with the U.S. average.

Example local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Usage Notes

- The dashboard is focused on the continental U.S. and excludes Alaska, Hawaii, and Puerto Rico for the main map view.
- The selected state view shows both the state’s projected temperatures and the national mean for the active model.
- The project includes a visible year marker and a temperature legend to help interpret the map.

## Project Writeup

A detailed project report is included here:

- `assets/Project 3 Writeup.pdf`

This document contains deeper background on the project goals, methodology, and interpretation of the climate data.

## License

MIT license

## Acknowledgments

- D3.js for interactive visualization tooling
- PublicaMundi mapping data for U.S. state geometry
- CMIP6-related climate model data used for temperature projections

## Summary

This repository is a compact, browser-based climate data exploration project that turns a large state-level dataset into an interactive map and time-series comparison tool. It is well suited for educational, analytical, or presentation use when communicating projected warming trends across the U.S.
