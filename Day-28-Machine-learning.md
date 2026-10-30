
# Day 28 – Decision Tree Classification and Overfitting (25/07/2026)

## 1. Goal of Today's Learning

The main goal of Day 28 was to understand and implement the Decision Tree Classification algorithm using Python and Scikit-learn. I focused on understanding how a decision tree makes decisions using conditions, how it divides data into different branches, and how to visualize its structure.

I also learned about overfitting by comparing a simple decision tree with an unrestricted decision tree and observing their training and testing accuracy.

## 2. Topics Covered

### 2.1 Introduction to Decision Tree

- Understood the concept of Decision Tree Classification.
- Learned that a Decision Tree is a supervised machine learning algorithm.
- Understood how a decision tree makes predictions using a sequence of conditions.
- Learned about the main components of a decision tree:
  - Root Node
  - Decision Nodes
  - Branches
  - Leaf Nodes
- Understood how the algorithm divides a dataset into smaller groups based on feature values.

### 2.2 Understanding Data Splitting Conditions

Practiced examining how the target variable `Is_High_Value` is distributed when the dataset is divided using different conditions.

**First condition: Price**

```python
print(df[df['Price'] > 300]['Is_High_Value'].value_counts())
print(df[df['Price'] <= 300]['Is_High_Value'].value_counts())
```

- Divided the dataset into two groups based on Price.
- Examined the distribution of `Is_High_Value` in both groups.
- Understood how a feature can help separate different classes.

**Second condition: Day**

```python
print("Left side")
print(df[df['Day'] > 15]['Is_High_Value'].value_counts())

print("Right side")
print(df[df['Day'] <= 15]['Is_High_Value'].value_counts())
```

- Divided the dataset based on the Day feature.
- Compared the target class distribution in both groups.
- Understood how decision tree conditions create branches.

### 2.3 Selecting Features and Target Variables

Selected the input features and target variable for classification.

```python
x = df[['Price', 'Quantity']]
y = df['Is_High_Value']
```

- `Price` and `Quantity` were selected as independent variables.
- `Is_High_Value` was selected as the target variable.
- Examined the first five rows of the feature dataset.
- Checked the unique target values.

### 2.4 Splitting the Dataset

Used `train_test_split()` to divide the dataset into training and testing portions.

```python
x_train, x_test, y_train, y_test = train_test_split(
    x, y, random_state=42, test_size=0.2
)
```

- Training data: 80%
- Testing data: 20%
- Random state: 42

Learned that training data is used to train the model, while testing data is used to evaluate its performance on unseen records.

### 2.5 Building a Decision Tree Classifier

Implemented a Decision Tree Classifier using Scikit-learn.

```python
tree_model = DecisionTreeClassifier(
    max_depth=2,
    random_state=42
)

tree_model.fit(x_train, y_train)
```

Important concepts:

- `DecisionTreeClassifier()` creates a classification model.
- `max_depth=2` restricts the tree to a maximum depth of two.
- `random_state=42` helps maintain reproducibility.
- `fit()` trains the model using the training dataset.

### 2.6 Making Predictions and Evaluating Accuracy

Used the trained model to predict the target values of the testing dataset.

```python
y_pred = tree_model.predict(x_test)

print(
    f"Accuracy: {accuracy_score(y_test, y_pred) * 100:.1f}%"
)
```

- Used `predict()` to generate predictions.
- Used `accuracy_score()` to compare predicted values with actual values.
- Converted accuracy into a percentage for easier interpretation.

### 2.7 Decision Tree Visualization

Visualized the trained decision tree using Matplotlib and Scikit-learn.

```python
plt.figure(figsize=(14, 7))

plot_tree(
    tree_model,
    feature_names=['Price', 'Quantity'],
    class_names=['No', 'Yes'],
    filled=True,
    rounded=True,
    fontsize=10
)

plt.tight_layout()
plt.show()
```

Learned the purpose of the visualization parameters:

- `feature_names`: Displays the names of input features.
- `class_names`: Displays the target class names.
- `filled=True`: Adds colors to the tree nodes.
- `rounded=True`: Gives the nodes rounded corners.
- `fontsize=10`: Controls the text size.

### 2.8 Understanding Overfitting in Decision Trees

Created another Decision Tree Classifier without restricting its maximum depth.

```python
overfit_tree = DecisionTreeClassifier(random_state=42)

overfit_tree.fit(x_train, y_train)
```

Calculated training and testing accuracy:

```python
train_acc = accuracy_score(
    y_train, overfit_tree.predict(x_train)
) * 100

test_acc = accuracy_score(
    y_test, overfit_tree.predict(x_test)
) * 100

print('Overfit tree')
print(f"{train_acc:.1f}%")
print(f"{test_acc:.1f}%")
```

Learned that an unrestricted decision tree can grow very deep and may memorize training examples instead of learning general patterns.

### 2.9 Comparing Simple Tree and Overfit Tree

Compared the performance of the restricted and unrestricted decision trees.

```python
train_acc = accuracy_score(
    y_train, tree_model.predict(x_train)
) * 100

test_acc = accuracy_score(
    y_test, tree_model.predict(x_test)
) * 100

print('Simple Tree')
print(f"{train_acc:.1f}%")
print(f"{test_acc:.1f}%")
```

