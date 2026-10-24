[README.md](https://github.com/user-attachments/files/33903926/README.md)

# Retail Sales Analysis with Google Sheets & Gemini AI

**Retail Sales Performance Analysis | KPI Reporting, Category Profitability, Regional Performance & Sales Trends**

## 📌 Project Overview

This project explores retail transaction data using **Google Sheets with assistance from Gemini AI** to build a structured sales analysis and reporting workbook. It summarizes sales and profit performance, calculates key business metrics, compares product categories and regions, reviews monthly performance, and ranks the top 10 sub-categories by sales.

The workflow combines source-data review, KPI summaries, formatted analytical tables, charts, and business insights. The purpose is to turn transaction-level records into clear information that can support commercial performance reviews and better-informed business decisions.

> **Data coverage note:** The provided dataset contains 199 records from **January 1 to February 29, 2024**. It does not include the full 2024–2025 period, so the monthly comparison in this project covers January and February 2024 only.

## 🎯 Business Problem Statement

Retail teams need to understand where revenue is generated, which categories and regions contribute most to profit, and how performance changes over time. A dataset alone does not provide an easy executive overview without consistent metrics and clear visualizations.

This project addresses the following business questions:

- What are total sales, total profit, profit margin, units sold, average order value, and average discount?
- Which product categories generate the highest sales and profit?
- How do sales and profit compare across the East, North, South, and West regions?
- How did sales and profit change from January to February 2024?
- Which sub-categories contribute the most to total sales?
- What opportunities should be investigated to improve profitability and reporting?

## 🧰 Tech Stack

- **Google Sheets** — source-data review, formulas, summary tables, formatting, and charts.
- **Google Gemini AI** — assistance with creating KPI summaries, drafting initial insight statements, formatting analytical tables, and building visualizations.
- **CSV** — source and analysis-ready data files.
- **GitHub Markdown** — project documentation and screenshot presentation.

*Python, SQL, Power BI, and Tableau are not claimed as tools used to create this workbook.*

## 📂 Project Structure

```text
retail-sales-analysis/
├── Dataset/
│   ├── retail_sales_raw.csv
└── screenshots/
│   ├── 01-raw-dataset.png
│   ├── 02-kpi-summary.png
│   ├── 03-key-insights.png
│   ├── 04-category-summary-initial.png
│   ├── 05-category-summary-formatted.png
│   ├── 06-total-sales-by-category.png
│   ├── 07-profit-share-by-category.png
│   ├── 08-region-summary-and-sales-chart.png
│   ├── 09-monthly-sales-profit-trend.png
│   ├── 10-top-10-subcategories.png
│   └── 11-final-graphs-sheet.png
└── 📄 README.md
```

## 📊 Dataset Information

- **Dataset file:** [`retail_sales_raw.csv`](data/retail_sales_raw.csv)

### Column descriptions

| Column | Business meaning |
|---|---|
| `Order ID` | Identifier assigned to an order |
| `Order Date` | Date associated with the order record |
| `Region` | Sales region |
| `City` | City associated with the order |
| `Customer Segment` | Customer segment classification |
| `Category` | Product category |
| `Sub-Category` | Product sub-category |
| `Quantity` | Quantity recorded for the transaction |
| `Unit Price` | Unit price recorded |
| `Discount` | Discount rate |
| `Sales` | Sales amount |
| `Profit` | Profit amount |
| `Ship Mode` | Shipping method |

The dataset includes category and sub-category dimensions, four regions, customer segments, cities, discounts, quantities, sales, profit, and shipping modes.

## 🔄 Data Preparation and Methodology

The project workflow includes the following steps:

1. **Review the source data** — inspected the field names and sample records in Google Sheets.
2. **Validate data quality** — checked the supplied CSV for missing values and exact duplicate rows.
3. **Prepare analysis dates** — created an analysis-ready copy with consistently interpreted order dates.
4. **Calculate KPIs** — summarized sales, profit, profit margin, order records, units sold, average order value, and average discount.
5. **Group the data** — summarized sales and profit by category, region, and month; ranked sub-categories by sales.
6. **Create visuals** — built charts and formatted tables in the `Graphs` sheet with Gemini AI assistance.
7. **Review findings** — compared the reported figures with calculations from the supplied CSV before documenting the results.

The raw CSV is retained separately so the original source remains available for comparison.

## 📈 KPI Summary

| KPI | Result |
|---|---:|
| Total Sales | $8,435,420.58 |
| Total Profit | $809,228.02 |
| Overall Profit Margin | 9.59% |
| Order Records | 199 |
| Unique Order IDs | 199 |
| Total Units Sold | 836 |
| Average Order Value | $42,389.05 |
| Average Discount | 7.44% |

**Metric notes:** Profit margin is calculated as total profit divided by total sales. Average order value is total sales divided by the number of unique order IDs. Average discount is the mean of the row-level discount values. The source contains 199 rows and 199 unique order IDs; confirm the business definition of an order before interpreting this count as a count of completed customer orders.

## 📊 Dashboard and Visualization

The Google Sheets `Graphs` sheet brings together the main summaries and charts for a compact performance review.

### 1. KPI Summary and Initial Insights

The KPI table summarizes overall sales, profit, margin, order records, units sold, average order value, and average discount.


### 2. Sales and Profit by Category

The category summary compares sales and profit for Clothing, Electronics, Furniture, Grocery, and Office Supplies.

![Category summary before formatting](screenshots/04-category-summary-initial.png)

![Professionally formatted category summary](screenshots/05-category-summary-formatted.png)

### 3. Total Sales by Category

The column chart compares sales across product categories, making the largest sales contributor easy to identify.

![Total sales by category chart](screenshots/06-total-sales-by-category.png)

### 4. Profit Share by Category

The pie chart shows each category's contribution to total profit. This complements the sales chart because the highest-selling category is not necessarily the category with the highest profit margin.

![Profit share by category pie chart](screenshots/07-profit-share-by-category.png)

### 5. Sales and Profit by Region

The regional summary table compares sales and profit for East, North, South, and West. A companion column chart highlights differences in regional sales.

![Regional summary table and sales chart](screenshots/08-region-summary-and-sales-chart.png)

### 6. Monthly Sales and Profit Trend

The monthly table and chart compare January and February 2024. The data currently supports only a two-month comparison, not a complete 2024–2025 trend.

![Monthly sales and profit trend](screenshots/09-monthly-sales-profit-trend.png)

### 7. Top 10 Sub-Categories by Sales

The ranked table and horizontal bar chart identify the ten sub-categories with the highest total sales in the supplied dataset.

![Top 10 sub-categories by sales](screenshots/10-top-10-subcategories.png)

### 8. Final Graphs Sheet

The final screenshot shows the assembled report layout and the main visual elements together.

![Final Google Sheets graphs sheet](screenshots/11-final-graphs-sheet.png)

## 🔍 Key Insights

1. **Electronics dominates sales.** Electronics generated **$6,084,971.16**, approximately **72.14%** of total sales, and contributed **$598,296.66** in profit. The business should understand which products, customers, and pricing factors drive this concentration.

2. **East leads regional performance.** The East region recorded **$2,562,914.89** in sales and **$253,292.63** in profit, the highest totals among the four regions in this dataset. Its performance may offer practices worth investigating for other regions.

3. **Sales leadership and margin leadership differ.** Clothing generated **$360,076.71** in sales and **$69,644.02** in profit, giving it an approximate **19.34%** profit margin. Furniture generated **$1,739,889.46** in sales and **$109,789.82** in profit, an approximate **6.31%** margin. This shows why revenue should be reviewed alongside profitability.

4. **February sales declined while profit increased.** Sales decreased from **$4,304,431.99** in January to **$4,130,988.59** in February, a decrease of approximately **4.03%**. Profit increased from **$360,266.32** to **$448,961.70**, an increase of approximately **24.62%**. This two-month result is worth investigating, but it is not enough to establish a long-term trend or explain the cause.

5. **Cameras is the highest-selling sub-category.** Cameras generated **$2,118,280.88** in sales, followed by Mobiles at **$1,745,778.74** and Accessories at **$1,395,555.51**. These leading sub-categories account for a substantial share of recorded sales and deserve closer review of stock availability, margins, and demand patterns.

*Insights above are calculated from the provided dataset. They describe this sample and should not be generalized to periods or records that are not included.*

## 💡 Business Recommendations

- **Investigate Electronics concentration:** Review sales and profit by Electronics sub-category, city, customer segment, discount, and shipping mode to understand the drivers of its large sales share.
- **Study regional best practices:** Compare East-region product mix, discounts, and customer segments with other regions before recommending changes elsewhere.
- **Optimize for profit, not only revenue:** Monitor category-level profit margin alongside sales and review pricing, discounting, and costs for lower-margin categories such as Furniture.
- **Investigate February's margin improvement:** Check product mix, discounts, and other available transaction attributes to determine why profit rose despite lower sales. The current dataset alone does not establish causation.
- **Monitor high-sales sub-categories:** Track demand, stock availability, profit, and discount levels for Cameras, Mobiles, and Accessories.
- **Extend the reporting period:** Add the remaining months of 2024 and data for 2025 before building a full-year or year-over-year trend.
- **Validate order definitions:** Confirm whether each row represents a complete order or an order line before using row counts as a formal order KPI.

These are recommendations for further investigation; the project does not claim that these actions have already been implemented or that they have delivered business results.

## 📌 Skills Demonstrated

- Spreadsheet-based data exploration and validation.
- KPI definition and summary reporting.
- Sales and profitability analysis.
- Category, sub-category, and regional comparisons.
- Month-over-month performance comparison.
- Data visualization and chart selection.
- Business insight writing and recommendation development.
- AI-assisted spreadsheet workflow using Google Gemini.
- GitHub documentation with Markdown and embedded screenshots.

## 👨‍🎓 Author

**anchoori swapnith**

*Data Analyst Portfolio Project — Retail Sales Analysis using Google Sheets and Gemini AI*
