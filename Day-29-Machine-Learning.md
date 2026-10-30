
# Day 29 – Random Forest Classification and Model Comparison (26/07/2026)

## 1. Goal of Today's Learning

The main goal of Day 29 was to understand and implement the Random Forest Classification algorithm using Python and Scikit-learn.

I focused on understanding how Random Forest works, how it combines multiple decision trees to make predictions, and how its performance compares with a single Decision Tree model.

I also practiced Label Encoding, feature selection, training and testing data splitting, and examining how changing the number of trees affects model accuracy.

## 2. Topics Covered

### 2.1 Introduction to Random Forest

- Understood the concept of Random Forest Classification.
- Learned that Random Forest is an ensemble learning algorithm.
- Understood that Random Forest combines multiple Decision Trees to make predictions.
- Learned that each tree contributes to the final prediction.
- Understood that classification predictions are generally determined through majority voting.
- Learned that using multiple decision trees can help improve model stability and reduce overfitting compared with an individual tree.

### 2.2 Loading and Exploring the Dataset

Loaded the Sales Dataset using Pandas.

```python
df = pd.read_excel('sales_data.xlsx')

print('Dataset shape:', df.shape)
print('Columns:', df.columns.tolist())

df.head()
```

Practiced:

- Loading an Excel dataset.
- Checking the dataset dimensions.
- Displaying column names.
- Examining the first five records.
- Understanding the available features and target variable.

### 2.3 Label Encoding

Applied Label Encoding to convert categorical columns into numerical values.

```python
le_product = LabelEncoder()
le_category = LabelEncoder()
le_day_of_week = LabelEncoder()

df['Product_Encoded'] = le_product.fit_transform(df['Product'])
df['Category_Encoded'] = le_category.fit_transform(df['Category'])
df['DayOfWeek_Encoded'] = le_day_of_week.fit_transform(df['DayOfWeek'])
```

Encoded the following categorical features:

- Product
- Category
- DayOfWeek

**Important concepts:**

- Machine learning algorithms generally require numerical input features.
- Label Encoding assigns numerical values to different categories.
- `fit_transform()` learns the category mapping and converts the categorical values into numbers.

### 2.4 Feature Selection and Target Variable

Selected seven input features for the machine learning models.

```python
feature_cols = [
    'Price',
    'Quantity',
    'Day',
    'WeekNumber',
    'Product_Encoded',
    'Category_Encoded',
    'DayOfWeek_Encoded'
]

x = df[feature_cols]
y = df['Revenue_Tier']
```

**Independent variables (Features):**

1. Price
2. Quantity
3. Day
4. WeekNumber
5. Product_Encoded
6. Category_Encoded
7. DayOfWeek_Encoded

**Dependent variable (Target):**

- Revenue_Tier

Understood that the model uses the selected features to predict the revenue category.

### 2.5 Splitting the Dataset

Used `train_test_split()` to divide the dataset into training and testing sets.

```python
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=42
)
```

Dataset division:

- Training data: 80%
- Testing data: 20%
- Random state: 42

Also checked the number of training and testing records and the unique target classes.

Learned that the model is trained using the training dataset and evaluated using the testing dataset.

### 2.6 Implementing Decision Tree Classification

Created a Decision Tree Classifier to use as a comparison model.

```python
dt = DecisionTreeClassifier(max_depth=2)

dt.fit(x_train, y_train)
```

- Created a Decision Tree model with a maximum depth of 2.
- Trained the model using the training dataset.
- Used the model as a baseline for comparison with Random Forest.

### 2.7 Implementing Random Forest Classification

Created and trained the Random Forest Classifier.

```python
rf = RandomForestClassifier(
    n_estimators=100,
    random_state=42
)

rf.fit(x_train, y_train)
```

**Important parameters:**

- `n_estimators=100`: Creates a forest containing 100 decision trees.
- `random_state=42`: Helps make the experiment reproducible.
- `fit()`: Trains the Random Forest model.

Understood that Random Forest combines predictions from multiple decision trees to produce the final classification.

### 2.8 Comparing Decision Tree and Random Forest

Compared the testing accuracy of both models.

```python
dt_acc = accuracy_score(
    y_test, dt.predict(x_test)
) * 100

rf_acc = accuracy_score(
    y_test, rf.predict(x_test)
) * 100

print(f'Decision Tree Accuracy: {dt_acc:.1f}%')
print(f'Random Forest Accuracy: {rf_acc:.1f}%')
```

Compared:

- Decision Tree accuracy.
- Random Forest accuracy.
- The effect of combining multiple decision trees.
- The difference between a single-tree model and an ensemble model.

This practical comparison helped me understand why ensemble learning is useful in machine learning.

### 2.9 Understanding the Effect of Number of Trees

Experimented with different values of `n_estimators` to understand how the number of trees affects Random Forest accuracy.

```python
tree_counts = [1, 5, 10, 25, 50, 100, 200, 300]

accuracies = []

for n in tree_counts:
    model = RandomForestClassifier(
        n_estimators=n,
        random_state=42
    )

    model.fit(x_train, y_train)

    acc = accuracy_score(
        y_test, model.predict(x_test)
    ) * 100

    accuracies.append(acc)

print(accuracies)
```

Tested the following numbers of trees:

