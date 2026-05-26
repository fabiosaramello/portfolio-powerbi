# Marketing Campaign Analysis with Power BI 📊

## 📌 Executive Summary
This project delivers a comprehensive Business Intelligence solution to evaluate marketing campaign performance, map customer purchasing behavior, and track global revenue streams. By transforming raw, unoptimized data into an interactive 4-page Power BI report, this project empowers stakeholders to make data-driven decisions regarding marketing budget allocation and customer targeting.

## 🏢 Business Scenario & Objectives
A global enterprise needed visibility into the ROI of its recent marketing campaigns and a deeper understanding of its customer base. The core objectives of this analysis were:
1. Identify the demographic profile of the most profitable customers.
2. Understand how family structure and education impact overall spending.
3. Calculate the conversion rate of marketing campaigns and identify success patterns.
4. Track revenue trends across different international markets over time.

## ⚙️ Data Architecture & Technical Pipeline
This project encompasses the entire data analysis workflow, from extraction to data visualization:

* **ETL & Data Quality (Power Query):** Conducted rigorous data profiling and cleaning. Identified and removed critical outliers (e.g., severe data entry errors in the "Annual Salary" column) to ensure metric accuracy and preserve the integrity of visual scales.
* **Data Modeling:** Structured the relational model to allow seamless cross-filtering across geographic, demographic, and temporal dimensions.
* **DAX Expressions:** Engineered dynamic measures for precise aggregations. A core implementation was calculating total cross-category spending respecting row context using iterator functions:
  ```dax
  TotalGasto = SUMX(
      DadosMarketing, 
      DadosMarketing[Gasto com Alimentos] + DadosMarketing[Gasto com Brinquedos] + 
      DadosMarketing[Gasto com Eletronicos] + DadosMarketing[Gasto com Moveis] + 
      DadosMarketing[Gasto com Utilidades] + DadosMarketing[Gasto com Vestuario]
  )


🚀 Navigating the Dashboard
Customer View: High-level demographic KPIs.
dash1.png

Behavioral View: Deep dive into spending habits using Decomposition Trees.
dash2.png

Campaign View: Conversion rates and specific audience targeting.
dash3.png

POS View: Geographic and temporal sales distribution.
dash4.ong
