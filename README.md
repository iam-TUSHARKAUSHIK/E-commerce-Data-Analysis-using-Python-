E-Commerce Sales & Profit Analysis

📌 Project Overview

This project analyzes an E-commerce dataset to gain insights into sales, profit, and customer trends using Python, pandas, and plotly. The goal is to extract valuable business insights and visualize trends effectively.

📂 Dataset

The dataset contains transactional records with the following key attributes:

Order Date – Date when the order was placed.

Sales – Revenue from the sale.

Profit – Profit earned per sale.

Category & Sub-Category – Classification of products.

Customer Segment – Type of customer (e.g., Consumer, Corporate, Home Office).

Region – Location of sales, and more.

🛠️ Installation

To run this project, install the necessary dependencies:

pip install pandas plotly jupyter notebook

📊 Problems Analyzed

This project focuses on solving the following key problems (See attached image for details):

1️⃣ Monthly Sales Analysis: Identify the months with the highest and lowest sales.

2️⃣ Category-Based Sales Analysis: Determine which product category has the highest and lowest sales.

3️⃣ Sub-Category Sales Analysis: Perform a detailed breakdown by sub-category.

4️⃣ Monthly Profit Analysis: Find the month with the highest profit.

5️⃣ Profit Analysis by Category & Sub-Category: Analyze profitability across product categories.

6️⃣ Sales & Profit by Customer Segment: Compare performance across different customer segments.

7️⃣ Sales-to-Profit Ratio Analysis: Evaluate efficiency by calculating the sales-to-profit ratio.



📊 Data Analysis & Visualizations

1️⃣ Monthly Sales Analysis

import pandas as pd
import plotly.express as px

data['Order Date'] = pd.to_datetime(data['Order Date'])
data['Month'] = data['Order Date'].dt.strftime('%Y-%m')

monthly_sales = data.groupby('Month')['Sales'].sum().reset_index()

fig = px.line(monthly_sales, x='Month', y='Sales', title='Monthly Sales Trend')
fig.show()

2️⃣ Sales & Profit by Category

category_sales = data.groupby('Category')[['Sales', 'Profit']].sum().reset_index()

fig = px.bar(category_sales, x='Category', y=['Sales', 'Profit'], barmode='group', title='Sales & Profit by Category')
fig.show()

3️⃣ Sales-to-Profit Ratio Calculation

data['Sales_to_Profit_Ratio'] = data['Profit'] / data['Sales']
ratio = data['Sales_to_Profit_Ratio'].mean()
print(f'Overall Sales-to-Profit Ratio: {ratio:.2f}')

🔥 Key Insights

The best and worst months for sales and profit.

The most profitable product categories and customer segments.

The relationship between sales and profit to optimize pricing strategies.


🏆 Acknowledgments

Dataset Source: [Sample - Superstore.csv]

Libraries Used: pandas, plotly

📌 Author: Tushar Kaushik 📅 Date: February 2025

