# Multi-Table E-Commerce ETL & Revenue Pipeline

## Project Overview
This project outlines a Data Merging Pipeline in Python that consolidates disparate Data Sources ( Users, Orders, and Product Catalogs), validate that data integrity checks (foreign key matches/orphaned data), and builds summary views for Customer LTV and Regional revenue performance data.
## Tech Stack
* **Language:** Python
* **Libraries:** Pandas (Relation Merging, Foreign Key Auditing, Multi-Level Aggregation)

## Key Data Engineering Milestones
1. **Relational Merging Strategy:** Utilized multi-stage `left` merges against `Orders`, `Users`, and `Products` tables to preserve raw order volume, pulling only user and product attributes..
2. **Data Integrity & Orphaned Record Detection:** Removing missing values (`NaN`) resulting from invalid product SKUs and inactive user signups - stop the bad telemetry impacting the revenue metrics.
3. **Multi-Dimensional Business Analytics:** Aggregated sanitized spend data groubed by `['region', 'category']` ordered by top users by Customer Lifetime Value (LTV).

## Core Insights
* Successfully removing invalid transaction payloads (missing product price metadata) prior to running monetary summaries.
* Identified regional category performance trends to highlight top revenue drivers across geographically split user segments.