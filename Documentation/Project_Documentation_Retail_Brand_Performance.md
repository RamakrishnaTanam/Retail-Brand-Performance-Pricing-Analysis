# Project Documentation

## 1. Project Overview

**Retail Brand Performance & Pricing Analytics** is an end-to-end Business Intelligence project built to analyze men's T-shirt product data across brands.

The project combines **Azure SQL Database, SQL, Power BI and DAX** to transform product-level data into an interactive dashboard focused on **pricing, discounts, product variety and profitability**.

---

## 2. Business Objective

The analysis was designed to answer key business questions:

- Which brands offer the highest average discounts?
- Which brands have the highest average profit percentage?
- Which brands have the largest product variety?
- Which brands have the highest average selling prices?
- Which brands have the lowest average profitability?
- How do pricing and discount patterns differ across brands?

---

## 3. Data Source

The project uses a men's T-shirt retail dataset containing product and pricing information.

### Main fields

| Field | Description |
|---|---|
| Brand | Product brand |
| Title | Product name/title |
| Cost Price | Product cost |
| Marked Price | Original/listed price |
| Sale Price | Selling price |
| Discount Percentage | Discount applied to the product |
| Profit % | Product profitability percentage |

The dataset was loaded into **Azure SQL Database** before being connected to Power BI.

---

## 4. Data Preparation

### Step 1 — Load Data

The source data was loaded into an **Azure SQL Database** table.

### Step 2 — SQL Data Cleaning

Initial data preparation and cleaning were performed in Azure SQL to improve data quality before reporting.

### Step 3 — Connect Power BI

Power BI was connected to Azure SQL Database using the database connection.

### Step 4 — Power BI Data Preparation

Additional preparation and validation were performed in Power BI before creating the analytical model.

### Step 5 — DAX Calculations

DAX was used to create analytical calculations required for discount, cost, profit and pricing analysis.

---

## 5. Analytical Approach

The analysis is performed primarily at the **brand level**.

### Discount Analysis
Brands are compared using average discount percentage to identify differences in discount strategies.

### Profitability Analysis
Average profit percentage is used to identify stronger and weaker-performing brands.

### Product Variety Analysis
Product titles are counted to compare the breadth of each brand's product assortment.

### Pricing Analysis
Average sale price is compared across brands to identify higher-priced brands.

### Top & Bottom Analysis
The dashboard highlights top-performing and bottom-performing brands to make comparisons easier for business users.

---

## 6. Dashboard Pages

### Brands Overview

The overview page provides a high-level view of brand performance and includes:

- Top 5 brands by average discount %
- Top 5 brands by average profit %
- Top 5 brands by product variety
- Top 5 brands by average sale price
- Bottom 5 brands by average profit %

### Brand Details / Navigation

A dedicated brand-focused page provides a structured interface for exploring the available brands and supporting interactive analysis.

---

## 7. Visualizations Used

| Visualization | Business Purpose |
|---|---|
| Bar Chart | Compare top brands by average discount |
| Donut Chart | Compare product variety among leading brands |
| Ribbon Chart | Compare average sale prices |
| Area Chart | Compare highest average profit percentages |
| Pie/Circle Chart | Highlight bottom-performing brands |

The dashboard was designed to keep the analysis focused on **comparisons and business questions** rather than displaying raw data.

---

## 8. Power BI Service

After completing the report, it was:

1. Published to **Power BI Service**
2. Configured for online access
3. Shared through a Power BI App

This demonstrates an end-to-end workflow from **cloud database → analytics → dashboard → deployment**.

---

## 9. Key Skills Demonstrated

### Data & Database
- Azure SQL Database
- SQL data loading
- SQL data cleaning
- Data validation

### Power BI
- Azure SQL connectivity
- Data preparation
- Data modeling
- DAX
- Interactive reporting
- Dashboard design
- Power BI Service

### Data Analysis
- Brand-level aggregation
- Pricing analysis
- Discount analysis
- Profitability analysis
- Product assortment analysis
- Top/bottom performer analysis

### Business Intelligence
- Translating business questions into KPIs
- Selecting appropriate visualizations
- Presenting analytical findings
- Publishing and sharing reports

---

## 10. End-to-End Architecture

```text
                Retail Product Dataset
                         │
                         ▼
                ┌─────────────────┐
                │  Azure SQL DB   │
                │ Load + Cleaning │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │    Power BI     │
                │ Data Preparation│
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │      DAX       │
                │ Calculations & │
                │   Metrics      │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │    Dashboard    │
                │ Brand Analytics │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Power BI Service │
                │ Publish + Share │
                └─────────────────┘
```

---

## 11. Business Value

The solution provides a quick way to compare brands based on **discounting, pricing, product variety and profitability**.

It can support decisions related to:

- Pricing strategy
- Discount strategy
- Product assortment
- Brand performance
- Identification of low-performing brands

---

## 12. Project Outcome

The completed solution demonstrates the ability to take a retail dataset through a practical BI workflow:

**Data → SQL → Cloud Database → Power BI → DAX → Analysis → Visualization → Business Insights → Deployment**

This project is intended to demonstrate practical **Data Analyst / Business Intelligence** capabilities rather than only dashboard-building skills.

---

## 13. Security

No Azure credentials, passwords, connection strings containing secrets, API keys or other sensitive information are included in the repository.
