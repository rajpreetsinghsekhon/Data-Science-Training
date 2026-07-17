# Data Science Training Diary – Day 4

## Topic: Data Cleaning and Preprocessing with Pandas

### Overview

On the fourth day of my Data Science training, I focused on **Data Cleaning and Preprocessing using Pandas**. Since real-world datasets are often incomplete and inconsistent, I learned how to identify and resolve common data quality issues before performing analysis or building machine learning models.

To practice these concepts, I worked on a **retail sales dataset** containing missing values, duplicate records, inconsistent text formatting, incorrect data types, and outliers. Throughout the session, I learned the complete workflow of cleaning a dataset from start to finish.

---

# Topics Covered

## 1. Introduction to Data Cleaning

I began by understanding:

- What is Data Cleaning?
- Why data cleaning is important in Data Science.
- Common problems found in real-world datasets.
- Difference between Data Assessment and Data Cleaning.

---

## 2. Loading and Exploring a Messy Dataset

I loaded a retail sales dataset into Pandas and explored its structure using different DataFrame methods.

I used:

- `head()`
- `tail()`
- `info()`
- `describe()`
- `shape`
- `columns`
- `dtypes`

to understand the dataset before starting the cleaning process.

---

## 3. Handling Missing Values

One of the major topics covered was handling missing values.

I learned how to:

- Detect missing values
- Count missing values
- Calculate the percentage of missing values
- Identify missing values in specific columns

Methods practiced:

```python
isnull()
isna()
sum()
dropna()
fillna()
```

I also learned different ways to remove missing values, including:

- Removing rows containing missing values.
- Removing rows based on specific columns using `subset`.
- Filling missing values instead of deleting rows.

---

## 4. Filling Missing Values

I practiced different techniques to replace missing values based on the data type.

For numerical columns, I learned to fill missing values using:

- Mean
- Median

For categorical columns, I learned to replace missing values using:

- Mode

This helped me understand when each technique should be used.

---

## 5. Missing Value Analysis

I also learned how to calculate:

- Total missing values
- Missing value percentage
- Remaining values after removing missing records

This helped evaluate the quality of the dataset before and after cleaning.

---

## 6. Detecting and Removing Duplicate Records

I learned how duplicate records affect data analysis and practiced:

- Detecting duplicate rows
- Removing duplicate rows

Methods used:

```python
duplicated()
drop_duplicates()
```

---

## 7. Fixing Data Types

Another important topic was correcting incorrect data types.

I learned how to:

- Check column data types
- Convert text into numeric values
- Convert text into datetime format

Methods practiced:

```python
dtypes
astype()
pd.to_datetime()
pd.to_numeric()
```

---

## 8. Date and Time Processing

After converting text into datetime format, I extracted useful date information, including:

- Year
- Month
- Month Name
- Day
- Day Name

This demonstrated how date features can be generated for analysis.

---

## 9. Cleaning Text Columns

I learned different string operations used for cleaning text data.

Methods practiced:

```python
.str.strip()
.str.lower()
.str.upper()
.str.title()
.str.replace()
```

These methods helped standardize textual information by removing unnecessary spaces, correcting letter casing, and replacing unwanted characters.

---

## 10. Applying Text Cleaning on the Sales Dataset

After learning the individual string methods, I applied them to the retail sales dataset to make categorical columns consistent and easier to analyze.

---

## 11. Outlier Detection

I learned how unusual values (outliers) can affect statistical analysis and machine learning models.

I practiced detecting outliers using the **Interquartile Range (IQR) Method**.

The process included:

- Calculating Q1
- Calculating Q3
- Finding IQR
- Determining lower and upper bounds
- Identifying outlier values

---

## 12. Handling Outliers

After detecting outliers, I learned different techniques to manage them.

Methods practiced:

- Capping
- Clipping

These techniques helped reduce the effect of extreme values without removing important observations from the dataset.

---

# Practical Exercises

During today's session, I solved several practical exercises on:

- Handling missing values
- Removing duplicate records
- Filling missing values using mean, median, and mode
- Converting data types
- Cleaning text columns
- Working with datetime columns
- Detecting and handling outliers
- Building a complete data cleaning workflow using Pandas

These exercises helped strengthen my understanding of real-world data preprocessing.

---

# Learning Outcome

By the end of today's training session, I developed a solid understanding of **data cleaning and preprocessing using Pandas**. I learned how to identify data quality issues, handle missing values, remove duplicate records, correct data types, clean textual data, process datetime columns, and detect and handle outliers using the IQR method. I also gained practical experience in building a complete data cleaning pipeline for a real-world retail sales dataset, which is an essential step before performing data analysis or developing machine learning models.

---

# Key Skills Acquired

- Data Cleaning Fundamentals
- Missing Value Analysis
- `dropna()` and `fillna()`
- Mean, Median, and Mode Imputation
- Duplicate Detection and Removal
- Data Type Conversion
- DateTime Processing
- Text Data Cleaning
- Outlier Detection using IQR
- Outlier Handling using Capping and Clipping
- Building a Complete Data Cleaning Pipeline using Pandas

---

# Progress Summary

Today's training session strengthened my understanding of one of the most important phases of the Data Science workflow—**Data Cleaning**. I am now more confident in preparing raw datasets for analysis and machine learning by applying industry-standard preprocessing techniques using the Pandas library.
