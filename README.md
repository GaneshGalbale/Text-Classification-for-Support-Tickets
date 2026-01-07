# Customer Support Ticket Classification using NLP

## Overview
This project implements an end-to-end Natural Language Processing (NLP) pipeline to classify customer support tickets into predefined categories such as Billing Inquiry, Cancellation Request, Product Inquiry, Refund Request, and Technical Issue. The objective is to demonstrate a complete text classification workflow including data preprocessing, feature extraction, model training, and evaluation.

---

## Dataset
The dataset contains customer support ticket records with fields such as:
- Ticket Description (text data)
- Ticket Type (category/label)

The **Ticket Description** field is used as input text, and **Ticket Type** is used as the target label for classification.

-THIS DATASET WAS DOWNLOADED FROM KAGGLE https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset?resource=download**
---

## Approach

### 1. Data Preprocessing
- Converted text to lowercase
- Removed punctuation and numbers
- Removed English stopwords
- Applied lemmatization using NLTK

### 2. Feature Extraction
- Used **TF-IDF Vectorization** with unigrams and bigrams to convert text into numerical features

### 3. Model Training
- Evaluated multiple baseline models:
  - Logistic Regression
  - Multinomial Naive Bayes
  - Linear Support Vector Machine (SVM)
- **Linear SVM** was selected for final submission due to better stability on high-dimensional text data

### 4. Evaluation
- Precision, Recall, and F1-score per category
- Confusion Matrix visualization for error analysis

---

## Results & Observations
The model achieves baseline performance due to:
- High semantic overlap between ticket categories (e.g., billing, refund, cancellation)
- Presence of boilerplate and template text across multiple classes
- Real-world ambiguity where multiple intents can coexist in a single ticket

This behavior reflects realistic customer support data challenges. The primary goal of this project is to demonstrate a clean and complete NLP pipeline rather than optimize for dataset-specific performance.

---

## Technologies Used
- Python
- Pandas, NumPy
- NLTK (text preprocessing)
- Scikit-learn (TF-IDF, SVM, evaluation)
- Matplotlib, Seaborn (visualization)

## How to run:
- Download customer_support_tickets.csv file import into Google Colab runtime.
- Download the ticket_classification.ipynb file and run in Google Colab.

## Notes
This project was developed as part of a recruitment task to demonstrate practical NLP implementation for customer support ticket classification.
---


