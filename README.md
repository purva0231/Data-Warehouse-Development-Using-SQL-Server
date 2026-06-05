# Data Warehouse Development Using SQL Server

I designed and implemented a modern Data Warehouse solution in Microsoft SQL Server using the Medallion Architecture (Bronze, Silver, and Gold layers) to integrate and transform data from multiple business systems, including CRM and ERP sources. The primary objective of the project was to create a centralized, scalable, and high-performance analytical platform for reporting and business intelligence.

### Key Components of the Architecture

## 1. Bronze Layer (Raw Data Ingestion)

Loaded raw data from CRM and ERP source systems without significant transformations.
Stored source tables such as:
crm_sales_details
crm_cust_info
crm_prd_info
erp_cust_az12
erp_loc_a101
erp_px_cat_g1v2
Maintained original source data to ensure traceability and support auditing requirements.

2. Silver Layer (Data Cleansing and Standardization)

Performed data cleansing, validation, and standardization.
Removed duplicates, handled missing values, and standardized formats across different source systems.
Applied business rules to improve data quality and consistency.
Created refined datasets that served as the foundation for analytical modeling.

3. Gold Layer (Business Data Model)

Built a Star Schema optimized for reporting and analytics.
Created one Fact Table and two Dimension Tables:
fact_sales
dim_customers
dim_products
Data Model Design

Fact Table – fact_sales

Stores transactional sales data.
Contains measures such as:
Sales Amount
Quantity
Price
Includes business dates:
Order Date
Shipping Date
Due Date

Sales Amount is calculated using:

Sales = Quantity × Price

Uses foreign keys to connect with customer and product dimensions.

Dimension Table – dim_customers

Stores customer-related attributes including:
Customer ID
Customer Number
First Name
Last Name
Gender
Marital Status
Birthdate
Country

Dimension Table – dim_products

Stores product-related information including:
Product ID
Product Name
Category and Subcategory
Product Line
Cost
Maintenance Status
Start Date
Project Outcome
Established a single source of truth for enterprise data.
Improved reporting performance through dimensional modeling.
Enabled efficient sales, customer, and product analysis.
