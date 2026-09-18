# OIBSIP Data Analytics Internship — Level 1 Task 1

## Exploratory Data Analysis on Retail Sales Data

**Intern:** Majd Zouaoui
**Track:** Data Analytics
**Level:** Level 1
**Task:** Task 1 — Exploratory Data Analysis on Retail Sales Data
**Internship:** Oasis Infobyte (OIBSIP)
**Deadline:** October 15, 2026

---

## 📌 Project Overview

This project is part of the **OIBSIP Data Analytics Internship**, Level 1, Task 1.

The objective of this task is to perform **data cleaning and exploratory data analysis (EDA)** on a retail sales dataset in order to understand sales performance, customer characteristics, product performance, and relationships between numerical variables.

The project follows a structured workflow:

1. Inspect the raw dataset
2. Clean and prepare the data
3. Perform exploratory data analysis
4. Visualize important patterns and trends
5. Identify meaningful business insights
6. Provide actionable recommendations

---

## 📂 Dataset

The project uses an **Indian Retail Sales Dataset** obtained from Kaggle.

### Original Dataset

- **Rows:** 4,310
- **Columns:** 21

### Cleaned Dataset

After data cleaning:

- **Rows:** 4,180
- **Columns:** 21

The cleaned dataset is used for the exploratory data analysis.

### Main Data Categories

The dataset contains information related to:

- Orders
- Customers
- Order dates
- Customer demographics
- Regions and cities
- Product categories
- Products
- Quantities
- Unit prices
- Discounts
- Sales amounts
- Profit
- Shipping costs
- Customer satisfaction
- Shipping time
- Payment/status information

---

## 🗂️ Project Structure

```text
DataAnalytics-L1-EDARetailSales/
│
├── data/
│   ├── retail_sales_dataset.csv
│   └── cleaned_retail_sales_dataset.csv
├── screenshots/
├── 01_data_cleaning.ipynb
├── 02_eda.ipynb
└── README.md
```

### Files Description

#### `retail_sales_dataset.csv`

The original raw retail sales dataset obtained from Kaggle.

#### `cleaned_retail_sales_dataset.csv`

The cleaned dataset used for the EDA phase.

#### `data_cleaning.ipynb`

Contains the data inspection and cleaning process, including:

- Initial dataset inspection
- Handling empty rows
- Removing duplicate records
- Standardizing categorical values
- Converting the `order_date` column to datetime
- Handling invalid age values
- Handling missing numerical values
- Correcting invalid negative values
- Removing invalid quantity values such as zero and 999
- Checking the cleaned dataset for consistency

The cleaning process reduced the dataset from **4,310 rows to 4,180 rows**.

Missing values in `customer_satisfaction` were retained where appropriate rather than introducing potentially misleading values.

#### `eda_retail_sales.ipynb`

Contains the exploratory data analysis performed on the cleaned dataset.

---

# 📊 Exploratory Data Analysis

The EDA covers the following areas.

## 1. Descriptive Statistics

Descriptive statistics were calculated for the numerical variables using:

- Mean
- Median
- Standard deviation
- Mode

The numerical variables analyzed include:

- `age`
- `quantity`
- `unit_price`
- `discount_pct`
- `sales_amount`
- `profit`
- `shipping_cost`
- `customer_satisfaction`
- `days_to_ship`

The large difference between the mean and median of `sales_amount` indicates that sales values are not evenly distributed and that some orders have considerably higher values than typical orders.

---

## 2. Monthly Sales Trend

Monthly sales were calculated by grouping orders by month and summing `sales_amount`.

The analysis was used to identify changes in sales performance over time and periods of relatively higher or lower sales activity.

The visualization highlights noticeable variation in monthly sales rather than a constant sales level throughout the period.

---

## 3. Quarterly Sales Trend

Sales were also aggregated by quarter to provide a higher-level view of sales performance.

The quarterly analysis makes it easier to compare broader periods and identify changes in overall sales activity without the month-to-month fluctuations.

---

## 4. Customer Demographics

Customer demographics were explored using:

- Age groups
- Gender

