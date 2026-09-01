# 📊 E-Commerce Data Analytics & Executive Dashboard

### PostgreSQL • SQL • Power BI • DAX • Power Query • Data Modeling • Business Intelligence

## 📌 Project Overview

An end-to-end **E-Commerce Data Analytics and Business Intelligence project** designed to transform transactional e-commerce data into actionable business insights using **PostgreSQL, SQL, Power Query, Data Modeling, DAX, and Power BI**.

The project delivers a **4-page interactive Executive Dashboard** covering:

* Revenue & sales performance
* Order volume and order status
* Product category performance
* Customer acquisition & retention
* Customer cohort analysis
* Delivery & logistics performance
* Seller performance
* Customer satisfaction

The dashboard analyzes approximately **99K orders and 96K customers**, with transaction data spanning **September 2016 to October 2018**.

---

## 🎯 Business Objective

The primary objective is to provide decision-makers with a centralized analytical view of e-commerce operations and identify opportunities for:

* Revenue growth
* Product category optimization
* Customer retention
* Logistics improvement
* Seller performance management
* Customer satisfaction enhancement

Rather than presenting descriptive charts alone, the project combines **data preparation, relational data modeling, analytical calculations, and interactive visualization** to support data-driven business decisions.

---

# 🛠️ Technical Skills Demonstrated

| Area                    | Technologies / Techniques                                               |
| ----------------------- | ----------------------------------------------------------------------- |
| **Database**            | PostgreSQL                                                              |
| **Querying**            | SQL                                                                     |
| **BI & Visualization**  | Power BI Desktop                                                        |
| **Data Transformation** | Power Query                                                             |
| **Data Modeling**       | Star Schema, Fact & Dimension Tables                                    |
| **Analytics**           | DAX                                                                     |
| **Time Intelligence**   | YoY Growth, YTD Analysis                                                |
| **Customer Analytics**  | New vs. Returning Customers, Cohort Analysis                            |
| **Business Analytics**  | Sales, Revenue, Logistics, Seller & Customer Analysis                   |
| **Visualization**       | KPI Cards, Time-Series Analysis, Category Analysis, Geographic Analysis |

---

# 🔄 End-to-End Data Analytics Workflow

```text
Raw E-Commerce Data
        ↓
PostgreSQL
        ↓
SQL Querying & Data Extraction
        ↓
Power Query
(Data Cleaning & Transformation)
        ↓
Data Modeling
(Star Schema)
        ↓
DAX Measures
(KPI & Analytical Calculations)
        ↓
Power BI Visualization
        ↓
Business Insights
        ↓
Strategic Recommendations
```

This workflow demonstrates the ability to work across the **full BI/data analytics pipeline**, from data extraction to executive-level reporting.

---

# 🗄️ Data Modeling

The Power BI data model follows a **Star Schema** structure to support analytical queries and interactive filtering.

### Fact Tables

* `public.orders`
* `public.order_items`

### Dimension Tables

* `Dim_Date`
* `public.customers`
* `public.products`
* `public.sellers`
* `public.order_reviews`

The model was designed to support analysis across multiple business dimensions, including:

**Time → Customer → Product → Seller → Order → Review**

Relationship configuration was also considered to prevent **ambiguous filtering paths** between related entities such as customers, sellers, and geolocation data.

---

# 🧮 SQL & DAX Analytics

## Revenue Calculation

Revenue is calculated from product price and freight value:

```DAX
Total Revenue =
SUMX(
    'public order_items',
    'public order_items'[price] +
    'public order_items'[freight_value]
)
```

## Key Analytical Measures

The dashboard implements analytical measures for:

* **Total Revenue**
* **Total Orders**
* **Total Customers**
* **Average Order Value (AOV)**
* **Revenue YoY Growth**
* **Revenue YTD**
* **New Customers**
* **Returning Customers**
* **Customer Cohort Metrics**
* **Average Delivery Days**
* **Late Order Rate**
* **Average Review Score**

These calculations combine DAX functions such as `SUMX`, `CALCULATE`, `DIVIDE`, and context-aware aggregation to produce dynamic KPIs.

---

# 📊 Dashboard & Analytical Results

## 01 — Executive Overview

The executive overview provides a high-level snapshot of overall business performance.

### Key Performance Indicators

| KPI                     |      Result |
| ----------------------- | ----------: |
| **Total Revenue**       |  **$15.8M** |
| **Total Orders**        |     **99K** |
| **Total Customers**     |     **96K** |
| **Average Order Value** | **$159.33** |
| **Revenue YoY Growth**  | **207.21%** |

The dashboard also provides monthly revenue and Revenue YTD trends, enabling analysis of business performance over time.

### Business Value

The executive page allows decision-makers to quickly assess:

* Overall revenue scale
* Order volume
* Customer base
* Average transaction value
* Revenue growth trajectory

---

# 02 — Sales & Product Analysis

The sales analysis evaluates revenue and order performance across product categories.

### Top Revenue-Generating Categories

| Rank | Category                 | Orders |    Revenue |
| ---: | ------------------------ | -----: | ---------: |
|   🥇 | Beleza & Saúde           |  8,836 | **$1.44M** |
|   🥈 | Relógios & Presentes     |  5,624 | **$1.31M** |
|   🥉 | Cama, Mesa & Banho       |  9,417 | **$1.24M** |
|    4 | Esporte & Lazer          |  7,720 | **$1.16M** |
|    5 | Informática & Acessórios |  6,689 | **$1.06M** |

