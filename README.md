Sales Insights — Interactive Power BI Dashboard
A multi-page, production-quality business intelligence report built in Microsoft Power BI that transforms raw sales, product, customer, and returns data into actionable executive insights. The report is designed for decision-makers who need a fast, visual path from raw numbers to strategic conclusions.

Table of Contents

Project Overview
Dashboard Pages
Key Metrics Tracked
Data Model
Visualizations Used
DAX Measures
Interactivity Features
Tools and Technologies
Getting Started
Project Structure
Skills Demonstrated


Project Overview
Sales Insights is a fully interactive Power BI report that consolidates data from multiple business domains — sales transactions, product catalog, customer demographics, regional geography, and return records — into a single cohesive analytical experience.
The report is built around a star-schema data model and uses DAX measures to compute KPIs. It is structured for real-world business use, with navigation buttons on a landing page, dynamic slicers, and a drillthrough page for granular product-level investigation.
Tool: Microsoft Power BI Desktop (2026.04 release)
File format: .pbix
Report canvas size: 1280 x 720 px (16:9)

Dashboard Pages
The report contains five pages, organized for a logical flow from high-level to granular:
Page 1 — Navigation Hub
A dedicated landing page with four styled action buttons that navigate to each analytical section. This keeps the report clean and presentation-ready.
Executive Overview
The top-level summary page presenting organization-wide performance at a glance.
Visuals on this page:

Four KPI cards — Total Profit, Total Orders, Return Rate, Total Sales
Line chart — Total Revenue trend by Year-Month
Donut chart — Revenue breakdown by Customer Segment
Bar chart — Revenue by Product Name
Clustered bar chart — Revenue by Region
Slicers for Year, Quarter, Customer Segment, and Product Category

Product Analysis
A deep-dive into product performance covering revenue, profitability, and margin.
Visuals on this page:

Three KPI cards — Total Revenue, Total Units Sold, Profit Margin %
Pivot table — Category and Sub-Category breakdown showing Revenue, Profit, and Margin %
Bar chart — Revenue by Product Name
Donut chart — Revenue split by Product Category
Slicers for Category, Sub-Category, and Price range

Customer and Returns Analysis
Focused on customer behavior and return patterns to surface operational risk and segment value.
Visuals on this page:

Four KPI cards — Total Customers, Average Order Value, Return Rate, Return Rate Status
Bar chart — Top customers by Total Profit and Total Revenue (dual measure)
Pivot table — Customer Segment vs. Region matrix showing Revenue, Orders, and Return Rate
Bar chart — Return Rate by Return Reason with tooltip showing Return Rate Status
Slicers for Customer Segment, Region, and Return Reason

Drillthrough: Product Detail
A drillthrough page accessible by right-clicking any product in the report. It shows product-specific performance in full context.
Visuals on this page:

Four KPI cards — Total Revenue, Total Units Sold, Total Profit, Total Returns
Line chart — Total Revenue trend over time (Year-Month)
Detail table — Customer names, Segments, Regions, and individual order amounts for that product


Key Metrics Tracked
MetricDescriptionTotal RevenueSum of all sales transaction amountsTotal ProfitRevenue net of costProfit Margin %Profit as a percentage of revenueTotal OrdersCount of distinct ordersTotal Units SoldQuantity of items soldTotal CustomersCount of distinct customersAverage Order ValueRevenue divided by order countReturn RateReturns as a proportion of ordersReturn Rate StatusCategorized label (e.g., High / Normal / Low)Total ReturnsCount of returned items

Data Model
The report is built on a star schema with the following tables:
Sales_Fact — the central fact table containing transaction-level records including Customer Segment and TotalAmount per order.
Returns_Fact — stores return records with a ReturnReason field used for root-cause analysis.
Product_Dim — product master data including ProductName, Category, SubCategory, and Price.
Customer_Dim — customer master data including Full Name and demographic attributes.
Region_Dim — geographic dimension with RegionName used for spatial performance analysis.
Date_Dim — date dimension table supporting time-intelligence calculations, with Year, Quarter, and Year-Month attributes.
Table (Measures table) — a dedicated DAX measures table holding all calculated KPIs to keep the model organized and scalable.
Relationships are structured as one-to-many joins from dimension tables to the fact tables, enabling clean cross-filtering across all report pages.

Visualizations Used
Visual TypePurposeCard VisualKPI headline metricsLine ChartRevenue trend over timeBar ChartRanked comparisons (products, regions, customers, return reasons)Clustered Bar ChartMulti-dimensional regional comparisonDonut ChartProportional breakdowns (segment, category)Pivot TableMulti-level row/column breakdowns with multiple value fieldsDetail Table (tableEx)Row-level transaction detail in the drillthrough pageSlicerStandard filter panel (category, year, region)Advanced SlicerEnhanced search-enabled filter (segment, product category)Action ButtonNavigation and drillthrough back-button with page links

