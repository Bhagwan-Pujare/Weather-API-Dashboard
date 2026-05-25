# 📊 HR Attrition Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Data Analytics](https://img.shields.io/badge/Data_Analytics-0078D4?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Data_Modeling-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

# 🌦️ Weather Analytics & Visualization Dashboard (Power BI)

An interactive, visually rich **Weather Dashboard** built using **Microsoft Power BI**. This project demonstrates end-to-end business intelligence workflows, including data extraction, data transformations via Power Query, data modeling, dynamic DAX calculations, and UI/UX design optimized for data storytelling.

---

## 📊 Project Overview

This dashboard transforms multi-city/regional weather datasets into meaningful, interactive insights. It allows users to track historical or real-time atmospheric shifts, analyze seasonal weather anomalies, and evaluate climate metrics over customizable timeframes.

* **Tools Used:** Microsoft Power BI Desktop, Power Query, DAX
* **Core File:** `Weather Dashboard.pbix`
* **Primary Metrics:** Temperature, Humidity, Precipitation/Rainfall, Wind Speed, Air Quality Index (AQI)

---

## 🛠️ Technical Implementation & Architecture

### 1. Data Cleaning & Transformation (Power Query)
* Connected to weather datasets (via API / CSV / database logs).
* Used **Power Query M Language** to normalize column schemas, adjust timezone parameters, and impute missing data points.
* Structured relational schemas by breaking data down into appropriate dimension tables (Date, City/Location) and fact tables (Weather Records).

### 2. Data Modeling & DAX Measures
* Formulated a star-schema model to keep calculations optimized and lightning-fast.
* Developed custom **DAX (Data Analysis Expressions)** to track specific metrics and dynamic behavior:
  ```dax
  // Example DAX Measure for Average Temperature
  Avg Temperature = AVERAGE('Weather Fact Table'[Temperature])
  
  // Example DAX for Dynamic Visual Color Indicators based on Humidity
  Humidity Color Indicator = 
  IF([Avg Humidity] > 70, "#FF4D4D", "#4CAF50")