Across the product-category analysis, the dashboard reports **97,277 orders and approximately $15.64M in revenue**.

### Business Value

This analysis can support:

* Product portfolio prioritization
* Marketing allocation
* Category performance monitoring
* Inventory planning
* Revenue contribution analysis

---

# 03 — Customer Analytics

Customer analytics focuses on customer acquisition, repeat purchasing, and cohort behavior.

### Customer Metrics

| Metric                                     |           Result |
| ------------------------------------------ | ---------------: |
| **New Customers**                          | **93K (96.88%)** |
| **Returning Customers**                    |   **3K (3.12%)** |
| **Customers in Cohort Analysis**           |       **96,096** |
| **Returning Customers in Cohort Analysis** |        **2,997** |

The dashboard indicates that the customer base is heavily dominated by new customers, while returning customers represent a much smaller proportion.

### Analytical Focus

Customer cohort analysis groups customers according to their **First Order Quarter**, allowing the business to evaluate repeat purchasing behavior across customer acquisition cohorts.

### Business Value

The analysis highlights opportunities for:

* Customer retention strategies
* Loyalty programs
* Personalized promotions
* Re-engagement campaigns
* Repeat-purchase optimization

---

# 04 — Logistics & Customer Satisfaction

The operational analysis combines **delivery performance, late orders, and customer reviews**.

### Operational KPIs

| KPI                       |          Result |
| ------------------------- | --------------: |
| **Average Delivery Time** |   **12.5 days** |
| **Late Order Rate**       |       **7.87%** |
| **Average Review Score**  | **4.09 / 5.00** |

The dashboard also evaluates delivery performance across customer states, with observed average delivery times ranging from approximately **8.7 to 29.3 days**, indicating significant geographical differences in logistics performance.

Seller-level review analysis shows displayed average seller ratings ranging from approximately **3.5 to 4.3**.

### Business Value

This analysis can help identify:

* Regions with longer delivery times
* Potential logistics bottlenecks
* Sellers associated with higher/lower satisfaction
* Opportunities to improve delivery reliability
* Customer experience improvement areas

---

# 💡 Key Business Insights

### 📈 1. Strong Revenue Growth

The business generated approximately **$15.8M in revenue from 99K orders**, with reported **207.21% YoY revenue growth**.

### 🛍️ 2. Revenue Concentration

**Beleza & Saúde** generated the highest revenue among the displayed categories at approximately **$1.44M**, followed by **Relógios & Presentes** at approximately **$1.31M**.

### 👥 3. Customer Retention Opportunity

With **93K new customers versus approximately 3K returning customers**, customer retention represents a major opportunity for future growth.

### 🚚 4. Regional Logistics Variability

Average delivery time varies considerably by customer state, indicating that logistics performance should be monitored at a **regional level**, rather than relying solely on the overall average.

### ⭐ 5. Customer Satisfaction

The overall average review score of **4.09/5.00** indicates generally positive customer feedback, while seller-level variation provides an additional dimension for performance evaluation.

---

# 🚀 Strategic Recommendations

Based on the analytical findings, the dashboard suggests several potential business actions:

### 1. Increase Customer Retention

Develop targeted retention initiatives for first-time customers through loyalty programs, personalized offers, and post-purchase engagement.

### 2. Prioritize High-Performing Categories

Use category-level revenue and order data to prioritize high-performing product segments for marketing and inventory planning.

### 3. Optimize Regional Logistics

Investigate regions with substantially higher delivery times and identify potential opportunities for fulfillment and transportation optimization.

### 4. Monitor Seller Performance

Combine seller-level order activity, revenue contribution, and customer review scores to identify high-performing sellers and improvement opportunities.

### 5. Establish Continuous KPI Monitoring

Use Power BI's interactive reporting capabilities to continuously monitor revenue, customer, logistics, and satisfaction KPIs.

---

# 📁 Project Structure

```text
E-Commerce-Executive-Dashboard/
│
├── README.md
│
├── E-Commerce Executive Dashboard.pdf
│
├── SQL/
│   └── queries.sql
│
├── PowerBI/
│   └── e-commerce-dashboard.pbix
│
└── Dataset/
    └── ...
```

---

# 📌 Project Highlights for Recruiters

This project demonstrates practical experience in:

* **PostgreSQL & SQL data extraction**
* **Data cleaning and transformation**
* **Power Query**
* **Power BI dashboard development**
* **DAX analytical modeling**
* **Star Schema data modeling**
* **Time-series analysis**
* **Customer cohort analysis**
* **Customer retention analysis**
* **Sales & revenue analytics**
* **Logistics performance analysis**
* **Seller performance analysis**
* **Business KPI development**
* **Data-driven business recommendations**

---

# 🎓 Skills & Keywords

`PostgreSQL` · `SQL` · `Power BI` · `DAX` · `Power Query` · `Data Analytics` · `Business Intelligence` · `Data Visualization` · `Data Modeling` · `Star Schema` · `ETL` · `KPI Development` · `Time Intelligence` · `Cohort Analysis` · `Customer Analytics` · `Sales Analytics` · `Revenue Analytics` · `Logistics Analytics`

---

## 👨‍💻 Project Purpose

This project was developed as a portfolio demonstration of an **end-to-end Business Intelligence and Data Analytics workflow**, showcasing how transactional data can be transformed into an interactive executive reporting solution and translated into actionable business insights.
