# Business Performance Intelligence Dashboard

## Project Title

**Business Performance Intelligence Dashboard**

A Power BI business intelligence project designed to analyze the performance of a Nigerian retail company and provide management with data-driven insights into revenue, profitability, customers, sales performance, and areas requiring attention.

---

## Project Overview

The **Business Performance Intelligence Dashboard** is an interactive Power BI analytics project developed to help a Nigerian retail company understand how its business is performing, what factors are driving that performance, and where management should focus its attention.

The project transforms transactional sales and supporting business data into an interactive management dashboard. The analysis covers key business areas including revenue, profitability, customer performance, regional performance, salesperson performance, products, categories, payment methods, inventory, expenses, and sales targets.

The dashboard is structured into three main report pages:

### 1. Executive Overview

Provides a high-level view of the company's overall performance using key performance indicators, sales trends, and summary analysis.

Key metrics include:

* Total Sales
* Total Cost
* Total Profit
* Profit Margin
* Total Orders
* Total Quantity
* Average Order Value
* Average Quantity per Order
* Monthly sales trends
* Sales growth

### 2. Sales & Profit Analysis

Provides detailed analysis of the factors driving revenue and profitability.

Management can investigate performance by:

* Product
* Category
* Region
* Salesperson
* Customer segment
* Payment method
* Revenue
* Profit
* Profit margin
* Quantity
* Orders

### 3. Management Analysis

Transforms the analysis into actionable business insights by answering:

> **What should management do next?**

This page identifies:

* Biggest business opportunity
* Biggest business problem
* Best-performing segment
* Worst-performing segment
* Products requiring attention
* Recommended management actions

The dashboard also includes interactive navigation and report-page tooltips to allow users to explore the data more efficiently.

---

## Business Problem

The business has access to sales and operational data, but raw transactional data alone does not provide management with a clear understanding of business performance.

Management needs to determine:

1. How much revenue the company is generating.
2. Which months are producing the strongest sales.
3. Which products and categories generate the most revenue.
4. Which categories and products are the most profitable.
5. Whether some products generate high revenue but relatively low profit.
6. Which customer segments contribute the most revenue.
7. Which regions have the strongest customer presence.
8. Which payment methods customers use most frequently.
9. Which salespeople are performing strongly.
10. Which salespeople generate high sales but comparatively poor profit.
11. Which regions are underperforming.
12. Where the company has the greatest opportunity for improvement.
13. Which products or business segments require management attention.

The primary business problem is therefore the lack of a centralized analytical view that allows management to move from **raw sales data to actionable business decisions**.

The project addresses this problem by developing an interactive Power BI dashboard that combines multiple business dimensions and performance indicators into a single analytical environment.

---

## Project Objectives

The main objectives of the project are to:

* Analyze overall business performance.
* Measure revenue and profitability.
* Identify major revenue drivers.
* Identify the most profitable products and categories.
* Compare sales performance across regions and salespeople.
* Analyze customer segments and payment methods.
* Identify high-revenue but low-profit products.
* Identify underperforming regions and salespeople.
* Analyze sales trends over time.
* Calculate month-over-month and year-over-year growth.
* Provide management with actionable recommendations.
* Create an interactive dashboard suitable for executive decision-making.

---

## Tools and Technologies Used

### Microsoft Power BI

Used for:

* Data transformation
* Data modeling
* DAX calculations
* Interactive visualizations
* Dashboard development
* Report-page tooltips
* Navigation
* Business intelligence analysis

### Microsoft Excel

Used as the source data format and for initial data inspection.

### Power Query

Used for:

* Data cleaning
* Data type correction
* Handling missing values
* Identifying inconsistencies
* Preparing tables for analysis

### DAX

Used to create calculated measures and business performance indicators, including:

* Total Sales
* Total Quantity
* Total Cost
* Total Profit
* Profit Margin %
* Total Orders
* Average Order Value
* Previous Month Sales
* Sales Growth %
* Previous Year Sales
* YoY Growth %
* Average Quantity per Order

Additional measures were created where required to support the business analysis.

---

## Dataset

The project uses the **IFEXA Business Intelligence Master Dataset**, provided as an Excel workbook.

The dataset contains multiple fact and dimension tables that support sales, customer, product, employee, date, inventory, expenses, and target analysis.

### Data Model

The workbook contains the following tables:

| Table            | Type      | Purpose                                           |
| ---------------- | --------- | ------------------------------------------------- |
| `Fact_Sales`     | Fact      | Contains transactional sales information          |
| `Dim_Customers`  | Dimension | Contains customer information                     |
| `Dim_Products`   | Dimension | Contains product information                      |
| `Dim_Employees`  | Dimension | Contains salesperson/employee information         |
| `Dim_Date`       | Dimension | Provides calendar and time intelligence fields    |
| `Fact_Inventory` | Fact      | Contains inventory and stock movement information |
| `Fact_Expenses`  | Fact      | Contains business expense information             |
| `Fact_Targets`   | Fact      | Contains employee sales and customer targets      |

