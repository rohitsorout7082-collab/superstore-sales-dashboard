#  Superstore Sales Analytics Dashboard (Power BI)

An executive-level interactive Power BI sales dashboard built to analyze retail e-commerce performance across regional distributions, customer segments, top-selling inventory, and monthly sales trends.

---

 Dashboard Preview

![Dashboard Screenshot](dashboard_screenshot.png.png
)

---

 Project Overview & Business Problem

Retail businesses often face challenges tracking real-time profitability, seasonal revenue fluctuations, and product performance across diverse customer categories. 

This project transforms raw transactional data into actionable insights, helping business managers answer:
- What is our current revenue pace and average order value?
- Which product lines and customer segments drive the majority of revenue?
- How do geographic regions compare, and where are seasonal demand peaks?

---

 Key Insights & Features

- **Executive KPI Cards**: Real-time high-level visibility into **Total Sales (₹ 2.26M)**, **Total Orders (5K)**, and **Average Order Value (₹ 459.48)**.
- **Monthly Revenue Trend (Line Chart)**: Tracks seasonality and demand spikes from January through December.
- **Top 10 Products by Revenue (Bar Chart)**: Identifies top-performing inventory items to optimize stock levels.
- **Category Sales Split (Pie Chart)**: Analyzes revenue distribution across Technology, Furniture, and Office Supplies.
- **Customer Segmentation (Column Chart)**: Breakdown of sales across Consumer, Corporate, and Home Office segments.
- **Interactive Multi-Level Slicers**: Dynamic buttons for immediate cross-filtering by **Year (2015–2018)** and **Region (Central, East, South, West)**.

---

 Technical Stack & Architecture

- **BI Platform**: Microsoft Power BI Desktop
- **Data Modeling**: Star Schema Design
- **Data Cleaning & ETL**: Power Query Editor
  - Configured Locale formatting (English - India) for accurate date parsing
  - Text transformation on Postal Codes
  - Custom column extraction for `Year`
- Analytics & Calculations (DAX)**:
  - `Total Sales = SUM(train[Sales])`
  - `Total Orders = DISTINCTCOUNT(train[Order ID])`
  - `Average Sales = DIVIDE([Total Sales], [Total Orders], 0)`
  - `Order Year = YEAR(train[Order Date])`

---

 Repository Structure

```text
├── superstore_sales_dashboard.pbix   # Main Power BI project file
├── dashboard_screenshot.png          # High-resolution dashboard preview
└── README.md                         # Project documentation
 How to Run Locally
Clone or download this repository:

Bash
git clone [https://github.com/rohitsorout7082-collab/superstore-sales-dashboard.
