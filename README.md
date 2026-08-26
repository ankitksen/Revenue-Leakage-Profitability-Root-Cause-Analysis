# Revenue Leakage & Profitability Root Cause Analysis

## 📌 Project Overview

Revenue growth does not always mean business profitability is improving. A company can generate strong sales while losing profit because of excessive discounts, product returns, high shipping costs, low-margin products, or unprofitable customer and regional segments.

This project focuses on identifying the major sources of **revenue leakage and declining profitability** by analyzing sales, profit, discounts, returns, shipping costs, customers, products, and regional performance.

The project combines **SQL, Python, Excel, and Power BI** to perform data cleaning, exploratory analysis, root cause analysis, profitability analysis, and executive-level reporting.

---

## 🎯 Business Problem

The business is experiencing profitability pressure despite generating revenue through multiple products, customers, and regions.

Management wants to understand:

* Why is profitability declining?
* Which products generate revenue but have poor margins?
* Which customers or customer segments are causing profit leakage?
* How much profit is lost because of discounts?
* Are product returns significantly affecting profitability?
* Which regions are underperforming?
* How much does shipping cost affect margins?
* Which products, customers, and regions require immediate attention?
* What actions can management take to improve profitability?

The goal is not simply to report sales and profit.

The goal is to identify **where profit is being lost, why it is being lost, and what the business should do about it.**

---

## 💡 Why This Project Matters

A traditional sales dashboard may show:

**Revenue → $X**

**Profit → $Y**

But this does not explain the reason behind the profit.

For example:

A product may generate high revenue but have:

* High discount percentage
* High return rate
* High shipping cost
* Low gross margin

As a result, the product may appear successful from a revenue perspective while actually destroying profitability.

This project approaches the problem from a **root-cause-analysis perspective**.

---

# 🎯 Project Objectives

### Primary Objectives

1. Analyze revenue and profitability trends.
2. Identify major sources of profit leakage.
3. Measure the impact of discounts on profitability.
4. Analyze the financial impact of product returns.
5. Evaluate shipping costs and their impact on margins.
6. Identify low-margin and loss-making products.
7. Identify unprofitable customer segments.
8. Compare profitability across regions.
9. Perform root cause analysis using SQL and Python.
10. Build an executive Power BI dashboard.
11. Provide actionable business recommendations.

---

# 📊 Key Business Questions

### Revenue & Profitability

* What is the overall revenue?
* What is the total profit?
* What is the overall profit margin?
* How is profitability changing over time?
* Which products contribute the most revenue?
* Which products contribute the most profit?

### Discount Analysis

* Which products receive the highest discounts?
* Does higher discounting lead to lower margins?
* How much potential profit is lost through discounts?
* Which customers receive excessive discounts?

### Return Analysis

* Which products have the highest return rates?
* Which regions have the highest returns?
* What is the revenue impact of returns?
* What is the estimated profit impact of returns?

### Shipping Analysis

* Which products have the highest shipping costs?
* Which regions have expensive shipping?
* Does shipping cost significantly reduce product margins?

### Customer Analysis

* Which customers generate the highest revenue?
* Which customers generate the highest profit?
* Which customers generate revenue but very little profit?
* Which customer segments have negative profitability?

### Regional Analysis

* Which regions generate the highest revenue?
* Which regions generate the highest profit?
* Which regions have low profit margins?
* Are some regions affected by high shipping or return costs?

---

# 🗂️ Data Requirements

The project can be built using transactional business data containing fields such as:

### Sales

* Order ID
* Order Date
* Customer ID
* Product ID
* Quantity
* Sales Amount
* Discount
* Cost
* Profit

### Customer

* Customer ID
* Customer Name
* Customer Segment
* Customer Region

### Product

* Product ID
* Product Name
* Category
* Sub-Category
* Product Cost

### Shipping

* Shipping Cost
* Shipping Method
* Shipping Region

### Returns

* Order ID
* Return Status
* Return Date
* Return Reason

The final dataset should support analysis at **order, product, customer, and regional levels**.

---

# 🏗️ Data Architecture

The project will follow a structured analytics workflow:

```text
Raw Data
   ↓
Data Validation
   ↓
Data Cleaning
   ↓
Data Transformation
   ↓
SQL Analysis
   ↓
Python EDA
   ↓
Root Cause Analysis
   ↓
Data Modeling
   ↓
Power BI
   ↓
Business Insights
   ↓
Recommendations
```

---

# 🧹 Data Cleaning & Validation

Before performing analysis, the dataset will be checked for:

* Duplicate records
* Missing values
* Invalid dates
* Incorrect data types
* Negative or unrealistic values
* Duplicate customers
* Duplicate products
* Incorrect discount values
* Missing product costs
* Missing shipping costs
* Invalid return records

