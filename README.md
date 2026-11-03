# Bank Muamalat x Rakamin - Virtual Internship Experience (VIX)
## Final Task: Business Intelligence (BI) Analyst

![Bank Muamalat](https://img.shields.io/badge/Bank_Muamalat-BI_Analyst-purple)
![Looker Studio](https://img.shields.io/badge/Visualization-Looker_Studio-green)
![MS Access](https://img.shields.io/badge/Database-MS_Access-red)

## 📌 Project Overview
This repository contains the final project for the **Virtual Internship Experience (VIX) as a BI Analyst at Bank Muamalat**. 

**Background:**
As a BI Analyst at PT Sejahtera Bersama, the objective of this project was to analyze detailed transaction data to help the company maintain and increase sales performance. The raw dataset was fragmented across four separate tables, requiring a comprehensive ETL (Extract, Transform, Load) process before meaningful visualization could occur.

## 🛠️ Tools Used
*   **Microsoft Access:** For relational database management, building relationships, and creating the Master Data query.
*   **Microsoft Excel / Google Sheets:** For data cleaning, CSV formatting, and validation.
*   **Looker Studio (Google Data Studio):** For building the interactive, executive-level business dashboard.
*   **GitHub:** For version control and documentation.

---

## 🗄️ Database Structure & Relational Model
The raw data consisted of 4 distinct tables. To integrate them, a relational model was built using Primary Keys (PK) and Foreign Keys (FK):

1.  **Customers** (PK: `CustomerID`) - Contains demographic and contact information.
2.  **Orders** (PK: `OrderID`, FK: `CustomerID`, `ProdNumber`) - Contains transaction date, quantity, and customer references.
3.  **Products** (PK: `ProdNumber`, FK: `CategoryID`) - Contains product details, price, and category references.
4.  **ProductCategory** (PK: `CategoryID`) - Contains the name and abbreviation of product categories.

*The integration process was executed by performing JOIN operations across these four tables to generate a single **Master Data** table containing 8 specific columns (order_date, category_name, product_name, product_price, order_qty, total_sales, cust_email, cust_city).*

---

## 📊 Dashboard & Key Insights
The interactive dashboard was built using Looker Studio. You can view the live dashboard here: **[Insert Looker Studio Link Here]**

**Key Insights Extracted:**
*   **Total Revenue:** The company generated a total sales revenue of **$14,657,324** across all periods.
*   **Top Performing Categories:** **Training Videos** and **eBooks** are the primary revenue drivers for the company, contributing significantly to both total sales and order quantity.
*   **Geographic Distribution:** The map visualization indicates that the majority of customers and sales are concentrated in specific regions (e.g., Washington, Houston, and San Diego).
*   **Customer Base:** The company served approximately **1,671 unique customers** during the observed period.

## 💡 Business Recommendations
Based on the data analysis and dashboard insights, the following strategic recommendations are proposed to maintain and increase sales:
1.  **Focus on High-Yield Categories:** Allocate more marketing budget and create bundling promotions for the "Training Videos" and "eBooks" categories, as they are proven to be the highest revenue generators.
2.  **Targeted Regional Campaigns:** Launch localized digital marketing campaigns in top-performing cities (Washington, Houston) to retain market share, while conducting market research in lower-performing cities to identify untapped potential.
3.  **Product Optimization:** Evaluate the pricing strategy or inventory for low-performing categories (like "Robot Kits") and consider diversifying the product variations to attract a broader audience.

---

## 🚧 Challenges Faced & Solutions
During the completion of this project, several technical challenges were encountered:
1.  **CSV Delimiter & Encoding Issue:** Exporting data from MS Access to CSV initially caused errors in Looker Studio because the delimiter format was incompatible.
    *   *Solution:* The CSV was imported into Google Sheets to standardize the formatting (comma-delimited) and then re-downloaded as a UTF-8 CSV before being uploaded to Looker Studio.
2.  **Data Integrity in Access:** Ensuring the JOIN operations did not result in duplicated data (cartesian products) due to incorrect relationships.
    *   *Solution:* Carefully verified the `Enforce Referential Integrity` settings and ensured that only unique Primary Keys were used for the relationships.
3.  **Looker Studio Geo-Chart Error:** The map visualization initially failed to render ("Invalid Dimension") because the city names were recognized as plain text.
    *   *Solution:* Manually changed the geographic data type for the `cust_city` field from "Text" to "City" within the Looker Studio data source settings.

---

## 🚀 How to Run / View
1.  Download the `.accdb` file to view the MS Access database and relationships.
2.  Download the `Master_Data.csv` to view the integrated dataset.
3.  Click the **[Insert Looker Studio Link Here]** to interact with the final dashboard.

---
*Created by Arnawan Dwi Nugraha as part of the Bank Muamalat VIX Final Task.*