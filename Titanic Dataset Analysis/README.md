# 🚢 Titanic Dataset Analysis

A comprehensive binary classification project predicting passenger survival on the Titanic using machine learning algorithms. This project demonstrates essential techniques in data preprocessing, exploratory data analysis, feature engineering, and model comparison.

## 📋 Project Overview

The sinking of the Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during its maiden voyage, the Titanic sank after colliding with an iceberg, resulting in the deaths of over 1,500 of the 2,224 passengers and crew aboard.

This dataset contains information about the passengers aboard the Titanic, and the goal is to **predict which passengers survived the disaster** based on available features such as:
- **Personal Information**: Age, Gender, Socioeconomic Status
- **Travel Details**: Ticket Class, Embarking Port
- **Family Information**: Number of Siblings/Spouses, Number of Parents/Children

## 🛠️ Data Preprocessing

### 1. Missing Data Handling

### 2. Feature Encoding
Categorical features converted to numerical format using Label Encoding:
- **Sex**: male → 1, female → 0
- **Embarked**: C → 0, Q → 1, S → 2

### 3. Feature Selection
Selected features for model training:
- `Pclass`, `Sex`, `Embarked`, `Age`, `SibSp`, `Parch`

## 🤖 Machine Learning Models

### Model 1: Logistic Regression
- **Type**: Linear binary classifier
- **Advantages**: Fast, interpretable, good baseline
- **Use Case**: Quick baseline performance evaluation

### Model 2: Support Vector Machine (SVM)
- **Type**: Non-linear classifier
- **Advantages**: Effective in high-dimensional spaces, robust to outliers
- **Use Case**: Capturing complex decision boundaries

## 📈 Model Evaluation

### Metrics Used
- **Accuracy**: Overall correctness of predictions
- **Classification Report**: Precision, Recall, and F1-Score for each class
- **Confusion Matrix**: True Positives, False Positives, True Negatives, False Negatives

### Performance Comparison
Both models are trained on 80% of the data and evaluated on 20% test set using stratified train-test split.


## 📝 Workflow

The analysis follows this workflow:

1. **Data Loading**: Read the CSV file into a Pandas DataFrame
2. **Exploratory Analysis**: Examine data structure and statistics
3. **Visualization**: Create visualizations to understand patterns
4. **Preprocessing**: Handle missing values and encode categorical features
5. **Model Training**: Train Logistic Regression and SVM models
6. **Evaluation**: Compare model performance using multiple metrics
7. **Results**: Display accuracy scores and classification reports

## 💡 Machine Learning Concepts Demonstrated

- ✨ Binary Classification
- ✨ Data Cleaning and Preprocessing
- ✨ Exploratory Data Analysis (EDA)
- ✨ Feature Engineering and Selection
- ✨ Train-Test Split (80-20)
- ✨ Label Encoding for Categorical Variables
- ✨ Model Comparison
- ✨ Performance Evaluation Metrics
- ✨ Classification Reports

**Last Updated**: May 2026
