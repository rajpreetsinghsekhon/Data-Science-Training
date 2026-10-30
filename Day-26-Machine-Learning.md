
# Day 26 – Supervised Learning and Data Preprocessing

**Date:** 23/07/2026

## Goal of Today's Learning

Today's objective was to understand the fundamentals of Supervised Machine Learning and learn different data preprocessing techniques required before training machine learning models.

I explored how supervised learning works using a Decision Tree Classifier and practiced separating datasets into training and testing portions. I also learned numerical feature scaling techniques, including StandardScaler and MinMaxScaler, along with categorical encoding techniques such as Label Encoding and One-Hot Encoding.

Practical implementation was performed using Python, Pandas, NumPy, and Scikit-learn on a Sales Dataset.

## Topics Covered

### 1. Introduction to Supervised Learning

Learned the fundamentals of Supervised Machine Learning and how models learn from labelled datasets.

Covered:

- What is Supervised Learning?
- How Supervised Learning works.
- Training data and testing data.
- Features (Input Variables).
- Target (Output Variable).
- Learning patterns from labelled datasets.
- Making predictions using trained models.

Understood that supervised learning uses labelled data to train a machine learning model and predict outputs for new observations.

### 2. Practical Implementation of Decision Tree Classification

Implemented a Decision Tree Classifier using Scikit-learn.

Used the Sales Dataset to predict whether a transaction belongs to the high-value category.

Selected:

- Features: Price and Quantity.
- Target Variable: Is_High_Value.
- Algorithm: Decision Tree Classifier.

Practiced:

- Importing DecisionTreeClassifier.
- Creating a classification model.
- Training the model using `fit()`.
- Generating predictions using `predict()`.
- Predicting whether a transaction belongs to the high-value category.

**Python Implementation:**

```python
from sklearn.tree import DecisionTreeClassifier

x = df[['Price', 'Quantity']]
y = df['Is_High_Value']

model = DecisionTreeClassifier()

model.fit(x, y)

prediction = model.predict([[800, 3]])

print("Prediction:", prediction[0])
```

Observed how the trained Decision Tree model uses input features to predict a target category.

### 3. Training and Testing Data Split

Learned why datasets are divided into training and testing portions before evaluating a machine learning model.

Covered:

- Purpose of training data.
- Purpose of testing data.
- Train-test splitting.
- Test size.
- Random state.
- Understanding training and testing dataset dimensions.
- Checking target distribution in both datasets.

Practiced using:

```python
from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(
    x,
    y,
    test_size=0.2,
    random_state=4
)
```

Practical observations:

- Total records: 85
- Training records: 68
- Testing records: 17
- Training percentage: 80%
- Testing percentage: 20%

Also performed another train-test split using:

- Features: Price, Quantity, and Revenue.
- Target: Is_High_Value.
- Training percentage: 70%.
- Testing percentage: 30%.
- Random state: 10.

Learned how to examine the distribution of target classes in training and testing datasets.

### 4. Introduction to Feature Scaling

Learned why numerical features sometimes need to be scaled before applying machine learning algorithms.

Covered:

- Meaning of Feature Scaling.
- Importance of scaling numerical variables.
- Differences between Standardization and Normalization.
- Understanding different numerical ranges.
- How feature scaling transforms numerical data.

Examined the ranges of:

- Price: 150 to 1000.
- Quantity: 1 to 5.

Understood that features with different numerical ranges may affect algorithms that depend on distances or numerical magnitudes.

### 5. StandardScaler (Standardization)

Learned how StandardScaler transforms numerical features using their mean and standard deviation.

**Formula:**

Z = (X - μ) / σ

Where:

- Z = Standardized value.
- X = Original value.
- μ = Mean of the feature.
- σ = Standard deviation of the feature.

Practiced:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

x_train_scaled = scaler.fit_transform(x_train)

x_test_scaled = scaler.transform(x_test)
```

Learned:

- `fit_transform()` calculates scaling parameters from training data and transforms it.
- `transform()` applies the previously learned parameters to testing data.
- Standardized training features have approximately zero mean and unit variance.

### 6. MinMaxScaler (Normalization)

Learned how MinMaxScaler transforms numerical values into a specified range, normally between 0 and 1.

**Formula:**

X_scaled = (X - X_min) / (X_max - X_min)

Where:

- X = Original value.
- X_min = Minimum value.
- X_max = Maximum value.
- X_scaled = Transformed value.

Practiced:

```python
from sklearn.preprocessing import MinMaxScaler

minmax_scaler = MinMaxScaler()

x_train_minmax = minmax_scaler.fit_transform(x_train)

