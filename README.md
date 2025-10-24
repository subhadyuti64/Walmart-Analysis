📖 Overview
This project focuses on exploring Walmart’s weekly sales data to uncover trends, patterns, and relationships between key variables like temperature, CPI, unemployment, and fuel prices.
It also includes a simple Linear Regression model that predicts weekly sales based on macroeconomic indicators.
The project is ideal for beginners learning EDA (Exploratory Data Analysis), data visualization, and basic regression modeling using Python.

🎯 Objective
1.Perform data cleaning and exploratory analysis on Walmart’s weekly sales data.
2.Identify patterns, correlations, and insights affecting store sales.
3.Build a Linear Regression model to predict Weekly_Sales from economic indicators.

📊 Dataset Description
File: Walmart_Sales.csv
Rows: 6,435  Columns: 8

🧹 Data Cleaning
✔️ Checked for missing values → none found
✔️ Removed duplicates (0 duplicates)
✔️ Converted Date column to datetime format
✔️ Created new time features — Year and Month
✔️ Outlier detection on Weekly_Sales using the IQR method

📈 Exploratory Data Analysis (EDA)
The notebook performs extensive visual and statistical analysis using Matplotlib and Seaborn.

🔍 Key Visualizations
1.Distribution of Weekly Sales → Histogram & boxplot show variation and outliers.
2.Sales Over Time → Line chart of total sales per week.
3.Correlation Heatmap → Shows relationships among numerical features.
4.Store-wise Sales Comparison → Top-performing stores identified.
5.Holiday vs Non-Holiday Sales → Sales patterns around holidays.
6.Yearly & Monthly Sales Trends → Seasonal sales insights.

Insights
1.No missing or duplicate data.
2.Top-performing stores: 20, 4, 14, 13, and 2.
3.Holiday sales are significantly higher than regular weeks.
4.Sales vary seasonally, peaking in specific months and years.
5.Correlations indicate weak relationships between macroeconomic indicators and weekly sales.

🤖 Regression Model — Predicting Weekly Sales
🎯 Goal: Predict Weekly_Sales using numeric economic indicators.

🧠 Model Details
Model Type:	Linear Regression
Train/Test Split:	80% / 20%
R² Score:	0.0175
Intercept:	1,789,909.78
Coefficients:	Fuel_Price (-22,242), CPI (-1,632), Temperature (-686), Unemployment (-43,597)

📊 Interpretation
R² = 0.0175 → Only ~1.7% of variance explained.
Indicates that economic variables alone are poor predictors of weekly sales.
Suggests adding categorical and seasonal variables (e.g., Store, Holiday_Flag, Month) for improvement.
