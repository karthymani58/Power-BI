# E-Commerce Sales Analysis — Power BI

An end-to-end Business Intelligence project analyzing e-commerce sales data to evaluate performance, revenue drivers, profit margins, regional trends, and target achievements.

## 📊 Dashboard Preview

## 📌 Project Overview

This project provides a comprehensive overview of sales performance for an e-commerce platform. It transforms raw operational data into interactive, actionable business intelligence using Power BI, Power Query, and DAX. Stakeholders can monitor key performance indicators (KPIs), evaluate sales against targets, analyze geographic distributions, and understand profit drivers by category and sub-category.

## 🛠️ Tools & Technologies

* **Power BI**: Dashboard Design, Data Modeling & Visualization

* **DAX (Data Analysis Expressions)**: Calculated Columns, Measures & Time-Intelligence Functions

* **Power Query**: Data Extraction, Cleaning & Transformation

* **Data Sources**: CSV Files (`List of Orders`, `Order Details`, `Sales target`)

* **Business Intelligence**: KPI Development & Data Analysis

## 🎯 Skills Demonstrated

* Power BI Dashboard Development

* Data Cleaning & Transformation (Power Query)

* Data Modeling & Relationship Building

* Calculated Columns & Measures (DAX)

* KPI Development & Target vs. Actual Analysis

* Sales, Profit & Product Analysis

* Time-Series & Geographic Analysis

* Data Visualization & UX Layout Design

## 🔄 Project Workflow

```
Raw CSV Files 
  └──> Data Import 
        └──> Data Cleaning (Power Query) 
              └──> Data Modeling & Relationships 
                    └──> Calculated Columns 
                          └──> DAX Measures 
                                └──> KPI Development 
                                      └──> Visualizations 
                                            └──> Dashboard Design 
                                                  └──> Business Analysis

```

## 💡 Key Business Questions Answered

* What is the total sales amount generated?

* How do actual sales perform compared to planned targets?

* Which product categories and sub-categories generate the most sales and profits?

* What is the monthly sales trend and YTD (Year-to-Date) performance?

* Which cities and states generate higher order volumes and sales performance?

* What is the relationship between product quantity sold and overall profit?

* What are the target levels across different customer segments?

## 📐 DAX Calculations

### 1. Calculated Columns

* **Category Type**

  ```
  Category Type =
  'Order Details'[Category] & " - " & 'Order Details'[Sub-Category]
  
  ```

* **Revenue per Order**

  ```
  Revenue per Order =
  'Order Details'[Amount] * 'Order Details'[Quantity]
  
  ```

* **Sales Category**

  ```
  Sales Category =
  IF(
      'Order Details'[Amount] >= AVERAGE('Order Details'[Amount]),
      "Above Average",
      "Below Average"
  )
  
  ```

### 2. Measures

* **Order Count**

  ```
  Order Count =
  DISTINCTCOUNT('Order Details'[Order ID])
  
  ```

* **Total Sales**

  ```
  Total Sales =
  SUM('Order Details'[Amount])
  
  ```

* **Total Profit**

  ```
  Total Profit =
  SUM('Order Details'[Profit])
  
  ```

* **Total Quantity**

  ```
  Total Quantity =
  SUM('Order Details'[Quantity])
  
  ```

* **Sales Target**

  ```
  Sales Target =
  SUM('Sales target'[Target])
  
  ```

* **Average Profit in Delhi**

  ```
  Average Profit in Delhi =
  CALCULATE(
      AVERAGE('Order Details'[Profit]),
      'List of Orders'[City] = "Delhi"
  )
  
  ```

* **YTD Sales**

  ```
  YTD Sales =
  TOTALYTD(
      [Total Sales],
      'List of Orders'[Order Date]
  )
  
  ```

## 🔑 Key KPIs

| KPI | Description | 
 | ----- | ----- | 
| **Total Sales** | Overall sales amount generated | 
| **Sales Target** | Planned sales target goal | 
| **Order Count** | Total number of unique orders placed | 
| **Total Quantity** | Aggregate quantity of items sold | 
| **Total Profit** | Overall profit generated | 
| **Average Profit** | Average profit earned per transaction | 
| **YTD Sales** | Year-to-date total cumulative sales | 
| **Sales vs Target** | Performance comparison between actual sales and target | 

## 📈 Data Visualizations

 1. **Sales Target Achievement by Category** (*Clustered Column Chart*)

    * **Axis:** Category | **Values:** Total Sales, Sales Target

    * **Purpose:** Compare actual sales with sales targets by category.

 2. **Max Profit Margin by Sub-Category** (*Donut Chart*)

    * **Legend:** Sub-Category | **Values:** Maximum Profit Margin

    * **Purpose:** Analyze profit margin across sub-categories.

 3. **Monthly Sales Trend** (*Line Chart*)

    * **X-Axis:** Order Date / Month | **Y-Axis:** Total Sales

    * **Purpose:** Analyze monthly sales trends over time.

 4. **Profit vs Quantity by Sub-Category** (*Scatter Chart*)

    * **X-Axis:** Quantity | **Y-Axis:** Profit | **Details:** Sub-Category

    * **Purpose:** Analyze the relationship between quantity sold and profit.

 5. **Total Sales Amount vs Target** (*Card*)

    * **Fields:** Total Sales, Sales Target

    * **Purpose:** Quickly compare actual sales against targets.

 6. **Minimum Target by Segment** (*Multi-Row Card*)

    * **Fields:** Segment, Minimum Target

    * **Purpose:** Display minimum target for each customer segment.

 7. **Sales Performance Matrix** (*Matrix*)

    * **Rows:** Category | **Columns:** Month | **Values:** Total Sales, Sales Target

    * **Purpose:** Compare actual sales with targets across categories and months.

 8. **Geographic Sales Analysis** (*Map*)

    * **Location:** City | **Values:** Total Sales

    * **Purpose:** Identify geographic sales patterns across cities.

 9. **Sales Distribution by Sub-Category** (*Treemap*)

    * **Group:** Sub-Category | **Values:** Total Sales

    * **Purpose:** Analyze sales distribution across product sub-categories.

10. **Order Count Analysis by State** (*Funnel Chart*)

    * **Group:** State | **Values:** Order Count

    * **Purpose:** Analyze order volume distribution across states.

## 📁 Repository Structure

```
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

```

## 👤 Author

**M. Karthik**

*Data Analyst*

**Specializations**: Power BI | DAX | Data Analytics | Business Intelligence | E-Commerce Analytics