---

## Key Dataset Fields

### Fact_Sales

The `Fact_Sales` table is the primary transactional table used for the sales and profitability analysis.

Key fields include:

* `Order_ID` - Unique identifier for each order
* `Order_Date` - Date the order was placed
* `Customer_ID` - Identifier for the customer
* `Product_ID` - Identifier for the product
* `Employee_ID` - Identifier for the employee/salesperson
* `Channel` - Sales channel
* `Payment_Method` - Payment method used for the transaction
* `Order_Status` - Current status of the order
* `Quantity` - Number of units sold
* `Unit_Price` - Selling price per unit
* `Discount` - Discount applied to the order
* `Gross_Sales` - Sales value before discounts
* `Discount_Amount` - Monetary value of the discount
* `Net_Sales` - Sales value after discounts

### Dim_Customers

Contains information about customers.

Key fields include:

* `Customer_ID`
* `Customer_Name`
* `Segment`
* `State`
* `City`
* `Region`
* `Join_Date`
* `Customer_Rating`

These fields support customer, segment, geographical, and regional analysis.

### Dim_Products

Contains product information.

Key fields include:

* `Product_ID`
* `Product_Name`
* `Category`
* `Brand`
* `Unit_Cost`

These fields are used to analyze product revenue, cost, profit, and profitability.

### Dim_Employees

Contains employee and salesperson information.

Key fields include:

* `Employee_ID`
* `Employee_Name`
* `Department`
* `Job_Level`
* `Region`

These fields support salesperson and employee performance analysis.

### Dim_Date

Provides the calendar structure required for time-based analysis and DAX time intelligence.

Key fields include:

* `Date`
* `Year`
* `Month_Number`
* `Month_Name`
* `Quarter`
* `Week_Number`
* `Day_Name`
* `Is_Weekend`

The date dimension supports monthly trends, previous-month comparisons, year-over-year analysis, and other time-based calculations.

### Fact_Inventory

Contains inventory information.

Key fields include:

* `Inventory_ID`
* `Date`
* `Product_ID`
* `Warehouse`
* `Opening_Stock`
* `Stock_In`
* `Stock_Out`
* `Reorder_Level`
* `Closing_Stock`

### Fact_Expenses

Contains business expense information.

Key fields include:

* `Expense_ID`
* `Expense_Date`
* `Department`
* `Expense_Type`
* `Employee_ID`
* `Amount`
* `Approval_Status`

### Fact_Targets

Contains employee performance targets.

Key fields include:

* `Target_ID`
* `Month`
* `Employee_ID`
* `Sales_Target`
* `Customer_Target`

---

## Data Preparation

Before developing the dashboard, the dataset was prepared and validated to improve the quality and reliability of the analysis.

The preparation process included:

* Reviewing the available tables and fields.
* Checking and correcting data types.
* Reviewing blank and missing values.
* Checking for duplicate records.
* Reviewing categorical fields for inconsistencies.
* Establishing relationships between fact and dimension tables.
* Creating and validating the Date Table.
* Organizing the data model into appropriate fact and dimension tables.
* Preparing the model for DAX calculations and time-intelligence analysis.

---

## Data Modeling

The Power BI data model follows a dimensional modeling approach, with transactional fact tables connected to relevant dimension tables.

The main relationships include:

* `Fact_Sales[Customer_ID]` → `Dim_Customers[Customer_ID]`
* `Fact_Sales[Product_ID]` → `Dim_Products[Product_ID]`
* `Fact_Sales[Employee_ID]` → `Dim_Employees[Employee_ID]`
* `Fact_Sales[Order_Date]` → `Dim_Date[Date]`

The model allows sales transactions to be analyzed across customers, products, employees, regions, and time.

---

## Key DAX Measures

The dashboard uses DAX measures to calculate important business performance indicators.

Core measures include:

```DAX
Total Sales
Total Quantity
Total Cost
Total Profit
Profit Margin %
Total Orders
Average Order Value
Previous Month Sales
Sales Growth %
Previous Year Sales
YoY Growth %
Average Quantity per Order
```

These measures allow the dashboard to move beyond basic totals and provide comparative and performance-based analysis.

---

## Business Questions Addressed

### Revenue

* What is the company's total revenue?
* Which month generated the highest sales?
* Which product generated the most revenue?
* Which category contributes the most revenue?

### Profitability

* Which category is the most profitable?
* Which product has the highest profit margin?
* Are there products generating high revenue but low profit?

### Customers

* Which customer type generates the most revenue?
* Which region has the highest number of customers?
* What payment method is most commonly used?