Data quality checks will be documented before analysis.

---

# 🧮 Core Business Metrics

## Revenue

```text
Revenue = Sum of Sales Amount
```

## Gross Cost

```text
Gross Cost = Product Cost + Shipping Cost
```

## Profit

```text
Profit = Revenue - Product Cost - Shipping Cost - Other Applicable Costs
```

## Profit Margin

```text
Profit Margin = Profit / Revenue
```

## Discount Rate

```text
Discount Rate = Discount Amount / Gross Sales
```

## Return Rate

```text
Return Rate = Returned Orders / Total Orders
```

## Average Order Value

```text
AOV = Revenue / Number of Orders
```

## Revenue Per Customer

```text
Revenue Per Customer = Revenue / Unique Customers
```

---

# 🔎 Root Cause Analysis Framework

The project will investigate profitability leakage across five major dimensions.

## 1. Product-Level Leakage

Identify products that:

* Generate high revenue but low profit
* Have high discount rates
* Have high return rates
* Have high shipping costs
* Have negative or very low margins

### Example Question

> Is the company generating revenue from products that are not actually profitable?

---

## 2. Customer-Level Leakage

Identify customers who:

* Generate high revenue but low profit
* Receive excessive discounts
* Have high return activity
* Create high servicing or shipping costs

### Example Question

> Which customers look valuable based on revenue but are actually low-profit?

---

## 3. Regional Leakage

Compare regions based on:

* Revenue
* Profit
* Profit Margin
* Discount
* Return Rate
* Shipping Cost

### Example Question

> Which regions have strong sales but weak profitability?

---

## 4. Discount Leakage

Analyze whether aggressive discounting is reducing profitability.

Example analysis:

```text
Discount % → Profit Margin
```

The objective is to determine whether higher discounts are associated with lower profitability.

---

## 5. Return & Shipping Leakage

Analyze the combined impact of:

```text
Returns + Shipping Costs + Product Costs
```

on final profitability.

A product with high sales but high returns and shipping expenses may create significant hidden leakage.

---

# 🧠 SQL Analysis

SQL will be used for:

* Data validation
* Aggregation
* Customer analysis
* Product analysis
* Regional analysis
* Profitability analysis
* Window functions
* Ranking
* CTE-based analysis
* Root cause analysis

Example analysis areas:

```text
Top Revenue Products
Top Profit Products
Lowest Margin Products
High Discount Customers
High Return Products
Regional Profitability
Monthly Profit Trends
Customer Profitability Ranking
```

Advanced SQL techniques will include:

* JOINs
* CTEs
* CASE statements
* Window functions
* Aggregations
* Subqueries
* Views
* Ranking
* Conditional analysis

---

# 🐍 Python Analysis

Python will be used for:

### Data Preparation

* Pandas
* NumPy

### Exploratory Data Analysis

* Distribution analysis
* Trend analysis
* Correlation analysis
* Outlier detection
* Segment analysis

### Root Cause Analysis

Python will help investigate relationships such as:

```text
Discount → Profit Margin

Return Rate → Profitability

Shipping Cost → Profit Margin

Revenue → Profit

Product Category → Profitability
```

Visualization libraries can be used to identify patterns that may not be immediately visible through tabular analysis.

---

# 📊 Power BI Dashboard

The final solution will include an executive Power BI dashboard.

## Page 1 — Executive Overview

Key KPIs:

* Total Revenue
* Total Profit
* Profit Margin
* Total Orders
* Average Order Value
* Return Rate
* Discount Rate
* Shipping Cost

Visuals:

* Revenue Trend
* Profit Trend
* Profit Margin Trend
* Revenue vs Profit
* Regional Performance
* Product Category Performance

---

# Page 2 — Profitability Analysis

Focus:

* Product profitability
* Category profitability
* Margin analysis
* Revenue vs Profit

Visuals:

* Revenue vs Profit scatter plot
* Profit Margin by Category
* Top/Bottom Products
* Profitability matrix
* Margin distribution

---

# Page 3 — Revenue Leakage Analysis

Focus on identifying hidden profit loss.

Analysis:

* Discount leakage
* Return leakage
* Shipping leakage
* Low-margin products
* High-revenue/low-profit products

The dashboard should make it easy for management to identify **where the leakage is occurring**.

---

# Page 4 — Customer Profitability

Analyze:

* Customer Revenue
* Customer Profit
* Customer Margin
* Customer Orders
* Discount received
* Return behavior

Customer segmentation can be used to classify customers into groups such as:

```text
High Revenue / High Profit
High Revenue / Low Profit
Low Revenue / High Profit
Low Revenue / Low Profit
```

The most important segment is:

**High Revenue + Low Profit**

because these customers may appear valuable but could be contributing disproportionately to profitability leakage.