Compared the following:

- Training accuracy of the simple tree.
- Testing accuracy of the simple tree.
- Training accuracy of the unrestricted tree.
- Testing accuracy of the unrestricted tree.

This comparison helped me understand how model complexity affects generalization.

### 2.10 Visualizing the Overfit Decision Tree

Visualized the unrestricted decision tree to examine its structure.

```python
plt.figure(figsize=(14, 7))

plot_tree(
    overfit_tree,
    feature_names=['Price', 'Quantity'],
    class_names=['No', 'Yes'],
    filled=True,
    rounded=True,
    fontsize=10
)

plt.tight_layout()
plt.show()
```

Observed how an unrestricted tree can create more branches and decision rules compared with a tree having a limited depth.

## 3. Functions Practiced

### Pandas
- `pd.read_excel()`
- `df.head()`
- `df.value_counts()`
- `df.unique()`
- Conditional filtering using `df[]`

### Matplotlib
- `plt.figure()`
- `plt.tight_layout()`
- `plt.show()`

### Scikit-learn
- `DecisionTreeClassifier()`
- `train_test_split()`
- `accuracy_score()`
- `plot_tree()`

### Model Methods
- `fit()`
- `predict()`

## 4. Concepts I Understood Today

- Decision Tree is a supervised machine learning algorithm used for classification and regression.
- A decision tree makes decisions through feature-based conditions.
- The root node represents the starting point of the tree.
- Decision nodes divide data into branches.
- Leaf nodes represent the final prediction.
- `max_depth` controls the maximum depth of a decision tree.
- Training and testing accuracy help evaluate model performance.
- Overfitting occurs when a model learns the training data too closely and performs poorly on unseen data.
- A deeper decision tree can become more complex and may overfit.
- Restricting tree depth can help control model complexity.

## 5. Key Learnings Today

- Learned the working principle of Decision Tree Classification.
- Practiced dividing data using feature-based conditions.
- Selected appropriate input features and target variables.
- Implemented a Decision Tree Classifier using Scikit-learn.
- Practiced training and testing data splitting.
- Generated predictions and calculated classification accuracy.
- Visualized decision tree structures using `plot_tree()`.
- Compared a restricted tree with an unrestricted tree.
- Understood the practical meaning of overfitting.
- Learned why model complexity should be controlled.

## 6. Challenges Faced

- Understanding how decision tree conditions divide the dataset.
- Understanding the relationship between features and target classes.
- Interpreting the decision tree visualization.
- Understanding why an unrestricted tree can become overfitted.
- Comparing training accuracy with testing accuracy.

## 7. How I Solved Them

- Examined target class distributions using conditional filtering.
- Practiced selecting `Price` and `Quantity` as input features.
- Visualized the trained decision tree to understand its branches.
- Created two models with different depth restrictions.
- Compared their training and testing accuracy.
- Studied how excessive model complexity can affect performance on unseen data.

## 8. Practical Skills Gained

- Implementing Decision Tree Classification.
- Preparing features and target variables.
- Splitting datasets into training and testing sets.
- Training classification models.
- Making predictions using trained models.
- Evaluating classification accuracy.
- Visualizing decision tree structures.
- Comparing restricted and unrestricted decision trees.
- Identifying possible overfitting through model performance comparison.

## 9. Reflection

Today I learned how the Decision Tree algorithm works and how it makes predictions using conditions based on input features.

The most important part of today's learning was understanding overfitting. By creating a simple decision tree with `max_depth=2` and comparing it with an unrestricted decision tree, I understood why controlling model complexity is important.

I also gained practical experience in visualizing decision trees and evaluating their performance using training and testing accuracy.

## 10. Progress

- [x] Understood Decision Tree Classification.
- [x] Studied feature-based splitting conditions.
- [x] Selected features and target variables.
- [x] Applied train-test splitting.
- [x] Created a Decision Tree Classifier.
- [x] Trained the classification model.
- [x] Generated predictions.
- [x] Calculated model accuracy.
- [x] Visualized the simple decision tree.
- [x] Created an unrestricted decision tree.
- [x] Compared training and testing accuracy.
- [x] Visualized the unrestricted decision tree.
- [x] Understood the concept of overfitting.

**Today's Learning Progress: 100% of the activities covered in the notebook.**

## 11. Next Learning Goals

- Understand the K-Nearest Neighbors (KNN) algorithm.
- Learn how KNN classifies data using distance measurements.
- Study the importance of feature scaling in distance-based algorithms.
- Understand the Naive Bayes classification algorithm.
- Practice comparing different classification algorithms.
- Continue learning model evaluation and overfitting prevention techniques.

## 12. Resources Used

- Python
- Pandas Documentation
- Matplotlib Documentation
- Scikit-learn Documentation
- Jupyter Notebook
- Sales Dataset

## 13. Daily Summary

On Day 28, I studied and implemented Decision Tree Classification using Python and Scikit-learn. I learned how decision trees divide data using feature-based conditions and how to train a classification model using selected features.

I also practiced visualizing decision trees, calculating accuracy, and comparing restricted and unrestricted trees. The session helped me understand overfitting and the importance of controlling model complexity to achieve better performance on unseen data.
