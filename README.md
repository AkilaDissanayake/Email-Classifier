# 📧 Email Spam Classifier

![Python](https://img.shields.io/badge/python-3.10-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3.0-green)
![License](https://img.shields.io/badge/license-Educational-lightgrey)

---

## Overview
This project implements a **machine learning-based email spam classifier** using **Python** and **scikit-learn**. The model classifies emails as **spam** or **non-spam (ham)** using **TF-IDF vectorization** and **Multinomial Naive Bayes**.  

The project demonstrates how to preprocess raw email text, convert it into features, train a model, and evaluate its performance.

---

## Dataset
- **Source:** `emails.csv` (local CSV file)  
- **Columns:**  
  - `text` → Full content of the email, including the "Subject:" line  
  - `spam` → Label: `1` for spam, `0` for non-spam  
- **Distribution:**  
  - Spam emails: 1365  
  - Non-spam emails: 4363  

> **Note:** The dataset is ordered by label, so a **stratified train-test split** is used to maintain class balance.

---

## Preprocessing Steps
1. Remove `"Subject:"` from the start of each email.  
2. Count the number of words in each email (optional analysis).  
3. Prepare the cleaned email list (`R_X`) for TF-IDF vectorization.  

## Evaluation

The model is evaluated using **precision, recall, F1-score**, and **accuracy**.  

Example output from the classifier:

          precision    recall  f1-score   support

       0       0.99      0.99      0.99       872
       1       0.96      0.96      0.96       274

accuracy                           0.98      
       

