# 📰 Fake News Predictions

A comprehensive machine learning project that detects and classifies fake news articles using advanced **Natural Language Processing (NLP)** techniques and the **Logistic Regression** algorithm. This project demonstrates practical applications of text preprocessing, feature extraction, and binary classification in combating misinformation.

## 📋 Project Overview

In the digital age, misinformation spreads rapidly across social media and news platforms. This project aims to build an intelligent system that can **automatically identify fake news articles** and distinguish them from genuine, credible news sources.

The model analyzes article content (title + text) using sophisticated text preprocessing and TF-IDF vectorization, enabling accurate classification of news articles as either **Real** or **Fake**.

## 🎯 Key Features

- **Text Normalization & Preprocessing**: Lowercase conversion, special character removal, and text cleaning
- **Advanced Stemming**: Porter Stemmer algorithm for reducing words to their root form
- **Stop Words Removal**: Eliminates common English words to focus on meaningful content
- **TF-IDF Feature Extraction**: Converts raw text into numerical features capturing word importance
- **Logistic Regression Classification**: Binary classification model (Real/Fake)
- **Stratified Train-Test Split**: Balanced data distribution (80% training, 20% testing)
- **Model Evaluation**: Comprehensive accuracy metrics for performance assessment

## 📚 Libraries Used

- **Scikit-learn**:
  - **`LabelEncoder`**: Encodes categorical labels (Fake → 0, Real → 1)
  - **`train_test_split`**: Splits dataset into training (80%) and testing (20%) with stratification
  - **`TfidfVectorizer`**: Converts raw text into TF-IDF (Term Frequency-Inverse Document Frequency) feature matrix
    - Removes common English stop words for focused analysis
    - Captures the relative importance of words across documents
  - **`LogisticRegression`**: Binary classification model for distinguishing real from fake news
  - **`accuracy_score`**: Evaluates model performance on training and test data

- **NLTK (Natural Language Toolkit)**:
  - **`PorterStemmer`**: Reduces words to their root/stem form (e.g., "running" → "run")
  - **`stopwords`**: English stop words corpus for filtering common, non-informative words
  - **`re` (Regular Expressions)**: Pattern matching for text cleaning and normalization

## 📊 Dataset

The project uses the **`fake_or_real_news.csv`** file containing:

| Column | Description |
|--------|-------------|
| **title** | Headline of the news article |
| **text** | Full article content |
| **label** | Classification label: "FAKE" or "REAL" |

The combined title and text provide comprehensive content for training the classification model.

## 🧹 Data Preprocessing Details

### Stemming Process
Stemming reduces related words to their common root form:
- "running", "runner", "ran" → "run"
- "classification", "classify", "classifier" → "classifi"

This improves model performance by:
- Reducing vocabulary size
- Grouping semantically similar words
- Focusing on word meaning rather than variations

### Stop Words
Common English words (the, is, and, a, etc.) are removed because they:
- Don't contribute meaningful information
- Reduce feature space dimensionality
- Improve model focus on discriminative words

## 🤖 Model Architecture

**Logistic Regression**:
- Type: Linear binary classification algorithm
- Advantages: 
  - Fast training and inference
  - Interpretable decision boundaries
  - Excellent baseline performance for text classification
  - Works well with high-dimensional sparse data (TF-IDF features)

## 💡 Use Cases & Applications

- **Social Media Monitoring**: Identify false information in user-generated content
- **News Curation**: Filter unreliable sources from news feeds
- **Fact-Checking Automation**: Assist in automated verification workflows
- **Content Moderation**: Support editorial teams in content validation
- **Information Security**: Detect misinformation campaigns early

## 🚀 Future Enhancements
- **Ensemble Methods**: Combine multiple models (e.g., Random Forest, SVM) for improved accuracy
- **Deep Learning**: Explore LSTM or BERT for contextual understanding of text

<br />

**Type**: Binary Classification <br />
**Algorithms**: Logistic Regression  <br />
**Text Vectorization**: TF-IDF <br />
**Last Updated**: May 2026
