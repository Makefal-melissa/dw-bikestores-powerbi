# dw-bikestores-powerbi
Power BI executive dashboard built on a SQL Server star schema — tracks revenue, average order value, and sales performance through 16 DAX measures.
# 📊 DW_BikeStores — Executive Overview Dashboard (Power BI)

A decision-support dashboard built on a star-schema data warehouse, tracking revenue, sales performance, and customer distribution.

## 🎯 Context & Objective

This project reproduces a classic BI use case: starting from raw sales data, build a data warehouse modeled as a star schema, then an executive dashboard to monitor key business indicators (revenue, active customers, average order value, sales rep performance).

## 🏗️ Architecture

**Star schema** implemented in SQL Server (SSMS):

- **Fact table**: `fact_orders`
- **Dimensions**: `dim_date`, `dim_customers`, `dim_store`, `dim_staffs`, `dim_product`

The `dim_date` table was built entirely in SQL to support time-based analysis (monthly comparisons, trends). The `fact_orders` table was rebuilt to include order status (`order_status`), required for several measures.

## 📐 DAX Measures

16 DAX measures were defined to power the dashboard, including:

- `Total Revenue`
- `Revenue Variation %`
- `Active Customers`
- `Average Order Value`

> Technical note: table names with the `dwh` prefix require single quotes in DAX formulas (e.g. `'dwh Fact_Orders'[...]`).

## 📊 Dashboard Content

The **Executive Overview** dashboard is organized into several areas:

1. **Slicers** — period, store, product category
2. **KPI cards** — total revenue, variation, active customers, average order value
3. **Sales rep leaderboard**
4. **Customer distribution by state/region**

**Visual palette**: teal / coral / blue / amber on white, designed for quick reading of trends (positive/negative) without visual clutter.

## 🖼️ Preview

*(add 2-3 dashboard screenshots here: overview, KPI zoom, customer distribution zoom)*

## 🛠️ Tools Used

- SQL Server / SSMS (modeling, table creation scripts)
- Power BI (dashboard, DAX measures)

## 📌 What This Project Demonstrates

- Designing a star-schema data model suited for decision-support analysis
- Writing DAX measures for business KPIs (revenue, average order value, variation rate)
- Building an executive dashboard incrementally, from filtering to advanced visualizations

---

*Project completed as part of a Business Intelligence internship.*
