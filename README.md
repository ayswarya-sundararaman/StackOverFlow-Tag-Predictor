

# StackOverflow Tag Prediction

This project predicts tags for StackOverflow questions using machine learning models, specifically designed to address the multi-label classification problem of assigning relevant tags based on the content of the question.

## Dataset
- **Source**: Kaggle Facebook Recruiting III - Keyword Extraction competition.
- **Features**: Question titles, bodies, and associated tags.
- **Size**: 6 million rows of training data (questions with tags).

## Problem Statement
- **Objective**: Predict tags for StackOverflow questions based on the question’s title and body.
- **Challenge**: Multi-label classification where each question can have multiple tags.

## Techniques Used
1. **Data Preprocessing**:
   - Removed HTML tags and special characters.
   - Applied tokenization and stemming.
   - Vectorized text data using **TF-IDF** and **CountVectorizer**.

2. **Clustering and Dimensionality Reduction**:
   - Used **Truncated SVD** for dimensionality reduction on high-dimensional text data.

3. **Models Implemented**:
   - **Logistic Regression** with **OneVsRestClassifier** for multi-label classification.
   - **SGDClassifier** with L1 penalty for improved tag prediction accuracy.
   - **Multilabel K-Nearest Neighbors (MLkNN)** for tag prediction.

## Results
- **Evaluation Metrics**: F1 score (micro and macro), Hamming Loss.
- **Best Model Performance**:
  - Macro F1 score: 0.77
  - Micro F1 score: 0.85
  - Hamming Loss: 0.14

## Conclusion
The project effectively predicts relevant tags for StackOverflow questions by leveraging multi-label classification techniques, with optimized performance through data preprocessing and model selection.
