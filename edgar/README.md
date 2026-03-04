# EDGAR GHG Emissions Explorer

Interactive visualization of EDGAR v2025 greenhouse gas emissions by sector and country (1970–2024).

## Files

- `index.html` — main visualization (single-page app, no build step needed)
- `edgar_data.json` — processed data from EDGAR Excel (~2.2 MB)
- `process_data.py` — script to regenerate data from the original Excel

## Features

- Country search and selection (223 countries)
- Year range slider (1970–2024)
- Sector checkboxes with color coding (37 sectors)
- Chart types: Stacked Bar, Grouped Bar, Lines, Area
- Unit toggle: Gg CO₂eq / Mt CO₂eq
- Peak year and latest year totals

## Data Source

JRC EDGAR v2025 — https://edgar.jrc.ec.europa.eu/dataset_ghg2025
GWP-100 AR5, fossil emissions only, IPCC 2006 sector classification.

## To update with new EDGAR data

```bash
pip install pandas openpyxl
python process_data.py
```
