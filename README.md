[![繁體中文](https://img.shields.io/badge/繁體中文-點擊查看-blue?style=for-the-badge)](README.zh-TW.md)
&nbsp;&nbsp;
[![简体中文](https://img.shields.io/badge/简体中文-点击查看-blue?style=for-the-badge)](README.zh-CN.md)

# Business Intelligence Portfolio — Ross Tang

Welcome to my BI portfolio. This repository documents my self-directed transition into data analytics and business intelligence — built entirely through hands-on project work, online study, and practical application at my current employer.

---

## About Me

I am an operations professional with extensive hands-on experience in shipping coordination, import/export documentation, warehouse support, inventory tracking, and business process coordination. Since moving into a BI & Operations Coordinator role in 2025, I have been transitioning toward Business Intelligence and Operations Analyst positions.

My operational background gives me a practical edge in data work: I understand how inventory moves through a supply chain, how freight documentation maps to cost centres, and how warehouse KPIs (turnover, dead stock, reorder point) reflect real business decisions — not just numbers in a dashboard.

I build end-to-end BI portfolio projects using SQL, PostgreSQL, Power BI, dbt, and BigQuery to analyse sales performance, customer journeys, advertising ROI, and inventory operations. My goal is to bridge domain knowledge with data engineering, turning messy operational data into clear, actionable insights for business stakeholders.

---

## Skills & Tools

**Programming & Querying**
- SQL (MySQL, PostgreSQL, BigQuery)
- Python (pandas, openpyxl)

**BI & Visualization**
- Power BI (DAX, data modeling, interactive dashboards)

**Data Engineering & Modeling**
- dbt (data build tool) — staging/marts layered modeling
- Star Schema / Snowflake Schema
- ETL pipeline design

**Other Tools**
- Excel (Pivot Tables, advanced formulas)
- Git / GitHub
- NAS & UPS system setup and maintenance

---

## Portfolio Projects

### 1. Sales & Profit Analysis
**MySQL · Python · Power BI**

Analyzed the Kaggle Superstore Sales Dataset (51,000+ rows, 2011–2014, 7 global markets) to uncover product profitability and discount strategy impact.

- Built a full Snowflake schema data warehouse in MySQL (staging → dimensions → fact → views)
- Performed bidirectional reconciliation to validate data integrity across all pipeline layers
- Delivered a 3-page interactive Power BI dashboard covering executive KPIs, product performance, and promotion impact

<div align="left">
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis">
    <img src="https://img.shields.io/badge/View_Project-01_Superstore_Sales_Analysis-blue?style=for-the-badge&logo=github" alt="Superstore Sales Analysis">
  </a>
</div>

---

### 2. E-Commerce Customer Journey Analytics
**BigQuery · PostgreSQL · dbt · Power BI**

End-to-end customer journey analysis using the GA4 Obfuscated Sample E-Commerce dataset (Google BigQuery public data, Nov 2020, 30 days).

- Extracted and loaded raw GA4 event data from BigQuery into PostgreSQL
- Built a dbt transformation pipeline (staging → marts) with incremental models, surrogate keys, and data quality tests
- Modelled a funnel fact table (`fact_sessions`) and customer lifetime value dimension (`dim_customers`)
- Analysed conversion rates across traffic sources, devices, and geographies

<div align="left">
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey">
    <img src="https://img.shields.io/badge/View_Project-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="Ecommerce Customer Journey">
  </a>
</div>

---
### 3. Traffic Sources & Ad ROI Analysis
**Python · Google BigQuery · SQL · Power BI**

Analysed advertising effectiveness and return on investment (ROI) across five traffic channels — Google Ads, Facebook Ads, Email, Organic, and Direct — using simulated full-year 2024 data.

- Generated reproducible simulated data using Python (pandas, NumPy, Faker) with `seed=42`
- Executed a full ETL cleaning pipeline in BigQuery (NULL checks, deduplication, field standardisation, derived fields)
- Built a star schema data model (`campaigns` → `ad_impressions` / `sessions` / `conversions`) with 5 sets of analytical SQL Views
- Delivered a 3-page interactive Power BI dashboard covering channel performance, CTR vs CVR analysis, and campaign ROI ranking
- Key finding: Email Abandoned Cart achieves ROAS 45.12x at CPA $2.27; Google Display Remarketing is the sole negative-ROI campaign (ROAS 0.70x, -30%)

<div align="left">
  <a href="https://github.com/ross-bi/03_Traffic_Sources_Ad_ROI_Analysis">
    <img src="https://img.shields.io/badge/View_Project-03_Traffic_Sources_Ad_ROI_Analysis-blue?style=for-the-badge&logo=github" alt="Traffic Sources Ad ROI Analysis">
  </a>
</div>

---

### 4. Inventory Performance Analysis
**PostgreSQL · Power BI · Python · SQL**

Analysed full-year 2016 inventory performance of a multi-store liquor retailer using the PwC × Kaggle Inventory Analysis Case Study dataset (~12.8 million sales transactions, 80 stores).

- Built a Python bulk loader (`psycopg2` + `COPY`) to handle the 12.8M-row sales file that exceeds standard tool limits
- Executed a three-layer ELT pipeline (raw → staging → marts) with defensive casting and 7-section data quality validation
- Designed a star schema with `dim_product`, `dim_store`, `dim_vendor`, `dim_date`, `fact_sales`, and `fact_inventory_snapshot`
- Implemented static ABC Classification in PostgreSQL using window functions to avoid Power BI Import Mode computation timeouts
- Calculated 5 inventory KPIs: Inventory Turnover (4.24x), DSI (86 days), Stockout Rate (3.22%), Dead Stock % (2.56%), Reorder Point
- Delivered a 3-page interactive Power BI dashboard covering executive overview, inventory risk analysis, and replenishment prioritisation

<div align="left">
  <a href="https://github.com/ross-bi/04_Inventory_Performance_Analysis">
    <img src="https://img.shields.io/badge/View_Project-04_Inventory_Performance_Analysis-blue?style=for-the-badge&logo=github" alt="Inventory Performance Analysis">
  </a>
</div>

---

## Professional Certificates (via Coursera)

### Data Analytics & BI

| Certificate | Institution | Verification |
|---|---|---|
| Google Business Intelligence Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/P6RVCIH4QIRA"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logoColor=white"></a> |
| Google Data Analytics Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Data Analyst Professional Certificate | IBM | <a href="https://coursera.org/verify/professional-cert/2VW236K260MZ"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Generative AI for BI Analysts Specialization | IBM | <a href="https://coursera.org/verify/specialization/142IUDS1KXQV"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logoColor=white"></a> |
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | <a href="https://coursera.org/verify/professional-cert/JZMXX254FKRO"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logoColor=white"></a> |

### Business & Strategy

| Certificate | Institution | Verification |
|---|---|---|
| Business Analytics Specialization | Wharton School, University of Pennsylvania | <a href="https://coursera.org/verify/specialization/645M6SNKGD6Q"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |
| AI for Business Specialization | University of Pennsylvania | <a href="https://coursera.org/verify/specialization/VD2YUSGHNWFK"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |
| Business Strategy Specialization | University of Virginia | <a href="https://coursera.org/verify/specialization/K1JDTG148466"><img src="https://img.shields.io/badge/Verify-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |

---

## Contact

[![Notion](https://img.shields.io/badge/Notion-Portfolio-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
