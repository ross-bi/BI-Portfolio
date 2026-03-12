[![English](https://img.shields.io/badge/English-Click_Here-blue?style=for-the-badge)](README.md)
&nbsp;&nbsp;
[![简体中文](https://img.shields.io/badge/简体中文-点击查看-blue?style=for-the-badge)](README.zh-CN.md)

# 商業智慧作品集 — Ross Tang（鄧仲文）

歡迎瀏覽我的 BI 作品集。這個 repo 記錄了我從行政運營背景自學轉職數據分析的完整歷程，所有成果均來自實際專案、線上課程以及在現職公司的親身應用。

---

## 關於我

我是一名**商業智慧暨運營協調員**，現居香港，自 2021 年 5 月起任職於一家小型批發貿易公司。多年來，我獨立使用 Excel 建立及維護公司的倉庫管理系統、出入口文件流程，以及 NAS 網路儲存伺服器基礎架構。

**2025 年 10 月**起，我在原有運營職責之上正式兼任 BI 分析工作，將公司存放於 NAS 的銷售 Excel 文件接入 Power BI，打造互動式視覺化儀表板，為管理決策提供數據支援。

我沒有大學學歷，從純行政背景出發，在過去一年投入有系統的自學，完成了涵蓋數據分析、BI 及商業策略的 **8 張專業證書**。以下專案是我所學的實際應用成果。

---

## 技能與工具

**程式語言與資料查詢**
- SQL（MySQL、PostgreSQL、BigQuery）
- Python（pandas、openpyxl）

**BI 與視覺化**
- Power BI（DAX、資料建模、互動式儀表板）
- Tableau

**資料工程與建模**
- dbt（data build tool）— 分層建模（staging / marts）
- 星型綱要 / 雪花綱要
- ETL 流程設計

**其他工具**
- Excel（樞紐分析表、進階公式）
- Git / GitHub
- NAS 及 UPS 系統建置與維護

---

## 作品集專案

### 1. 銷售與利潤分析
**MySQL · Python · Power BI**

使用 Kaggle Superstore 銷售資料集（51,000+ 筆資料，2011–2014 年，涵蓋 7 個全球市場），深入分析產品盈利能力與折扣策略的實際影響。

- 在 MySQL 中建立完整雪花綱要資料倉儲（staging → 維度表 → 事實表 → 視圖）
- 執行雙向資料核對，驗證整條 pipeline 的資料完整性
- 交付 3 頁互動式 Power BI 儀表板，涵蓋執行摘要 KPI、產品表現及促銷影響分析

<div align="left">
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis">
    <img src="https://img.shields.io/badge/查看專案-01_Superstore_Sales_Analysis-blue?style=for-the-badge&logo=github" alt="Superstore Sales Analysis">
  </a>
</div>

---

### 2. 電商顧客旅程分析
**BigQuery · PostgreSQL · dbt · Power BI**

使用 Google BigQuery 公開資料集（GA4 Obfuscated Sample E-Commerce，2020 年 11 月，共 30 天資料），進行端對端電商顧客旅程分析。

- 從 BigQuery 提取 GA4 原始事件資料並載入 PostgreSQL
- 建立 dbt 資料轉換流程（staging → marts），包含遞增模型、代理鍵及資料品質測試
- 建模購物漏斗事實表（`fact_sessions`）及顧客終身價值維度表（`dim_customers`）
- 分析各流量來源、裝置及地區的轉換率表現

<div align="left">
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey">
    <img src="https://img.shields.io/badge/查看專案-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="Ecommerce Customer Journey">
  </a>
</div>

---

## 專業證書（Coursera · 2025 年）

### 數據分析與商業智慧

| 證書名稱 | 發證機構 | 驗證連結 |
|---|---|---|
| Google Business Intelligence Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/P6RVCIH4QIRA"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| Google Data Analytics Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Data Analyst Professional Certificate | IBM | <a href="https://coursera.org/verify/professional-cert/2VW236K260MZ"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Generative AI for BI Analysts Specialization | IBM | <a href="https://coursera.org/verify/specialization/142IUDS1KXQV"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | <a href="https://coursera.org/verify/professional-cert/JZMXX254FKRO"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |

### 商業與策略

| 證書名稱 | 發證機構 | 驗證連結 |
|---|---|---|
| Business Analytics Specialization | Wharton School, University of Pennsylvania | <a href="https://coursera.org/verify/specialization/645M6SNKGD6Q"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |
| AI for Business Specialization | University of Pennsylvania | <a href="https://coursera.org/verify/specialization/VD2YUSGHNWFK"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |
| Business Strategy Specialization | University of Virginia | <a href="https://coursera.org/verify/specialization/K1JDTG148466"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logo=ibm&logoColor=white"></a> |

---

## 聯絡方式

[![Notion](https://img.shields.io/badge/Notion-作品集-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-聯絡我-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 授權條款

本專案採用 MIT License 授權。詳見 [LICENSE](./LICENSE) 文件。
