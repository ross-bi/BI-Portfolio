[![English](https://img.shields.io/badge/English-Click_Here-blue?style=for-the-badge)](README.md)
&nbsp;&nbsp;
[![简体中文](https://img.shields.io/badge/简体中文-点击查看-blue?style=for-the-badge)](README.zh-CN.md)

# 商業智慧作品集 — Ross Tang

這個 GitHub 整理我在 Power BI、資料分析及營運報表方面的項目。我的背景來自物流營運及中小企商務支援，現正逐步發展 Operations + BI 路線，並把 Power BI、Excel 及 SQL 應用到銷售、產品、客戶及發票分析之中。

---

## 技能與工具

**程式語言與資料查詢**
- SQL（MySQL、PostgreSQL、BigQuery）
- Python（pandas、openpyxl）

**BI 與視覺化**
- Power BI（DAX、資料建模、互動式儀表板）

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
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis/blob/master/README.zh-TW.md">
    <img src="https://img.shields.io/badge/查看專案-01_Superstore_Sales_Analysis-blue?style=for-the-badge&logo=github" alt="Superstore Sales Analysis">
  </a>
</div>

---

### 2. 電商客戶旅程分析
**BigQuery · PostgreSQL · dbt · Power BI**

使用 Google BigQuery 公開資料集（GA4 Obfuscated Sample E-Commerce，2020 年 11 月，共 30 天資料），進行端對端電商顧客旅程分析。

- 從 BigQuery 提取 GA4 原始事件資料並載入 PostgreSQL
- 建立 dbt 資料轉換流程（staging → marts），包含遞增模型、代理鍵及資料品質測試
- 建模購物漏斗事實表（`fact_sessions`）及顧客終身價值維度表（`dim_customers`）
- 分析各流量來源、裝置及地區的轉換率表現

<div align="left">
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey/blob/main/README.zh-TW.md">
    <img src="https://img.shields.io/badge/查看專案-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="Ecommerce Customer Journey">
  </a>
</div>

---
### 3. 流量來源與廣告 ROI 分析
**Python · Google BigQuery · SQL · Power BI**

以模擬的 2024 年全年資料，分析五大流量渠道（Google Ads、Facebook Ads、Email、自然流量、直接流量）的廣告效益與投資回報率（ROI）。

- 使用 Python（pandas、NumPy、Faker）以 `seed=42` 生成可重現的模擬資料
- 在 BigQuery 執行完整 ETL 清洗流程（NULL 檢查、去重、欄位標準化、衍生欄位）
- 建立星型結構資料模型（`campaigns` → `ad_impressions` / `sessions` / `conversions`），並建立 5 組分析 SQL Views
- 交付 3 頁互動式 Power BI 儀表板，涵蓋渠道績效、CTR vs CVR 分析及活動 ROI 排名
- 關鍵發現：Email Abandoned Cart 以每次獲客成本 $2.27 達成 ROAS 45.12x；Google Display Remarketing 為唯一負 ROI 活動（ROAS 0.70x，-30%）

<div align="left">
  <a href="https://github.com/ross-bi/03_Traffic_Sources_Ad_ROI_Analysis/blob/main/README.zh-TW.md">
    <img src="https://img.shields.io/badge/查看專案-03_Traffic_Sources_Ad_ROI_Analysis-blue?style=for-the-badge&logo=github" alt="Traffic Sources Ad ROI Analysis">
  </a>
</div>

---

### 4. 庫存績效分析
**PostgreSQL · Power BI · Python · SQL**

使用 PwC × Kaggle 庫存分析案例資料集（約 1,280 萬筆銷售交易、80 家門市），分析一家多門市酒類零售商 2016 年全年的庫存績效。

- 建立 Python 批次載入器（`psycopg2` + `COPY`），處理超出標準工具上限的 1,280 萬筆銷售檔案
- 執行三層 ELT 流程（raw → staging → marts），包含防禦性型別轉換與 7 節資料品質驗證
- 設計星型結構，包含 `dim_product`、`dim_store`、`dim_vendor`、`dim_date`、`fact_sales` 及 `fact_inventory_snapshot`
- 在 PostgreSQL 以視窗函數實作靜態 ABC 分類，避免 Power BI Import Mode 計算逾時
- 計算 5 個庫存 KPI：庫存週轉率（4.24x）、DSI（86 天）、缺貨率（3.22%）、死庫存率（2.56%）、再訂購點
- 交付 3 頁互動式 Power BI 儀表板，涵蓋管理層總覽、庫存風險分析及補貨優先排序

<div align="left">
  <a href="https://github.com/ross-bi/04_Inventory_Performance_Analysis/blob/master/README.zh-TW.md">
    <img src="https://img.shields.io/badge/查看專案-04_Inventory_Performance_Analysis-blue?style=for-the-badge&logo=github" alt="Inventory Performance Analysis">
  </a>
</div>

---

## 專業證書與專項課程

| 證書名稱 | 發證機構 | 驗證連結 |
|---|---|---|
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | <a href="https://coursera.org/verify/professional-cert/JZMXX254FKRO"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| Google Business Intelligence Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/P6RVCIH4QIRA"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Generative AI for BI Analysts Specialization | IBM | <a href="https://coursera.org/verify/specialization/142IUDS1KXQV"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| Google Data Analytics Professional Certificate | Google | <a href="https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |
| IBM Data Analyst Professional Certificate | IBM | <a href="https://coursera.org/verify/professional-cert/2VW236K260MZ"><img src="https://img.shields.io/badge/驗證-blue?style=for-the-badge&logoColor=white"></a> |



---

## 聯絡方式

[![Notion](https://img.shields.io/badge/Notion-作品集-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-聯絡我-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 授權條款

本專案採用 MIT License 授權。詳見 [LICENSE](./LICENSE) 文件。
