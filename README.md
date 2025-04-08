# Store-Sales-Analysis-Power-BI



## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Preparation](#data-preparation)
- [Data Modeling](#data-modeling)
- [DAX Measures](#dax-measures)
- [Visualizations](#visualizations)
- [Insights and Findings](#insights-and-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

### 📌 Project Overview

This project analyzes store-level retail sales performance using a dataset from Kaggle. The analysis explores sales trends, the effect of holidays, and the impact of external features such as temperature, fuel prices, CPI, and unemployment.

![Store Sales Dashboard](https://github.com/IanMaing1/Store-Sales-Analysis-Power-BI/blob/main/Store%20Sales%20Analysis.png?raw=true)

The dashboard was built in Power BI and aims to help stakeholders make informed business decisions.

![Retail Sales Dashboard](https://github.com/user-attachments/assets/your-dashboard-image-path.png) <!-- Replace with actual image URL -->

---

### 📦 Data Sources

Dataset: [Retail Dataset - Kaggle](https://www.kaggle.com/datasets/manjeetsingh/retaildataset)

This dataset includes three main files:
1. **Sales Data**: Weekly sales per store and department.
2. **Features Data**: External features (temperature, fuel price, CPI, unemployment, markdowns).
3. **Store Data**: Store type and size.

---

### 🛠 Tools Used

- **Excel**: For data cleaning and preprocessing.
- **Power BI**: For data modeling, DAX calculations, and dashboard creation.

---

### 🧹 Data Preparation

Key steps involved:
1. **Missing Values**: Handled missing entries, especially in markdown columns.
2. **Data Formatting**: Set correct data types for each column.
3. **Date Table**: Created a `DateTable` using DAX covering the entire dataset period.

---

### 🧩 Data Modeling

**Relationships Created**:
- `Sales` ⟷ `Store` via `Store ID`
- `Sales` ⟷ `Features` via `Store ID` and `Date`
- `Sales` ⟷ `DateTable` via `Date`

---

### 📊 DAX Measures

**Sales Measures**:
- Total Sales  
- Holiday Sales (`IsHoliday = TRUE`)  
- Non-Holiday Sales (`IsHoliday = FALSE`)  

**Feature Averages**:
- Avg Temperature (°F)  
- Avg Fuel Price  
- Avg CPI  
- Avg Unemployment  

---

### 📈 Visualizations

**Top KPIs**:
- Total Sales  
- Holiday Sales  
- Non-Holiday Sales  

**Feature Cards**:
- Avg Temperature  
- Avg Fuel Price  
- Avg CPI  
- Avg Unemployment  

**Main Charts**:
- **Sales Over Time** (Year & Quarter)  
- **Holiday vs. Non-Holiday Sales**  
- **Total Sales by Store**  
- **Sales by Store Type** (Donut Chart)

**Slicers**:
- Year  
- Month  
- Store Type  
- IsHoliday  

---

### 🔍 Insights and Findings

#### 🏖️ Holiday Sales Impact
- Certain stores experience spikes or dips during holidays, varying by region.

#### 🏬 Store Type Performance
- Store Type A consistently outperforms others in terms of total sales.

#### 🌡️ Temperature & Sales
- A possible inverse relationship: warmer months don’t always equal higher sales.

#### 📉 Macro-Economic Indicators
- Trends in CPI and unemployment appear to align with fluctuations in sales volume.

---

### 💡 Recommendations

- **Holiday Campaigns**: Optimize marketing during holidays with high sales impact.
- **Store Strategy**: Analyze successful store types to improve underperforming locations.
- **Economic Monitoring**: Track CPI and unemployment to better forecast sales and adjust pricing/promotions.

---

### ⚠️ Limitations

- **Time Range**: Data may not reflect current trends post-COVID or inflation.
- **Holiday Label**: `IsHoliday` is binary and may oversimplify complex seasonal effects.
- **Markdowns**: Sparse and incomplete markdown data was not deeply analyzed.

---

### 📚 References

- Dataset: [Kaggle - Retail Dataset](https://www.kaggle.com/datasets/manjeetsingh/retaildataset)

---

Would you like help embedding your Power BI dashboard if you’re publishing it online? Or should I help generate a `README.md` file you can upload right away?
