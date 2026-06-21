# Dashboard Examples

A small portfolio of end-to-end data pipelines: raw transactional data in, cleaned and modeled output out, rendered as interactive dashboards.

## Live demos

- [UK E-Commerce Performance](https://raymondapople-afk.github.io/Dashboard-examples/uk_ecommerce_dashboard.html)
- [Coffee Shop Performance](https://raymondapople-afk.github.io/Dashboard-examples/coffee_shop_dashboard.html)
- [Hotel Bookings Performance](https://raymondapople-afk.github.io/Dashboard-exaples/hotel_bookings_dashboard.html)

## What this demonstrates

Each dashboard is generated from a single, config-driven pipeline rather than three separate one-off scripts:

1. **Ingest** — read a raw CSV export with an arbitrary schema
2. **Clean** — handle missing values, duplicates, and invalid rows (e.g. cancellations, zero-price line items)
3. **Transform** — map source columns onto a standard schema via a per-dataset YAML config, with category/segment inference where the source data doesn't already provide it
4. **Export** — output both a flat CSV (for tools like Looker Studio) and structured JSON (for the web dashboards above)

The three examples deliberately span different business shapes — product/SKU sales, daily transaction volume, and lead-time/cancellation-based bookings — to test that the pipeline adapts via configuration rather than requiring new code per client.

## Tech stack

- **Pipeline:** Python (pandas), YAML-based client configs
- **Dashboards:** HTML/CSS/JS, Chart.js
- **Testing:** pytest, run against both fixture data and full real datasets

## Data sources

Built using public datasets (Kaggle) for demonstration purposes — not real client data.

## About

Built by Raymond Pople. [LinkedIn](#) · [Contact](#)
