Supply Chain Visibility & Optimization - Milestone 1
Objective
Transforming a raw, flat supply chain dataset into an optimized relational Star Schema data model in Power BI.

Dataset Source
https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis

Data Cleaning and Transformation Steps
Duplicated primary datasets into dedicated dimension tables (Dim_Customer, Dim_Product, Dim_Category, Dim_Shipping, Dim_location, Dim_Department).
Removed duplicates across key categorical and structural columns.
Constructed custom dynamic date calendars utilizing DAX functions.
Established indexing surrogate key logic for tracking changes without duplicates.
Data Model Overview
A clean Star Schema containing 1 central Fact_table linked via 1-to-many relationships to 7 surrounding dimension tables.

Tools Used
Power BI Desktop
Power Query Editor
DAX (Data Analysis Expressions)
