# ☕ Coffee-Shop-Sales-Power-BI-MySQL





![Dashboard Preview](https://github.com/Nikhillonkar19-code/-Coffee-Shop-Sales-Power-BI-MySQL/blob/main/Coffee-Shop-Sales.png)

An end-to-end business intelligence project analyzing real coffee shop transactional data. Designed and implemented a fully interactive Power BI dashboard connected to MySQL, delivering actionable insights into sales, orders, and product performance trends.




---

## 📖 Project Description

This project simulates a **real-world retail analytics** scenario for a coffee shop chain with multiple locations.

### Process Overview
- **Data Extraction & Loading** — Load raw transactional CSV files into **MySQL**.
- **Data Transformation** — Clean and shape data in **Power Query**.
- **Data Modeling** — Build a **star schema** with:
  - **Fact Table:** `Transactions`
  - **Dimension Table:** `Date Table`
- **DAX Measures** — Create KPIs:
  - Total Sales, Total Orders, Total Quantity Sold
  - Month-over-Month (MoM) growth and difference
  - Daily average sales
- **Visualization Design** — Build interactive visuals to:
  - Detect sales trends
  - Compare category and store performance
  - Highlight peak sales periods

---

## 🛠 Problem Statement

The coffee shop chain required a **sales performance dashboard** to monitor business health, identify trends, and optimize product and store strategies. The dashboard needed to answer:

- How are sales trending compared to last month?
- Which days and hours have the highest demand?
- How do weekends compare to weekdays in revenue?
- Which product categories and items are top performers?
- Which store locations are improving or declining?

---

## 📊 KPI Requirements

### 1. Total Sales Analysis
- Monthly total sales
- MoM percentage change
- Absolute difference vs. previous month

### 2. Total Orders Analysis
- Monthly total orders
- MoM percentage change
- Difference vs. previous month

### 3. Total Quantity Sold Analysis
- Monthly total quantity
- MoM percentage change
- Difference vs. previous month

---

## 📈 Chart Requirements

1. **Calendar Heat Map**
   - Daily sales visualized via a color gradient
   - Dynamic by selected month
   - Tooltips show Sales, Orders, Quantity

2. **Weekday vs Weekend Comparison**
   - Segment sales to reveal patterns

3. **Sales by Store Location**
   - Show per-store sales and MoM change
   - Conditional color coding (e.g., green for growth)

4. **Daily Sales with Average Line**
   - Highlight days above or below daily average

5. **Sales by Product Category**
   - Identify high-performing categories

6. **Top 10 Products by Sales**
   - Showcase best-selling items

7. **Sales by Days & Hours**
   - Heat map of demand by weekday and hour
   - Tooltips provide summary metrics

---

## 🗄 Data Model Overview

### Fact Table: `Transactions`
**Core fields:**
- Hour, product_category, product_detail, product_id, product_type  
- sales, store_id, store_location  
- transaction_id, transaction_date, transaction_time, transaction_city  
- unit_price, transaction_qty  

**Calculated measures:**
- Current Month (CM): CM Orders, CM Quantity, CM Sales  
- Previous Month (PM): PM Orders, PM Quantity, PM Sales  
- MoM Growth & Difference (Sales, Orders, Quantity)  
- Total Orders, Total Quantity Sold, Total Sales  
- Daily Avg Sales, TT for Hour, Colour For Bars  
- Label For Product Category / Type / Store Location, Foot Note, Place Holder  

---

### Dimension Table: `Date Table`
- Date, Day Name, Day Number  
- Month, Month Number, Month Year  
- Week Day Number, Week Number  
- Weekend / Weekday flag  

---

**Relationship**
- One-to-many: `Date Table[Date]` → `Transactions[transaction_date]`

---

## 💡 Why This Model Works for BI
- **Star schema** ensures clarity and performant design  
- **Granularity** allows row-level transactional analysis  
- **Date dimension** enables:
  - Heat maps
  - Time intelligence
  - Weekday/weekend splits
- **Pre-computed measures** reduce DAX complexity  
- **Labels & formatting** enhance storytelling  

---

## 📷 Visuals
- Calendar Heat Map  
- Weekday vs Weekend Comparison  
- Store-level MoM Bar Chart  
- Daily Sales with Average Line  
- Product Category & Type Breakdowns  
- Top 10 Products by Sales  
- Day × Hour Heat Map  

---

## 🔄 Reproduction Steps
1. Load sample data into MySQL  
2. Create `Date Table` in Power Query  
3. Model relationships  
4. Implement DAX measures  
5. Build visuals based on requirements  

---

## 🖼 Screenshots
- **Main Dashboard:**  
![Main Dashboard](https://github.com/Nikhillonkar19-code/-Coffee-Shop-Sales-Power-BI-MySQL/blob/main/Coffee-Shop-Sales.png)  

- **Data Model (ER Diagram):**  
![Data Model](https://github.com/Nikhillonkar19-code/-Coffee-Shop-Sales-Power-BI-MySQL/blob/main/Coffee%20shop%20Data%20Model.png)

---
## 🔗 Live Project
[![View Live Dashboard](https://img.shields.io/badge/Live-Dashboard-blue?style=for-the-badge&logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiNjIzYjhlMTItNmQ5Ny00MDZjLTk1YzQtYTI0OWY1ODAzMDY3IiwidCI6IjNiYTNhODMxLTFkMzItNDA4My1hMzBjLWQ0YTk0NGYzNWI3ZSJ9)



---

## 👤 Author
**Nikhil Lonkar** — [LinkedIn](https://linkedin.com/in/nikhil-lonkar-0436a1338)