x_test_minmax = minmax_scaler.transform(x_test)
```

Learned:

- How numerical values are converted into a common range.
- How MinMaxScaler differs from StandardScaler.
- Why the scaler should be fitted using training data only.
- How to examine minimum and maximum values after scaling.

### 7. Introduction to Label Encoding

Learned how categorical data can be converted into numerical values using Label Encoding.

Covered:

- What are categorical variables?
- Why categorical values need numerical representation.
- Identifying categorical columns.
- Finding unique categorical values.
- Converting categorical labels into numerical values.

Examined categorical columns from the Sales Dataset:

- Product
- Category
- DayOfWeek
- Revenue_Tier
- Is_High_Value

Practiced identifying categorical columns using:

```python
df.select_dtypes(include='object').columns.tolist()
```

Also examined unique categorical values using:

```python
df['Product'].unique()
df['Category'].unique()
df['Revenue_Tier'].unique()
df['Is_High_Value'].unique()
```

### 8. Label Encoding Using Scikit-learn

Implemented Label Encoding using the LabelEncoder class.

Practiced encoding the Is_High_Value column:

```python
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

df['Is_High_Value_Encoded'] = le.fit_transform(
    df['Is_High_Value']
)

print(df[['Is_High_Value', 'Is_High_Value_Encoded']].head(10))
```

Observed the conversion:

- No → 0
- Yes → 1

Also performed Label Encoding on:

- Category
- Revenue_Tier
- DayOfWeek

Learned how to inspect encoded values and compare them with their original categorical labels.

### 9. Manual Label Mapping

Practiced manually assigning numerical values to ordered categorical values using the Pandas `map()` function.

Example:

```python
tier_mapping = {
    'Low': 0,
    'Medium': 1,
    'High': 2
}

df['Revenue_Tier_MapEncoded'] = df['Revenue_Tier'].map(
    tier_mapping
)
```

Compared the results of LabelEncoder with manual mapping.

Understood that manual mapping is useful when categories have a meaningful order, such as Low, Medium, and High.

Also learned that automatically assigned numerical labels do not necessarily represent the actual order or importance of categories.

### 10. Introduction to One-Hot Encoding

Learned how One-Hot Encoding converts categorical variables into multiple binary columns.

Covered:

- What is One-Hot Encoding?
- Why One-Hot Encoding is used.
- Binary representation of categories.
- Creating separate columns for categorical values.
- Understanding 0 and 1 representations.
- Difference between Label Encoding and One-Hot Encoding.

Practiced One-Hot Encoding on the Product column.

Product categories included:

- Headphones
- Laptop
- Smartphone
- Smartwatch
- Tablet

### 11. One-Hot Encoding Using Pandas

Implemented One-Hot Encoding using the `pd.get_dummies()` function.

```python
product_encoded = pd.get_dummies(
    df['Product'],
    dtype=int
)

print(product_encoded.head(10))
```

Combined the original Product column with its encoded columns using:

```python
result = pd.concat(
    [df['Product'], product_encoded],
    axis=1
)

print(result.head(10))
```

Learned how each product category receives an individual binary column.

For example, a Smartphone record receives:

- Headphones = 0
- Laptop = 0
- Smartphone = 1
- Smartwatch = 0
- Tablet = 0

### 12. One-Hot Encoding Using Scikit-learn

Also implemented One-Hot Encoding using the OneHotEncoder class.

```python
from sklearn.preprocessing import OneHotEncoder

ohe = OneHotEncoder(sparse_output=False)

product_ohe = ohe.fit_transform(df[['Product']])

product_ohe_df = pd.DataFrame(
    product_ohe,
    columns=ohe.get_feature_names_out()
)

print(product_ohe_df.head(10))
```

Learned:

- Creating an OneHotEncoder object.
- Applying `fit_transform()`.
- Converting encoded arrays into a Pandas DataFrame.
- Generating encoded feature names using `get_feature_names_out()`.

### 13. Combined Data Preprocessing Practice

Performed additional preprocessing exercises by combining multiple techniques.

Practiced:

- Selecting numerical input features.
- Separating the target variable.
- Splitting data into training and testing sets.
- Applying StandardScaler.
- Examining transformed numerical values.
- Checking mean and standard deviation.
- Encoding the DayOfWeek column.
- Creating dummy variables for Product categories.
- Comparing original categorical values with encoded values.

Also explored different ways to implement encoding using both Pandas and Scikit-learn.

## Functions Practiced

### Python Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### Supervised Learning

```python
from sklearn.tree import DecisionTreeClassifier

DecisionTreeClassifier()
model.fit()
model.predict()
```

### Train-Test Splitting

```python
from sklearn.model_selection import train_test_split

train_test_split()
```

### Feature Scaling

```python
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler

StandardScaler()
MinMaxScaler()

scaler.fit_transform()
scaler.transform()
```

### Label Encoding

```python
from sklearn.preprocessing import LabelEncoder

LabelEncoder()
le.fit_transform()
df.map()
```

### One-Hot Encoding

```python
pd.get_dummies()
pd.concat()

from sklearn.preprocessing import OneHotEncoder

