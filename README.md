# -Coffee-Shop-Sales-Power-BI-MySQL
Got it — I’ll integrate your **Problem Statement** and **KPI/Chart Requirements** directly under the *Project Description* so your README reads like a professional case study.

Here’s the **fully integrated README.md**:

---

# ☕ Coffee Shop Sales — Power BI + MySQL (Portfolio Project)

![Portfolio Hero](images/coffee-portfolio-hero.png)

> An end-to-end business intelligence project analyzing real coffee shop transactional data. Designed and implemented a fully interactive Power BI dashboard connected to MySQL, delivering actionable insights into sales, orders, and product performance trends.

---

## 📖 Project Description

This project simulates a **real-world retail analytics** scenario for a coffee shop chain with multiple locations.

### Process Overview

* **Data Extraction & Loading** — Loaded raw transactional CSV files into **MySQL**.
* **Data Transformation** — Cleaned and shaped data in **Power Query**.
* **Data Modeling** — Built a **star schema** with:

  * **Fact Table:** `Transactions`
  * **Dimension Table:** `Date Table`
* **DAX Measures** — Created KPIs:

  * Total Sales
  * Total Orders
  * Total Quantity Sold
  * Month-over-Month (MoM) growth and difference
  * Daily average sales
* **Visualization Design** — Built interactive visuals to:

  * Detect sales trends
  * Compare performance across stores and categories
  * Highlight peak sales days/hours

---

## 📌 Problem Statement

The coffee shop chain needed a **comprehensive sales performance dashboard** to monitor business health, identify trends, and optimize product and store strategies. The dashboard had to answer key business questions such as:

* How are sales trending compared to last month?
* Which days and hours have the highest demand?
* How do weekends compare to weekdays in terms of revenue?
* Which product categories and items are top performers?
* Which store locations are improving or declining?

---

## 📊 KPI Requirements

### 1. **Total Sales Analysis**

* Calculate monthly total sales
* Determine MoM % increase/decrease
* Show absolute difference vs previous month

### 2. **Total Orders Analysis**

* Calculate monthly total orders
* Determine MoM % change
* Show difference vs previous month

### 3. **Total Quantity Sold Analysis**

* Calculate monthly total quantity sold
* Determine MoM % change
* Show difference vs previous month

---

## 📈 Chart Requirements

1. **Calendar Heat Map**

   * Color-coded by sales volume
   * Dynamic per selected month
   * Tooltips with Sales, Orders, Quantity

2. **Weekday vs Weekend Sales**

   * Segment data for performance comparison
   * Highlight differences in patterns

3. **Sales by Store Location**

   * Visualize sales per store
   * MoM difference metrics
   * Color coding for increase/decrease

4. **Daily Sales with Average Line**

   * Compare each day to daily average
   * Highlight above/below average

5. **Sales by Product Category**

   * Identify top-performing categories

6. **Top 10 Products by Sales**

   * Quickly visualize best sellers

7. **Sales by Days & Hours**

   * Heat map for demand peaks
   * Tooltips with key metrics

---

## 📦 Data Model

### **Fact Table: Transactions**

**Core fields:**

* Hour, product\_category, product\_detail, product\_id, product\_type
* sales, store\_id, store\_location
* transaction\_id, transaction\_date, transaction\_city, transaction\_time
* unit\_price, transaction\_qty

**Calculated measures:**

* CM Orders, CM Quantity, CM Sales
* PM Orders, PM Quantity, PM Sales
* MoM Growth & Difference (Sales, Orders, Quantity)
* Total Orders, Total Quantity Sold, Total Sales
* Daily Avg Sales
* TT for Hour, Colour For Bars
* Labels for Product Category, Product Type, Store Location
* Foot Note, Place Holder

---

### **Dimension Table: Date Table**

* Date, Day Name, Day Number
* Month, Month Number, Month Year
* Week Day Number, Week Number
* Weekend / Weekday

**Relationship**

* One-to-Many: `Date Table[Date]` → `Transactions[transaction_date]`

---

## 💡 Why This Model Works for BI

* Star schema for clean separation of facts/dimensions
* Date table enables:

  * Calendar heat maps
  * MoM & YoY trends
  * Weekday/weekend splits
* Prebuilt measures simplify visuals
* Conditional formatting improves storytelling

---

## 📸 Visuals

1. Calendar Heat Map
2. Weekday vs Weekend comparison
3. Store Location MoM bar chart
4. Daily Sales with Average line
5. Product Category & Type breakdown
6. Top 10 Products by sales
7. Day × Hour heat map

---

## 🧪 Reproduction Steps

1. Load sample CSVs into MySQL
2. Build `Date Table` in Power Query
3. Create relationship as above
4. Implement DAX measures
5. Recreate visuals per requirements

---





## 🙋‍♂️ Author

Your Name — [LinkedIn](#) · [Email](#)

---



