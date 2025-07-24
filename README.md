# Task 1 – Walmart Sales Analysis 🛒📊

This project analyzes Walmart's sales data to uncover business insights such as sales trends, top-performing cities, and product categories.

## 🧠 Objective

Analyze sales data using Python and extract insights with visualizations.

## 📁 Files

- `sales_analysis.ipynb` – Jupyter notebook with full analysis
- `sales_analysis.py` – Python script version
- `walmart_sales.csv` – Sales dataset
- `Reports/` – Saved figures and results
- `city_sales_pie_chart.png` – Visualization of city-wise sales

---

## 🧪 Sample Code

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv('walmart_sales.csv')

# Convert Date column to datetime
df['Date'] = pd.to_datetime(df['Date'])

# Plot sales by city
city_sales = df.groupby('City')['Total'].sum()
city_sales.plot(kind='pie', autopct='%1.1f%%')
plt.title('Total Sales by City')
plt.show()
