# Online Retail Sales Database Design Project

## Introduction
This project focuses on designing a normalized SQL database system for an online retail sales platform. The goal is to manage and analyze data related to products, customers, orders, and payments efficiently using SQL and relational database design principles.

## Tools Used
- **Database System**: MySQL
- **ER Diagram Tool**: MySQL Workbench
- **Platform**: MySQL Workbench + GitHub

## Database Design Overview

The database consists of five main entities:

###  Customers
Stores information about buyers.
- Customer_ID (Primary Key)
- Customer_Name
- Email
- Address

###  Products
Holds product details and unit prices.
- Product_ID (Primary Key)
- Product_Name
- Price
- Product_Quantity

###  Orders
Records customer orders.
- Order_ID (Primary Key)
- Customer_ID (Foreign Key referencing Customers)
- Order_Date

###  OrderDetails
Maps each order to products and their quantities.
- OrderDetail_ID (Primary Key)
- Order_ID (Foreign Key referencing Orders)
- Product_ID (Foreign Key referencing Products)
- Quantity

###  Payments
Stores payment information.
- Payment_ID (Primary Key)
- Order_ID (Foreign Key referencing Orders)
- Payment_Method
- Amount_Paid

> The schema is fully normalized to **Third Normal Form (3NF)** to eliminate redundancy and ensure data consistency across the database.

##  Sample Data
Each table is populated with mock data to simulate real-world transactions, customer records, product inventories, and payments. *I used ChatGPT to generate sample records for the tables.*

## Key Queries and Reports
The project includes SQL queries that demonstrate business reporting, such as:
- Total amount spent by each customer
- Order details with customer and payment information
- Quantity sold per product
- Monthly revenue generated from sales

These queries use JOIN, GROUP BY, aggregate functions (SUM, COUNT, AVG), and filtering clauses.

## Views Created
To streamline frequent reports, the following views are included:
1. **CustomerOrdersView** – Lists all customer orders with order date and amount paid.
2. **ProductSalesView** – Displays each product with the total quantity sold.
3. **MonthlyRevenueView** – Summarizes total revenue per month and year using YEAR() and MONTH() functions.

## Conclusion
This project demonstrates a complete SQL-based approach to designing and analyzing an e-commerce database. It includes ER modeling, normalization to 3NF, DDL scripts, data population, business queries, and view creation. The project lays the foundation for scalable and analyzable retail database systems and can be expanded further for dashboards or front-end applications.

