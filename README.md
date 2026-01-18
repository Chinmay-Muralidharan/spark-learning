# 🚀 Databricks + PySpark E-Commerce Analytics Project (14-Day Challenge)

This repository documents my learning journey in **Databricks Community Edition** using **PySpark** on a real-world **e-commerce events dataset**.  
The goal is to build strong fundamentals in **data exploration, transformation, feature engineering, and Delta Lake storage**.

---

## 📌 Project Objectives
- Learn how to work with large datasets using **Apache Spark**
- Perform safe and scalable **data exploration**
- Create derived features for analysis (**feature engineering**)
- Store structured datasets using **Delta Lake**
- Build workflows that are relevant for a **Data Analyst role**

---

## 🛠️ Tools & Tech Stack
- **Databricks Community Edition**
- **Apache Spark / PySpark**
- **Spark SQL**
- **Delta Lake**
- Dataset: **E-commerce events** (views / clicks / cart / purchase)

---

## 📂 Dataset Overview
The dataset contains event-level user activity such as:
- `event_time`
- `event_type` (view / cart / purchase)
- product + category details
- user + session identifiers
- `price` and `brand`

This dataset is useful for analytics tasks like:
- funnel analysis
- pricing segmentation
- category-level insights
- user session behavior


# ✅ Progress Log (Day 1 → Day 4)

## ✅ Day 1 — Databricks Setup & First PySpark Run
**Main Goal:** Get comfortable with Databricks workspace + load the dataset into Spark for basic exploration.

**Notes:**
- Set up notebook and imported dataset
- Checked schema and basic columns
- Ran simple `select()` and `filter()` operations

---

## ✅ Day 2 — Spark DataFrame Exploration (Safe Data Inspection)
**Main Goal:** Learn safe ways to explore large datasets without crashing the driver.

**Notes:**
- Tried `collect()` on large data → kernel crashed (OOM)
- Understood Spark is distributed and driver memory is limited
- Used safer methods: `filter()` + `select()` + `limit()` + `show()`

---

## ✅ Day 3 — Feature Engineering (Segmentation with PySpark)
**Main Goal:** Create reusable derived columns for analysis using PySpark transformations.

**Notes:**
- Created `price_bucket` column:
  - low (<100)
  - medium (<500)
  - high (>=500)
- Implemented the same logic using a Python UDF for comparison
- Conclusion: Spark-native functions are more scalable, UDF helps for custom logic

---

## ✅ Day 4 — Delta Lake Basics (Parquet + Reliability)
**Main Goal:** Store cleaned/transformed data in Delta format and understand Delta table internals.

**Notes:**
- Converted dataset to Delta format using `.format("delta")`
- Observed Parquet part-files + `_delta_log` folder
- Learned `_delta_log` tracks commits and supports version history (time travel)
