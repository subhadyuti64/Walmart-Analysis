
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

### ⚙️ Model Setup
```python
from sklearn.linear_model import LinearRegression
X = data[['Fuel_Price', 'CPI', 'Temperature', 'Unemployment']]
y = data['Weekly_Sales']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
model = LinearRegression()
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
