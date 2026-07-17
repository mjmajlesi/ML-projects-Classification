# 📊 Customer Churn Prediction

A comprehensive binary classification project predicting whether a telecom customer will **churn (leave the service)** based on their account information, service subscriptions, and billing details. This project demonstrates practical applications of data preprocessing, exploratory data analysis, feature engineering, and multi-model comparison in the domain of **customer retention analytics**.

## 📋 Project Overview

Customer churn is one of the most critical challenges for subscription-based businesses, especially in the **telecommunications industry**. Acquiring a new customer is estimated to cost **5-25 times more** than retaining an existing one, making churn prediction an essential business intelligence task.

This project uses the **IBM Telco Customer Churn** dataset to build classification models that can **identify customers at risk of leaving** based on features such as:
- **Demographics**: Gender, Senior Citizen status, Partner, Dependents
- **Account Info**: Tenure, Contract type, Payment method, Monthly/Total charges
- **Services**: Phone, Internet, Online Security, Tech Support, Streaming

## 🎯 Key Features

- **Comprehensive EDA**: Distribution analysis, churn patterns by contract, payment, and services
- **Data Cleaning**: Handling missing values, type conversion for TotalCharges
- **Label Encoding**: Categorical features converted to numerical format
- **Feature Scaling**: StandardScaler normalization for optimal model performance
- **Multiple Model Comparison**: Logistic Regression, Random Forest, SVM, and Gradient Boosting
- **Visualization**: Count plots, distribution plots, heatmaps, confusion matrices, and feature importance
- **Model Evaluation**: Accuracy, classification reports, confusion matrices, and comparison charts

## 📚 Libraries Used

### Core Data Processing
- **NumPy**
- **Pandas**

### Visualization
- **Matplotlib**
- **Seaborn**

### Machine Learning & Data Processing
- **Scikit-learn**:
  - **`train_test_split`**: Splits dataset into training (80%) and testing (20%) subsets
  - **`StandardScaler`**: Normalizes numerical features to zero mean and unit variance
  - **`LabelEncoder`**: Converts categorical text features into numerical labels
  - **`LogisticRegression`**: Linear binary classifier as baseline model
  - **`RandomForestClassifier`**: Ensemble method with 100 decision trees
  - **`SVC`**: Support Vector Machine with RBF kernel for non-linear classification
  - **`GradientBoostingClassifier`**: Sequential ensemble method with boosted decision trees
  - **`accuracy_score`**: Evaluates model performance on training and test data
  - **`classification_report`**: Provides precision, recall, and F1-score for each class
  - **`confusion_matrix`**: Visualizes correct and incorrect predictions per class

## 📊 Dataset

The project uses the **`customer_churn.csv`** file located in the `data/` directory containing:

| Column | Description |
|--------|-------------|
| **customerID** | Unique customer identifier |
| **gender** | Customer gender (Male/Female) |
| **SeniorCitizen** | Whether the customer is a senior citizen (0/1) |
| **Partner** | Whether the customer has a partner (Yes/No) |
| **Dependents** | Whether the customer has dependents (Yes/No) |
| **tenure** | Number of months the customer has stayed |
| **PhoneService** | Whether the customer has phone service (Yes/No) |
| **MultipleLines** | Whether the customer has multiple lines (Yes/No/No phone service) |
| **InternetService** | Customer's internet service type (DSL/Fiber optic/No) |
| **OnlineSecurity** | Whether the customer has online security (Yes/No/No internet service) |
| **OnlineBackup** | Whether the customer has online backup (Yes/No/No internet service) |
| **DeviceProtection** | Whether the customer has device protection (Yes/No/No internet service) |
| **TechSupport** | Whether the customer has tech support (Yes/No/No internet service) |
| **StreamingTV** | Whether the customer has streaming TV (Yes/No/No internet service) |
| **StreamingMovies** | Whether the customer has streaming movies (Yes/No/No internet service) |
| **Contract** | Contract term (Month-to-month/One year/Two year) |
| **PaperlessBilling** | Whether the customer has paperless billing (Yes/No) |
| **PaymentMethod** | Payment method (Electronic check/Mailed check/Bank transfer/Credit card) |
| **MonthlyCharges** | Amount charged monthly |
| **TotalCharges** | Total amount charged |
| **Churn** | Whether the customer churned (Yes/No) — **Target Variable** |

### Dataset Statistics
- **Total Samples**: 7,043
- **Features**: 20 (after dropping customerID)
- **Target Classes**: 2 (Churn: Yes / No)
- **Class Distribution**: Imbalanced (~73% No Churn, ~27% Churn)

## 🧹 Data Preprocessing Details

