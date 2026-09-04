# Customer Shopping Behavior Analysis

An end-to-end data analytics project analyzing retail customer shopping behavior — from raw data cleaning to SQL-driven business analysis and an interactive Power BI dashboard.

## Problem Statement

A retail company wants to better understand its customers' shopping behavior to improve sales, satisfaction, and long-term loyalty. This project answers: **how can shopping data be used to identify trends, improve engagement, and optimize marketing and product strategy?**

## Tech Stack

- **Python** (pandas) — data cleaning and feature engineering
- **PostgreSQL** (SQLAlchemy) — relational data modeling
- **SQL** — business-question-driven analysis
- **Power BI** — interactive dashboard and visualization

## Dataset

3,900 customer records with 23 attributes, including demographics, purchase amount, category, review rating, subscription status, shipping type, discount usage, and purchase frequency.

## Approach

1. **Data Preparation (Python)** — Imputed 37 missing review ratings using the median rating per product category, standardized column names, dropped a fully redundant column (`promo_code_used`), and engineered `age_group` and `purchase_frequency_days` features.
2. **Data Modeling** — Loaded the cleaned dataset into PostgreSQL for structured querying.
3. **SQL Analysis** — Answered 10 business questions using aggregations, subqueries, CTEs, and window functions.
4. **Dashboard (Power BI)** — Built an interactive dashboard with slicers for subscription status, gender, category, and shipping type.

## Key Findings

- **Revenue split:** Male customers generated $157,890 vs. $75,191 from female customers — more than double.
- **Discount behavior:** 839 customers used a discount yet still spent above the $59.76 average purchase amount.
- **Top-rated products:** Gloves (3.86), Sandals (3.84), Boots (3.82), Hats (3.80), Skirts (3.78).
- **Loyalty vs. subscription gap:** The base is 80% loyal customers (3,116 of 3,900), but only 27% are subscribed — loyalty isn't converting into subscriptions. Among repeat buyers (5+ purchases), non-subscribers outnumber subscribers 2,518 to 958.
- **Discount concentration:** Hats, Sneakers, and Coats each have discounts on nearly half of all purchases.
- **Age groups:** Revenue is fairly even across age groups, from $55,763 (Senior) to $62,143 (Young Adult).

## Dashboard

![Customer Behavior Dashboard](dashboard/dashboard_screenshot.png)

KPIs: 3.9K customers · $59.76 average purchase amount · 3.75 average review rating

## Recommendations

- Launch subscription incentives targeted at loyal, non-subscribed repeat buyers
- Investigate the drivers behind the male/female revenue gap
- Re-evaluate blanket discounting on Hats, Sneakers, and Coats
- Promote Express shipping, which correlates with higher spend
- Leverage top-rated products (Gloves, Sandals, Boots) in merchandising

## How to Reproduce

1. Run `notebooks/Analysis.ipynb` to clean the data and load it into PostgreSQL
2. Run the queries in `sql/sql.sql` against the loaded `customer` table
3. Open the Power BI file in `dashboard/` to explore the dashboard

## Author

Muhammed Muzammil
