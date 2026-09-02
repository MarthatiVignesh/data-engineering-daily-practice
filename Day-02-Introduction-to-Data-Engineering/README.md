DAY 2 - INTRODUCTION TO DATA ENGINEERING
=========================================

OVERVIEW
--------

This day covers the fundamental concepts of Data Engineering,
including Data Warehouses, Data Lakes, Data Marts, Data Modelling,
Data Warehouse Schemas and a business case study.


TOPICS COVERED
--------------

1. Data Warehouse Fundamentals
2. Data Lake
3. Data Mart
4. Data Modelling Basics
5. Star Schema
6. Snowflake Schema
7. Third Normal Form (3NF)
8. Business Case Study


THEORY
------

The theory folder contains detailed notes on:

- Data Warehouse
- Data Lake
- Data Mart
- Data Modelling
- Star Schema
- Snowflake Schema
- 3NF


DIAGRAMS
--------

The diagrams folder contains:

- Data Warehouse architecture
- Data Lake architecture


PRACTICAL CASE STUDY
---------------------

Scenario:

An online shopping company needs to store and analyze
customer, product, order and sales data along with raw
website and application data.

Decision:

DATA WAREHOUSE
- Used for structured and curated business data.
- Used for reporting and analytics.
- Suitable for historical analysis.

DATA LAKE
- Used for raw and diverse data.
- Can store structured, semi-structured and unstructured data.
- Suitable for future analytics and machine learning.

STAR SCHEMA
- Selected for the analytical Data Warehouse.
- Contains a central Sales Fact table.
- Connected to Product, Customer, Store and Date dimensions.

GRAIN
- One row represents one product line in one order.


SAMPLE DATA
-----------

File:

practice/sales_data.csv

The dataset contains:

- Order ID
- Product
- Customer
- City
- Quantity
- Sales Amount


ACTUAL ANALYSIS
---------------

Ubuntu awk commands were used to analyze the sales dataset.

1. TOTAL SALES

Total Sales = 145500


2. SALES BY CITY

Vijayawada = 4500
Hyderabad = 67000
Warangal = 74000


3. SALES BY PRODUCT

Keyboard = 4500
Laptop = 100000
Monitor = 36000
Mouse = 5000


4. SALES BY CUSTOMER

Sita = 25500
Arjun = 12000
Kiran = 3000
Priya = 50000
Ravi = 55000


KEY LEARNINGS
-------------

- A Data Warehouse stores curated analytical data.
- A Data Lake stores raw data in different formats.
- A Data Mart serves a specific business area.
- Data Modelling defines entities, relationships and grain.
- Star Schema is simple and analytics-friendly.
- Snowflake Schema provides more normalized dimensions.
- 3NF focuses on normalization and reducing redundancy.
- Grain defines exactly what one row represents.
- Ubuntu command-line tools can be used to perform basic
  data analysis on CSV data.


FOLDER STRUCTURE
----------------

Day-02-Introduction-to-Data-Engineering/
|
+-- README.md
|
+-- theory/
|   +-- data-warehouse.txt
|   +-- data-lake.txt
|   +-- data-mart.txt
|   +-- data-modeling.txt
|   +-- schemas.txt
|
+-- diagrams/
|   +-- data-warehouse.txt
|   +-- data-lake.txt
|
+-- practice/
|   +-- ecommerce-case-study.txt
|   +-- sales_data.csv
|
+-- outputs/
    +-- total-sales.txt
    +-- sales-by-city.txt
    +-- sales-by-product.txt
    +-- sales-by-customer.txt


CONCLUSION
----------

Day 2 provided an introduction to Data Engineering concepts
and demonstrated how business requirements can be mapped to
data storage and modelling decisions.

A practical e-commerce dataset was created and analyzed
using Ubuntu command-line tools.
