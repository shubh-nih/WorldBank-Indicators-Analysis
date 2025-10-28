# 🌍 World Indicators Analysis

<img width="779" height="512" alt="image" src="https://github.com/user-attachments/assets/2de19b5e-38c0-441c-bce1-ffc30d91aa63" />


An **end to end data analysis and visualization project** leveraging the **World Bank API** to explore global trends across economy, health, environment, technology, and labor indicators.  
This project demonstrates how to extract real world data using Python, process it into a clean analytical dataset, and visualize global insights through an interactive **Power BI dashboard**.

---

## 📘 Project Overview

The **World Indicators Analysis** project focuses on analyzing major world development indicators from 2016–2024 using **data fetched directly from the World Bank API**.  
The cleaned dataset was exported and visualized in **Power BI** to uncover patterns and relationships between economic growth, internet usage, health spending, renewable energy, and more.

> **Goal:** To understand how different regions perform across multiple socio economic dimensions and visualize the evolving trends over time.

---

## 🧩 Workflow

1 **Data Extraction:**  
   Fetched country level and indicator level data using the [World Bank API](https://publicapi.dev/world-bank-api).

2 **Data Cleaning & Preparation (Python):**  
   - Removed unnecessary columns and filtered years (2016–2024)  
   - Merged multiple indicator categories into a unified dataset  
   - Added country metadata (region, income level, lending type)

3 **Dataset Export:**  
   - Final cleaned dataset saved as CSV for Power BI use

4 **Visualization (Power BI):**  
   - Built an interactive dashboard for cross regional and time series analysis  
   - Added dynamic filters and KPIs for global insights

---

## 🧠 Key Objectives

- Fetch global development data programmatically using REST API  
- Analyze indicators related to:
  - Economy & Growth  
  - Labor Market  
  - Trade & Globalization  
  - Health & Immunization  
  - Environment & Renewable Energy  
  - Technology & Internet Usage  
- Identify patterns, trends, and correlations between metrics

---

## 🧰 Tools & Technologies

| Purpose | Tools / Libraries |
|----------|------------------|
| **Data Extraction** | Python, Requests |
| **Data Cleaning & Processing** | Pandas, NumPy |
| **Visualization** | Power BI |
| **API Source** | [World Bank API](https://publicapi.dev/world-bank-api) |
| **File Format** | JSON → CSV |

--- 

##  📊 Power BI Dashboard Highlights
### 🔹 Regional KPIs
- Average GDP per Capita: $17.8K
- Average Trade Value: $964.67 B
- Average Health Spending: 6.7 % of GDP
- Average GDP Growth: 2.75 %
- % of Land Area under Forest: 31.69 %

### 🔹 Visual Insights

1. Spending on Health (% of GDP):
- North America leads with 14.1 %
- South Asia and Sub-Saharan Africa have < 6 %

2. Internet vs Immunization:
- Higher internet penetration correlates with better child immunization rates.

3. Internet vs Unemployment:
- Increased connectivity shows a decline in youth unemployment.

4. Renewable Energy Trend (2016–2022):
- Consumption peaked in 2020 at 30.35 %, slight dip afterward.

5. Multi-Indicator Time Series:
- Shows trends for GDP growth, energy use, mobile subscriptions, forest area, and unemployment.

--- 

## 🐍 Python Data Processing

The data pipeline script automates fetching multiple categories of indicators:

```python
# Example: Fetching World Bank data
base_url = "https://api.worldbank.org/countries/all/indicators/{}?format=json&per_page=1000&page={}"
indicator_groups = {
    "economic_activity_growth": ["NY.GDP.MKTP.KD.ZG", "NY.GDP.PCAP.CD"],
    "health_indicators": ["SH.XPD.CHEX.GD.ZS", "SH.IMM.IDPT", "SP.POP.65UP.TO.ZS"],
    "environmental_indicators": ["EG.FEC.RNEW.ZS", "AG.LND.FRST.ZS"]
}
```
- Loops through all indicators by category
- Collects pages of data per indicator
- Filters recent years (>2015)
- Merges indicator data with country metadata
- Exports final dataset for dashboard use

---

## 🧭 Key Indicator Categories

| **Category**     | **Example Indicators** |
|------------------|------------------------|
| **Economic**     | GDP per capita, GDP growth |
| **Labor Market** | Unemployment (total, youth) |
| **Trade**        | Imports & Exports (Goods & Services) |
| **Health**       | Life expectancy, Immunization rate, Health expenditure |
| **Environment**  | Renewable energy usage, Forest area |
| **Technology**   | Internet users, Mobile subscriptions |