- 1 tree
- 5 trees
- 10 trees
- 25 trees
- 50 trees
- 100 trees
- 200 trees
- 300 trees

**Important observations:**

- `n_estimators` controls the number of decision trees in the forest.
- Increasing the number of trees can improve prediction stability.
- Accuracy does not necessarily increase every time more trees are added.
- Adding more trees increases computational time.
- The best number of trees should be selected based on model performance and computational cost.

## 3. Functions Practiced

### Pandas
- `pd.read_excel()`
- `df.head()`
- `df.shape`
- `df.columns.tolist()`

### NumPy
- `numpy` library import and basic numerical data handling.

### Scikit-learn Preprocessing
- `LabelEncoder()`
- `fit_transform()`

### Scikit-learn Models
- `DecisionTreeClassifier()`
- `RandomForestClassifier()`
- `train_test_split()`

### Model Evaluation
- `accuracy_score()`

### Model Methods
- `fit()`
- `predict()`

### Python Concepts
- Lists
- For loops
- Variables
- List append operation
- Formatted print statements

## 4. Concepts I Understood Today

- Random Forest is an ensemble learning algorithm.
- It combines multiple Decision Trees to make predictions.
- Decision Tree uses a single tree, whereas Random Forest uses multiple trees.
- Majority voting is used to determine the final classification.
- Label Encoding converts categorical features into numerical values.
- Features are the input variables used by the model.
- The target variable is the output that the model needs to predict.
- Training and testing datasets are used for model development and evaluation.
- `n_estimators` controls the number of trees in Random Forest.
- Increasing the number of trees can improve stability but also increases computational requirements.
- Model accuracy is used to compare classification performance.

## 5. Key Learnings Today

- Learned the fundamentals of Random Forest Classification.
- Understood the concept of ensemble learning.
- Practiced converting categorical data into numerical form.
- Selected multiple features for model training.
- Implemented Decision Tree and Random Forest models.
- Compared the accuracy of both algorithms.
- Experimented with different numbers of decision trees.
- Understood the relationship between model complexity, prediction stability, and computational cost.
- Learned how multiple decision trees contribute to a final classification.

## 6. Challenges Faced

- Understanding how Random Forest combines multiple decision trees.
- Understanding the difference between Decision Tree and Random Forest.
- Converting categorical columns into numerical values.
- Selecting appropriate input features and the target variable.
- Understanding the purpose of the `n_estimators` parameter.
- Interpreting accuracy results for different numbers of trees.

## 7. How I Solved Them

- Studied the working principle of ensemble learning.
- Compared a single Decision Tree with a Random Forest model.
- Used Label Encoding to convert categorical columns.
- Selected seven input features and one target variable.
- Trained both models using the same training dataset.
- Tested different values of `n_estimators`.
- Compared model accuracy to understand the effect of the number of trees.

## 8. Practical Skills Gained

- Loading and exploring Excel datasets using Pandas.
- Encoding categorical features using LabelEncoder.
- Selecting multiple input features.
- Preparing training and testing datasets.
- Implementing Decision Tree Classification.
- Implementing Random Forest Classification.
- Comparing different classification algorithms.
- Experimenting with Random Forest hyperparameters.
- Evaluating classification models using accuracy.
- Understanding the practical application of ensemble learning.

## 9. Reflection

Today I learned Random Forest Classification and understood how it improves the prediction process by combining multiple decision trees.

The most important part of today's learning was comparing Decision Tree and Random Forest using the same dataset. I also experimented with different numbers of trees to understand how the `n_estimators` parameter affects model performance.

This session improved my understanding of ensemble learning and gave me practical experience in training, comparing, and evaluating classification models.

## 10. Progress

- [x] Understood the fundamentals of Random Forest.
- [x] Loaded and explored the Sales Dataset.
- [x] Applied Label Encoding.
- [x] Selected input features and target variable.
- [x] Split the dataset into training and testing sets.
- [x] Implemented Decision Tree Classification.
- [x] Implemented Random Forest Classification.
- [x] Trained both models.
- [x] Compared Decision Tree and Random Forest accuracy.
- [x] Experimented with different numbers of trees.
- [x] Understood the effect of `n_estimators`.

**Today's Learning Progress: 100% of the activities covered in the notebook.**

## 11. Next Learning Goals

- Learn the K-Nearest Neighbors (KNN) algorithm.
- Understand distance-based classification.
- Study Euclidean and Manhattan distances.
- Understand why feature scaling is important for KNN.
- Learn the Naive Bayes classification algorithm.
- Compare different supervised machine learning algorithms.
- Continue practicing model evaluation and optimization.

## 12. Resources Used

- Python
- Pandas Documentation
- NumPy Documentation
- Scikit-learn Documentation
- Jupyter Notebook
- Sales Dataset (`sales_data.xlsx`)

## 13. Daily Summary

On Day 29, I studied and implemented Random Forest Classification using Python and Scikit-learn. I learned how Random Forest combines multiple decision trees to make predictions and practiced encoding categorical features using LabelEncoder.

I implemented both Decision Tree and Random Forest models and compared their testing accuracy. I also experimented with different values of `n_estimators`, ranging from 1 to 300, to understand how the number of trees affects model performance.

This session strengthened my understanding of ensemble learning and provided practical experience in building and comparing supervised machine learning models.
