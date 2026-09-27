# 📊 E-Commerce Sales Analysis – Power BI

## 📌 Project Overview

This project is a **Power BI E-Commerce Sales Analysis Dashboard** developed to analyze sales performance, profitability, order trends, sales targets, product categories, and geographic performance.

The project focuses on **DAX, data modeling, calculated columns, calculated measures, and interactive Power BI visualizations**.

---

## 🎯 Project Objectives

- Analyze overall sales performance
- Compare actual sales against sales targets
- Analyze profitability by category and sub-category
- Track monthly sales trends
- Analyze order count by state
- Identify geographic sales patterns
- Compare profit and quantity sold
- Analyze sales distribution by sub-category
- Create KPI cards for quick performance monitoring
- Apply DAX for business calculations

---

## 📂 Dataset

The project uses three CSV files:

| Dataset | Description |
|---|---|
| `List of Orders.csv` | Order-level information including Order ID, Order Date, City, State, Region, and Segment |
| `Order Details.csv` | Product-level information including Category, Sub-Category, Amount, Quantity, and Profit |
| `Sales target.csv` | Sales target information by category and segment |

---

## 🏗️ Data Modeling

The data model was created before developing the visualizations.

### Main Tables

```text
List of Orders
      |
      | Order ID
      ↓
Order Details

Sales Target
      |
      | Category / Segment
      ↓
Sales Analysis
