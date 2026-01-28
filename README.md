# H&M Customer Behavior Analysis Dashboard (2020)

## Project Overview

This project focuses on analyzing and visualizing H&M's sales performance and customer behavior during the **2020 fiscal year**.  

Using [**H&M Personalized Fashion Recommendations**](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data) which is a massive dataset of **over 31 million records**, the project transforms raw data into **actionable business insights** through a high-performance **Power BI dashboard**.

The analysis highlights a business model driven by **large-scale operations** with **deep divergence in customer behavior**, particularly across **demographics** and **price sensitivity**.

---

## Key Business Insights (Executive Summary)

- **Revenue Pillars**  
  Ladieswear and the **"Regular" price segment** are vital, contributing nearly **50% of total revenue**.

- **The Demographic Paradox**  
  While **Young customers (20–25)** generate the highest traffic, **Adults (25–54)** are the true revenue engine, purchasing **3× more units**.

- **Marketing Opportunity**  
  **62% of customers** are not subscribed to fashion news, revealing a major gap in CRM strategy and strong potential for **personalized remarketing**.

- **Consumer Preferences**  
  Customers prioritize **utility and "safe" fashion**, favoring **Solid patterns** and neutral colors such as **Black, White, and Beige**.

- **Price Sensitivity**  
  Demand is **extremely elastic**, with consumption heavily concentrated in the **low-price range (0.0 – 0.05 units)**.

---

## Tech Stack & Skills

- **Tool:** Power BI Desktop  
- **Data Processing:** Power Query (ETL for **31M+ rows**)  
- **Modeling:** Star Schema (Transactions, Customers, Articles)  
- **Analysis:** DAX (Data Analysis Expressions) for complex KPIs and time-intelligence  
- **Visualization:** Interactive dashboards with **Cross-filtering**, **Page Navigation**, and **Slicers**

---

## ETL Process (Data Preparation)
Given the scale of the dataset (**31M+ rows**), a robust ETL process was implemented using **Power Query** to ensure report performance:
1.  **Data Cleaning**: 
    * Handled missing values in the `Club Member Status` and `Fashion News Frequency` columns.
    * Filtered out inconsistent records to maintain data integrity.
2.  **Data Transformation**:
    * **Normalization**: Applied data type conversions for date and numerical fields.
    * **Feature Engineering**: Created custom age groups (Young, Adult, Senior) and price segments (Regular, Premium, Luxury) to enhance categorical analysis.
3.  **Data Modeling**: Built a **Star Schema** to optimize DAX calculations and cross-filtering performance between the Transactions (Fact) and Dimension tables (Customers, Articles).

---

## Data Modeling & Features

### 1. Sales Performance & Trends

- **Seasonality**  
  Sales grew steadily in **H1 2020**, peaking in **June (~43K units)** before a sharp decline in **September (~27K units)**.

- **Category Share**  
  **Ladieswear** dominates with **47.5% of total revenue**.

- **Product Leaders**  
  Essential items such as **Trousers** and **Dresses** lead revenue, ensuring stable cash flow compared to short-term fashion trends.

---

### 2. Customer & Behavior Deep-Dive

- **Membership Paradox**  
  Active members show a lower **AOV (0.027)** than **"Left Club" customers (0.034)**.  
  Loyal customers shop **more frequently but with smaller baskets**, while less engaged customers place **rare but larger orders**.

- **Interactive Design**  
  The dashboard features **custom navigation** and **cross-filtering**.  
  For example, selecting the **"Adult"** age group dynamically filters all product preferences (colors, patterns) for that segment.

---

## Dashboard Key Performance Indicators (KPIs)

| KPI | Value | Strategic Significance |
|---|---|---|
| **Total Revenue** | 298.17K | Scaled transaction value after normalization |
| **Total Quantity Sold** | 11 Million Units | Measures inventory turnover speed |
| **Total Customers** | 862.72K | Strategic asset for behavior analysis |
| **Average Order Value (AOV)** | 0.03 | Relative measure for Upselling / Cross-selling effectiveness |

---

## Strategic Recommendations

1. **Differentiated Marketing**  
   Deploy brand-image and trend-focused campaigns for the **Young segment**, while prioritizing **bundle promotions and loyalty rewards** for **Adults** to maximize purchasing power.

2. **CRM Optimization**  
   Introduce instant incentives to convert the **62% "passive" customers** into subscribers.

3. **Inventory Management**  
   Maintain high stock levels for core **"pillars"** (Solid Trousers & Dresses) and leverage the **June peak** for mid-season clearance.

---

## Installation & Usage
Since the `.pbix` file exceeds GitHub's size limit (due to the 31M+ records), please follow these steps to view the dashboard:

1.  **Download the Dashboard**: Click the link below to download the Power BI file from Google Drive:
    * [**Download H&M_Dashboard.pbix**](https://drive.google.com/file/d/1lYctxd54RNfgIsUe6PWof52lHguDYogk/view?usp=drive_link)
2.  **Software Requirement**: Ensure you have **Power BI Desktop** installed (latest version recommended).
3.  **Open the File**: Launch Power BI Desktop and open the downloaded `.pbix` file.
4.  **Interaction**: Use the navigation buttons and slicers on the left/top panels to explore different analytical views.

---

## Limitations & Notes
* **Order Identity**: Due to the lack of an `order_id` in the source data, metrics like "Average Order Value" are approximated based on `customer_id` and `transaction_date`.
* **Anonymized Values**: Revenue and Price values have been normalized/anonymized in the original dataset for privacy, representing relative proportions rather than absolute currency values.
* **Context**: The 2020 data reflects consumer behavior during a global pandemic, which may influence typical seasonality patterns.

---

## Project Structure
- Screenshots: Folder containing images of the **Overview** and **Customer Behavior** Dashboard.
- Report.pdf: Detailed project documentation and strategic recommendations.

---

**Author:** Nguyen Minh Dat  
**Contact:** 
- **LinkedIn**: linkedin.com/in/nmdattt
- **Email**: minhdat18061999.ag@gmail.com
