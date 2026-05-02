# 📊 Retail Business Analytics Dashboard (Excel)

## 🧠 Overview
<img width="6443" height="3492" alt="Dashboard Preview" src="https://github.com/user-attachments/assets/9f860b7d-4ed3-4739-ac3b-a9e8d57d5043" />

This project demonstrates an end-to-end analytics workflow built entirely in Microsoft Excel, transforming raw operational data into a weekly performance dashboard.

The dashboard evaluates business performance across the behavioral funnel:

* 📱 App Users
* 👀 Store Views
* 🔗 Product Link Shared
* 🛒 Orders
* 💰 Order Revenue

Instead of manual calculation, the workbook simulates a real analytics pipeline using lookup logic and aggregation modeling.

---

## 🗂️ Data Architecture

### 1. Raw Event Tables

Each sheet represents event-level activity (similar to database tables):

* `Store View` → users visiting store pages
* `Product Link Shared` → engagement activity
* `Order` → transaction events
* `Order Revenue` → payment confirmation & revenue
* `Active App User` → daily active users

---

### 2. Analytics Layer (Transformation)

Sheet: **Analytics**

Acts as a semantic model built using Excel formulas:

* `XLOOKUP` joins between tables
* Paid vs Not Paid validation
* Weekly grouping (Week Num & Week Range)
* Monthly labeling
* Unique user logic

This layer functions similarly to a SQL transformation stage.

---

### 3. Aggregation Layer

Pivot tables aggregate the analytics dataset into metrics:

* Weekly Active Users
* Weekly Unique Users
* Weekly Orders
* Weekly Revenue

The pivot tables act as an OLAP cube inside Excel.

---

### 4. Visualization Layer

Charts visualize weekly performance trends:

* 📈 Weekly Order Revenue
* 📦 Weekly Orders
* 👤 Weekly Users
* 🧍 Weekly Unique Users

---

## 🔍 Key Insights

* There is a simultaneous drop in users, orders, and revenue in early April
* Indicates traffic disruption rather than product issue
* Recovery afterwards suggests campaign or seasonal effect

---

## 🛠 Tools Used

* Microsoft Excel
* Pivot Tables
* XLOOKUP
* Dynamic Array Functions
* Spreadsheet Data Modeling

---

## 🎯 Why This Project Matters

This project replicates a simplified BI workflow:

**Raw Events → Transformation → Aggregation → Visualization → Insight**

It demonstrates how business logic can be validated in spreadsheets before implementing in SQL/BI tools.

---

## 📁 File

`Store Performance Analytics.xlsx` — contains full working dashboard and data model

---

## Author

Bayu Chandra Putra | Data Analyst | Computer Science

---
← Back to Portfolio Index:  

https://github.com/bayucp30/portfolio-data-analyst
