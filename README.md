
---

## 🎯 Objective

1. **Analyze** Walmart’s weekly sales across multiple stores and years.  
2. **Identify** trends, patterns, and key factors that affect sales.  
3. **Predict** weekly sales using a simple regression model based on economic indicators.

---

## 📊 Dataset Overview

**File:** `Walmart_Sales.csv`  
**Rows:** 6,435  **Columns:** 8  

| Column | Description |
|:--------|:------------|
| `Store` | Store ID (1–45) |
| `Date` | Week of sales record |
| `Weekly_Sales` | Total sales revenue for that store-week |
| `Holiday_Flag` | `1` if the week includes a holiday, else `0` |
| `Temperature` | Average temperature (°F) |
| `Fuel_Price` | Average fuel price during the week |
| `CPI` | Consumer Price Index |
| `Unemployment` | Unemployment rate |

---

## 🧠 Data Cleaning & Preprocessing

✔️ No missing values found  
✔️ No duplicate rows  
✔️ Converted `Date` column to datetime format  
✔️ Extracted `Year` and `Month` for time-based analysis  
✔️ Checked for outliers in `Weekly_Sales` using IQR  

---

## 📈 Exploratory Data Analysis (EDA)

### 🧩 Key Visualizations
- 📊 Distribution of Weekly Sales  
- 📈 Sales Trends Over Time  
- 🔥 Correlation Heatmap (CPI, Unemployment, Fuel Price, Temperature)  
- 🏪 Store-wise Sales Comparison  
- 🎉 Holiday vs Non-Holiday Sales  
- 📅 Yearly and Monthly Sales Trends  

### 🧾 Observations
1. The dataset contains weekly sales data from **45 stores (2010–2012)**.  
2. No missing or duplicate records.  
3. **Store 20, 4, 14, 13, and 2** are the top-performing stores.  
4. Sales increase significantly during holidays.  
5. Sales vary seasonally, with certain months consistently outperforming others.  

---

## 🤖 Regression Model — Predicting Weekly Sales

### 🎯 Goal
To predict **`Weekly_Sales`** using macroeconomic and environmental indicators.

## 📊 Results

| **Metric** | **Value** |
|:------------|-----------:|
| **R² Score** | 0.0175 |
| **Intercept** | 1,789,909.78 |

### 🔹 Main Coefficients

| **Feature** | **Coefficient** |
|:-------------|----------------:|
| Fuel_Price | -22,242.58 |
| CPI | -1,632.23 |
| Temperature | -686.16 |
| Unemployment | -43,596.97 |

---

## 🧩 Interpretation

- **R² = 0.0175** → Model explains approximately **1.7% of the variation** in weekly sales → indicates **weak predictive power**.  
- **Negative coefficients** show slight inverse relationships — higher fuel prices or unemployment lead to lower weekly sales.  
- The model is **underfitted**, as it only uses a few macroeconomic variables and ignores store-specific or seasonal factors.


Author : Subhadyuti Rath
