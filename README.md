# 📊 Store Performance Analytics Dashboard (Excel)

## Overview

This project demonstrates an end-to-end analytics workflow built entirely in Microsoft Excel, transforming raw operational data into a weekly performance dashboard.

The dashboard tracks store performance across multiple behavioral funnels:

* App Users
* Store View Activity
* Product Link Shared
* Orders
* Order Revenue

Instead of manually calculating metrics, the file simulates a real analytics pipeline using lookup logic and aggregation modeling.

---

## Data Architecture

The workbook is structured as a layered data model:

### 1. Raw Event Tables

These sheets represent different user activities (simulating database tables):

* `Store View` → users visiting store pages
* `Product Link Shared` → users sharing product links
* `Order` → transaction events
* `Order Revenue` → payment confirmation & revenue data
* `Active App User` → daily active users

Each sheet contains timestamped event-level data.

---

### 2. Analytics Layer (Transformation Layer)

Sheet: **Analytics**

This sheet acts as a semantic model built using Excel formulas:

Key transformations:

* XLOOKUP joins between tables
* Status validation (Paid vs Not Paid)
* Week grouping (Week Num & Week Range)
* Monthly labeling
* Deduplication logic for unique users

Essentially this sheet functions similar to a SQL transformation layer.

---

### 3. Aggregation Layer

Pivot tables are created from the Analytics sheet to compute metrics:

Metrics calculated:

* Weekly Active Users
* Weekly Unique Users
* Weekly Orders
* Weekly Revenue

The pivot tables serve as an OLAP cube inside Excel.

---

### 4. Visualization Layer

Charts are built on top of pivot outputs:

* Weekly Number of Order Revenue
* Weekly Number of Orders
* Weekly Unique Users
* Weekly Users

Pivot output is referenced through helper tables to allow flexible axis labeling (week ranges instead of week numbers).

---

## Key Excel Concepts Demonstrated

* Data modeling in spreadsheets
* Multi-table joins using XLOOKUP
* Handling event vs unique user metrics
* Pivot tables as aggregation engine
* Separation of semantic layer & visualization layer
* Building dashboards without BI tools

---

## Why This Project Matters

Many analytics roles require validating business logic before data warehouse implementation.
This project shows how a complete analytics workflow can be prototyped using spreadsheet modeling before moving to SQL/BI environments.

It mirrors real analytics architecture:

Raw Events → Transformation → Aggregation → Visualization

---

## Tools Used

* Microsoft Excel (Pivot Tables, XLOOKUP, Dynamic Arrays)
* Spreadsheet Data Modeling Techniques

---

## Author

Bayu Chandra Putra
Data Analyst
