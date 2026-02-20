# Library-Sales-Data-Analysis
Excel data modeling and financial analysis project for a multi-location book store.

A Data Transformation & Business Intelligence Case Study

Project Overview
This project demonstrates the transition from raw, fragmented data into a structured relational data model. The goal is to provide a library manager with actionable insights into sales performance, profitability, and inventory levels across multiple locations (Portsmouth, London, and Southampton).

Raw Data Sample (Before):
ORD-101, 15/02/26, BK001, portsmouth, 2
ORD-102, 2026-02-15, BK003, London, 5

Step 1: Data Cleaning & Organisation
The raw transaction data was initially inconsistent. I performed the following cleaning steps:

Deduplication: Audited the Order_ID sequence to ensure data integrity and unique transaction records.
Casing Standardisation: Standardised Store_Location entries using the =PROPER() function to fix casing errors (e.g., "portsmouth" to "Portsmouth").
Date Normalisation: Converted various date strings into a uniform format (YYYY-MM-DD) to allow for accurate time-series analysis.

Step 2: Relational Data Modelling
Instead of maintaining one massive, inefficient sheet, I structured the data into three relational tables:

Tab_Sales: Daily transaction logs.
Tab_Products: Master product list with pricing and cost data.
Tab_Managers: Store-specific metadata including staffing levels.

Technical Implementation:

Converted all data ranges into Official Excel Tables (Ctrl + T).
Used XLOOKUP to dynamically pull Unit Price and Unit Cost from the Products table into the Sales table.
Established Data Relationships within the Excel Data Model to link tables via Book_ID and Store_Location.

Step 3: Financial Logic & Metrics
I engineered specific columns to track business health:

Total Revenue: [Units_Sold] * [Unit_Price]
Total Cost: [Units_Sold] * [Unit_Cost]
Total Profit: [Total_Revenue] - [Total_Cost]
