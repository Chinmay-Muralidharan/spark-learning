Databricks + PySpark E-Commerce Analytics Project (14-Day Challenge)

This repository documents my learning journey in Databricks Community Edition using PySpark on a real-world e-commerce events dataset.
The goal is to build strong fundamentals in data exploration, transformation, feature engineering, and Delta Lake storage.

📌 Project Objectives

Learn how to work with large datasets using Apache Spark

Perform safe and scalable data exploration

Create derived features for analysis (feature engineering)

Store structured datasets using Delta Lake

Build workflows that are relevant for a Data Analyst role

🛠️ Tools & Tech Stack

Databricks Community Edition

Apache Spark / PySpark

Spark SQL

Delta Lake

Dataset: E-commerce events (views/clicks/cart/purchase)

📂 Dataset Overview

The dataset contains event-level user activity like:

event time

event type (view / cart / purchase)

product/category details

user and session identifiers

price and brand

This makes it suitable for analytics tasks such as:

funnel analysis

pricing segmentation

category-level insights

user session behavior

✅ Progress Log (Day 1 → Day 4)
✅ Day 1 — Getting Started with Databricks & PySpark

Focus: Setting up the environment and understanding Spark basics.

What I worked on

Navigated Databricks Workspace, Compute, and Data Explorer

Created my first Databricks notebook

Read data using PySpark DataFrames

Practiced filtering, selection, and schema inspection

Understood schema and data types differences vs Pandas

✅ Day 2 — Spark DataFrame Exploration (Safe Data Inspection)

Focus: Learning how to explore large datasets safely.

Key learnings

Spark DataFrames are lazily evaluated

Using collect() on large datasets can crash the driver (OOM issue)

Safer exploration methods:

filter()

select()

limit()

show()

✅ Goal: inspect data without pulling the full dataset into driver memory.

✅ Day 3 — Feature Engineering in PySpark

Focus: Creating derived features for analysis and segmentation.

What I implemented

Created a price_bucket column:

low (<100)

medium (<500)

high (>=500)

Extra learning

Implemented the same logic using a Python UDF to compare approaches

Conclusion:

Spark-native functions are generally more scalable

UDFs are useful when custom logic is needed

✅ Day 4 — Delta Lake Introduction (Parquet + Reliability)

Focus: Storing structured datasets using Delta format.

What I worked on

Converted the events dataset into Delta format

Observed Delta storage structure:

Parquet part-files

_delta_log folder (transaction/version tracking)

Key takeaway

Delta Lake adds reliability and structure on top of Parquet, making data easier to manage for analytics workflows.

📸 Screenshots

This repo includes screenshots showing:

Spark exploration (collect() crash vs safe filtering)

Feature engineering (price_bucket creation)

Delta storage structure (_delta_log + part-files)

✅ Key Skills Demonstrated (Data Analyst Focus)

Large dataset exploration in Spark

Safe query patterns (filter/select/limit)

Derived feature creation for segmentation

Understanding Spark execution and memory limits

Delta Lake fundamentals and storage understanding

🔜 Next Steps

Planned improvements in upcoming days:

Aggregations + KPI building (groupBy, counts, revenue)

Delta schema enforcement testing

MERGE/UPSERT concepts

Time travel queries in Delta

Basic funnel analysis from events dataset

🙌 Credits

Thanks to Databricks Codebasics Indian Data Club for the learning challenge.