### Sales Performance

* Who is the best-performing salesperson?
* Which salesperson generates high sales but poor profit?
* Which region is underperforming?

---

## Dashboard Features

### Interactive KPI Cards

The dashboard uses KPI cards to provide an immediate overview of major business metrics such as:

* Sales
* Cost
* Profit
* Profit Margin
* Orders
* Quantity
* Average Order Value

### Sales Trend Analysis

Time-based visualizations are used to identify changes in sales performance and highlight periods of strong or weak performance.

### Product and Category Analysis

Visuals allow management to compare products and categories based on revenue, profit, and profit margin.

### Regional Analysis

Regional analysis helps identify differences in customer and sales performance across geographical areas.

### Salesperson Analysis

Salesperson performance is analyzed using sales and profitability metrics to identify strong performers and areas requiring attention.

### Report Page Tooltip

A custom report-page tooltip provides additional details when users hover over relevant data points.

The tooltip includes metrics such as:

* Sales
* Profit
* Profit Margin
* Quantity
* Orders

### Report Navigation

The dashboard includes navigation buttons for:

* Home / Executive Overview
* Sales Analysis
* Management Analysis
* Back navigation where necessary

This allows users to move between report pages without relying solely on the standard Power BI page tabs.

---

## Management Analysis

The final dashboard page translates the analysis into management-focused insights.

The analysis focuses on:

### Biggest Opportunity

Identifying the product, category, region, customer segment, or other business area with the greatest potential for improvement or growth based on the available data.

### Biggest Problem

Identifying areas where performance is weak, such as declining sales, low profitability, underperforming regions, or products with unfavorable revenue-to-profit relationships.

### Best-Performing Segment

Identifying the segment that demonstrates strong performance based on relevant business metrics.

### Worst-Performing Segment

Identifying the segment with comparatively weak performance.

### Products Requiring Attention

Identifying products that may require management attention because of factors such as:

* High sales but low profit
* Low profit margin
* Weak sales performance
* Other unfavorable performance indicators

### Recommended Actions

Recommendations are derived from the patterns identified in the data rather than from assumptions.

---

## Key Insights

The completed dashboard provides five key business insights based on the analysis of the dataset.

The insights focus on:

1. Overall revenue and sales growth.
2. Major products and categories driving revenue.
3. Profitability and margin performance.
4. Regional, customer, and salesperson performance.
5. Business areas requiring management attention.

> The specific numerical findings are presented in the completed Power BI dashboard and should be updated here after the final dashboard analysis is completed.

---

## Recommendations

Based on the findings from the dashboard, management recommendations focus on three main areas:

1. **Improve profitability** by investigating products or segments where revenue is strong but profit margins are comparatively low.

2. **Focus resources on growth opportunities** identified through high-performing products, categories, regions, or customer segments.

3. **Address underperforming areas** by investigating weak regions, salespeople, products, or other segments and implementing targeted improvement strategies.

The final recommendations should be directly linked to the numerical findings displayed in the dashboard.

---

## Dashboard Structure

```text
Business Performance Intelligence Dashboard
│
├── Page 1: Executive Overview
│   ├── KPI Summary
│   ├── Sales Trend
│   ├── Revenue Analysis
│   └── Overall Performance
│
├── Page 2: Sales & Profit Analysis
│   ├── Product Analysis
│   ├── Category Analysis
│   ├── Regional Analysis
│   ├── Salesperson Analysis
│   ├── Revenue
│   ├── Profit
│   └── Profit Margin
│
└── Page 3: Management Analysis
    ├── Biggest Opportunity
    ├── Biggest Problem
    ├── Best-Performing Segment
    ├── Worst-Performing Segment
    ├── Products Requiring Attention
    └── Recommended Actions
```

---

## Expected Business Value

The dashboard provides management with a centralized view of business performance and makes it easier to identify trends, compare business segments, and investigate performance differences.

Instead of relying only on raw transaction totals, management can use the dashboard to understand:

**What is happening → Why it is happening → Where the opportunity or problem is → What action should be considered.**

This supports more informed, data-driven business decision-making.

---

## Project Deliverables

The final project includes:

1. **Power BI `.pbix` file**
2. **Screenshot of the completed dashboard**
3. **Five key business insights**
4. **Three management recommendations**
5. **README documentation**

---

## Conclusion

The Business Performance Intelligence Dashboard demonstrates how transactional business data can be transformed into an interactive business intelligence solution.

The project combines data preparation, dimensional modeling, DAX, visualization, interactive navigation, and business analysis to provide management with a clear view of revenue, profitability, customer behavior, sales performance, and areas requiring attention.

The ultimate goal is not simply to display numbers, but to use those numbers to identify meaningful business patterns and support informed management decisions.
