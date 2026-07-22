# Day 13 – Data Exploration on the Superstore Dataset using Pandas

Date:6/07/2026

---

# Goal of Today's Learning

Today's objective was to perform **Data Exploration (Exploratory Data Analysis - EDA)** on the Superstore dataset using Pandas. I learned how to load a dataset, inspect its structure, understand its columns and data types, identify unique values, and answer basic business questions using Pandas functions. This process helped me understand the dataset before moving on to data cleaning and visualization.

---

# Topics Covered

## 1. Loading the Dataset

- Importing the Superstore Dataset
- Reading CSV Files using Pandas
- Displaying the First Five Rows
- Displaying the Last Five Rows

---

## 2. Exploring the Dataset

- Finding Number of Rows and Columns
- Displaying Column Names
- Understanding Data Types
- Checking Dataset Information
- Viewing Statistical Summary

---

## 3. Understanding the Dataset Structure

- Shape of the Dataset
- Number of Columns
- Number of Records
- Numerical Columns
- Categorical Columns

---

## 4. Exploring Important Columns

Analyzed the following columns:

- Category
- Sub-Category
- Segment
- Region

Practiced:

- Finding Unique Values
- Counting Unique Categories
- Understanding Business Categories

---

## 5. Basic Business Analysis

Answered analytical questions such as:

- How many rows are present in the dataset?
- How many columns are present?
- How many unique categories are there?
- Which region appears most frequently?
- What is the total sales amount?
- Which category has the highest sales?
- Understanding the overall dataset structure.

---

## 6. Data Inspection Functions

Practiced the following functions:

- `head()`
- `tail()`
- `shape`
- `columns`
- `dtypes`
- `info()`
- `describe()`
- `unique()`
- `nunique()`
- `value_counts()`
- `sum()`

---

## 7. Practice Tasks

Completed practical tasks on the Superstore dataset:

- Loaded the dataset successfully.
- Displayed the first and last five records.
- Explored column names and data types.
- Generated dataset summary using `info()` and `describe()`.
- Found unique values in Category, Sub-Category, Segment, and Region.
- Calculated total sales.
- Identified the category with the highest sales.
- Answered business-related questions using Pandas functions.

---

# Functions Practiced

```python
pd.read_csv()

head()
tail()

shape
columns
dtypes

info()
describe()

unique()
nunique()
value_counts()

sum()

max()

idxmax()
```

---

# Concepts I Understood Today

- Every data analysis project begins with understanding the dataset.
- `head()` and `tail()` provide a quick overview of the data.
- `info()` displays column names, data types, and missing values.
- `describe()` provides statistical summaries for numerical columns.
- `unique()` and `value_counts()` help analyze categorical variables.
- Exploring the dataset before cleaning helps identify potential issues.

---

# Key Learnings

Today I learned how to perform the first stage of Exploratory Data Analysis (EDA). By loading the Superstore dataset and examining its structure, I understood how to identify important columns, inspect data types, generate summary statistics, and answer basic business questions. This step is essential before cleaning data, creating visualizations, or building machine learning models.

---

# Challenges Faced

- Understanding the large number of columns in the dataset.
- Interpreting the output of `info()` and `describe()`.
- Identifying which columns were categorical and numerical.
- Writing Pandas queries to answer business-related questions.

---

# How I Solved Them

- Explored each column individually.
- Practiced different Pandas inspection functions.
- Compared outputs from multiple functions.
- Solved each task step by step using the Superstore dataset.

---

# Practical Skills Gained

After today's learning, I can now:

- Load datasets using Pandas.
- Explore dataset structure efficiently.
- Understand column names and data types.
- Generate statistical summaries.
- Analyze categorical columns.
- Answer basic business questions using Pandas.
- Perform the initial stage of Exploratory Data Analysis (EDA).

---

# Reflection

Today's session introduced me to the process of understanding a real-world dataset before performing any analysis. Working with the Superstore dataset showed me that data exploration is a critical first step in every Data Science project. By examining the dataset's structure, identifying important columns, and answering business-related questions, I developed a better understanding of how analysts begin working with raw data.

This session also improved my confidence in using Pandas functions to inspect datasets and extract useful information. It provided a strong foundation for the next stages of data cleaning, feature engineering, and visualization.

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
- Data Selection & Filtering
- Data Exploration (EDA Basics)

**Overall Progress in Pandas:** **40% Completed**

---

# Next Learning Goals

- Data Cleaning
- Missing Value Handling
- Duplicate Removal
- Feature Engineering
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

Today I performed an exploratory data analysis on the Superstore dataset using Pandas. I successfully loaded the dataset, explored its structure, examined column names and data types, generated statistical summaries, identified unique values in important categorical columns, and answered several business-related questions such as total sales, the most frequent region, and the category with the highest sales. This practical exercise strengthened my understanding of dataset exploration and prepared me for the upcoming stages of data cleaning, feature engineering, and data visualization.
