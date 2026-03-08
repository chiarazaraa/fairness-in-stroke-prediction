# Fairness in Stroke Prediction

## Project Overview

This project investigates the presence of gender bias in machine learning models for stroke prediction using a healthcare dataset.
The goal is to evaluate whether predictive models disadvantage female patients in terms of detection performance, even when gender is excluded from the training features.

The analysis compares baseline models and fairness-aware mitigation strategies to understand the trade-off between predictive performance and fairness.

---

## Dataset

The project uses the **Healthcare Stroke Prediction Dataset**, which contains demographic and clinical information for 4,908 patients.

Key variables include:

* age
* hypertension
* heart disease
* average glucose level
* BMI
* smoking status

### Preprocessing

The following preprocessing steps were applied:

* removal of missing BMI values
* one-hot encoding of categorical variables
* standardization of continuous features
* exclusion of gender from model training features

The dataset is highly imbalanced, with stroke cases representing a small minority of the observations.

---

## Models

Two machine learning models were implemented and compared:

* **Logistic Regression** (with class balancing)
* **XGBoost**

Both models were evaluated in terms of predictive performance and fairness across gender groups.

---

## Fairness Methods

The project explores several fairness-aware interventions:

* **FN-aware thresholding**
* **Equalized Odds constraints** using the *Fairlearn* library
* **Equalized Odds threshold tuning**

These methods aim to reduce disparities in True Positive Rate (TPR) between male and female patients.

---

## Evaluation Metrics

Model performance and fairness were evaluated using:

* Accuracy
* True Positive Rate (TPR)
* False Positive Rate (FPR)
* TPR gap between gender groups
* Trade-off between fairness and predictive performance

---

## Key Findings

* Baseline models achieved similar overall accuracy but showed **higher TPR for male patients**, indicating potential gender bias.
* Bias persisted **even after removing gender from the feature set**, suggesting indirect discrimination through correlated variables.
* **FN-aware thresholding** provided the best balance between fairness and predictive performance.
* Strong **Equalized Odds constraints** significantly reduced bias but also reduced predictive usefulness due to class imbalance.

---

## Repository Structure

```
fairness-in-stroke-prediction
│
├── fairness_stroke_prediction.ipynb
├── report.pdf
└── README.md
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Fairlearn
* Matplotlib
* Jupyter Notebook

---

## Author 
Project developed as part of a university coursework on Trustworthy Machine Learning and Fairness in AI by Chiara Zara and Pavlína Křenková

Project developed as part of a university coursework on **Trustworthy Machine Learning and Fairness in AI**.

