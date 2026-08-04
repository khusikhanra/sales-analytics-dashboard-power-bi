# Sales Analytics Dashboard | Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Analytics-4472C4)
![Power Query](https://img.shields.io/badge/Power%20Query-M-217346)
![Status](https://img.shields.io/badge/status-completed-2EA44F)
![License](https://img.shields.io/badge/license-MIT-green)

An interactive **Power BI Sales Analytics Dashboard** designed to transform chocolate sales data into actionable business insights across revenue, profitability, products, geography, sales teams, and time-based performance.

The project demonstrates **data modeling, DAX measures, time intelligence, interactive reporting, KPI design, and business-focused dashboard development**.

---

## Dashboard Preview

<p align="center">
  <img src="assets/dashboard-showcase.png" alt="Sales Analytics Dashboard - 8 Page Power BI Showcase" width="100%">
</p>

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

# Report Pages

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

# Data Model

The Power BI semantic model follows a **star-schema approach** with a central fact table, supporting dimension data, and a dedicated calendar table.

### Fact Table

**Shipment Data**

Contains transactional sales information including:

- Sales Person
- Geography
- Product
- Date
- Sales
- Boxes Shipped

### Dimension Data

**Dimension Data**

Provides descriptive attributes used for filtering and analysis:

- Product
- Category
- Cost per Box
- Geography
- Region
- Sales Person
- Team

### Date Dimension

**Calendar Table**

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

---

# About the Developer

**Khusi Khanra**

Data Analyst focused on transforming business data into clear, actionable insights using **SQL, Excel, Power BI, DAX, and Python**.

### Connect

- **GitHub:** [@khusikhanra](https://github.com/khusikhanra)
