# Olist_Ecommerce
End-to-end PySpark data processing pipeline on Google Cloud Dataproc using the Olist Brazilian E-Commerce dataset — includes ingestion, cleaning, integration, optimization, and serving for analytical insights.




cat <<'EOF' > README.md
# 🚀 Data Processing and Optimization on Google Cloud Dataproc using PySpark  
### *Powered by the Olist Brazilian E-Commerce Dataset (Kaggle)*

---

## 📖 Overview
This project demonstrates a **complete big data engineering pipeline** using **Apache Spark on Google Cloud Dataproc**.  
It covers the full data lifecycle — from **data ingestion and cleaning** to **integration, optimization, aggregation**, and **data serving** — leveraging the **Olist Brazilian E-Commerce dataset** from Kaggle.

The main goal is to build a **scalable, high-performance PySpark pipeline** that applies data transformation, integration, and optimization best practices for analytics and reporting.

---

## 🧠 Dataset Description — Olist Brazilian E-Commerce
The **[Olist dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)** is a real-world dataset from **Olist**, the largest department store in Brazilian marketplaces.  
It includes detailed order-level information from **2016 to 2018**, spanning customers, sellers, products, payments, reviews, and delivery logistics.

### 📊 Key Datasets

| Dataset | Description |
|----------|--------------|
| `olist_customers_dataset.csv` | Customer information: unique IDs, city, and state. |
| `olist_orders_dataset.csv` | Order details: timestamps, status, and delivery info. |
| `olist_order_items_dataset.csv` | Items per order: product, seller, and shipping limits. |
| `olist_products_dataset.csv` | Product attributes: category, weight, and dimensions. |
| `olist_sellers_dataset.csv` | Seller data: location and unique identifiers. |
| `olist_order_reviews_dataset.csv` | Customer feedback: scores, comments, and timestamps. |
| `olist_order_payments_dataset.csv` | Payment info: type (credit, boleto, voucher) and installments. |
| `product_category_name_translation.csv` | Portuguese-to-English mapping for product categories. |

### 🎯 Use Cases
- Analyze sales and delivery performance  
- Identify customer satisfaction trends  
- Study payment method usage  
- Measure seller performance and geographic distribution  

---

## 🧩 Module Breakdown

### **Module 1 — Data Exploration and Understanding**
- Import raw datasets into Dataproc using PySpark  
- Explore schema, datatypes, and relationships between tables  
- Identify missing values, duplicates, and inconsistencies  

---

### **Module 2 — Data Cleaning and Transformation**
- Handle missing/null values and incorrect data types  
- Standardize timestamps, column names, and formats  
- Derive new columns (e.g., delivery time, payment delay)  
- Save cleaned datasets in **Parquet** format for optimized querying  

---

### **Module 3 — Data Integration and Aggregation**
#### 🔹 Data Integration
- Join datasets (`orders`, `customers`, `items`, `payments`, `reviews`, etc.)  
- Create a unified analytical table with customer, product, and seller insights  

#### 🔹 Optimized Joins, Aggregations, and Window Functions
- Apply **broadcast joins** and **repartitioning** for performance  
- Compute metrics like total revenue, delivery delay, and review averages  
- Use **window functions** for ranking, moving averages, and cumulative stats  

#### 🔹 Advanced Enrichment
- Integrate additional external or derived data sources  
- Build KPIs such as:
  - *Average delivery delay by region*  
  - *Monthly revenue per seller*  

---

### **Module 4 — Spark Configuration and Optimization**
- Tune Spark configuration parameters:
  - Executor memory & cores  
  - Shuffle partitions  
  - Dynamic allocation & caching  
- Optimize joins and shuffle behavior to minimize execution time  

#### 🔹 Join Optimization Strategies
- Compare join strategies: **sort-merge**, **shuffle-hash**, and **broadcast**  
- Use **partitioning** and **bucketing** to improve performance on repeated joins  

---

## 💾 Data Serving Layer
- Store final processed and aggregated data in:
  - **HDFS** or **Google Cloud Storage (GCS)**  
- Enable downstream consumption by:
  - BI tools (Looker Studio, Power BI)  
  - Data warehouses (BigQuery)  
  - Machine learning pipelines  

---

## 🛠️ Tech Stack

| Category | Tools / Technologies |
|-----------|----------------------|
| Programming | Python (PySpark) |
| Platform | Google Cloud Dataproc |
| Storage | HDFS / Google Cloud Storage |
| Libraries | PySpark SQL, DataFrame API, Window, Functions |
| File Formats | CSV, Parquet, ORC |

---

