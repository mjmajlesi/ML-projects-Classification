# Toxic Comment Classification

## Overview

This project implements a machine learning-based toxic comment classifier that detects whether an online comment is **toxic** or **clean**. The classifier uses **Logistic Regression** with **TF-IDF vectorization** to analyze comment text and accurately identify toxic behavior.

The model is trained on a dataset of labeled comments and achieves high accuracy in distinguishing between toxic and non-toxic content. This project demonstrates practical applications of text classification and natural language processing (NLP) in content moderation and online safety.

## Key Features

- **Text Preprocessing**: Handling of missing values and text normalization
- **Binary Label Conversion**: Aggregation of six toxicity categories into a single clean/toxic label
- **TF-IDF Feature Extraction**: Converts raw comment text into numerical features
- **Logistic Regression Classification**: Binary classification model (Toxic/Clean)
- **Stratified Train-Test Split**: Balanced class distribution (80% training, 20% testing)
- **Model Evaluation**: Comprehensive accuracy and classification report metrics on training and test data
- **User Input Testing**: Predict classification for custom comment messages

## Libraries Used

### Core Data Processing
- **NumPy**
- **Pandas**

### Machine Learning & Text Processing
- **Scikit-learn**
  - Comprehensive machine learning library
  - **`train_test_split`**: Splits dataset into training (80%) and testing (20%) subsets with stratification
  - **`TfidfVectorizer`**: Converts raw comment text into TF-IDF (Term Frequency-Inverse Document Frequency) feature matrix
    - Removes common English stop words
    - Captures the importance of words in each comment
  - **`LogisticRegression`**: Binary classification model that learns to distinguish toxic from clean comments
  - **`accuracy_score`**: Evaluates model performance on training and test data
  - **`classification_report`**: Provides precision, recall, and F1-score for each class

## Project Workflow

1. **Data Loading**: Read comment data from `train.csv` containing comment text and toxicity labels
2. **Data Exploration**: Examine dataset structure, data types, and missing values
3. **Data Cleaning**:
   - Handle categorical toxicity labels
   - Convert six toxicity categories into a single binary label (toxic = 1, clean = 0)
4. **Data Splitting**: Divide data into 80% training and 20% testing sets with stratification
5. **Feature Extraction**: Transform raw comment text into numerical TF-IDF features
6. **Model Training**: Train Logistic Regression classifier on training features
7. **Model Evaluation**: Test accuracy and classification report on both training and testing data
8. **Prediction**: Make predictions on new comment messages

## Dataset

The project uses the `train.csv` file located in the `data/` directory containing:

| Column | Description |
|--------|-------------|
| **id** | Unique identifier for each comment |
| **comment_text** | Raw text content of the comment |
| **toxic** | Toxicity label (1 = toxic, 0 = not toxic) |
| **severe_toxic** | Severe toxicity label (1/0) |
| **obscene** | Obscene content label (1/0) |
| **threat** | Threat label (1/0) |
| **insult** | Insult label (1/0) |
| **identity_hate** | Identity hate label (1/0) |

The six toxicity labels are aggregated into a single binary target: if any category is active, the comment is classified as **toxic**; otherwise it is **clean**.

## Results

The trained model provides:
- Training accuracy metrics
- Test accuracy metrics
- Precision, recall, and F1-score per class
- Ability to classify new comments as toxic or clean

---

**Type**: Binary Classification  <br />
**Algorithms**: Logistic Regression  <br />
**Text Vectorization**: TF-IDF <br />
**Last Updated**: June 2026
