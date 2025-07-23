# Real Estate Listings and Analytics

## Introduction
This project is designed to manage and analyze real estate property listings, agents, buyers, and transactions. The goal is to generate valuable insights, such as average regional property prices, identify high-demand areas, and observe market trends using SQL window functions.

## Tools Used
- **Database System**: MySQL  
- **SQL IDE**: MySQL Workbench  
- **Data Source**: Generated using ChatGPT  
- **Platform**: GitHub

## Database Schema Overview

The project includes the following four normalized relational tables:

### 🔹 Agents
Stores agent profiles and agency information.  
- Agent_ID *(Primary Key)*  
- Agent_Name  
- Email  
- Phone_Number  
- Agency_Name  

### 🔹 Properties
Details of real estate listings.  
- Property_ID *(Primary Key)*  
- Title  
- Address  
- City  
- Region  
- Price  
- Size_sqft  
- Property_Type  
- Listing_Date  
- Agent_ID *(Foreign Key referencing *Agents*)*  

### 🔹 Buyers
Information about interested buyers.  
- Buyer_ID *(Primary Key)*  
- Buyer_Name  
- Email  
- Phone_Number  
- Budget  

### 🔹 Transactions
Captures sales activity between properties and buyers.  
- Transaction_ID *(Primary Key)*  
- Property_ID *(Foreign Key referencing -Properties-)*  
- Buyer_ID *(Foreign Key referencing -Buyers-)*  
- Agent_ID *(Foreign Key referencing -Agents-)*  
- Sales_Price  
- Transaction_Date  

> The schema is logically structured and normalized for efficient queries and integrity.

## Sample Data
Each table has been populated with 10 mock records to simulate realistic real estate listings and transactions.  
*Sample data was created using ChatGPT to match diverse property types, locations, and buyers.*

## Key Queries and Reports

The project includes the following analysis:

- **Average Prices by Region**: Compares property prices by region.
- **Sorted Price Insights**: Finds regions with the highest average prices.
- **High-Demand Area Identification**: A view that highlights cities/regions with multiple transactions.
- **Price Trend Analysis**: Uses window functions like LAG() and LEAD() to identify past and future price trends per city.

SQL Concepts Used:
- GROUP BY and aggregate functions (AVG, COUNT)  
- JOIN for combining tables  
- ORDER BY, HAVING for filtering insights  
- WINDOW FUNCTIONS for time-series analysis  
- CREATE VIEW for reusable query layers

## Views Created

### 🔸 High_Demand_Areas
This view identifies cities and regions with 2 or more transactions and shows average sales prices, helping to highlight active real estate markets.

## Trend Reports (Window Functions)
Using LAG() and LEAD(), trend reports were generated to show:

- **Previous Price** of a property sold in the same city
- **Future Price** expected based on sale chronology

This allows observation of pricing fluctuations over time per city.

## Exported CSV Reports

The following result tables were exported and saved under a dedicated folder:

1. avg_price_by_region.csv  
2. avg_price_by_region_desc.csv  
3. high_demand_areas.csv  
4. price_trend_report.csv  

These contain query results and are useful for presentation or dashboard integration.

## Project Features
- Logical and normalized relational database design  
- Realistic mock dataset simulating real-world real estate activity  
- Insightful SQL reports with window functions  
- Clean, structured SQL file for reproducibility  
- Exported CSVs ready for use in data analysis tools  

## Conclusion
This project fulfills all the internship objectives — from schema modeling and data population to complex SQL querying and trend analysis.  
It sets a strong foundation for building real estate analytics dashboards using tools like Power BI, Tableau, or web-based applications.
