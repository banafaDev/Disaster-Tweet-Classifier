# Disaster Relief Tweet Classification

A machine learning project that classifies disaster-related tweets to support emergency response systems.

## Overview

This project builds a classification model to automatically identify tweets related to disasters. The model analyzes social media text data and predicts whether a tweet is disaster-related or not, enabling faster information processing during emergencies.

**Main Application**: Emergency management, disaster response, and real-time situation awareness.

## Dataset

- **File**: `train.csv`
- **Content**: Labeled tweets with disaster/non-disaster classification
- **Columns**: text, target, keyword, location

## Project Workflow

### 1. Data Loading
- Load training data from CSV file
- Explore dataset structure and distribution

### 2. Text Preprocessing
Clean and prepare text data:
- Remove URLs and HTML tags
- Remove special characters and numbers
- Convert to lowercase
- Tokenize text
- Remove stopwords (except "not" for sentiment)
- Apply stemming to normalize words

### 3. Feature Engineering
- Convert cleaned text to numerical vectors using TF-IDF
- Split data into 80% training and 20% test sets

### 4. Model Training
Train and evaluate multiple models:
- **Naive Bayes** - Fast probabilistic classifier
- **Logistic Regression** - Linear classification model
- **Support Vector Machine (SVM)** - Powerful for high-dimensional data
- **Random Forest** - Ensemble tree-based model

### 5. Hyperparameter Tuning
- Use GridSearchCV with 5-fold cross-validation
- Find optimal parameters for each model
- Evaluate on test set

### 6. Model Selection
**Selected Model: Logistic Regression**
- **Accuracy**: 80%
- **Precision**: 0.81
- **Recall**: 0.77
- **F1-Score**: 0.78

**Why Logistic Regression?**
- Highest precision - minimizes false positives
- Fast and efficient inference
- Easy to interpret and maintain
- Excellent performance-to-complexity ratio

## Results

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Naive Bayes | 80% | 0.80 | 0.78 | 0.79 |
| Logistic Regression | 80% | 0.81 | 0.77 | 0.78 |
| SVM | 80% | 0.80 | 0.78 | 0.79 |
| Random Forest | ~75% | - | - | - |

## Use Cases

### Real-Time Crisis Detection
- Automatically identify disaster-related tweets as they appear
- Alert emergency teams to active incidents

### Resource Allocation
- Prioritize deployment to high-risk areas
- Direct resources based on disaster severity

### Post-Disaster Analysis
- Assess damage through social media analysis
- Plan recovery efforts for affected communities

## Installation

### Requirements
- Python 3.7+
- Jupyter Notebook

### Dependencies
```bash
pip install pandas numpy scikit-learn nltk
```

### NLTK Resources
```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
```

## Files Included

- **NLP.ipynb** - Complete Jupyter notebook with all analysis steps
- **train.csv** - Labeled tweet dataset

## Key Technologies

- **Python** - Programming language
- **pandas** - Data manipulation and analysis
- **scikit-learn** - Machine learning models and metrics
- **NLTK** - Natural language processing
- **numpy** - Numerical computing

## Performance Notes

- All models achieved approximately 80% testing accuracy
- Results are comparable across Naive Bayes, Logistic Regression, and SVM
- Logistic Regression selected for optimal balance of simplicity and performance

## Future Improvements

- Add deep learning models (LSTM, BERT)
- Implement ensemble methods combining multiple models
- Expand dataset for better generalization
- Add real-time prediction API
- Deploy model for production use

## Author

**Ahmed Banafa**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ahmed-banafi-4b5034313/)

## License

### MIT License

Copyright (c) 2026 Ahmed Banafa

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

**Note**: This model is trained on specific disaster tweet data. Performance may vary on different text data or domains.
