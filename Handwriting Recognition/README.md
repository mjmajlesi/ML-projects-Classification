# ✍️ Handwriting Recognition

A comprehensive machine learning project that recognizes and classifies **handwritten digits (0-9)** using multiple classification algorithms on the **MNIST dataset**. This project demonstrates practical applications of image preprocessing, feature scaling, and multi-class classification in the domain of **optical character recognition (OCR)**.

## 📋 Project Overview

Handwriting recognition is a classic machine learning problem with real-world applications in **postal mail sorting**, **bank check processing**, **digital note-taking**, and **automated form processing**. This project aims to build intelligent systems that can **automatically identify handwritten digits** from pixel data.

The model processes 28×28 grayscale images of handwritten digits, using pixel intensity values as features. Multiple classification algorithms are trained and compared to find the most effective approach for multi-class digit recognition.

## 🎯 Key Features

- **Pixel Intensity Analysis**: 784 pixel features (28×28 grayscale images) used as input
- **Feature Scaling**: StandardScaler normalization for optimal model performance
- **Multi-Class Classification**: Distinguishes between 10 digit classes (0-9)
- **Stratified Train-Test Split**: Balanced data distribution (80% training, 20% testing)
- **Multiple Model Comparison**: Logistic Regression, Random Forest, and SVM
- **Visualization**: Sample digit display, confusion matrices, and feature importance maps
- **Model Evaluation**: Comprehensive accuracy metrics, classification reports, and comparison charts

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
  - **`StandardScaler`**: Normalizes pixel features to zero mean and unit variance
  - **`LogisticRegression`**: Multi-class classification using one-vs-rest strategy
  - **`RandomForestClassifier`**: Ensemble method with 100 decision trees for robust classification
  - **`SVC`**: Support Vector Machine with RBF kernel for non-linear classification
  - **`accuracy_score`**: Evaluates model performance on training and test data
  - **`classification_report`**: Provides precision, recall, and F1-score for each digit class
  - **`confusion_matrix`**: Visualizes correct and incorrect predictions per class

## 📊 Dataset

The project uses the **`mnist_digits.csv`** file located in the `data/` directory containing:

| Column | Description |
|--------|-------------|
| **split** | Data split indicator: "train" or "test" |
| **label** | Classification label (digit 0-9) |
| **pixel_0** to **pixel_783** | Grayscale pixel values (28×28 = 784 pixels) |

### Dataset Statistics
- **Total Samples**: 70,000
- **Training Samples**: 60,000
- **Testing Samples**: 10,000
- **Image Size**: 28×28 pixels (784 features)
- **Classes**: 10 (digits 0-9)
- **Class Distribution**: Balanced across all digits

## 🧹 Data Preprocessing Details

### Feature Scaling
Pixel values (0-255) are normalized using **StandardScaler**:
- Transforms features to zero mean and unit variance
- Improves convergence speed for gradient-based algorithms (Logistic Regression)
- Ensures equal feature contribution for distance-based algorithms (SVM)

### Train-Test Split
- **80% Training** (56,000 samples) for model learning
- **20% Testing** (14,000 samples) for unbiased evaluation
- **Random State**: 42 for reproducibility

## 🤖 Model Architecture

### Logistic Regression
- **Type**: Linear multi-class classifier (One-vs-Rest)
- **Advantages**: Fast training, interpretable, excellent baseline
- **Max Iterations**: 1000 (for convergence on large dataset)

### Random Forest Classifier
- **Type**: Ensemble of 100 decision trees
- **Advantages**: Handles non-linear relationships, provides feature importance
- **Estimators**: 100 trees

### Support Vector Machine (SVM)
- **Type**: Non-linear classifier with RBF kernel
- **Advantages**: Effective in high-dimensional spaces, robust to overfitting
- **Kernel**: Radial Basis Function (RBF)

## 📈 Model Evaluation

### Metrics Used
- **Accuracy**: Overall correctness of predictions
- **Classification Report**: Precision, Recall, and F1-Score for each digit class
- **Confusion Matrix**: True Positives, False Positives, True Negatives, False Negatives
- **Feature Importance**: Random Forest-based pixel importance analysis

### Performance Comparison
All three models are trained on 80% of the data and evaluated on the 20% test set.

## 📝 Workflow

1. **Data Loading**: Read the MNIST CSV file into a Pandas DataFrame
2. **Data Exploration**: Examine dataset structure, statistics, and class distribution
3. **Visualization**: Display sample digits, average pixel intensities, and label distribution
4. **Preprocessing**: Drop unnecessary columns, check for missing values
5. **Feature Scaling**: Normalize pixel values using StandardScaler
6. **Data Splitting**: Divide data into 80% training and 20% testing sets
7. **Model Training**: Train Logistic Regression, Random Forest, and SVM models
8. **Evaluation**: Compare model performance using accuracy, classification reports, and confusion matrices
9. **Feature Importance**: Analyze which pixels are most important for classification
10. **Prediction**: Test models on individual samples and display results

## 💡 Machine Learning Concepts Demonstrated

- ✨ Multi-Class Classification (10 classes)
- ✨ Image Data as Features (Pixel Intensity)
- ✨ Feature Scaling and Normalization
- ✨ Exploratory Data Analysis (EDA)
- ✨ Train-Test Split (80-20)
- ✨ Model Comparison and Selection
- ✨ Confusion Matrix Analysis
- ✨ Feature Importance Analysis
- ✨ Ensemble Methods (Random Forest)
- ✨ Support Vector Machines
- ✨ Performance Metrics and Evaluation

## 💡 Use Cases & Applications

- **Postal Mail Sorting**: Automatic zip code recognition on envelopes
- **Bank Check Processing**: Reading handwritten amounts on checks
- **Digital Note-Taking**: Converting handwritten notes to digital text
- **Form Processing**: Automated data entry from handwritten forms
- **Education**: Student answer sheet grading and analysis

## 🚀 Future Enhancements
- **Convolutional Neural Networks (CNN)**: Deep learning approach for improved image classification
- **Data Augmentation**: Rotation, scaling, and shifting to improve model generalization
- **Hyperparameter Tuning**: Grid search and cross-validation for optimal model parameters

<br />

**Type**: Multi-Class Classification <br />
**Algorithms**: Logistic Regression, Random Forest, SVM <br />
**Feature Scaling**: StandardScaler <br />
**Last Updated**: July 2026