DAX Measures
All measures are centralized in a dedicated measures table. Key calculated fields include:

Total Revenue — aggregates TotalAmount from Sales_Fact
Total Profit — computed from revenue minus cost fields
Profit Margin % — ratio of profit to revenue, formatted as a percentage
Total Orders — count of order records
Total Units Sold — sum of quantity sold
Total Customers — distinct count of customers
Avg Order Value — average per-order revenue
Return Rate — returns divided by total orders, formatted as a percentage
Return Rate Status — a conditional DAX measure that categorizes the return rate into a readable status label
Total Returns — count of return records


Interactivity Features
Cross-filtering: All visuals on a page filter each other on selection. Clicking a region on the clustered bar chart, for example, filters the KPI cards, line chart, and donut chart simultaneously.
Slicers: Each page has dedicated slicers so users can isolate specific years, quarters, segments, categories, and regions without navigating away.
Page navigation: The landing page uses Power BI action buttons wired to page navigation bookmarks, providing a clean app-like experience without using the report's default tab bar.
Drillthrough: Users can right-click any product name across the report and drill through to the Product Detail page, which renders that product's complete performance breakdown automatically.
Tooltips: The Return Rate bar chart includes a tooltip showing Return Rate Status, giving users context without adding visual clutter to the chart itself.

Tools and Technologies

Microsoft Power BI Desktop 2026.04
DAX (Data Analysis Expressions) for all KPI calculations
Power Query (M language) for data shaping and transformation
Star-schema data modeling
Power BI action buttons and bookmark navigation
Power BI drillthrough functionality


Getting Started
Prerequisites: Microsoft Power BI Desktop must be installed. It is available free at powerbi.microsoft.com.
Steps to open and explore the report:

Clone or download this repository.
Open sales_insights.pbix in Power BI Desktop.
Start on the navigation hub (Page 1) and click any section button to explore.
Use the slicers on each page to filter by time period, segment, region, or category.
Right-click any product bar in the Product Analysis or Executive Overview pages to access the drillthrough product detail view.


Project Structure
sales-insights-powerbi/
│
├── sales_insights.pbix        # Main Power BI report file
└── README.md                  # Project documentation
If you export screenshots or PDF snapshots of each page, a recommended structure would be:
sales-insights-powerbi/
│
├── sales_insights.pbix
├── README.md
└── screenshots/
    ├── 01_navigation_hub.png <img width="1346" height="575" alt="image" src="https://github.com/user-attachments/assets/09b568a4-d00c-4dfb-b551-95f97fc75adf" />

    ├── 02_executive_overview.png<img width="1411" height="795" alt="Screenshot 2026-04-28 173137" src="https://github.com/user-attachments/assets/959900b1-4598-4caa-acf5-0e3068a53c1d" />

    ├── 03_product_analysis.png<img width="1409" height="784" alt="image" src="https://github.com/user-attachments/assets/f0c85252-16e0-48ab-8bbd-0fcefef5fff5" />

    ├── 04_customer_returns.png<img width="1405" height="784" alt="image" src="https://github.com/user-attachments/assets/d25e77a9-2f3a-4b05-863f-7de24f45a21e" />

    └── 05_drillthrough_product_detail.png<img width="1411" height="790" alt="image" src="https://github.com/user-attachments/assets/e96b9fe1-733d-4e7d-afe4-20dce1a89e60" />

Adding screenshots to the repository is strongly recommended — GitHub will render them inline in this README and significantly increases visibility with recruiters.
To add a screenshot to this README, replace the placeholder path in the following pattern:
markdown![Executive Overview]



Skills Demonstrated
This project demonstrates practical, employer-relevant skills across the full business intelligence workflow:
Data Modeling — designing a normalized star schema with clearly separated fact and dimension tables and correctly structured relationships.
DAX Development — writing calculated measures for financial KPIs, ratio metrics, conditional status labels, and time-based aggregations.
Report Design — structuring a multi-page report with logical navigation flow, consistent layout, and purposeful visual selection aligned to the analytical question each page answers.
Interactivity and UX — implementing page navigation buttons, drillthrough pages, cross-filtering, and contextual tooltips to create a self-service reporting experience.
Business Domain Knowledge — translating sales, product, customer, and returns data into metrics that map directly to executive decision-making: profitability, customer value, return risk, and regional performance.