OneHotEncoder()
ohe.fit_transform()
ohe.get_feature_names_out()
```

### Pandas Functions

```python
df.shape
df.head()
df.value_counts()
df.unique()
df.select_dtypes()
df.drop_duplicates()
df.sort_values()
df.min()
df.max()
df.mean()
```

## Concepts I Understood Today

- Supervised learning uses labelled datasets to train predictive models.
- Features represent input variables, while the target represents the output variable.
- Decision Tree Classifier is used for classification problems.
- Training and testing datasets serve different purposes.
- Feature scaling transforms numerical variables into comparable scales.
- StandardScaler uses the mean and standard deviation for standardization.
- MinMaxScaler normally transforms numerical values into the range of 0 to 1.
- Label Encoding converts categorical labels into numerical values.
- One-Hot Encoding creates separate binary columns for individual categories.
- Manual mapping is useful when categorical values have a meaningful order.
- Scikit-learn provides preprocessing tools for preparing datasets before machine learning.

## Key Learnings Today

Today I learned the fundamental process of preparing data for supervised machine learning.

I implemented a Decision Tree Classifier and practiced separating datasets into training and testing portions. I also explored two important feature scaling techniques: StandardScaler and MinMaxScaler.

Additionally, I learned how to handle categorical variables using Label Encoding and One-Hot Encoding through both Pandas and Scikit-learn.

These techniques are important because properly prepared data helps machine learning algorithms process input features effectively.

## Challenges Faced

- Understanding the difference between supervised learning and other machine learning approaches.
- Understanding the purpose of training and testing datasets.
- Differentiating StandardScaler from MinMaxScaler.
- Understanding the difference between Label Encoding and One-Hot Encoding.
- Selecting an appropriate encoding technique for categorical variables.
- Understanding the numerical representation of categorical values.
- Handling transformed numerical arrays and converting them back into DataFrames.

## How I Solved Them

- Practiced supervised learning using a Sales Dataset.
- Implemented a Decision Tree Classifier to understand the prediction process.
- Compared training and testing datasets by examining their dimensions and records.
- Applied both scaling techniques and examined their transformed values.
- Encoded categorical columns using LabelEncoder and OneHotEncoder.
- Compared original categorical columns with their encoded representations.
- Practiced the same preprocessing operations using Pandas and Scikit-learn.
- Examined the output of different preprocessing functions to understand their results.

## Practical Skills Gained

After today's learning, I can now:

- Understand the basic workflow of supervised machine learning.
- Identify features and target variables.
- Implement a Decision Tree Classifier.
- Train a model and generate predictions.
- Split a dataset into training and testing portions.
- Apply StandardScaler to numerical features.
- Apply MinMaxScaler to numerical features.
- Convert categorical variables using Label Encoding.
- Perform manual categorical mapping.
- Apply One-Hot Encoding using Pandas.
- Apply OneHotEncoder using Scikit-learn.
- Perform basic data preprocessing before machine learning model development.

## Reflection

Today's session introduced me to the practical foundations of supervised machine learning and data preprocessing.

Through the Sales Dataset, I understood how a machine learning model uses input features to predict an output. Implementing the Decision Tree Classifier helped me understand the basic training and prediction process.

I also explored the importance of preparing data before model development. Practicing StandardScaler and MinMaxScaler improved my understanding of numerical feature transformation, while Label Encoding and One-Hot Encoding helped me learn how categorical information can be converted into machine-readable numerical representations.

Overall, today's hands-on session strengthened my understanding of supervised learning and provided practical experience with important preprocessing techniques used in real-world machine learning.

## Progress

### Machine Learning Fundamentals

- [x] Introduction to Supervised Learning
- [x] Features and Target Variables
- [x] Decision Tree Classification
- [x] Model Training and Prediction
- [x] Training and Testing Data Split

### Data Preprocessing

- [x] Introduction to Feature Scaling
- [x] StandardScaler
- [x] MinMaxScaler
- [x] Introduction to Categorical Encoding
- [x] Label Encoding
- [x] Manual Label Mapping
- [x] One-Hot Encoding Using Pandas
- [x] OneHotEncoder Using Scikit-learn

**Overall Progress in Today's Learning: 100% Completed**

## Next Learning Goals

- Understanding other supervised learning algorithms.
- Studying Regression and Classification in greater detail.
- Learning model evaluation techniques.
- Understanding prediction accuracy and classification metrics.
- Practicing additional data preprocessing techniques.
- Applying machine learning algorithms to practical datasets.

## Resources Used

- Python Documentation
- Pandas Documentation
- Scikit-learn Documentation
- Scikit-learn Decision Tree Documentation
- Scikit-learn Preprocessing Documentation
- Sales Dataset
- Jupyter Notebook
- Self-written Python Programs
- Practical Coding Exercises

## Daily Summary

Today I studied the fundamentals of Supervised Machine Learning and practiced data preprocessing techniques using Python and Scikit-learn. I implemented a Decision Tree Classifier using a Sales Dataset, separated the data into training and testing sets, and explored numerical feature scaling using StandardScaler and MinMaxScaler.

I also learned categorical data encoding through Label Encoding, manual mapping, and One-Hot Encoding using both Pandas and Scikit-learn. These practical exercises helped me understand how raw datasets are transformed into suitable inputs for machine learning algorithms.

This session strengthened my understanding of supervised learning and data preprocessing and prepared me for learning additional machine learning algorithms and model evaluation techniques.
