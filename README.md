# 🌍 Global Earthquake Risk & Seismic Analytics Dashboard

An end-to-end Interactive **Power BI Dashboard** for global seismic activity analysis, magnitude trends, depth distribution, and automated risk scoring based on USGS earthquake data.

---

## 📌 Executive Summary

This project provides a comprehensive analysis of global earthquake patterns, seismic risks, and temporal trends. Designed with dark-mode aesthetic principles and optimized UX/UI, the dashboard helps synthesize complex geographic and temporal data into actionable insights through custom metrics and interactive drill-downs.

---

## 📸 Dashboard Overview & Key Features

### 1. **Global Overview**
* **KPI Metrics:** Track Average Depth, Average Magnitude, Magnitude Standard Deviation, Max Magnitude, and Total Earthquakes.
* **Geographic Mapping:** Interactive global map showing epicenters categorized by severity (*Micro, Minor, Light, Moderate, Strong, Major*).
* **Magnitude Distribution:** Bar chart breaking down total seismic events by magnitude category.

### 2. **Temporal & Trend Analysis**
* **Daily Trends & Volatility:** Line charts showing total earthquakes by date/hour and daily percentage variance.
* **Peak Activity Heatmaps:** Day-of-week and hourly analysis to identify peak seismic occurrence windows.

### 3. **Magnitude & Depth Analysis**
* **Scatter & Depth Correlation:** Analysis of seismic depth vs. magnitude to classify *Shallow, Intermediate,* and *Deep* activity.
* **Regional Breakdown:** Detailed tabular matrix of average depth and maximum magnitude by region.
* **Custom Report Tooltips:** Hover-activated dynamic tooltips displaying detailed event logs for pinpointed data points.

### 4. **Risk Assessment & Alert Systems**
* **Custom Risk Score Index:** A composite metric incorporating Magnitude, Depth, and Impact factors:
  $$\text{RiskScore} = f(\text{Magnitude}, \text{Depth})$$
* **Gauges & Alerts:** Visual indicators and limit alarms for high-risk zones requiring urgent attention.
* **Tsunami Risk Ratio:** Percentage analysis of earthquakes linked to potential tsunami alerts.

---

## 🛠️ Data Architecture & Tech Stack

* **Business Intelligence Tool:** Microsoft Power BI Desktop
* **Data Transformation:** Power Query (GeoJSON/CSV parsing, data cleaning, and conditional column creation)
* **Data Modeling:** Star Schema design with dedicated `Calendar` and `Measure` tables.
* **DAX Formulas:** Custom measures for dynamic time intelligence, standard deviation calculations, and conditional risk alerts.

---

## 📂 Repository Structure

```text
├── Data/
│   └── earthquake_data_raw.csv        # USGS seismic dataset
├── DAX/
│   └── Measures.dax                   # Key DAX formulas used in the report
├── Report/
│   └── Analiza_Termetesh.pbix         # Power BI project file
├── Screenshots/
│   ├── Global_Overview.png
│   ├── Time_Analysis.png
│   ├── Magnitude_Depth.png
│   ├── Regional_Analysis.png
│   └── Risk_Alerts.png
└── README.md                          # Project documentation
