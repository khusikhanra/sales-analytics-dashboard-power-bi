# Sales Analytics Dashboard

A Power BI dashboard for analyzing chocolate sales performance across markets, product categories, and sales teams — built to answer where revenue is concentrated, which teams and regions are under/over-performing, and how shipment volume trends over time.

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data%20Analysis%20Expressions-yellow)
![Status](https://img.shields.io/badge/status-in%20progress-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Overview

This project models and visualizes a chocolate sales dataset (Feb 2023 – Feb 2024) covering 6,113 transactions across 6 countries, 22 products, and 25 sales reps. It's built as a portfolio piece demonstrating star-schema data modeling, DAX time intelligence, and Power BI report design — intended for recruiters, hiring managers, and other analysts reviewing BI/analytics engineering work.

## Key Metrics

| Metric | Value |
|---|---|
| Total Sales | $34,042,511.25 |
| Total Boxes Shipped | 2,077,844 |
| Transactions | 6,113 rows |
| Date Range | Feb 2023 – Feb 2024 |
| Products | 22 SKUs across 3 categories (Bars, Bites, Other) |
| Markets | 6 countries — USA, UK, Canada, India, Australia, New Zealand |
| Regions | Americas, APAC, Europe |
| Sales Reps | 25, across 4 teams (Yummies, Delish, Jucies, Tempo) |

## Preview

![Sales Analytics Dashboard Screenshot](assets/dashboard-screenshot.png)

*[Fill in: the header on this composite graphic says "8 Interactive Pages," but only 6 distinct pages are legible in the image (see Report Pages below) — reconcile that count, and swap in a GIF walkthrough if you have one: `![Dashboard Demo](assets/dashboard-demo.gif)`.]*

## Data Model

The semantic model is a star schema with one fact table, one shared dimension table, and a dedicated date table for time intelligence.

- **Shipment Data** (fact table) — one row per transaction: Sales Person, Geography, Product, Date, Sales ($), Boxes Shipped.
- **Dimension Data** (lookup table) — attributes for filtering and grouping: Product → Category → Cost per box; Geography → Region; Sales Person → Team.
- **Calendar Table** — a dedicated 396-day date dimension, marked as the model's date table to support DAX time intelligence functions (e.g. `DATESYTD`, `SAMEPERIODLASTYEAR`).

```
                 ┌───────────────────┐
                 │   Calendar Table   │
                 │   (396-day dim)    │
                 └─────────┬──────────┘
                           │ Date
                           │
┌────────────────┐   ┌─────▼──────────┐
│ Dimension Data  ├───┤ Shipment Data   │
│ (lookup table)  │   │ (fact table)    │
│                 │   │                 │
│ Product→Category│   │ Sales Person    │
│ →Cost per box   │   │ Geography       │
│ Geography→Region│   │ Product         │
│ SalesPerson→Team│   │ Date            │
│                 │   │ Sales ($)       │
│                 │   │ Boxes Shipped   │
└─────────────────┘   └─────────────────┘
```

## Report Pages

Six pages are legible in the dashboard preview. Descriptions below are inferred from the visible chart titles on each page — verify wording against the live report before publishing, and confirm whether the "8 Interactive Pages" claim in the banner refers to two additional pages not shown clearly in the screenshot.

| # | Page | Answers |
|---|---|---|
| 1 | Executive Overview | Top-line KPIs (sales, profit, margin %, shipments, boxes, avg selling price) plus sales trend, sales by product/geography/team, profit by region, and top 10 salespeople — a one-screen performance summary. |
| 2 | Sales Performance | Monthly sales trend, sales vs. profit, running total sales, month-over-month growth %, top/bottom 10 products, and sales by category. |
| 3 | Product Analysis | Product count, top products by sales and by profit, a sales-vs-profit scatter, and product contribution % — which SKUs and categories actually drive the numbers. |
| 4 | Geography Analysis | Sales by country and by region, profit by region, and a regional performance table (sales, profit, margin %, shipments, avg selling price by region). |
| 5 | Salesperson Performance | Top 10 reps by sales and by profit, a performance scatter plot, and detailed ranking/performance tables against target. |
| 6 | Time Intelligence | Monthly sales and profit trends, sales vs. previous year, running total sales, and a monthly performance breakdown — YoY and growth-rate views. |

*[Fill in: replace inferred descriptions with your own if they don't match the actual page content, and add any pages beyond these 6.]*

## Key DAX Measures

*[Fill in: paste the actual DAX measures used in the model. Do not use the examples below as-is — they are structural placeholders only, not verified code from this project.]*

```dax
Total Sales = [Fill in: actual measure formula]

Total Boxes Shipped = [Fill in: actual measure formula]

Sales YoY % = [Fill in: actual measure formula]

Avg Cost per Box = [Fill in: actual measure formula]
```

## Interactivity

*[Fill in: describe the actual interactive features implemented in the report, e.g.:]*
- **Slicers:** [Fill in: which fields — e.g. Region, Category, Date range]
- **Drill-through:** [Fill in: which page(s) support drill-through, and from where]
- **Bookmarks:** [Fill in: what states/views are bookmarked, if any]
- **Tooltips:** [Fill in: custom tooltip pages or default tooltips]

## Tech Stack

- **Power BI Desktop** — report authoring (PBIP project format)
- **DAX** — measures and calculated columns
- **Power Query (M)** — data transformation and shaping
- **Excel** — source data

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd Sales-Analytics-Dashboard
   ```
2. **Open the project** — launch Power BI Desktop and open `Sales Analytics Dashboard.pbip`. This requires the [PBIP preview feature](https://learn.microsoft.com/power-bi/developer/projects/projects-overview) enabled in Power BI Desktop (File → Options → Preview features → Power BI Project (.pbip) save option).
3. **Repoint the data source** — the model reads from the source Excel file (`ac-sample-data.xlsx`). In Power Query Editor (Transform data), update the file path parameter to point to your local copy of the workbook.
4. **Refresh** — click Refresh on the Home ribbon to reload data from the repointed source.

## Repository Structure

```
Sales-Analytics-Dashboard/
├── Sales Analytics Dashboard.pbip
├── Sales Analytics Dashboard.Report/
│   ├── definition/
│   ├── StaticResources/
│   └── report.json
├── Sales Analytics Dashboard.SemanticModel/
│   ├── definition/
│   │   ├── tables/
│   │   ├── relationships.tmdl
│   │   └── model.tmdl
│   └── model.bim
├── data/
│   └── ac-sample-data.xlsx
├── assets/
│   └── dashboard-screenshot.png
└── README.md
```

## Key Insights

*[Fill in: 2-4 real findings drawn from analyzing the report, e.g. top-performing region, best-selling category, seasonal trend, or a rep/team performance gap. Each should be a specific, checkable claim, not a generic statement.]*

- [Fill in: insight 1]
- [Fill in: insight 2]
- [Fill in: insight 3]

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Author

**Khusi Khanra**
[Fill in: contact info — email, LinkedIn, portfolio site, etc.]
