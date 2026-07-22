# Day 16 – Data Cleaning on the Superstore Dataset

Date:09/07/2026

---

# Goal of Today's Learning

Today's objective was to clean the **Superstore dataset** and prepare it for further analysis. I learned how to identify and resolve common data quality issues such as missing values, duplicate records, incorrect data types, and formatting inconsistencies. Data cleaning is a critical preprocessing step because accurate and reliable data leads to better analysis and machine learning results.

---

# Topics Covered

## 1. Missing Value Handling

- Identifying Missing Values
- Counting Missing Values in Each Column
- Checking Missing Value Percentage
- Deciding Whether to Fill or Drop Missing Values
- Removing Rows with Excessive Missing Data
- Removing Columns with Excessive Missing Data
- Understanding the Importance of Missing Value Treatment

---

## 2. Duplicate Record Removal

- Detecting Duplicate Rows
- Counting Duplicate Records
- Removing Duplicate Rows
- Verifying Duplicate Removal
- Understanding the Impact of Duplicate Data

---

## 3. Data Type Inspection

- Checking Data Types
- Identifying Incorrect Data Types
- Converting Columns to Appropriate Data Types
- Working with Date Columns
- Understanding Why Correct Data Types Are Important

---

## 4. Data Formatting

- Removing Unwanted Spaces
- Standardizing Text Values
- Renaming Columns
- Ensuring Consistent Formatting
- Correcting Data Entry Issues

---

## 5. Dataset Verification

Verified the cleaned dataset using:

- Dataset Information
- Statistical Summary
- Missing Value Check
- Duplicate Check
- Data Type Validation

---

## 6. Data Cleaning Report

Prepared a report containing:

- Missing Value Treatment
- Duplicate Removal Summary
- Data Type Conversion
- Formatting Improvements
- Final Dataset Verification

---

## 7. Practice Tasks

Completed practical tasks on the Superstore dataset:

- Checked missing values.
- Removed unnecessary missing records.
- Identified duplicate rows.
- Removed duplicate records.
- Converted incorrect data types.
- Verified the cleaned dataset.
- Generated a complete data cleaning report.

---

# Functions Practiced

```python
isnull()

sum()

dropna()

fillna()

duplicated()

drop_duplicates()

astype()

info()

describe()

dtypes

rename()

str.strip()

shape
```

---

# Concepts I Understood Today

- Data cleaning is one of the most important stages of the Data Science workflow.
- Missing values should be handled carefully to maintain data quality.
- Duplicate records can lead to inaccurate analysis and should be removed.
- Correct data types improve memory efficiency and computational accuracy.
- Consistent formatting makes datasets easier to analyze and visualize.
- A cleaned dataset produces more reliable business insights.

---

# Key Learnings

Today I learned how to clean a real-world dataset using Pandas. I practiced identifying missing values, removing duplicate records, correcting data types, and standardizing the dataset. I also verified the cleaned dataset using various Pandas functions and documented the entire cleaning process in a structured data cleaning report.

---

# Challenges Faced

- Deciding whether to remove or fill missing values.
- Identifying duplicate records accurately.
- Determining the correct data type for each column.
- Maintaining data consistency after cleaning.

---

# How I Solved Them

- Analyzed the number of missing values before selecting a treatment method.
- Used Pandas duplicate detection functions to identify repeated records.
- Compared existing data types with the expected formats.
- Verified every cleaning step using dataset inspection functions.

---

# Practical Skills Gained

After today's learning, I can now:

- Detect and handle missing values.
- Remove duplicate records efficiently.
- Convert columns into appropriate data types.
- Standardize dataset formatting.
- Validate cleaned datasets.
- Prepare professional data cleaning reports.
- Prepare datasets for analysis and visualization.

---

# Reflection

Today's session demonstrated that data cleaning is a fundamental step before any analysis or machine learning task. Working with the Superstore dataset helped me understand how poor-quality data can affect analytical results and how systematic cleaning improves dataset reliability.

By performing missing value treatment, duplicate removal, data type correction, and final verification, I gained practical experience in preparing datasets for real-world business analysis. This session increased my confidence in handling raw datasets professionally.

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
- Data Cleaning

**Overall Progress in Pandas:** **60% Completed**

---

# Next Learning Goals

- Feature Engineering
- Creating New Features
- Data Transformation
- Feature Scaling
- Data Visualization using Matplotlib
- Exploratory Data Analysis (EDA)

---

# Resources Used

- Official Pandas Documentation
- Training Notes
- Superstore Dataset
- Practice Programs
- Self-written Exercises

---

## Daily Summary

Today I cleaned the Superstore dataset by identifying and handling missing values, removing duplicate records, correcting incorrect data types, and standardizing data formatting. After completing the cleaning process, I verified the dataset using functions such as `info()`, `describe()`, `isnull().sum()`, and `duplicated().sum()`. Finally, I prepared a comprehensive data cleaning report summarizing all preprocessing steps. This session provided valuable hands-on experience in preparing real-world datasets for analysis, visualization, and machine learning.
