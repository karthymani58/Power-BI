# E-Commerce Sales Analysis | Power BI

## Project Overview

This project is an E-Commerce Sales Analysis Dashboard developed using Microsoft Power BI.

The objective is to analyze sales performance, profitability, order trends, sales targets, product categories, customer segments, and geographic sales performance.

This project demonstrates an end-to-end Data Analyst workflow using Power BI, DAX, Power Query, data modeling, KPIs, and data visualization.

## Objectives

- Analyze overall sales performance
- Compare actual sales with sales targets
- Analyze profitability by category and sub-category
- Track monthly sales trends
- Analyze order count by state
- Analyze geographic sales performance
- Compare profit and quantity
- Analyze sales distribution by sub-category
- Calculate YTD sales
- Analyze customer segment targets
- Build an interactive Power BI dashboard

## Dataset

The project uses three CSV files:

1. List of Orders.csv
2. Order Details.csv
3. Sales target.csv

### List of Orders

- Order ID
- Order Date
- Customer Name
- City
- State
- Region
- Segment

### Order Details

- Order ID
- Category
- Sub-Category
- Amount
- Quantity
- Profit

### Sales Target

- Category
- Segment
- Target

## Data Modeling

The tables were connected using appropriate relationships before creating the dashboard.

Main relationship:

List of Orders → Order ID → Order Details

Sales Target → Category / Segment → Sales Analysis

## Data Preparation

- Imported CSV files into Power BI
- Checked data types
- Cleaned data
- Checked missing values
- Prepared date fields
- Created table relationships
- Created calculated columns
- Created DAX measures
- Prepared data for visualization

## DAX Calculated Columns

### 1. Category Type

```DAX
Category Type =
'Order Details'[Category] & " - " &
'Order Details'[Sub-Category]
2. Revenue per Order
Revenue per Order =
'Order Details'[Amount] *
'Order Details'[Quantity]
3. Sales Category
Sales Category =
IF(
    'Order Details'[Amount] >=
    AVERAGE('Order Details'[Amount]),
    "Above Average",
    "Below Average"
)
DAX Measures
1. Order Count
Order Count =
DISTINCTCOUNT('Order Details'[Order ID])
2. Total Sales
Total Sales =
SUM('Order Details'[Amount])
3. Total Profit
Total Profit =
SUM('Order Details'[Profit])
4. Total Quantity
Total Quantity =
SUM('Order Details'[Quantity])
5. Sales Target
Sales Target =
SUM('Sales target'[Target])
6. Average Profit in Delhi
Average Profit in Delhi =
CALCULATE(
    AVERAGE('Order Details'[Profit]),
    'List of Orders'[City] = "Delhi"
)
7. YTD Sales
YTD Sales =
TOTALYTD(
    [Total Sales],
    'List of Orders'[Order Date]
)
Data Visualizations
1. Sales Target Achievement by Category

Visual: Clustered Column Chart

Axis: Category
Values: Total Sales
Values: Sales Target

Purpose: Compare actual sales with sales targets by category.

2. Max Profit Margin by Sub-Category

Visual: Donut Chart

Legend: Sub-Category
Values: Maximum Profit Margin

Purpose: Analyze profit margin across sub-categories.

3. Monthly Sales Trend

Visual: Line Chart

X-Axis: Order Date / Month
Y-Axis: Total Sales

Purpose: Analyze monthly sales trends.

4. Profit vs Quantity by Sub-Category

Visual: Scatter Chart

X-Axis: Quantity
Y-Axis: Profit
Details: Sub-Category

Purpose: Analyze the relationship between quantity sold and profit.

5. Total Sales Amount vs Target

Visual: Card

Total Sales
Sales Target

Purpose: Quickly compare actual sales with the target.

6. Minimum Target by Segment

Visual: Multi-Row Card

Segment
Minimum Target

Purpose: Display minimum target for each segment.

7. Sales Performance Matrix

Visual: Matrix

Rows: Category
Columns: Month
Values: Total Sales
Values: Sales Target

Purpose: Compare actual sales with targets across categories and months.

8. Geographic Sales Analysis

Visual: Map

Location: City
Values: Total Sales

Purpose: Identify geographic sales patterns.

9. Sales Distribution by Sub-Category

Visual: Treemap

Group: Sub-Category
Values: Total Sales

Purpose: Analyze sales distribution across sub-categories.

10. Order Count Analysis by State

Visual: Funnel Chart

Group: State
Values: Order Count

Purpose: Analyze order distribution across states.

Key KPIs
KPI	Description
Total Sales	Overall sales amount
Sales Target	Planned sales target
Order Count	Number of unique orders
Total Quantity	Total quantity sold
Total Profit	Overall profit generated
Average Profit	Average profit
YTD Sales	Year-to-date sales
Sales vs Target	Actual sales compared with target
Business Questions
What is the total sales amount?
How do actual sales compare with the target?
Which categories generate the most sales?
Which sub-categories generate higher profit?
What is the monthly sales trend?
Which cities generate higher sales?
Which states have higher order volumes?
What is the relationship between quantity and profit?
Which sub-categories contribute most to sales?
What is the YTD sales performance?
What are the target levels for different customer segments?
Project Workflow

Raw CSV Files
→ Data Import
→ Data Cleaning
→ Power Query
→ Data Modeling
→ Relationships
→ Calculated Columns
→ DAX Measures
→ KPI Development
→ Visualizations
→ Dashboard Design
→ Business Analysis

Tools & Technologies
Power BI
DAX
Power Query
Data Modeling
Data Visualization
CSV
Business Intelligence
Skills Demonstrated
Power BI Dashboard Development
DAX
Power Query
Data Cleaning
Data Transformation
Data Modeling
Calculated Columns
Calculated Measures
KPI Development
Sales Analysis
Profit Analysis
Target vs Actual Analysis
Time-Series Analysis
Geographic Analysis
Product Analysis
Business Intelligence
Data Visualization
Repository Structure
E-Commerce-Sales-Analysis-PowerBI/
│
├── Dataset/
│   ├── List of Orders.csv
│   ├── Order Details.csv
│   └── Sales target.csv
│
├── PowerBI/
│   └── E-Commerce-Sales-Analysis.pbix
│
├── Screenshots/
│   └── Dashboard.png
│
└── README.md
Dashboard Preview

Author
M. Karthik

Data Analyst
Power BI | DAX | Data Analytics

Project Category
Power BI | Data Analytics | Business Intelligence | DAX | E-Commerce Analytics