---

# Page 5 — Regional Analysis

Analyze:

* Revenue by Region
* Profit by Region
* Profit Margin by Region
* Return Rate by Region
* Shipping Cost by Region

This page will help identify geographically driven profitability problems.

---

# 📐 Data Model

The Power BI model will follow a **Star Schema** where possible.

Example structure:

```text
                 Dim Customer
                      |
                      |
Dim Product —— Fact Sales —— Dim Date
                      |
                      |
                Dim Region
```

Additional tables such as Returns and Shipping can be integrated depending on the final dataset structure.

---

# ⚡ DAX Analysis

DAX will be used to create:

* Revenue measures
* Profit measures
* Profit Margin
* Discount Rate
* Return Rate
* AOV
* YoY Growth
* MoM Growth
* Variance
* Ranking
* Dynamic KPI calculations

The objective is to create reusable measures rather than relying heavily on calculated columns.

---

# 🚨 Root Cause Identification

The final analysis should answer:

### What is happening?

Profitability is declining or underperforming.

### Where is it happening?

Identify:

* Products
* Categories
* Customers
* Regions
* Time periods

### Why is it happening?

Investigate:

* Excessive discounts
* High returns
* High shipping costs
* Low product margins
* Unprofitable customers
* Regional cost differences

### What should the business do?

Provide specific recommendations based on the evidence.

---

# 💡 Business Recommendations

Recommendations will be generated from actual findings rather than assumptions.

Potential recommendation categories include:

### Discount Optimization

Review products and customers where discounting significantly reduces margins.

### Product Portfolio Optimization

Review consistently low-margin or loss-making products.

### Return Reduction

Investigate products with unusually high return rates and identify common return reasons.

### Shipping Optimization

Review high-cost shipping regions, products, and shipping methods.

### Customer Profitability Management

Prioritize high-profit customers and review pricing/discount strategies for high-revenue but low-profit customers.

### Regional Strategy

Investigate regions with strong revenue but weak profitability and determine the underlying cost drivers.

---

# 📈 Expected Business Outcome

The project is designed to help management:

* Understand profitability performance
* Identify hidden revenue leakage
* Reduce unnecessary discounting
* Improve product margins
* Reduce return-related losses
* Optimize shipping costs
* Identify profitable customer segments
* Improve regional profitability
* Make better pricing and business decisions

---

# 🛠️ Technology Stack

| Technology  | Purpose                            |
| ----------- | ---------------------------------- |
| SQL         | Data querying & business analysis  |
| Python      | EDA & advanced analysis            |
| Pandas      | Data manipulation                  |
| NumPy       | Numerical analysis                 |
| Excel       | Initial data validation & analysis |
| Power BI    | Dashboard & visualization          |
| DAX         | Business metrics                   |
| Power Query | Data transformation                |
| Git/GitHub  | Version control & documentation    |

---

# 📁 Repository Structure

```text
Revenue-Leakage-Profitability-Root-Cause-Analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── sql/
│   ├── data_validation.sql
│   ├── profitability_analysis.sql
│   ├── customer_analysis.sql
│   ├── product_analysis.sql
│   └── regional_analysis.sql
│
├── python/
│   └── revenue_leakage_analysis.ipynb
│
├── powerbi/
│   └── revenue_leakage_dashboard.pbix
│
├── excel/
│   └── data_validation.xlsx
│
├── screenshots/
│
├── README.md
└── requirements.txt
```

---

# 🔄 End-to-End Project Workflow

```text
1. Understand Business Problem
        ↓
2. Prepare Dataset
        ↓
3. Validate Data
        ↓
4. Clean & Transform Data
        ↓
5. Perform SQL Analysis
        ↓
6. Perform Python EDA
        ↓
7. Identify Profit Leakage
        ↓
8. Perform Root Cause Analysis
        ↓
9. Build Data Model
        ↓
10. Create DAX Measures
        ↓
11. Build Power BI Dashboard
        ↓
12. Generate Business Insights
        ↓
13. Provide Recommendations
        ↓
14. Document Project
```

---

# 📌 Key Deliverables

* Cleaned and validated dataset
* SQL analysis scripts
* Python EDA notebook
* Root cause analysis
* Power BI data model
* DAX measures
* Executive dashboard
* Business insights
* Actionable recommendations
* Complete GitHub documentation

---

# 🎯 Portfolio Objective

This project demonstrates the ability to go beyond basic dashboard creation and solve a complete business problem using a structured analytics approach:

**Business Problem → Data → Analysis → Root Cause → Visualization → Insight → Business Recommendation**

The primary focus is on demonstrating practical **Data Analyst / Business Intelligence skills** using SQL, Python, Power BI, Excel, statistics, data modeling, and business analysis.
