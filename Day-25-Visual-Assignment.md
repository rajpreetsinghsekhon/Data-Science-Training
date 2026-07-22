# Day 25 – Superstore Visualization Assignment

**Date:** 22/07/2026

---

# Goal of Today's Learning

Today's objective was to complete a comprehensive visualization assignment using the Superstore dataset. I applied the visualization techniques learned in Matplotlib and Seaborn to analyze sales, profit, discounts, regions, and categories. I also interpreted business insights from each visualization and understood how exploratory data analysis (EDA) helps prepare data before building machine learning models.

---

# Topics Covered

## 1. Monthly Sales Trend

Created a line chart to analyze monthly sales performance.

Analyzed:

- Highest Sales Month
- Lowest Sales Month
- Seasonal Sales Pattern
- Monthly Sales Trend

---

## 2. Sales by Category

Created a bar chart showing total sales by category.

Analyzed:

- Highest Sales Category
- Lowest Sales Category
- Relationship between Sales and Profit

---

## 3. Profit by Category

Created a bar chart showing total profit by category.

Compared:

- Category-wise Profit
- Category-wise Sales
- Profitability Across Categories

---

## 4. Profit by Sub-Category

Created a horizontal bar chart.

Identified:

- Highest Profit Sub-Category
- Highest Loss-Making Sub-Category
- Business Improvement Opportunities

---

## 5. Sales Distribution

Created a histogram for the Sales column.

Learned:

- Distribution of Sales
- Low-value vs High-value Orders
- Data Skewness
- Importance of Distribution Before Machine Learning

---

## 6. Profit Outlier Detection

Created a box plot for the Profit column.

Analyzed:

- Profit Outliers
- Loss Outliers
- Importance of Outliers
- Whether Outliers Should Be Removed

---

## 7. Count of Orders by Region

Created a count plot showing orders by region.

Analyzed:

- Region with Highest Orders
- Region with Lowest Orders
- Relationship Between Orders and Profit

---

## 8. Average Profit by Category

Created a Seaborn bar plot.

Compared:

- Average Profit Across Categories
- Category Performance
- Sales vs Average Profit

---

## 9. Discount vs Profit Relationship

Created a scatter plot.

Analyzed:

- Relationship Between Discount and Profit
- Impact of Discount on Business
- Importance of Discount as a Machine Learning Feature

---

## 10. Profit Distribution by Category

Created category-wise box plots.

Observed:

- Profit Variations
- Loss-making Categories
- Category-wise Outliers

---

## 11. Profit Status Count

Created a count plot.

Analyzed:

- Profit Orders
- Loss Orders
- Class Distribution
- Dataset Balance for Classification Models

---

## 12. Correlation Heatmap

Created a correlation heatmap for:

- Sales
- Quantity
- Discount
- Profit
- Delivery Days
- Profit Margin

Identified:

- Positive Correlations
- Negative Correlations
- Features Useful for Machine Learning

---

## 13. Business Insights

Generated business insights based on visualizations, including:

- Best Performing Category
- Highest Profit Category
- Loss-Making Sub-Categories
- Region with Most Orders
- Effect of Discount on Profit
- Sales and Profit Outliers
- Dataset Suitability for Prediction
- Important Features for Machine Learning

---

## 14. Final Conclusion

Summarized the complete analysis by discussing:

- Overall business performance
- Strong product categories
- Weak and loss-making areas
- Impact of discounts
- Importance of visualization before machine learning
- Features useful for predictive modeling

---

## 15. Bonus Task

Created a comparison chart showing:

- Category vs Sales
- Category vs Profit

Provided business recommendations based on the comparison.

---

# Charts Created

- Line Chart
- Bar Chart
- Horizontal Bar Chart
- Histogram
- Scatter Plot
- Box Plot
- Count Plot
- Heatmap
- Comparison Chart

---

# Libraries and Functions Practiced

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.plot()
plt.bar()
plt.barh()
plt.hist()
plt.scatter()
plt.boxplot()

sns.barplot()
sns.countplot()
sns.boxplot()
sns.scatterplot()
sns.heatmap()

plt.figure()
plt.xlabel()
plt.ylabel()
plt.title()
plt.grid()
plt.tight_layout()
plt.show()

groupby()
sum()
mean()
corr()
sort_values()
value_counts()
```

---

# Concepts I Understood Today

- Data visualization transforms raw data into meaningful business insights.
- Different chart types answer different analytical questions.
- Correlation analysis helps identify relationships between variables.
- Outlier detection is important before building machine learning models.
- Business insights derived from charts support better decision-making.
- Exploratory Data Analysis (EDA) is an essential step before predictive modeling.

---

# Key Learnings

Today I completed a full visualization assignment by creating multiple charts using Matplotlib and Seaborn. I interpreted business insights from sales, profit, discounts, and regional performance while understanding how visualization supports data exploration and prepares datasets for machine learning.

---

# Challenges Faced

- Choosing the most suitable visualization for different tasks.
- Interpreting correlations and outliers.
- Formatting charts professionally.
- Comparing insights across multiple visualizations.

---

# How I Solved Them

- Practiced different chart types using the Superstore dataset.
- Applied appropriate customization for readability.
- Compared visualizations to validate business findings.
- Reviewed each chart before drawing conclusions.

---

# Practical Skills Gained

After today's learning, I can now:

- Create professional business visualizations.
- Interpret trends and patterns from charts.
- Detect outliers and correlations.
- Compare category and regional performance.
- Generate business insights from visual data.
- Perform exploratory data analysis.
- Identify features useful for machine learning.

---

# Reflection

Today's visualization assignment allowed me to combine everything I learned in Matplotlib and Seaborn into one complete project. I analyzed sales, profit, discount, categories, regions, and customer behavior through various charts and translated these visualizations into meaningful business insights. This practical assignment strengthened my confidence in exploratory data analysis and demonstrated how visualization helps uncover patterns before building machine learning models.

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
- Feature Engineering
- Matplotlib
- Seaborn
- Visualization Assignment

**Overall Progress in Data Visualization:** **100% Completed**

---

# Next Learning Goals

- Introduction to Machine Learning
- Data Preprocessing for ML
- Train-Test Split
- Feature Scaling
- Classification Algorithms
- Regression Algorithms

---

# Resources Used

- Official Matplotlib Documentation
- Official Seaborn Documentation
- Training Notes
- Superstore Dataset
- Visualization Assignment
- Practice Programs

---

## Daily Summary

Today I completed a comprehensive visualization assignment on the Superstore dataset. I created line charts, bar charts, scatter plots, histograms, box plots, count plots, heatmaps, and comparison charts to analyze business performance from different perspectives. I interpreted trends, distributions, correlations, outliers, and category performance while generating business insights and recommendations. This assignment completed my visualization module and prepared me for the next phase of my Data Science training: Machine Learning.
