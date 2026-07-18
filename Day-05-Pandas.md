# Data Science Training Diary – Day 5

## Topic: Pandas Assignments – Data Exploration and Data Cleaning

### Overview

On the fifth day of my Data Science training, I completed the assignments provided by our mentor during the training session. These assignments were designed to strengthen my understanding of **data exploration, data analysis, and data cleaning using Pandas** by working with real-world datasets.

The session consisted of two practical assignments. The first assignment focused on **exploratory data analysis (EDA)** using a sales dataset, while the second assignment emphasized **data cleaning and preprocessing** using a messy Excel dataset.

---

# Assignment 1: Exploratory Data Analysis Using Pandas

The first assignment focused on understanding and exploring a dataset using various Pandas functions and analytical techniques.

## Question 1: Dataset Understanding

In this task, I explored the basic structure of the dataset and learned how to inspect the available information.

### Operations Performed

- Displayed the first few records using `head()`
- Examined the dataset structure
- Identified all column names
- Checked the data type of each column
- Understood the purpose of each column

Methods Used

```python
head()
columns
dtypes
info()
```

---

## Question 2: Dataset Analysis

In the second task, I performed several analytical operations to gain insights from the dataset.

### Operations Performed

- Calculated the total number of rows and columns
- Determined the number of unique products
- Determined the number of unique categories
- Identified the product with the highest number of transactions
- Calculated the total revenue
- Calculated the average revenue
- Displayed the top three transactions with the highest revenue

Methods Used

```python
shape
nunique()
value_counts()
sum()
mean()
sort_values()
head()
```

---

## Question 3: Exploratory Summary Report

The final task of Assignment 1 involved creating a complete exploratory summary of the dataset.

The report included:

- Dataset overview
- All column names
- Data type of each column
- Missing value count for every column
- Number of unique values in each column
- Statistical summary of numerical columns
- Top product based on transaction count
- Top category based on transaction count
- Total revenue
- Average revenue
- Maximum revenue

Methods Used

```python
info()
describe()
isnull().sum()
nunique()
value_counts()
sum()
mean()
max()
```

---

# Assignment 2: Data Cleaning Using Pandas

The second assignment focused on cleaning a messy sales dataset stored in an Excel file.

Dataset Used

```
sales_data_messy.xlsx
```

The objective was to transform the raw dataset into a clean and analysis-ready dataset.

---

## 1. Handling Missing Values

I learned how to identify and handle missing values in different ways.

### Operations Performed

- Counted missing values
- Filled missing values
- Removed missing values

Methods Used

```python
isnull().sum()
fillna()
dropna()
```

---

## 2. Removing Duplicate Records

I learned how duplicate records affect data quality and how to remove them.

### Operations Performed

- Checked duplicate rows
- Counted duplicate rows
- Removed duplicate records

Methods Used

```python
duplicated().sum()
drop_duplicates(inplace=True)
```

---

## 3. Inspecting and Fixing Data Types

I examined the data types of every column and corrected incorrect data formats.

### Operations Performed

- Checked column data types
- Converted date columns into datetime format

Methods Used

```python
dtypes
pd.to_datetime()
```

---

## 4. Cleaning Text Columns

I standardized text data by removing unnecessary spaces and formatting inconsistencies.

### Operations Performed

- Removed leading and trailing spaces
- Standardized text formatting

Methods Used

```python
.str.strip()
```

---

## 5. Verifying the Cleaned Dataset

After completing all cleaning operations, I verified that the dataset was ready for analysis.

### Validation Performed

- Checked dataset information
- Verified missing values
- Verified duplicate records

Methods Used

```python
info()
isnull().sum()
duplicated().sum()
```

---

# Practical Skills Developed

During today's assignments, I practiced:

- Exploring real-world datasets
- Understanding dataset structure
- Identifying data types
- Counting unique values
- Revenue analysis
- Product and category analysis
- Statistical data exploration
- Handling missing values
- Removing duplicate records
- Data type conversion
- Cleaning text columns
- Verifying cleaned datasets
- Applying Pandas functions to solve analytical problems

---

# Learning Outcome

By completing today's assignments, I strengthened my practical knowledge of **Exploratory Data Analysis (EDA)** and **Data Cleaning using Pandas**. I gained hands-on experience in inspecting datasets, generating summary statistics, identifying business insights, handling missing values, removing duplicate records, correcting data types, cleaning text columns, and validating cleaned datasets. These assignments improved my confidence in preparing real-world datasets for analysis and machine learning tasks.

---

# Key Pandas Methods Practiced

```python
head()
info()
describe()
columns
dtypes
shape
nunique()
unique()
value_counts()
sum()
mean()
max()
sort_values()
isnull()
fillna()
dropna()
duplicated()
drop_duplicates()
pd.to_datetime()
.str.strip()
```

---

# Progress Summary

Today's training session was entirely focused on practical assignments. By solving real-world data exploration and data cleaning problems, I reinforced the concepts learned in previous sessions and developed greater confidence in using Pandas for analyzing and preprocessing datasets. The assignments provided valuable hands-on experience that closely reflects the tasks performed by Data Analysts and Data Scientists when working with real-world business data.
