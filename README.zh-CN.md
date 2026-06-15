[![English](https://img.shields.io/badge/English-Click_Here-blue?style=for-the-badge)](README.md)
&nbsp;&nbsp;
[![繁體中文](https://img.shields.io/badge/繁體中文-点击查看-blue?style=for-the-badge)](README.zh-TW.md)

# 商业智慧作品集 — Ross Tang

欢迎浏览我的 BI 作品集。这个 repo 记录了我从行政运营背景自学转职数据分析的完整历程，所有成果均来自实际项目、线上课程以及在现职公司的亲身应用。

---

## 关于我

我是一名营运专业人士，具备多年在船务协调、进出口文件、仓务支持、库存追踪及业务流程协调方面的实务经验。自 2025 年转任 BI & Operations Coordinator 以来，我一直逐步转向 Business Intelligence 与 Operations Analyst 相关职位。

我的运营背景让我在数据工作上具备实际优势：我了解库存如何在供应链中流动，了解货运单证如何映射到成本中心，也理解仓库 KPI（如库存周转、呆滞库存、补货点）如何反映真实的业务决策，而不只是仪表板上的数字。

我使用 SQL、PostgreSQL、Power BI、dbt 和 BigQuery 构建端到端 BI 作品集项目，分析销售表现、客户旅程、广告投资回报，以及库存运营。我的目标是结合业务领域知识与数据工程能力，将杂乱的运营数据转化为清晰、可执行的业务洞察，支持业务相关方作出更有效的决策。



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
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis/blob/master/README.zh-CN.md">
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
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey/blob/main/README.zh-CN.md">
    <img src="https://img.shields.io/badge/查看项目-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="Ecommerce Customer Journey">
  </a>
</div>

---
### 3. 流量来源与广告 ROI 分析
**Python · Google BigQuery · SQL · Power BI**

以仿真的 2024 年全年数据，分析五大流量渠道（Google Ads、Facebook Ads、Email、自然流量、直接流量）的广告效益与投资回报率（ROI）。

- 使用 Python（pandas、NumPy、Faker）以 `seed=42` 生成可重现的仿真数据
- 在 BigQuery 执行完整 ETL 清洗流程（NULL 检查、去重、字段标准化、衍生字段）
- 建立星型结构数据模型（`campaigns` → `ad_impressions` / `sessions` / `conversions`），并建立 5 组分析 SQL Views
- 交付 3 页交互式 Power BI 仪表板，涵盖渠道绩效、CTR vs CVR 分析及活动 ROI 排名
- 关键发现：Email Abandoned Cart 以每次获客成本 $2.27 达成 ROAS 45.12x；Google Display Remarketing 为唯一负 ROI 活动（ROAS 0.70x，-30%）

<div align="left">
  <a href="https://github.com/ross-bi/03_Traffic_Sources_Ad_ROI_Analysis/blob/main/README.zh-CN.md">
    <img src="https://img.shields.io/badge/查看专案-03_Traffic_Sources_Ad_ROI_Analysis-blue?style=for-the-badge&logo=github" alt="Traffic Sources Ad ROI Analysis">
  </a>
</div>

---

### 4. 库存绩效分析
**PostgreSQL · Power BI · Python · SQL**

使用 PwC × Kaggle 库存分析案例数据集（约 1,280 万笔销售交易、80 家门市），分析一家多门市酒类零售商 2016 年全年的库存绩效。

- 建立 Python 批次加载器（`psycopg2` + `COPY`），处理超出标准工具上限的 1,280 万笔销售档案
- 执行三层 ELT 流程（raw → staging → marts），包含防御性型别转换与 7 节数据质量验证
- 设计星型结构，包含 `dim_product`、`dim_store`、`dim_vendor`、`dim_date`、`fact_sales` 及 `fact_inventory_snapshot`
- 在 PostgreSQL 以窗口函数实作静态 ABC 分类，避免 Power BI Import Mode 计算逾时
- 计算 5 个库存 KPI：库存周转率（4.24x）、DSI（86 天）、缺货率（3.22%）、死库存率（2.56%）、再订购点
- 交付 3 页交互式 Power BI 仪表板，涵盖管理层总览、库存风险分析及补货优先排序

<div align="left">
  <a href="https://github.com/ross-bi/04_Inventory_Performance_Analysis/blob/master/README.zh-CN.md">
    <img src="https://img.shields.io/badge/查看专案-04_Inventory_Performance_Analysis-blue?style=for-the-badge&logo=github" alt="Inventory Performance Analysis">
  </a>
</div>

---

## 专业证书与专项课程

| 证书名称 | 发证机构 | 验证链接 |
|---|---|---|
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | <a href="https://coursera.org/verify/professional-cert/JZMXX254FKRO"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| Google Business Intelligence Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/P6RVCIH4QIRA"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Generative AI for BI Analysts Specialization | IBM | <a href="https://coursera.org/verify/specialization/142IUDS1KXQV"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| Google Data Analytics Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Data Analyst Professional Certificate | IBM | <a href="https://coursera.org/verify/professional-cert/2VW236K260MZ"><img src="https://img.shields.io/badge/验证-blue?style=for-the-badge&logoColor=white"></a> |


---

## 联系方式

[![Notion](https://img.shields.io/badge/Notion-作品集-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-联系我-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 授权条款

本项目采用 MIT License 授权。详见 [LICENSE](./LICENSE) 文件。