### Data Cleaning
- **customerID** column dropped (not useful for prediction)
- **TotalCharges** converted from string to numeric (some entries had empty strings)
- Missing TotalCharges values filled with the **median**

### Feature Encoding
All categorical features converted to numerical format using **LabelEncoder**:
- **gender**: Female → 0, Male → 1
- **Contract**: Month-to-month → 0, One year → 1, Two year → 2
- **Churn**: No → 0, Yes → 1
- And all other categorical columns

### Feature Scaling
Numerical features normalized using **StandardScaler**:
- Transforms features to zero mean and unit variance
- Improves convergence for gradient-based algorithms (Logistic Regression, Gradient Boosting)
- Ensures equal feature contribution for distance-based algorithms (SVM)

### Train-Test Split
- **80% Training** (5,634 samples) for model learning
- **20% Testing** (1,409 samples) for unbiased evaluation
- **Random State**: 42 for reproducibility

## 🤖 Machine Learning Models

### Logistic Regression
- **Type**: Linear binary classifier
- **Advantages**: Fast, interpretable, good baseline
- **Max Iterations**: 1000 (for convergence)

### Random Forest Classifier
- **Type**: Ensemble of 100 decision trees
- **Advantages**: Handles non-linear relationships, provides feature importance
- **Estimators**: 100 trees

### Support Vector Machine (SVM)
- **Type**: Non-linear classifier with RBF kernel
- **Advantages**: Effective in high-dimensional spaces, robust to overfitting
- **Kernel**: Radial Basis Function (RBF)

### Gradient Boosting Classifier
- **Type**: Sequential ensemble of boosted decision trees
- **Advantages**: High accuracy, handles mixed feature types, reduces bias and variance
- **Estimators**: 100 boosted trees

## 📈 Model Evaluation

### Metrics Used
- **Accuracy**: Overall correctness of predictions
- **Classification Report**: Precision, Recall, and F1-Score for each class
- **Confusion Matrix**: True Positives, False Positives, True Negatives, False Negatives
- **Feature Importance**: Random Forest and Gradient Boosting-based feature analysis

### Performance Comparison
All four models are trained on 80% of the data and evaluated on the 20% test set.

## 📝 Workflow

1. **Data Loading**: Read the Telco Customer Churn CSV file into a Pandas DataFrame
2. **Data Exploration**: Examine dataset structure, statistics, and class distribution
3. **Visualization**: Create count plots, distribution plots, and category-based churn analysis
4. **Data Cleaning**: Drop unnecessary columns, handle missing values, convert data types
5. **Feature Encoding**: Convert categorical variables to numerical using LabelEncoder
6. **Correlation Analysis**: Generate heatmap to understand feature relationships
7. **Feature Scaling**: Normalize features using StandardScaler
8. **Data Splitting**: Divide data into 80% training and 20% testing sets
9. **Model Training**: Train Logistic Regression, Random Forest, SVM, and Gradient Boosting models
10. **Evaluation**: Compare model performance using accuracy, classification reports, and confusion matrices
11. **Feature Importance**: Analyze which features are most important for churn prediction
12. **Prediction**: Test models on individual customer samples

## 💡 Machine Learning Concepts Demonstrated

- ✨ Binary Classification
- ✨ Exploratory Data Analysis (EDA)
- ✨ Data Cleaning and Preprocessing
- ✨ Feature Engineering and Encoding
- ✨ Feature Scaling and Normalization
- ✨ Handling Imbalanced Datasets
- ✨ Train-Test Split (80-20)
- ✨ Model Comparison and Selection
- ✨ Confusion Matrix Analysis
- ✨ Feature Importance Analysis
- ✨ Ensemble Methods (Random Forest, Gradient Boosting)
- ✨ Support Vector Machines
- ✨ Performance Metrics and Evaluation

## 💡 Use Cases & Applications

- **Telecom Industry**: Identify at-risk subscribers before they cancel
- **SaaS Businesses**: Predict customer cancellation and trigger retention campaigns
- **Banking**: Detect customers likely to close accounts or switch providers
- **Insurance**: Forecast policy non-renewals and prioritize retention efforts
- **Subscription Services**: Optimize marketing spend on high-risk customer segments

## 🚀 Future Enhancements
- **SMOTE Oversampling**: Address class imbalance for improved minority class prediction
- **XGBoost / LightGBM**: Advanced gradient boosting frameworks for better performance
- **Hyperparameter Tuning**: Grid search and cross-validation for optimal model parameters
- **Deep Learning**: Neural network approach for capturing complex feature interactions

<br />

**Type**: Binary Classification <br />
**Algorithms**: Logistic Regression, Random Forest, SVM, Gradient Boosting <br />
**Feature Scaling**: StandardScaler <br />
**Last Updated**: July 2026
