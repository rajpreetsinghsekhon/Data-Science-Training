
# Day 27 – Linear Regression, Logistic Regression and Model Evaluation
**Date:** 24/07/2026

## 1. Goal of Today's Learning

The main goal of Day 27 was to understand and implement two important supervised machine learning algorithms: Linear Regression and Logistic Regression. I also learned how to divide a dataset into training and testing sets, train machine learning models, make predictions, and evaluate their performance using different regression and classification metrics.

## 2. Topics Covered

### 2.1 Linear Regression

- Understood the concept of Linear Regression.
- Learned how Linear Regression is used to predict continuous numerical values.
- Understood the relationship between independent variables (features) and the dependent variable (target).
- Learned the basic equation of a straight-line regression model:

  `y = mx + c`

  Where:
  - `y` = predicted output
  - `x` = input feature
  - `m` = slope
  - `c` = intercept

- Practiced plotting actual data points and the best-fit regression line.
- Used NumPy's `polyfit()` function to calculate the slope and intercept.

**Practical example:**

Used temperature and lemonade sales data to understand the relationship between temperature and the number of cups sold.

- Temperature was used as the independent variable.
- Cups sold was used as the dependent variable.
- The calculated slope was approximately 1.23.
- This indicated that for every 1°C increase in temperature, approximately 1.23 additional cups were sold according to the fitted line.

### 2.2 Linear Regression Using a Sales Dataset

Implemented Linear Regression using the `sales_data.xlsx` dataset.

- Loaded the dataset using Pandas.
- Examined the dataset containing 85 rows and 13 columns.
- Selected `Price` and `Quantity` as independent variables.
- Selected `Revenue` as the target variable.
- Divided the dataset into training and testing sets.
- Trained the Linear Regression model.
- Generated predictions using the testing data.
- Compared actual revenue with predicted revenue.

**Dataset division:**

- Total records: 85
- Training records: 68 (80%)
- Testing records: 17 (20%)

**Model coefficients:**

- Price coefficient: 2.5957
- Quantity coefficient: 508.3742
- Intercept: -1217.5530

**New prediction:**

For a product with:
- Price = 500
- Quantity = 3

The predicted revenue was approximately **1605.40**.

### 2.3 Regression Model Evaluation

Learned how to evaluate the performance of a regression model using different evaluation metrics.

**Metrics covered:**

1. **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
2. **Mean Squared Error (MSE):** Calculates the average squared difference between actual and predicted values.
3. **Root Mean Squared Error (RMSE):** Represents the square root of MSE and expresses prediction error in the target variable's units.
4. **R² Score:** Measures how much variation in the target variable is explained by the regression model.

**Results obtained from the notebook:**

| Evaluation Metric | Result |
|---|---:|
| MAE | 364.50 |
| MSE | 197831.97 |
| RMSE | 444.78 |
| R² Score | 0.8373 |

The R² score of approximately 0.8373 indicates that the model explains around 83.73% of the variation in the target variable on the test dataset.

### 2.4 Logistic Regression

- Understood the concept of Logistic Regression.
- Learned that Logistic Regression is used for classification problems.
- Understood the difference between regression and classification.
- Used `Is_High_Value` as the target variable.
- Applied Label Encoding to convert categorical target values into numerical form.
- Used `Price` and `Quantity` as input features.
- Divided the dataset into training and testing sets.
- Applied feature scaling using StandardScaler.
- Trained the Logistic Regression model.
- Generated class predictions and prediction probabilities.

**Important concepts:**

- Logistic Regression predicts the probability of a class.
- `predict()` generates the predicted class.
- `predict_proba()` provides the probability of each class.
- Label Encoding converts categorical labels into numerical values.

### 2.5 Confusion Matrix

Learned about the Confusion Matrix and how it helps evaluate classification models.

The four important terms are:

- **True Positive (TP):** Model correctly predicts the positive class.
- **True Negative (TN):** Model correctly predicts the negative class.
- **False Positive (FP):** Model incorrectly predicts the positive class.
- **False Negative (FN):** Model incorrectly predicts the negative class.

The confusion matrix obtained in the notebook was:

| | Predicted No | Predicted Yes |
|---|---:|---:|
| Actual No | 8 | 3 |
| Actual Yes | 0 | 6 |

Therefore:

- True Negative = 8
- False Positive = 3
- False Negative = 0
- True Positive = 6

### 2.6 Classification Evaluation Metrics

Practiced different metrics used to evaluate classification models.

1. **Accuracy:** Measures the proportion of total predictions that are correct.
2. **Precision:** Measures how many positive predictions are actually positive.
3. **Recall:** Measures how many actual positive cases are correctly identified.
4. **F1 Score:** Represents the harmonic mean of precision and recall.

**Results obtained from the notebook:**

| Evaluation Metric | Result |
|---|---:|
| Accuracy | 82% |
| Precision | 67% |
| Recall | 100% |
| F1 Score | 80% |

Also practiced generating a detailed classification report containing precision, recall, F1 score, and support for each class.

## 3. Functions Practiced

### NumPy
- `np.array()`
- `np.polyfit()`
- `np.sqrt()`

