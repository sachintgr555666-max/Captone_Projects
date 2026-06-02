# E-Commerce Sales Analysis — Excel Capstone Project

> Data Cleaning, Analysis & Visualization with Excel | Prepared by **Sachin U**

![Tool](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)
![Dataset](https://img.shields.io/badge/Dataset-2000%20Orders-blue?style=flat)
![Period](https://img.shields.io/badge/Period-2023--2025-orange?style=flat)

---

## 📖 Table of Contents

1. [Project Overview](#project-overview)
2. [Data Source](#data-source)
3. [Tools & Technologies](#tools--technologies)
4. [Data Cleaning & Preparation](#data-cleaning--preparation)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [Key Insights](#key-insights)
7. [Recommendations](#recommendations)
8. [How to Use](#how-to-use)

---

## 📊 Project Overview

This project focuses on performing end-to-end data validation, cleaning, analysis, and visualization for a US-based e-commerce business using Microsoft Excel. The core business problem addressed is ensuring data reliability across multiple dimension tables — Customer, Product, and Store — and the central Sales Fact table, to identify mismatches, fill data gaps, and generate actionable revenue insights.

The analysis spans **2,000 sales orders** across **2023–2025**, covering customers from across the United States, products in six categories, and stores operating in four regions.

---

## 🗂️ Data Source

The dataset is a structured multi-table Excel workbook with the following components:

| Table | Description |
|---|---|
| `Customer_Dim` | 1,500 customers — name, age, gender, city/state, loyalty level (Bronze → Platinum) |
| `Product_Dim` | 100 products — category, sub-category, brand, cost, stock |
| `Store_Dim` | 20 stores — region (North/South/East/West), store type (Online/Outlet/Flagship) |
| `Sales_Fact` | 2,000 transactions — order date, quantity, unit price, discount, payment type, total amount, profit tier |

- **Size:** ~1,500 customers, 100 products, 20 stores, 2,000 sales records
- **Time Period:** 2023–2025
- **Geography:** United States (50 states)

---

## 🛠️ Tools & Technologies

- **Tool:** Microsoft Excel (sole tool — no Python, SQL, or BI software used)
- **Features Used:**
  - Tables & structured references
  - Conditional Formatting (missing value highlighting)
  - Find & Replace (data standardization)
  - Remove Duplicates
  - Pivot Tables
  - Dashboard with Charts & Slicers

---

## 🧹 Data Cleaning & Preparation

The raw data contained several quality issues that were resolved before analysis:

1. **Removed Duplicates** — Selected the full dataset and used Excel's built-in *Remove Duplicates* to eliminate exact duplicate rows across all dimension and fact tables.

2. **Converted to Excel Tables** — Transformed all sheets into structured Excel Tables to enable dynamic referencing, filtering, and Pivot Table compatibility.

3. **Standardized Inconsistent Values** — Used *Find & Replace* to correct inconsistencies such as:
   - Country field: "United States of America" and "usa" → standardized to "USA"
   - City names with extra whitespace (e.g., `   jonesbury ` → `Jonesbury`)
   - Name casing issues (e.g., `sheena bonilla` → proper case)

4. **Highlighted Missing Values** — Applied Conditional Formatting with a red fill to visually flag all blank/null cells across the dataset, making gaps immediately visible for review.

5. **Fixed Data Type Formatting** — Verified and corrected date formats (Order_Date stored as Excel serial numbers), numeric precision for Cost/Price/Discount fields, and ensured Quantity columns were integer type.

6. **Feature Engineering** — Duplicate validation columns (e.g., `Quantity2`, `Unit_Price3`, `Discount4`, `Total_Amount5`) were used to cross-check and verify calculated fields in the Sales Fact table.

---

## 🔍 Exploratory Data Analysis (EDA)

Key questions explored during the analysis:

- Which region generates the highest total sales revenue?
- What is the most popular store type (Online vs. Outlet vs. Flagship)?
- Which payment method do customers prefer?
- How does product category pricing compare across the catalog?
- What is the loyalty level distribution by gender?
- Which individual store performed best in 2025?

A **Pivot Table** sheet and an interactive **Dashboard** were built to answer these questions visually, with filters by region, store type, category, and time period.

---

## 💡 Key Insights

- **West Region Leads in Revenue:** The Western region significantly outperformed all other regions on average sales, with Store 8 being the top individual performer in 2025.

- **Online is the Dominant Store Type:** The majority of customers purchased through the Online channel, indicating a strong digital-first buying behavior in this customer base.

- **PayPal is the #1 Payment Method:** Among online transactions, PayPal was the most frequently used payment type, ahead of Credit Card and COD.

- **Clothing Has the Lowest Price Ceiling:** Compared to Electronics, Home, Sports, and Beauty categories, Clothing items consistently showed the lowest maximum unit prices in the catalog.

- **Female Customers Lead in Platinum Loyalty:** A higher proportion of female customers hold Platinum loyalty status compared to male customers, suggesting stronger long-term engagement among female shoppers.

---

## 🚀 Recommendations

1. **Double down on the West Region** — Allocate additional inventory, promotions, and staffing to western stores, particularly Store 8, which drove exceptional 2025 performance.

2. **Invest in Online Channel Optimization** — Since online is the top store type, improving the digital experience (faster checkout, better product discovery) can directly amplify revenue.

3. **Leverage PayPal for Promotions** — Partner promotions or cashback offers via PayPal could increase average order value, given its dominance as a payment method.

4. **Re-evaluate Clothing Pricing Strategy** — With significantly lower price ceilings in Clothing, consider premium product lines or bundle offers to raise average transaction values in this category.

5. **Build a Platinum Loyalty Program Targeting Female Customers** — Since female customers disproportionately hold Platinum status, targeted retention campaigns (exclusive deals, early access) can deepen this high-value segment.

---

## ⚙️ How to Use

1. **Open the workbook** in Microsoft Excel (2016 or later recommended for full Pivot Table and slicer support).

2. **Navigate the sheets** in this order:
   - `*_Original` sheets → raw data before cleaning
   - `*_Cleaned` sheets → processed, analysis-ready data
   - `Pivot Table` → aggregated summary views
   - `Dashboard` → interactive visual overview
   - `Summery` → project notes and conclusions

3. **Interact with the Dashboard** using the slicers/filters to explore sales by Region, Store Type, Category, or Time Period.

4. **No external dependencies** — this is a self-contained Excel file with no macros or add-ins required.

---

*Capstone Project — Data Analytics Excel Module | Prepared by Sachin U*

