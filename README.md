# Customer Purchase Prediction

A beginner-friendly Machine Learning project that predicts whether a customer will make a purchase using Logistic Regression.

This project was built to practice the complete basic Machine Learning workflow, from Exploratory Data Analysis (EDA) to model evaluation and improvement.

## 📌 Project Overview

The goal of this project is to predict whether a customer will purchase a product based on features such as:

- Age
- Salary
- Time spent on the website
- Previous purchases

The target variable is:

- `0` → Not Purchased
- `1` → Purchased

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## 🔄 Machine Learning Workflow

The project follows this workflow:

1. Load the dataset from a CSV file
2. Perform Exploratory Data Analysis (EDA)
   - Univariate analysis
   - Bivariate analysis
   - Multivariate analysis
3. Check and preprocess the data
4. Separate features and target variable
5. Split the dataset into training and testing sets
6. Scale the features using `StandardScaler`
7. Train a Logistic Regression model
8. Make predictions
9. Evaluate the model
10. Improve the model using class balancing
11. Compare the original and improved models

## 📊 Exploratory Data Analysis

The EDA phase was used to understand:

- Feature distributions
- Relationships between features
- Relationships between features and purchase behavior
- Correlations between numerical variables
- Distribution of the target classes

Visualizations were created using Matplotlib and Seaborn.

## 🤖 Model

The initial model used in this project is:

**Logistic Regression**

Since the target variable represents two classes (`Purchased` and `Not Purchased`), Logistic Regression is suitable for this binary classification problem.

### Feature Scaling

The numerical features were standardized using `StandardScaler`.

The scaler was fitted only on the training data and then used to transform both the training and testing data.

## 📈 Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

The classification report was used to evaluate the model's performance on both classes.

## ⚖️ Model Improvement

The dataset contains fewer `Purchased` examples than `Not Purchased` examples.

To handle this class imbalance, a second Logistic Regression model was trained using:

`class_weight="balanced"`

### Model Comparison

| Metric | Original Model | Balanced Model |
|---|---:|---:|
| Accuracy | 80% | 75% |
| Purchased Precision | 17% | 39% |
| Purchased Recall | 3% | 69% |
| Purchased F1-Score | 5% | 50% |

### Observation

The balanced model has slightly lower overall accuracy, but it performs significantly better at identifying customers who actually purchased.

The recall for the `Purchased` class increased from **3% to 69%**, while its F1-score increased from **5% to 50%**.

This demonstrates that accuracy alone is not always enough to evaluate a classification model, especially when the target classes are imbalanced.
