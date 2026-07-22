# Day 19 – Feature Engineering Project on Superstore Dataset

**Date:** 16/07/2026

---

# Goal of Today's Learning

Today's objective was to apply feature engineering techniques to the Superstore dataset by creating meaningful business features from existing data. The focus was on transforming date columns, generating new business metrics, calculating delivery time, creating profit-related features, and answering business questions using the newly engineered features. This project demonstrated how feature engineering enhances the value of raw data for analysis and machine learning.

---

# Topics Covered

## 1. Date Conversion

- Converted **Order Date** into DateTime format.
- Converted **Ship Date** into DateTime format.
- Verified both columns were successfully converted into the correct data type.

---

## 2. Order Year Feature

Created a new feature:

- **Order Year**

Extracted the year from the **Order Date** column for yearly sales and order analysis.

---

## 3. Order Month Feature

Created a new feature:

- **Order Month**

Extracted the month from the **Order Date** column to analyze monthly order trends.

---

## 4. Delivery Days Feature

Created a new feature:

- **Delivery Days**

Calculated the delivery time using:

> Delivery Days = Ship Date − Order Date

This feature helps evaluate delivery performance and shipping efficiency.

---

## 5. Profit Margin Feature

Created a new feature:

- **Profit Margin**

Calculated using:

> Profit Margin = (Profit ÷ Sales) × 100

This feature measures the profitability of each order.

---

## 6. Profit Status Feature

Created a categorical feature:

- **Profit Status**

Classification:

- **Profit** → Profit > 0
- **Loss** → Profit ≤ 0

This feature helps identify profitable and loss-making orders.

---

## 7. Business Analysis

Using the newly created features, answered the following questions:

- Which year has the highest number of orders?
- Which month has the highest number of orders?
- What is the average delivery time?
- Which orders are loss-making?
- What is the average profit margin?

---

## 8. Practical Tasks Completed

Successfully completed:

- Converted Order Date and Ship Date into DateTime format.
- Created Order Year.
- Created Order Month.
- Calculated Delivery Days.
- Calculated Profit Margin.
- Created Profit Status.
- Analyzed yearly and monthly order trends.
- Identified loss-making orders.
- Calculated average delivery time.
- Calculated average profit margin.

---

# Functions Practiced

```python
pd.to_datetime()

dt.year
dt.month

apply()

lambda

np.where()

mean()

groupby()

value_counts()

sort_values()

describe()

info()
```

---

# Concepts I Understood Today

- Feature engineering transforms existing data into meaningful business insights.
- Date columns contain valuable information that can be extracted for trend analysis.
- Delivery time is an important performance metric in logistics.
- Profit Margin provides a better understanding of business performance than profit alone.
- Creating categorical features such as Profit Status simplifies business reporting and analysis.

---

# Key Learnings

Today I learned how to engineer meaningful features from a real-world business dataset. By converting date columns, extracting year and month information, calculating delivery time, creating profit-related metrics, and categorizing orders based on profitability, I gained practical experience in preparing datasets for business intelligence and machine learning applications.

---

# Challenges Faced

- Converting date columns into the correct DateTime format.
- Calculating delivery days accurately.
- Creating the Profit Margin formula.
- Classifying orders into Profit and Loss categories.
- Verifying newly created features.

---

# How I Solved Them

- Used Pandas DateTime functions for date conversion.
- Applied arithmetic operations to calculate delivery time.
- Used formulas to calculate Profit Margin.
- Implemented conditional logic using `apply()` and `lambda` to create Profit Status.
- Verified each feature using sample records and summary statistics.

---

# Practical Skills Gained

After today's learning, I can now:

- Convert date columns into DateTime format.
- Extract year and month from date columns.
- Calculate delivery time.
- Create business-related features.
- Calculate Profit Margin.
- Classify orders as Profit or Loss.
- Analyze business performance using engineered features.
- Prepare datasets for visualization and machine learning.

---

# Reflection

Today's project demonstrated the importance of feature engineering in transforming raw business data into valuable analytical information. By creating new features such as Order Year, Order Month, Delivery Days, Profit Margin, and Profit Status, I learned how additional variables can reveal business trends and improve decision-making.

This practical project strengthened my confidence in applying feature engineering techniques to real-world datasets and prepared me for the next phase of my training—data visualization using Matplotlib and Seaborn.

---

# Progress

- Python Fundamentals
- Advanced Python
- Python Practice
- NumPy Fundamentals
- Advanced NumPy
- NumPy Practice
- NumPy Assignment
- Pandas Fundamentals
- Data Exploration
- Data Quality Assessment
- Data Cleaning
- Feature Engineering Basics
- Advanced Feature Engineering
- Feature Engineering Practice
- Feature Engineering Project

**Overall Progress in Feature Engineering:** **100% Completed**

---

# Next Learning Goals

- Introduction to Matplotlib
- Line Charts
- Bar Charts
- Scatter Plots
- Histograms
- Box Plots
- Seaborn Visualizations

---

# Resources Used

- Official Pandas Documentation
- Training Notes
- Superstore Dataset
- Practice Programs
- Self-written Exercises
- Feature Engineering Project

---

## Daily Summary

Today I completed a feature engineering project on the Superstore dataset. I converted the Order Date and Ship Date columns into DateTime format, extracted Order Year and Order Month, calculated Delivery Days, created Profit Margin and Profit Status features, and used these engineered features to answer important business questions such as identifying the year and month with the most orders, calculating the average delivery time, finding loss-making orders, and determining the average profit margin. This project enhanced my understanding of feature engineering and prepared the dataset for future visualization and machine learning tasks.
