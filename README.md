# Sales Insights — Interactive Power BI Dashboard

A multi-page, production-quality business intelligence report built in Microsoft Power BI that transforms raw sales, product, customer, and returns data into actionable executive insights. The report is designed for decision-makers who need a fast, visual path from raw numbers to strategic conclusions.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Dashboard Pages](#dashboard-pages)
- [Key Metrics Tracked](#key-metrics-tracked)
- [Data Model](#data-model)
- [Visualizations Used](#visualizations-used)
- [DAX Measures](#dax-measures)
- [Interactivity Features](#interactivity-features)
- [Tools and Technologies](#tools-and-technologies)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Skills Demonstrated](#skills-demonstrated)

---

## Project Overview

Sales Insights is a fully interactive Power BI report that consolidates data from multiple business domains — sales transactions, product catalog, customer demographics, regional geography, and return records — into a single cohesive analytical experience.

The report is built around a star-schema data model and uses DAX measures to compute KPIs. It is structured for real-world business use, with navigation buttons on a landing page, dynamic slicers, and a drillthrough page for granular product-level investigation.

**Tool:** Microsoft Power BI Desktop (2026.04 release)  
**File format:** .pbix  
**Report canvas size:** 1280 x 720 px (16:9)  
**Data period covered:** November 2024 – June 2025  
**Total Revenue:** 844.02K | **Total Profit:** 10.14K | **Total Orders:** 1K | **Total Customers:** 198

---

## Dashboard Pages

The report contains five pages, organized for a logical flow from high-level to granular.

---

### Page 1 — Navigation Hub

A dedicated landing page with four styled action buttons that navigate to each analytical section. This keeps the report clean and presentation-ready for stakeholder walkthroughs.

![Navigation Hub](screenshot_page1_navigation.png)
<img width="1346" height="575" alt="Screenshot 2026-04-28 173230" src="https://github.com/user-attachments/assets/105e19aa-1f3e-4d75-bc90-662f5dd762ad" />


---

### Executive Overview

The top-level summary page presenting organization-wide performance at a glance. KPI cards surface the four most critical business numbers immediately, while the line chart, donut chart, and bar charts allow the viewer to understand revenue trends, segment contribution, top products, and regional performance in a single scroll.

**Headline numbers:** Total Revenue 844.02K | Total Profit 10.14K | Total Orders 1K | Return Rate 0.05

![Executive Overview](screenshot_page2_executive_overview.png)
<img width="1411" height="795" alt="Screenshot 2026-04-28 173137" src="https://github.com/user-attachments/assets/72dfb36f-12e1-4bcd-adc9-4ca944550934" />


Visuals on this page:
- Four KPI cards — Total Revenue, Total Profit, Total Orders, Return Rate
- Line chart — Total Revenue trend by Year-Month (Nov 2024 – Jun 2025)
- Donut chart — Revenue by Customer Segment (Home Office 39.01%, Corporate 31.09%, Consumer 29.90%)
- Bar chart — Revenue by Product Name (top product: Generate Killer Info-Media)
- Clustered bar chart — Revenue by Region (South leads, followed by North, West, East)
- Slicers — Year, Quarter, Customer Segment, Product Category

---

### Product Analysis

A deep-dive into product performance covering revenue, units sold, profitability, and margin across three product categories: Furniture, Office Supplies, and Technology.

**Key insight:** Technology is the only profitable category (Profit Margin 0.16). Furniture and Office Supplies both show negative profit, making this page critical for pricing and portfolio decisions.

![Product Analysis](screenshot_page3_product_analysis.png)
<img width="1409" height="784" alt="Screenshot 2026-04-28 173350" src="https://github.com/user-attachments/assets/34fcaa3e-273e-471c-a3ca-59b1551f517e" />


Visuals on this page:
- Three KPI cards — Total Revenue 844.02K, Total Units Sold 6K, Profit Margin % 0.01
- Pivot table — Category and Sub-Category breakdown with Revenue, Total Profit, and Profit Margin %
  - Furniture: Revenue 2,74,569.59 | Profit -17,831.25 | Margin -0.06
  - Office Supplies: Revenue 3,03,150.69 | Profit -13,509.49 | Margin -0.04
  - Technology: Revenue 2,66,296.67 | Profit 41,476.23 | Margin 0.16
- Bar chart — Revenue by Product Name (top 5 products visible)
- Donut chart — Revenue split by Category (Office Supplies 35.92%, Furniture 32.53%, Technology 31.55%)
- Slicers — Category, SubCategory, Price range (11.92 to 497.92)

---

### Customer and Returns Analysis

Focused on customer behavior and return patterns to surface operational risk and segment value across four regions and three customer segments.

**Key insight:** Home Office segment in the North region carries the highest return rate (0.07). Customer Change is the leading return reason. Return Rate Status is flagged as "Monitor" at the overall level.

![Customer and Returns Analysis](screenshot_page4_customer_returns.png)
<img width="1405" height="784" alt="Screenshot 2026-04-28 173427" src="https://github.com/user-attachments/assets/82446fee-9926-48e7-984b-82306a78efac" />


Visuals on this page:
- Four KPI cards — Total Customers 198, Avg Order Value 844.02, Return Rate 0.05, Return Rate Status: Monitor
- Bar chart — Top customers by Total Profit and Total Revenue (Stacey Everett, Zachary Little, Jeremy Scott, Alyssa Hughes, Mary Brown)
- Pivot table — Customer Segment vs. Region matrix showing Revenue, Total Orders, and Return Rate per cell
- Bar chart — Return Rate by Return Reason (Customer Change, Defective, Late Delivery, Wrong Item)
- Slicers — Customer Segment, RegionName, ReturnReason

**Segment-Region summary from the pivot table:**

| Segment | Total Revenue | Total Orders | Return Rate |
|---|---|---|---|
| Consumer | 2,52,354.08 | 308 | 0.05 |
| Corporate | 2,62,422.06 | 295 | 0.05 |
| Home Office | 3,29,240.81 | 397 | 0.05 |
| **Total** | **8,44,016.95** | **1,000** | **0.04** |

---

### Drillthrough: Product Detail

A drillthrough page accessible by right-clicking any product name across the report. It renders that product's complete revenue, units, profit, returns, time-series trend, and individual customer transaction table automatically. A back-navigation button returns the user to the originating page.

![Drillthrough: Product Detail](screenshot_page5_product_detail.png)
<img width="1411" height="790" alt="Screenshot 2026-04-28 173455" src="https://github.com/user-attachments/assets/0374c946-d90e-4eff-8f8d-f25f94a9e697" />


Visuals on this page:
- Four KPI cards — Total Revenue 4.73K, Total Units Sold 31, Total Profit -420.93, Total Returns 1
- Line chart — Total Revenue trend by Year-Month for the selected product (Nov 2024 – May 2025)
- Detail table — Full Name, Customer Segment, RegionName, Sum of TotalAmount per customer row

---

## Key Metrics Tracked

| Metric | Description |
|---|---|
| Total Revenue | Sum of all sales transaction amounts (844.02K overall) |
| Total Profit | Revenue net of cost (10.14K overall; Technology drives all profitability) |
| Profit Margin % | Profit as a percentage of revenue (0.01 blended; 0.16 for Technology alone) |
| Total Orders | Count of distinct orders (1K) |
| Total Units Sold | Quantity of items sold (6K) |
| Total Customers | Count of distinct customers (198) |
| Average Order Value | Revenue divided by order count (844.02) |
| Return Rate | Returns as a proportion of orders (0.05) |
| Return Rate Status | Conditional DAX label — currently "Monitor" at the overall level |
| Total Returns | Count of returned items |

---

## Data Model

The report is built on a star schema with the following tables:

**Sales_Fact** — the central fact table containing transaction-level records including Customer Segment and TotalAmount per order.

**Returns_Fact** — stores return records with a ReturnReason field (Customer Change, Defective, Late Delivery, Wrong Item) used for root-cause analysis.

**Product_Dim** — product master data including ProductName, Category (Furniture, Office Supplies, Technology), SubCategory, and Price (range: 11.92 to 497.92).

**Customer_Dim** — customer master data including Full Name used for individual-level profitability analysis.

**Region_Dim** — geographic dimension with four regions: East, North, South, West.

**Date_Dim** — date dimension table supporting time-intelligence calculations, with Year, Quarter, and Year-Month attributes (data spans November 2024 to June 2025).

**Table (Measures table)** — a dedicated DAX measures table holding all calculated KPIs to keep the model organized and scalable.

Relationships are structured as one-to-many joins from dimension tables to the fact tables, enabling clean cross-filtering across all report pages.

---

## Visualizations Used

| Visual Type | Purpose |
|---|---|
| Card Visual | KPI headline metrics |
| Line Chart | Revenue trend over time |
| Bar Chart | Ranked comparisons (products, regions, customers, return reasons) |
| Clustered Bar Chart | Multi-dimensional regional comparison |
| Donut Chart | Proportional breakdowns (segment, category) |
| Pivot Table | Multi-level row/column breakdowns with multiple value fields |
| Detail Table (tableEx) | Row-level transaction detail in the drillthrough page |
| Slicer | Standard filter panel (category, year, region) |
| Advanced Slicer | Enhanced search-enabled filter (segment, product category) |
| Action Button | Navigation and drillthrough back-button with page links |

---

## DAX Measures

All measures are centralized in a dedicated measures table. Key calculated fields include:

- `Total Revenue` — aggregates TotalAmount from Sales_Fact (844.02K)
- `Total Profit` — computed from revenue minus cost fields (10.14K)
- `Profit Margin %` — ratio of profit to revenue, formatted as a percentage (0.01 blended)
- `Total Orders` — count of order records (1K)
- `Total Units Sold` — sum of quantity sold (6K)
- `Total Customers` — distinct count of customers (198)
- `Avg Order Value` — average per-order revenue (844.02)
- `Return Rate` — returns divided by total orders, formatted as a percentage (0.05)
- `Return Rate Status` — a conditional DAX measure that categorizes the return rate into a readable label; currently returns "Monitor" at the overall level
- `Total Returns` — count of return records

---

## Interactivity Features

**Cross-filtering:** All visuals on a page filter each other on selection. Clicking a region on the clustered bar chart filters the KPI cards, line chart, and donut chart simultaneously.

**Slicers:** Each page has dedicated slicers so users can isolate specific years, quarters, segments, categories, price ranges, and regions without navigating away.

**Page navigation:** The landing page uses Power BI action buttons wired to page navigation bookmarks, providing a clean app-like experience without using the report's default tab bar.

**Drillthrough:** Users can right-click any product name across the report and drill through to the Product Detail page, which renders that product's complete performance breakdown automatically. A back button returns the user to the originating page.

**Tooltips:** The Return Rate bar chart includes a tooltip showing Return Rate Status, giving users context without adding visual clutter to the chart itself.

---

## Tools and Technologies

- Microsoft Power BI Desktop 2026.04
- DAX (Data Analysis Expressions) for all KPI calculations
- Power Query (M language) for data shaping and transformation
- Star-schema data modeling
- Power BI action buttons and bookmark navigation
- Power BI drillthrough functionality

---

## Getting Started

**Prerequisites:** Microsoft Power BI Desktop must be installed. It is available free at [powerbi.microsoft.com](https://powerbi.microsoft.com/desktop).

**Steps to open and explore the report:**

1. Clone or download this repository.
2. Open `sales_insights.pbix` in Power BI Desktop.
3. Start on the navigation hub (Page 1) and click any section button to explore.
4. Use the slicers on each page to filter by time period, segment, region, or category.
5. Right-click any product bar in the Product Analysis or Executive Overview pages to access the drillthrough product detail view.

---

## Project Structure

```
sales-insights-powerbi/
│
├── sales_insights.pbix                        # Main Power BI report file
├── README.md                                  # Project documentation
├── screenshot_page1_navigation.png            # Navigation hub
├── screenshot_page2_executive_overview.png    # Executive Overview
├── screenshot_page3_product_analysis.png      # Product Analysis
├── screenshot_page4_customer_returns.png      # Customer and Returns Analysis
└── screenshot_page5_product_detail.png        # Drillthrough: Product Detail
```

---

## Skills Demonstrated

This project demonstrates practical, employer-relevant skills across the full business intelligence workflow:

**Data Modeling** — designing a normalized star schema with clearly separated fact tables (Sales_Fact, Returns_Fact) and dimension tables (Product_Dim, Customer_Dim, Region_Dim, Date_Dim) with correctly structured one-to-many relationships.

**DAX Development** — writing calculated measures for financial KPIs, ratio metrics, conditional status labels (Return Rate Status), and time-based aggregations across a multi-table model.

**Report Design** — structuring a five-page report with logical navigation flow, consistent layout, and purposeful visual selection aligned to the analytical question each page answers.

**Interactivity and UX** — implementing page navigation buttons, drillthrough pages, cross-filtering, price range slicers, and contextual tooltips to create a self-service reporting experience.

**Business Domain Knowledge** — translating sales, product, customer, and returns data into metrics that map directly to executive decision-making: category profitability analysis (Technology profitable; Furniture and Office Supplies loss-making), customer segment value, return risk monitoring, and regional revenue distribution.


