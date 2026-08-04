# Sales Analytics Dashboard | Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Analytics-4472C4)
![Power Query](https://img.shields.io/badge/Power%20Query-M-217346)
![Status](https://img.shields.io/badge/status-completed-2EA44F)
![License](https://img.shields.io/badge/license-MIT-green)

An interactive **Power BI Sales Analytics Dashboard** designed to transform chocolate sales data into actionable business insights across revenue, profitability, products, geography, sales teams, and time-based performance.

The project demonstrates **data modeling, DAX measures, time intelligence, interactive reporting, KPI design, and business-focused dashboard development**.

---

## Table of Contents

- [Dashboard Preview](#dashboard-preview)
- [Project Overview](#project-overview)
- [Key Metrics](#key-metrics)
- [Report Pages](#report-pages)
- [Data Model](#data-model)
- [Key DAX Measures](#key-dax-measures)
- [Interactivity](#interactivity)
- [Key Insights](#key-insights)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [License](#license)
- [About the Developer](#about-the-developer)

---

## Dashboard Preview

<img width="1536" height="1024" alt="Dashboard Demo images" src="https://github.com/user-attachments/assets/638bd5d9-6a44-4dd0-84a2-878ba7dbb081" />

> **8-page interactive Power BI dashboard covering executive reporting, sales performance, product analysis, geography, salesperson performance, time intelligence, business insights, and project information.**

---

## Project Overview

This project analyzes a chocolate sales dataset covering **February 2023 to February 2024**.

The dashboard was designed to answer practical business questions such as:

- Where is revenue concentrated?
- Which products and categories generate the most sales and profit?
- Which regions are performing best?
- Which salespeople are driving the strongest results?
- How are sales and profit changing over time?
- How does current performance compare with previous periods?
- Where are the biggest opportunities for business improvement?

The project is structured as a portfolio-ready Power BI solution demonstrating both **technical BI skills and business analysis**.

---

## Key Metrics

| Metric | Value |
|---|---:|
| **Total Sales** | **$34.04M** |
| **Total Profit** | **$20.52M** |
| **Profit Margin** | **60.29%** |
| **Total Shipments** | **6.11K** |
| **Boxes Shipped** | **2,077,844** |
| **Transactions** | **6,113** |
| **Products** | **22** |
| **Sales Reps** | **25** |
| **Markets** | **6 countries** |
| **Regions** | **3** |
| **Date Range** | **Feb 2023 – Feb 2024** |

### Product Categories

- Bars
- Bites
- Other

### Markets Covered

- USA
- UK
- Canada
- India
- Australia
- New Zealand

### Regions

- Americas
- APAC
- Europe

### Sales Teams

- Yummies
- Delish
- Jucies
- Tempo

---

## Report Pages

The report contains **8 interactive pages**, each designed for a specific analytical purpose.

| # | Page | Purpose |
|---|---|---|
| **01** | **Executive Overview** | High-level KPIs and overall sales, profit, shipment, product, geography, and salesperson performance. |
| **02** | **Sales Performance** | Sales trends, profit performance, growth analysis, running totals, product rankings, and category performance. |
| **03** | **Product Analysis** | Product-level sales, profit, contribution, margin, and performance comparison. |
| **04** | **Geography Analysis** | Regional and geographic sales, profit, margin, shipment, and performance analysis. |
| **05** | **Salesperson Performance** | Salesperson rankings, sales and profit performance, target analysis, and detailed performance comparisons. |
| **06** | **Time Intelligence** | Monthly trends, year-over-year comparisons, running totals, growth analysis, and monthly performance. |
| **07** | **Insights & Recommendations** | Key business insights, performance highlights, and actionable recommendations derived from the analysis. |
| **08** | **About & Information** | Project overview, dataset scope, analytics coverage, tools, technologies, and dashboard navigation. |

---

## Data Model

The Power BI semantic model follows a **star-schema approach** with a central fact table, supporting dimension data, and a dedicated calendar table.

### Fact Table — Shipment Data

Contains transactional sales information including:

- Sales Person
- Geography
- Product
- Date
- Sales
- Boxes Shipped

### Dimension Table — Dimension Data

Provides descriptive attributes used for filtering and analysis:

- Product
- Category
- Cost per Box
- Geography
- Region
- Sales Person
- Team

### Date Dimension — Calendar Table

A dedicated date table used to support time-intelligence calculations such as:

- Year-over-Year analysis
- Previous-period comparisons
- Running totals
- Monthly growth
- Date-based filtering

### Model Structure

```text
                    ┌─────────────────────┐
                    │   Calendar Table    │
                    │                     │
                    │ Date                │
                    │ Month               │
                    │ Year                │
                    │ Month Number        │
                    └──────────┬──────────┘
                               │
                               │ Date
                               │
┌─────────────────────┐   ┌────▼────────────────┐
│   Dimension Data    │   │    Shipment Data    │
│                     │   │                     │
│ Product             │   │ Sales Person        │
│ Category            │   │ Geography           │
│ Cost per Box        │   │ Product             │
│ Geography           │   │ Date                │
│ Region              │   │ Sales               │
│ Sales Person        │   │ Boxes Shipped       │
│ Team                │   │                     │
└──────────┬──────────┘   └─────────────────────┘
           │
           └────────────── Relationships
```

---

## Key DAX Measures

Measure **names** below are confirmed from the KPI cards across all 8 report pages. Formulas are not visible in a static screenshot — paste the actual DAX from Power BI Desktop before publishing; do not reuse the placeholder syntax below as real code.

```dax
Total Sales = [Fill in: actual measure formula]
Total Profit = [Fill in: actual measure formula]
Profit Margin % = [Fill in: actual measure formula]
Total Shipments = [Fill in: actual measure formula]
Total Boxes = [Fill in: actual measure formula]
Average Selling Price = [Fill in: actual measure formula]
Total Products = [Fill in: actual measure formula]
Total Salespersons = [Fill in: actual measure formula]
Total Countries = [Fill in: actual measure formula]
Sales Growth % = [Fill in: actual measure formula]
Profit Growth % = [Fill in: actual measure formula]
Running Total Sales = [Fill in: actual measure formula, e.g. CALCULATE + ALLSELECTED]
Monthly Growth % = [Fill in: actual measure formula]
Target Achievement % = [Fill in: actual measure formula]
Sales Comparison vs PY = [Fill in: actual measure formula]
Profit Comparison vs PY = [Fill in: actual measure formula]
Shipments Growth % = [Fill in: actual measure formula]
```

---

## Interactivity

Confirmed directly from the report (not placeholders):

- **Slicers:** Date, Region, Product, Team, and Sales Person on the Executive Overview, Sales Performance, Product Analysis, Geography Analysis, and Salesperson Performance pages. Date (last N), Year, and Month on the Time Intelligence page. Year, Quarter, Region, and Category on the Insights & Recommendations page.
- **Page navigation:** Standard Power BI page tabs across all 8 pages.
- **Sortable tables:** Product Details (Product Analysis), Regional Performance (Geography Analysis), Salesperson Performance Ranking / Details (Salesperson Performance), and Monthly Performance (Time Intelligence) all show sortable column headers.

*[Fill in: not visible in the screenshots reviewed — confirm and add if present:]*
- **Drill-through:** [Fill in: no drill-through menus were visible in the reviewed screenshots — add if configured]
- **Bookmarks:** [Fill in: no bookmark controls were visible — add if configured]
- **Custom tooltips:** [Fill in: no custom tooltip pages were visible — add if configured]

---

## Key Insights

Verified against the underlying charts (see note below on excluded items):

- **APAC is the strongest region by profitability** — 61.78% profit margin vs. 59.49% (Americas) and 57.25% (Europe), per the Regional Performance table on Geography Analysis.
- **New Zealand is the top-selling individual market** at ~$5.9M in sales, narrowly ahead of Canada and Australia (~$5.7M each), despite APAC and Americas being the stronger *regions* overall — worth noting since regional and country-level rankings diverge.
- **Organic Choco Syrup is the top individual product**, both in sales ($2.1M) and reported profit ($1.38M per the Insights page product card), consistent with its #1 ranking in Top 10 Products by Sales on both Sales Performance and Product Analysis.
- **Profit margin (60.29%) is high relative to typical CPG benchmarks**, driven by category mix — Bars leads categories at ~50% of total sales per the Product Analysis category donut.

*[Fill in / verify before publishing: the "Insights & Recommendations" page also lists "Top Performing Region: North," "Best Salesperson: Sean Miller," and "Best Sales Month: December 2023" — these don't reconcile with the region list (APAC/Americas/Europe), the Top 10 Salespersons lists, or the Monthly Sales Trend chart (which shows November 2023, not December, as the peak month) elsewhere in the report. Recommend re-checking whether that page's Key Business Insights panel is bound to live measures or contains static/template text before using those specific figures.]*

---

## Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Report authoring (PBIP project format), data visualization, and dashboarding |
| **DAX** | Measures, calculations, and data analysis |
| **Power Query (M)** | Data transformation and shaping |
| **Excel** | Source data preparation and cleaning |
| **Data Modeling** | Star schema design and table relationships |

---

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd Sales-Analytics-Dashboard
   ```
2. **Open the project** — launch Power BI Desktop and open `Sales Analytics Dashboard.pbip`. This requires the [PBIP preview feature](https://learn.microsoft.com/power-bi/developer/projects/projects-overview) enabled (File → Options → Preview features → Power BI Project (.pbip) save option).
3. **Repoint the data source** — the model reads from the source Excel file. In Power Query Editor (Transform Data), update the file path parameter to point to your local copy of the workbook.
4. **Refresh** — click Refresh on the Home ribbon to reload data from the repointed source.

---

## Repository Structure

```text
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

*[Fill in: confirm this matches your actual repo layout once the `.Report` and `.SemanticModel` folders are committed.]*

---

## License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## About the Developer

**Khusi Khanra**

Data Analyst focused on transforming business data into clear, actionable insights using **SQL, Excel, Power BI, DAX, and Python**.

### Connect

- **GitHub:** [@khusikhanra](https://github.com/khusikhanra)
