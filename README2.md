# 🛒 Supermart Grocery Sales Dashboard

An interactive business dashboard that analyses **sales, profit, products, discounts and geographic performance** for a grocery retailer, so management can answer key questions without going through the full dataset.

> **Note:** The dataset in this repository is **assumed (synthetic) data** generated for demonstration and learning. Replace it with real company data before drawing business conclusions.

---

## 📌 Project Context

Ram is building a Supermart Grocery Sales Dashboard for the management team. The goal is a simple, single-page view that explains how the business is performing and where to act.

This project is delivered in two forms:

| Format | File | Best for |
|---|---|---|
| Interactive web dashboard | `supermart-dashboard.html` | Exploring with filters, presenting |
| Excel workbook | `Supermart_Grocery_Sales_Dashboard.xlsx` | Editing data, formulas, sharing offline |

---

## 🎯 Business Objectives

### Objective 1: Overall Sales Performance
*How is the overall grocery business performing?*
- Total sales and total profit
- Share of sales by product category
- Sales trend over time
- Highest-selling regions

### Objective 2: Product Performance
*Which products and categories drive sales and profit?*
- Top categories and sub-categories by sales
- Products with high sales but comparatively low profit

### Objective 3: Profit and Discount
*How are discounts and profit related to business performance?*
- Highest-profit categories and regions
- Relationship between discount and profit

### Objective 4: Geographic Performance
*Which locations contribute most to the business?*
- Top states and cities by sales
- Locations with high sales but comparatively low profit

---

## ✨ Features

**Web dashboard**
- Filters for **Year**, **Region** and **Category**
- KPI cards: total sales, total profit, profit margin, orders, average discount
- Charts: category share (doughnut), sales and profit trend (line), region and state bars, sub-category comparison, discount vs margin scatter
- Tables that flag **low-margin products** and **low-margin cities**
- Auto-generated insight sentence for each objective
- Responsive layout with light and dark mode support

**Excel workbook**
- **Dashboard** sheet: KPI tiles, auto-updating insights and 8 charts
- **Analysis** sheet: category, region, sub-category, state, city, product, discount-band and monthly tables
- **Data** sheet: 1,800 orders with filters on every column
- All figures are **live formulas** (`SUMIFS`, `COUNTIFS`, `INDEX/MATCH`, `CORREL`), so editing the Data sheet refreshes everything

---

## 🗂️ Dataset

1,800 assumed orders from **January 2022 to December 2025**, with seasonal lift in October to December and year-on-year growth.

| Column | Description |
|---|---|
| Order ID | Unique order identifier |
| Date, Year, Month | Order date and its parts |
| Category | 7 categories (Beverages, Snacks, Food Grains, Fruits & Veggies, Bakery, Eggs Meat & Fish, Oil & Masala) |
| Sub-Category | 14 sub-categories |
| Product | 28 products |
| Region | North, South, East, West, Central |
| State / City | 9 states and 10 cities across India |
| Sales (₹) | Order sales value |
| Discount | 0% to 35% in 5% steps |
| Profit (₹) | Order profit (falls as discount rises) |
| Margin | Profit ÷ Sales (formula) |

---

## 📊 Sample Findings (on the assumed data)

- Overall margin is about **7%** on roughly **₹36 L** of sales
- **Oil & Masala** is the largest category by sales
- **West** is the top region and **Maharashtra** the top state
- **Edible Oil**, **Rice** and **Fish** sell a lot but earn thin margins
- Deeper discounts reduce margin sharply: about **12% at no discount** versus about **2% at 35%**
- **New Delhi** and **Mumbai** are high-sales but low-margin cities

Your numbers will differ once you load real data.

---

## 🚀 How to Use

**Web dashboard**
1. Download `supermart-dashboard.html`
2. Open it in any modern browser (internet needed once to load Chart.js from a CDN)
3. Use the Year, Region and Category filters

**Excel workbook**
1. Open `Supermart_Grocery_Sales_Dashboard.xlsx` in Excel or LibreOffice
2. View the **Dashboard** sheet for charts and insights
3. To use your own data, paste rows into the **Data** sheet using the same columns; the Analysis and Dashboard sheets recalculate (extend ranges if you add more than 1,800 rows)

---

## 🧰 Tech Stack

- HTML, CSS, JavaScript
- [Chart.js](https://www.chartjs.org/) 4.4.1
- Python (`openpyxl`) to build the Excel workbook
- Microsoft Excel formulas and native charts

---

## 📁 Repository Structure

```
.
├── README.md
├── supermart-dashboard.html
└── Supermart_Grocery_Sales_Dashboard.xlsx
```

---

## 🔭 Possible Improvements

- Load real data from CSV or a database
- Date-range slider and top-N toggles
- Map view of state-level performance
- Forecasting of monthly sales
- Export to PDF for management reports

---

## 👤 Author

Built as a **SapphireIQ student project** (*Brilliant Minds. Intelligent Solutions.*).

## 📄 License

Add a license of your choice (for example MIT) before publishing.
