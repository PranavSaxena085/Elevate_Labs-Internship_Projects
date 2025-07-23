# Real Estate Listings and Analytics

## Objective
To track real estate property listings and generate insightful reports using SQL. The focus is on analyzing average prices by region, identifying high-demand areas, and observing price trends using window functions.

## Tools Used
- **MySQL Workbench** for database design, SQL queries, and exporting results
- **ChatGPT** was used to generate sample records for all tables

## Database Schema

The project is based on a normalized relational database with the following tables:

1. **Agents**: Stores real estate agent details
2. **Properties**: Contains listing information for properties
3. **Buyers**: Stores buyer details and budgets
4. **Transactions**: Links properties to buyers and tracks sale information

## Steps Involved in Building the Project

1. Created the database and tables with appropriate foreign key constraints.
2. Inserted mock data into all four tables (Agents, Properties, Buyers, Transactions).
3. Wrote queries to:
   - Analyze average property prices by region.
   - Create a view of high-demand areas.
   - Generate price trend reports using window functions.
4. Exported query results into CSV files using MySQL Workbench's export feature.

## Queries & Reports Generated

### 1. Average Prices by Region  
**Query:** Calculates average prices across different regions.  
**CSV File:** avg_price_by_region.csv

### 2. Average Prices by Region (Descending Order)  
**Query:** Shows regions sorted by highest average prices.  
**CSV File:** avg_price_by_region_desc.csv

### 3. High-Demand Areas View  
**Query:** Creates a view for cities with 2 or more transactions and their average sales price.  
**CSV File:** high_demand_areas.csv

### 4. Price Trend Report using Window Functions  
**Query:** Uses LAG() and LEAD() functions to compare previous and next transaction prices per city.  
**CSV File:** price_trend_report.csv

## Conclusion

This project demonstrates how SQL can be used to design and analyze a real estate database. It covers key skills such as database design, JOINs, aggregation, views, and window functions. The output is cleanly organized through exported CSVs for further use or reporting.

## 📁 Deliverables

- SQL Script: Project 2. Real Estate Listings and Analytics.sql
- CSV Files:
  - avg_price_by_region.csv
  - avg_price_by_region_desc.csv
  - high_demand_areas.csv
  - price_trend_report.csv