### Pandas
- `pd.read_excel()`
- `pd.DataFrame()`
- `df.head()`
- `df.shape`
- `df.sample()`

### Matplotlib
- `plt.scatter()`
- `plt.plot()`
- `plt.figure()`
- `plt.title()`
- `plt.xlabel()`
- `plt.ylabel()`
- `plt.legend()`
- `plt.grid()`
- `plt.show()`

### Scikit-learn
- `train_test_split()`
- `LinearRegression()`
- `LogisticRegression()`
- `LabelEncoder()`
- `StandardScaler()`
- `mean_absolute_error()`
- `mean_squared_error()`
- `r2_score()`
- `confusion_matrix()`
- `ConfusionMatrixDisplay()`
- `accuracy_score()`
- `precision_score()`
- `recall_score()`
- `f1_score()`
- `classification_report()`

### Model Methods
- `fit()`
- `predict()`
- `predict_proba()`
- `fit_transform()`
- `transform()`
- `inverse_transform()`

## 4. Concepts I Understood Today

- Linear Regression is used to predict continuous numerical values.
- Logistic Regression is used for classification problems.
- Features are the input variables used by a machine learning model.
- The target is the variable that the model needs to predict.
- Training data is used to train a model, while testing data is used to evaluate it.
- Feature scaling helps bring input features onto comparable scales.
- Regression and classification require different evaluation metrics.
- A confusion matrix helps identify correct and incorrect classification predictions.
- Precision, recall, accuracy, and F1 score measure different aspects of classification performance.

## 5. Key Learnings Today

- Learned the practical implementation of Linear Regression using NumPy and Scikit-learn.
- Understood the meaning of slope, intercept, and the best-fit line.
- Practiced predicting revenue using product price and quantity.
- Learned how to evaluate regression models using MAE, MSE, RMSE, and R².
- Implemented Logistic Regression for a binary classification problem.
- Practiced Label Encoding and StandardScaler during classification.
- Learned how to interpret a confusion matrix.
- Understood the importance of classification evaluation metrics.

## 6. Challenges Faced

- Understanding the difference between Linear Regression and Logistic Regression.
- Understanding how coefficients and intercepts affect regression predictions.
- Interpreting different regression evaluation metrics.
- Understanding the four values of a confusion matrix.
- Differentiating between precision, recall, and F1 score.

## 7. How I Solved Them

- Practiced Linear Regression using a simple temperature and lemonade sales example.
- Implemented Linear Regression on a real sales dataset.
- Compared actual revenue with predicted revenue.
- Studied the meaning of each evaluation metric.
- Used the confusion matrix to understand correct and incorrect predictions.
- Practiced classification metrics through the Logistic Regression implementation.

## 8. Practical Skills Gained

- Implementing Linear Regression using Scikit-learn.
- Visualizing a regression line using Matplotlib.
- Selecting features and target variables from a dataset.
- Splitting datasets into training and testing sets.
- Training models and generating predictions.
- Predicting new values using a trained model.
- Evaluating regression and classification models.
- Implementing Logistic Regression for binary classification.
- Interpreting confusion matrices and classification reports.

## 9. Reflection

Today I learned two important supervised machine learning algorithms: Linear Regression and Logistic Regression.

I understood how Linear Regression predicts numerical values and how Logistic Regression predicts categories. I also gained practical experience in training models, making predictions, and evaluating their performance.

The most important learning was understanding that training a machine learning model is not enough. Evaluating its predictions is equally important to determine how well the model performs on unseen data.

## 10. Progress

- [x] Understood Linear Regression.
- [x] Practiced regression line visualization.
- [x] Implemented Linear Regression using a sales dataset.
- [x] Practiced training and testing data splitting.
- [x] Generated predictions for new data.
- [x] Learned MAE, MSE, RMSE, and R².
- [x] Understood Logistic Regression.
- [x] Practiced Label Encoding and feature scaling.
- [x] Implemented Logistic Regression.
- [x] Learned the Confusion Matrix.
- [x] Practiced Accuracy, Precision, Recall, and F1 Score.
- [x] Generated a classification report.

**Today's Learning Progress: 100% of the topics covered in the notebook.**

## 11. Next Learning Goals

- Understand K-Nearest Neighbors (KNN).
- Learn the Naive Bayes classification algorithm.
- Study Decision Tree and Random Forest in more detail.
- Understand the differences between classification algorithms.
- Practice evaluating different classification models.
- Work on practical machine learning problems using different algorithms.

## 12. Resources Used

- Python
- NumPy Documentation
- Pandas Documentation
- Matplotlib Documentation
- Scikit-learn Documentation
- Jupyter Notebook
- Sales Dataset (`sales_data.xlsx`)

## 13. Daily Summary

On Day 27, I studied and implemented Linear Regression and Logistic Regression using Python and Scikit-learn. I practiced predicting revenue with Linear Regression and classifying high-value transactions with Logistic Regression.

I also learned how to evaluate regression models using MAE, MSE, RMSE, and R², and classification models using a Confusion Matrix, Accuracy, Precision, Recall, F1 Score, and Classification Report.

This practical session strengthened my understanding of supervised machine learning and provided experience in building, testing, and evaluating machine learning models.
