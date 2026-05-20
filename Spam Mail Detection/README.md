# Spam Mail Detection

## Overview

This project implements a machine learning-based spam mail detection system that classifies emails as either **spam** or **ham** (legitimate emails). The classifier uses **Logistic Regression** with **TF-IDF vectorization** to analyze email text and accurately identify spam messages.

The model is trained on a dataset of labeled emails and achieves high accuracy in distinguishing between spam and legitimate communications. This project demonstrates practical applications of text classification and natural language processing (NLP) in email filtering.

## Key Features

- **Text Preprocessing**: Lowercase conversion and text normalization
- **TF-IDF Feature Extraction**: Converts raw email text into numerical features
- **Logistic Regression Classification**: Binary classification model (Spam/Ham)
- **Model Evaluation**: Comprehensive accuracy metrics on training and test data
- **User Input Testing**: Predict classification for custom email messages

## Libraries Used

### Core Data Processing
- **NumPy**
- **Pandas**

### Machine Learning & Text Processing
- **Scikit-learn**
  - Comprehensive machine learning library
  - **`train_test_split`**: Splits dataset into training (80%) and testing (20%) subsets
  - **`TfidfVectorizer`**: Converts raw email text into TF-IDF (Term Frequency-Inverse Document Frequency) feature matrix
    - Removes common English stop words
    - Captures the importance of words in each email
  - **`LogisticRegression`**: Binary classification model that learns to distinguish spam from ham
  - **`accuracy_score`**: Evaluates model performance on training and test data

## Project Workflow

1. **Data Loading**: Read email data from `mail_data.csv` containing message text and category labels
2. **Data Cleaning**: 
   - Convert all text to lowercase for consistency
   - Handle categorical variables (map "spam" → 0, "ham" → 1)
3. **Data Splitting**: Divide data into 80% training and 20% testing sets
4. **Feature Extraction**: Transform raw email text into numerical TF-IDF features
5. **Model Training**: Train Logistic Regression classifier on training features
6. **Model Evaluation**: Test accuracy on both training and testing data
7. **Prediction**: Make predictions on new email messages

## Dataset

The project uses the `mail_data.csv` file located in the `data/` directory containing:
- **Message**: Raw email text content
- **Category**: Label indicating if the email is "spam" or "ham"

## Results

The trained model provides:
- Training accuracy metrics
- Test accuracy metrics
- Ability to classify new emails as spam or legitimate

---

**Type**: Binary Classification  <br />
**Algorithms**: Logistic Regression  <br />
**Text Vectorization**: TF-IDF <br />
**Last Updated**: May 2026
