[![English](https://img.shields.io/badge/English-Click_Here-blue?style=for-the-badge)](README.md)
&nbsp;&nbsp;
[![繁體中文](https://img.shields.io/badge/繁體中文-点击查看-blue?style=for-the-badge)](README.zh-TW.md)

# 商业智慧作品集 — Ross Tang（邓仲文）

欢迎浏览我的 BI 作品集。这个 repo 记录了我从行政运营背景自学转职数据分析的完整历程，所有成果均来自实际项目、线上课程以及在现职公司的亲身应用。

---

## 关于我

我是一名**商业智慧暨运营协调员**，现居香港，自 2021 年 5 月起任职于一家小型批发贸易公司。多年来，我独立使用 Excel 建立及维护公司的仓库管理系统、进出口文件流程，以及 NAS 网络存储服务器基础架构。

**2025 年 10 月**起，我在原有运营职责之上正式兼任 BI 分析工作，将公司存放于 NAS 的销售 Excel 文件接入 Power BI，打造交互式可视化仪表板，为管理决策提供数据支撑。

我没有大学学历，从纯行政背景出发，在过去一年投入有系统的自学，完成了涵盖数据分析、BI 及商业战略的 **8 张专业证书**。以下项目是我所学的实际应用成果。

---

## 技能与工具

**编程语言与数据查询**
- SQL（MySQL、PostgreSQL、BigQuery）
- Python（pandas、openpyxl）

**BI 与可视化**
- Power BI（DAX、数据建模、交互式仪表板）

**数据工程与建模**
- dbt（data build tool）— 分层建模（staging / marts）
- 星型模式 / 雪花模式
- ETL 流程设计

**其他工具**
- Excel（数据透视表、高级公式）
- Git / GitHub
- NAS 及 UPS 系统搭建与维护

---

## 作品集项目

### 1. 销售与利润分析
**MySQL · Python · Power BI**

使用 Kaggle Superstore 销售数据集（51,000+ 条记录，2011–2014 年，涵盖 7 个全球市场），深入分析产品盈利能力与折扣策略的实际影响。

- 在 MySQL 中建立完整雪花模式数据仓库（staging → 维度表 → 事实表 → 视图）
- 执行双向数据核对，验证整条 pipeline 的数据完整性
- 交付 3 页交互式 Power BI 仪表板，涵盖执行摘要 KPI、产品表现及促销影响分析

<div align="left">
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis">
    <img src="https://img.shields.io/badge/查看项目-01_Superstore_Sales_Analysis-blue?style=for-the-badge&logo=github" alt="Superstore Sales Analysis">
  </a>
</div>

---

### 2. 电商客户旅程分析
**BigQuery · PostgreSQL · dbt · Power BI**

使用 Google BigQuery 公开数据集（GA4 Obfuscated Sample E-Commerce，2020 年 11 月，共 30 天数据），进行端对端电商客户旅程分析。

- 从 BigQuery 提取 GA4 原始事件数据并加载至 PostgreSQL
- 建立 dbt 数据转换流程（staging → marts），包含增量模型、代理键及数据质量测试
- 建模购物漏斗事实表（`fact_sessions`）及客户终身价值维度表（`dim_customers`）
- 分析各流量来源、设备及地区的转化率表现

<div align="left">
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey">
    <img src="https://img.shields.io/badge/查看项目-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="Ecommerce Customer Journey">
  </a>
</div>

---

## 专业证书（Coursera · 2025 年）

### 数据分析与商业智慧

| 证书名称 | 发证机构 | 验证链接 |
|---|---|---|
| Google Business Intelligence Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/P6RVCIH4QIRA"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| Google Data Analytics Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Data Analyst Professional Certificate | IBM | <a href="https://coursera.org/verify/professional-cert/2VW236K260MZ"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Generative AI for BI Analysts Specialization | IBM | <a href="https://coursera.org/verify/specialization/142IUDS1KXQV"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | <a href="https://coursera.org/verify/professional-cert/JZMXX254FKRO"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |

### 商业与战略

| 证书名称 | 发证机构 | 验证链接 |
|---|---|---|
| Business Analytics Specialization | Wharton School, University of Pennsylvania | <a href="https://coursera.org/verify/specialization/645M6SNKGD6Q"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |
| AI for Business Specialization | University of Pennsylvania | <a href="https://coursera.org/verify/specialization/VD2YUSGHNWFK"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |
| Business Strategy Specialization | University of Virginia | <a href="https://coursera.org/verify/specialization/K1JDTG148466"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |

---

## 联系方式

[![Notion](https://img.shields.io/badge/Notion-作品集-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-联系我-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 授权条款

本项目采用 MIT License 授权。详见 [LICENSE](./LICENSE) 文件。
