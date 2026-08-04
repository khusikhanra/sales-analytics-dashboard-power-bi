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
- [Interactivity](#interactivity)
- [Key Insights](#key-insights)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [License](#license)
- [About the Developer](#about-the-developer)

---

## Dashboard Preview

<img width="1536" height="1024" alt="Dashboard-screenshot" src="https://github.com/user-attachments/assets/b8c5c72c-ef16-418d-afb6-80100573a49d" />


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

---

## Key Metrics

| Metric | Value |
|---|---:|
| **Total Sales** | **$34.04M** |
| **Total Profit** | **$20.52M** |
| **Profit Margin** | **60.29%** |
| **Total Transactions** | **6,113** |
| **Boxes Shipped** | **2,077,844** |
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

## Interactivity

Confirmed directly from the report file:

- **Slicers:** Date, Region, Product, Team, and Sales Person on Executive Overview, Sales Performance, Product Analysis, Geography Analysis, and Salesperson Performance.
- **Time Intelligence filters:** Date (Last N), Year, and Month.
- **Insights & Recommendations filters:** Year, Quarter, Region, and Category.
- **Page navigation:** Standard Power BI page tabs across all 8 pages.
- **Sortable tables:** Product Details, Regional Performance, Salesperson Performance Ranking, Salesperson Performance Details, and Monthly Performance tables.

---

## Key Insights

The dashboard highlights several important business findings:

- **APAC is the strongest region by profitability**, with a **61.78% profit margin**, compared with 59.49% for Americas and 57.25% for Europe.
- **New Zealand is the top-selling individual market**, generating approximately **$5.9M in sales**, narrowly ahead of Canada and Australia.
- **Organic Choco Syrup is the top individual product**, generating approximately **$2.1M in sales** and reported profit of approximately **$1.38M**.
- **Bars is the highest-profit category**, generating approximately **$10.40M in profit** with a **60.87% profit margin**.
- Overall dashboard performance shows **$34.04M in sales**, **$20.52M in profit**, and a **60.29% profit margin** across the analyzed period.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Report authoring, data visualization, and dashboard development |
| **DAX** | Measures, calculations, KPIs, and time intelligence |
| **Power Query (M)** | Data transformation and shaping |
| **Excel** | Source data preparation and cleaning |
| **Data Modeling** | Star-schema design and table relationships |

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/khusikhanra/sales-analytics-dashboard-power-bi.git
cd sales-analytics-dashboard-power-bi
```

### 2. Open the Power BI Report

Launch **Power BI Desktop** and open:

```text
Sales Analytics Dashboard.pbix
```

The `.pbix` file contains the report, visuals, semantic model, and Power BI configuration required to explore the dashboard.

### 3. Update the Data Source

The report uses the source Excel dataset.

If the Excel file path differs on your machine:

1. Open **Power BI Desktop**.
2. Select **Transform Data**.
3. Open **Power Query Editor**.
4. Update the source file path to your local Excel file.
5. Apply the changes.

### 4. Refresh the Report

After updating the source path:

**Home → Refresh**

This reloads the data and updates the dashboard visuals.

---

## Repository Structure

```text
Sales-Analytics-Dashboard/
├── Sales Analytics Dashboard.pbix
├── data/
│   └── ac-sample-data.xlsx
├── assets/
│   └── dashboard-screenshot.png
├── LICENSE
└── README.md
```

---

## License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

## About the Developer

**Khusi Khanra**

Data Analyst focused on transforming business data into clear, actionable insights using **SQL, Excel, Power BI, DAX, and Python**.

### Connect

- **GitHub:** [@khusikhanra](https://github.com/khusikhanra)
