[![繁體中文](https://img.shields.io/badge/繁體中文-點擊查看-blue?style=for-the-badge)](README.zh-TW.md)
&nbsp;&nbsp;
[![简体中文](https://img.shields.io/badge/简体中文-点击查看-blue?style=for-the-badge)](README.zh-CN.md)

# Business Intelligence Portfolio — Ross Tang

Welcome to my BI portfolio. This repository documents my self-directed transition into data analytics and business intelligence — built entirely through hands-on project work, online study, and practical application at my current employer.

---

## About Me

I am a **Business Intelligence & Operations Coordinator** based in Hong Kong, currently working at a small wholesale trading company (since May 2021). Over the past few years I have independently built and maintained the company's warehouse management system, import/export documentation workflows, and NAS-based file infrastructure using Excel.

From **October 2025**, I formally took on a BI analyst role alongside my operations duties — connecting company sales files on our NAS to Power BI for interactive visualization and decision support.

With no formal university degree and having started from a purely administrative background, I have invested the past year in structured self-study: completing **8 professional certificates** across data analytics, BI, and business strategy. These projects represent the practical application of everything I have learned.

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

## Professional Certificates (Coursera · 2025)

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
