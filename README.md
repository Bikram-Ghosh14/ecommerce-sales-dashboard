# 📊 E-Commerce Sales Performance Dashboard

An interactive Power BI dashboard analyzing sales, profit, and return performance for a retail e-commerce business — built to help leadership identify underperforming regions, categories, and payment trends, and make faster, data-backed decisions.

![Dashboard Preview](E-Commerce%20Sales%20Dashboard.png)

---

## 🎯 Business Problem
A retail business experiencing uneven growth needed a single source of truth to answer:
- Which regions, categories, and segments are driving profit vs. dragging it down?
- How healthy are our margins, and how often are we losing revenue to returns?
- Which shipping and payment preferences are customers actually using?

This dashboard consolidates order-level sales data into a decision-ready view for stakeholders — no manual spreadsheet digging required.

---

## 🔧 Tools & Skills Used
- **Power BI Desktop** — data modeling, report design
- **Power Query** — data import and shaping from Excel source
- **DAX** — custom measures for margin, return rate, and totals
- **Data Visualization** — KPI cards, donut charts, geo maps, trend lines

---

## 📐 DAX Measures
```dax
Total Sales = SUM(Sheet1[Sales])

Total Profit = SUM(Sheet1[Profit])

Profit Margin % = DIVIDE([Total Profit], [Total Sales])

Return Rate % = 
DIVIDE(
    CALCULATE(COUNTROWS(Sheet1), Sheet1[Return Status] = "Order Returned"),
    COUNTROWS(Sheet1)
)
```

---

## 📊 Key Insights
- **Profit margin sits at 11.2%**, with **Office Supplies** and **Technology** as the strongest-selling categories by revenue
- **Return rate is 4.9%**, aligning closely with the "Order Returned" breakdown seen in the return-status view — a healthy, low-risk return rate for retail
- **Standard Class shipping** dominates at 58.5% of orders, suggesting cost-sensitive customer behavior over speed
- **Cash on Delivery (COD)** is the most-used payment mode (41.6%), ahead of card and online payments — relevant for any payment-processing strategy
- **Copiers and Accessories** are the top two most profitable sub-categories, outperforming higher-volume categories

---

## 📁 Dataset
Superstore-style retail sales dataset (widely used public sample dataset for BI practice), sourced via an online Power BI course. Contains ~5,900 order records across Sales, Profit, Region, Category, Shipping, and Payment fields.

---

## 📷 Preview
See `E-Commerce Sales Dashboard.png` in this repo for a full dashboard screenshot.

---

## 👤 Author
**Bikram Ghosh** — Data Analyst & BI Consultant
[LinkedIn](https://linkedin.com/in/bikram-ghosh1996721b9)
