# Olist_Ecommerce
End-to-end PySpark data processing pipeline on Google Cloud Dataproc using the Olist Brazilian E-Commerce dataset — includes ingestion, cleaning, integration, optimization, and serving for analytical insights.




Data Processing and Optimization on Google Cloud Dataproc using PySpark
Using the Olist Brazilian E-Commerce Dataset (Kaggle)
📖 Overview

This project demonstrates a complete big data engineering pipeline using Apache Spark on Google Cloud Dataproc.
It showcases every step of the data lifecycle — from data ingestion and cleaning to integration, optimization, aggregation, and data serving — using the Olist Brazilian E-Commerce dataset from Kaggle.

The pipeline focuses on applying PySpark best practices for efficient distributed processing, join optimization, and configuration tuning, making it ideal for scalable data analytics and reporting.

🧠 Dataset Description — Olist Brazilian E-Commerce

The Olist dataset
 is a real-world dataset containing detailed information about orders placed on Olist, the largest department store in Brazilian marketplaces.

It includes data collected between 2016 and 2018, covering multiple aspects of the e-commerce process — customers, sellers, products, payments, deliveries, and reviews.

Key Datasets and Their Purpose

| Dataset                                 | Description                                                                             |
| --------------------------------------- | --------------------------------------------------------------------------------------- |
| `olist_customers_dataset.csv`           | Customer details such as ID, location (city, state), and unique customer identifiers.   |
| `olist_orders_dataset.csv`              | Order-level information including purchase timestamp, order status, and delivery dates. |
| `olist_order_items_dataset.csv`         | Items within each order — product IDs, seller IDs, and shipping limits.                 |
| `olist_products_dataset.csv`            | Product catalog data — category, dimensions, and product descriptions.                  |
| `olist_sellers_dataset.csv`             | Seller information including location and ID mapping.                                   |
| `olist_order_reviews_dataset.csv`       | Customer review scores and comments for orders.                                         |
| `olist_order_payments_dataset.csv`      | Payment details such as type (credit card, boleto, voucher) and installment count.      |
| `product_category_name_translation.csv` | English translations for Portuguese product categories.                                 |


Use Case

The dataset enables rich analytical exploration, such as:

-- Tracking sales and delivery performance over time

-- Analyzing customer satisfaction through reviews

-- Studying payment preferences and trends

--Measuring seller performance and regional order distribution
