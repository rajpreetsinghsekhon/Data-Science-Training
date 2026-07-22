# Day 14 – Data Quality Assessment on the Superstore Dataset

Date:7/07/2026

---

# Goal of Today's Learning

Today's objective was to perform a **Data Quality Assessment** on the Superstore dataset. The primary focus was to inspect the dataset for common data quality issues such as missing values, duplicate records, inconsistent data, negative values, and anomalies. This assessment is an essential step before data cleaning, visualization, and machine learning because it ensures that the dataset is reliable and suitable for analysis.

---

# Topics Covered

## 1. Data Quality Assessment

- Understanding Data Quality
- Importance of Data Validation
- Identifying Data Quality Issues
- Inspecting Dataset Reliability

---

## 2. Missing Value Analysis

- Checking Missing Values
- Identifying Columns with Missing Data
- Detecting Null (`NaN`) Values
- Checking for Blank Values
- Identifying Question Marks (`?`) and Invalid Entries

---

## 3. Duplicate Record Analysis

- Identifying Duplicate Records
- Counting Duplicate Rows
- Understanding Duplicate Data
- Preparing Data for Duplicate Removal

---

## 4. Numerical Data Inspection

Analyzed important numerical columns:

- Sales
- Profit
- Quantity
- Discount

Performed:

- Mean Calculation
- Minimum Value
- Maximum Value
- Standard Statistical Summary
- Identifying Unusual Values

---

## 5. Categorical Data Inspection

Analyzed important categorical columns:

- Category
- Region
- Segment

Performed:

- Frequency Count
- Category Distribution
- Segment Distribution
- Region Distribution

---

## 6. Negative Value Detection

Inspected datasets for:

- Negative Profit
- Invalid Sales Values
- Abnormal Quantity Values
- Unexpected Discount Values

---

## 7. Date Relationship Validation

Verified relationships between:

- Order Date
- Ship Date

Checked whether:

- Ship Date occurs after Order Date
- Date values are logically consistent

---

## 8. Data Quality Report

Prepared a report including:

- Missing Values Summary
- Duplicate Records Summary
- Numerical Column Observations
- Categorical Column Observations
- Negative Value Analysis
- Date Validation Results
- Overall Data Quality Findings

---

## 9. Data Visualization

Created visualizations to understand data quality:

- Duplicate Record Distribution
- Missing Value Summary
- Category Distribution
- Region Distribution

---

# Functions Practiced

```python
isnull()
sum()

duplicated()

describe()

value_counts()

unique()

mean()

max()

min()

shape

info()

plot()

bar()

countplot()
```

---

# Concepts I Understood Today

- Data quality assessment is the first step before data preprocessing.
- Missing values can significantly affect analytical results.
- Duplicate records may produce misleading statistics.
- Statistical summaries help identify abnormal numerical values.
- Frequency analysis helps understand categorical variables.
- Date validation ensures chronological consistency within the dataset.
- Creating a data quality report provides a complete overview of dataset reliability.

---

# Key Learnings

Today I learned how to evaluate the quality of a real-world dataset before performing analysis. I inspected missing values, duplicate records, numerical statistics, categorical distributions, and date relationships. I also prepared a structured data quality report that summarized all observations. These steps are essential for identifying potential issues before data cleaning and machine learning.

---

# Challenges Faced

- Identifying all forms of missing values within the dataset.
- Interpreting statistical summaries to detect anomalies.
- Validating date relationships between Order Date and Ship Date.
- Summarizing multiple quality checks into a single report.

---

# How I Solved Them

- Used Pandas functions to inspect each column individually.
- Compared statistical summaries across numerical columns.
- Applied frequency analysis to categorical columns.
- Verified date consistency through logical comparisons.
- Documented all observations in a structured report.

---

# Practical Skills Gained

After today's learning, I can now:

- Perform a complete data quality assessment.
- Detect missing values and duplicate records.
- Analyze numerical and categorical columns.
- Identify negative or inconsistent values.
- Validate date relationships.
- Create a professional data quality report.
- Summarize dataset issues before preprocessing.

---

# Reflection

Today's session helped me understand that the success of any Data Science project depends heavily on the quality of the data. Before performing analysis or building machine learning models, it is essential to inspect the dataset thoroughly for inconsistencies and anomalies.

Working with the Superstore dataset allowed me to apply professional data quality assessment techniques used in real-world projects. Creating a structured report improved my understanding of how data analysts evaluate datasets before beginning data cleaning and feature engineering.

Overall, this session strengthened my ability to inspect datasets critically and prepared me for advanced data preprocessing tasks.

---

# Progress

- Python Fundamentals
- Advanced Python
- Python Practice
- NumPy Fundamentals
- Advanced NumPy
- NumPy Practice
- NumPy Assignment
- Pandas Basics
- Data Exploration
- Data Quality Assessment

**Overall Progress in Pandas:** **50% Completed**

---

# Next Learning Goals

- Data Cleaning
- Missing Value Treatment
- Duplicate Removal
- Outlier Detection
- Feature Engineering
- Data Visualization

---

# Resources Used

- Official Pandas Documentation
- Training Notes
- Superstore Dataset
- Practice Programs
- Self-written Exercises

---

## Daily Summary

Today I performed a comprehensive **Data Quality Assessment** on the Superstore dataset. I examined missing values, duplicate records, numerical statistics, categorical distributions, negative values, and the relationship between Order Date and Ship Date. Finally, I prepared a structured data quality report summarizing the dataset's overall condition. This practical exercise enhanced my understanding of data validation and prepared me for the next stage of data cleaning and feature engineering.