Age groups were created to make the distribution of customers easier to interpret.

The analysis helps identify which customer segments contribute to the dataset and allows sales activity to be examined from a demographic perspective.

Gender distribution was also visualized to compare the number of customers/orders across gender categories.

---

## 5. Top 10 Products

The top 10 products were analyzed based on sales performance.

This analysis helps identify the products generating the largest contribution to sales and provides a basis for decisions related to:

- Product availability
- Inventory planning
- Product promotion
- Sales strategy

---

## 6. Revenue by Product Category

Revenue was aggregated by `product_category` to compare the performance of different product categories.

The category-level analysis provides a broader view than individual products and helps identify where revenue is concentrated across the product portfolio.

---

## 7. Correlation Analysis

A correlation matrix was created for the numerical variables and visualized using a heatmap.

The heatmap was used to examine relationships between variables such as:

- Quantity
- Unit price
- Discount
- Sales amount
- Profit
- Shipping cost
- Customer satisfaction
- Days to ship
- Age

This helps identify variables that move together and relationships that may be useful for further business analysis.

Correlation does not imply causation, so the relationships identified in the heatmap should be interpreted as statistical associations rather than direct causal effects.

---

## 8. Additional Insight

An additional visualization was created to identify a non-obvious pattern in the retail sales data beyond the main required analyses.

This additional analysis complements the main EDA by examining the dataset from another perspective and helps move the project beyond simple descriptive statistics.

---

# 💡 Key Insights

The EDA provides several useful observations:

- Sales vary considerably from month to month.
- The dataset contains substantial differences between average and typical sales values, particularly for `sales_amount`.
- Customer demographics can be used to segment the customer base by age and gender.
- Product-level analysis highlights the products that contribute most to sales.
- Category-level revenue analysis shows how sales are distributed across product categories.
- The correlation heatmap provides insight into relationships between sales, profit, quantity, pricing, discounts, shipping, and other numerical variables.
- The additional visualization provides another perspective for identifying patterns that may not be visible from the main analyses.

---

# 📌 Business Recommendations

Based on the EDA, the following actions can support retail decision-making:

### 1. Monitor sales trends over time

Track monthly and quarterly sales regularly to identify periods of high and low performance and support better sales planning.

### 2. Focus on high-performing products

Use the top-product analysis to prioritize product availability, inventory planning, and promotional activities for products that generate strong sales.

### 3. Analyze customer segments

Use age and gender segmentation to better understand customer groups and develop more targeted marketing and sales strategies.

### 4. Monitor product-category performance

Compare revenue across categories to identify areas of strong performance and categories that may require further analysis or strategic attention.

### 5. Use data relationships for further analysis

The correlation analysis can be used as a starting point for investigating relationships between sales, profit, discounts, quantity, shipping, and customer satisfaction in future analyses.

---

# 🛠️ Technologies & Tools

The project was developed using:

- **Python**
- **Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**

Python was used for data preparation, analysis, statistical calculations, and visualization.

---

# 🔄 Project Workflow

```text
Raw Dataset
     │
     ▼
Data Inspection
     │
     ▼
Data Cleaning
     │
     ▼
Cleaned Dataset
     │
     ▼
Exploratory Data Analysis
     │
     ├── Descriptive Statistics
     ├── Monthly Sales Trends
     ├── Quarterly Sales Trends
     ├── Customer Demographics
     ├── Top 10 Products
     ├── Revenue by Category
     ├── Correlation Analysis
     └── Additional Insight
     │
     ▼
Business Insights
     │
     ▼
Actionable Recommendations
```

---

# 🎯 Conclusion

This project demonstrates a complete introductory **data analytics workflow**, from raw retail data cleaning to exploratory analysis and business interpretation.

The cleaned dataset provides a consistent foundation for analysis, while the EDA reveals patterns in sales performance, customer demographics, products, categories, and numerical relationships.

The project also demonstrates how Python-based data analysis can transform a raw retail dataset into useful information that can support business decisions.

---

## 👤 Author

**Majd Zouaoui**

Data Analytics Intern — OIBSIP 2026
