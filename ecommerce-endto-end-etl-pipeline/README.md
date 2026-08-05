# 🛒 E-Commerce Data Engineering Pipeline using Databricks, PySpark & Delta Lake

## 📌 Project Overview

This project demonstrates an **end-to-end Data Engineering pipeline**
for an **E-Commerce** business using **Databricks**, **Apache Spark
(PySpark)**, **Delta Lake**, and **Unity Catalog**. It follows the
**Medallion Architecture (Bronze → Silver → Gold)** to transform raw CSV
files into trusted, analytics-ready datasets.

The project showcases industry-standard ETL development, scalable data
processing, Delta Lake best practices, and dimensional modeling for
reporting and dashboards.

------------------------------------------------------------------------

## 🚀 Key Features

- End-to-end ETL pipeline using PySpark
- Medallion Architecture implementation
- Delta Lake for ACID-compliant storage
- Unity Catalog for data governance
- Data cleansing and validation
- Star schema with Fact and Dimension tables
- Dashboard-ready Gold layer
- Modular and scalable design

------------------------------------------------------------------------

## 🛠️ Technology Stack

| Technology         | Purpose                     |
|--------------------|-----------------------------|
| Databricks         | Data Engineering Platform   |
| PySpark            | Distributed Data Processing |
| Delta Lake         | Reliable Storage Layer      |
| Unity Catalog      | Metadata & Governance       |
| Python             | ETL Development             |
| SQL                | Data Analysis               |
| CSV                | Source Data                 |
| Git & GitHub       | Version Control             |
| Power BI / Tableau | Dashboard Reporting         |

------------------------------------------------------------------------

# 🏗️ Project Architecture

``` text
              Raw CSV Files
                    │
                    ▼
      Unity Catalog Volume (source_data/raw)
                    │
                    ▼
          Bronze Layer (Raw Data)
                    │
                    ▼
      Silver Layer (Clean & Validated Data)
                    │
                    ▼
     Gold Layer (Fact & Dimension Tables)
                    │
                    ▼
      Power BI / Tableau Dashboards
```

------------------------------------------------------------------------

# 📂 Unity Catalog Structure

``` text
ecommerce
│
├── source_data
│   └── raw
│
├── bronze
│   ├── brz_products
│   ├── brz_brands
│   ├── brz_category
│   ├── brz_customers
│   ├── brz_date
│   └── brz_order_items
│
├── silver
│   ├── slv_products
│   ├── slv_brands
│   ├── slv_category
│   ├── slv_customers
│   ├── slv_date
│   └── slv_order_items
│
└── gold
    ├── gld_dim_products
    ├── gld_dim_customers
    ├── gld_dim_date
    └── gld_fact_order_items
```

------------------------------------------------------------------------

# 📥 Source Datasets

| Dataset     | Description              |
|-------------|--------------------------|
| Products    | Product master data      |
| Brands      | Brand master             |
| Category    | Product category master  |
| Customers   | Customer information     |
| Date        | Calendar dimension       |
| Order_Items | Transactional sales data |

------------------------------------------------------------------------

# 🥉 Bronze Layer

**Schema:** `ecommerce.bronze`

Stores raw CSV data exactly as received.

### Tables

- brz_products
- brz_brands
- brz_category
- brz_customers
- brz_date
- brz_order_items

**Processing** - Read CSV files - Apply schema - Add ingestion
metadata - Save as Delta tables - Preserve historical data

------------------------------------------------------------------------

# 🥈 Silver Layer

**Schema:** `ecommerce.silver`

Cleanses and standardizes data.

### Tables

- slv_products
- slv_brands
- slv_category
- slv_customers
- slv_date
- slv_order_items

**Transformations** - Remove duplicates - Handle null values - Data type
conversion - Standardize formats - Business validation - Data quality
improvements

------------------------------------------------------------------------

# 🥇 Gold Layer

**Schema:** `ecommerce.gold`

Business-ready dimensional model.

### Dimension Tables

- gld_dim_products
- gld_dim_customers
- gld_dim_date

### Fact Table

- gld_fact_order_items

**Business Outputs** - Sales analytics - Customer analytics - Product
performance - Time-based reporting - Dashboard KPIs

------------------------------------------------------------------------

# ⭐ Star Schema

``` text
               gld_dim_customers
                      │
                      │
gld_dim_products ─ gld_fact_order_items ─ gld_dim_date
```

------------------------------------------------------------------------

# ⚙️ ETL Workflow

1.  Upload CSV files into Unity Catalog Volume.
2.  Read files using PySpark.
3.  Load raw data into Bronze Delta tables.
4.  Clean and validate data in Silver.
5.  Create Dimension and Fact tables in Gold.
6.  Optimize Delta tables.
7.  Connect BI tools to Gold tables.

------------------------------------------------------------------------

# 📊 Dashboard KPIs

- Total Revenue
- Total Orders
- Total Customers
- Monthly Sales
- Average Order Value
- Top Selling Products
- Category-wise Revenue
- Brand Performance
- Customer Purchase Trends
- Sales Trend Analysis

------------------------------------------------------------------------

# ⚡ Delta Lake Features

- ACID Transactions
- Schema Enforcement
- Schema Evolution
- Time Travel
- MERGE INTO
- OPTIMIZE
- VACUUM

------------------------------------------------------------------------

# 📈 Future Enhancements

- Auto Loader
- Structured Streaming
- Delta Live Tables (DLT)
- Databricks Workflows
- CI/CD Integration
- Real-time Dashboards

------------------------------------------------------------------------

# 👨‍💻 Author

**Sharath Gourishetty**

**Data Engineer**

**Skills:** Databricks • PySpark • Delta Lake • SQL • Python • Unity
Catalog • ETL • Data Engineering
