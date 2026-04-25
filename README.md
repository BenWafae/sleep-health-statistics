# 😴 Sleep Health Statistics & ML Prediction

> Statistical analysis and Machine Learning prediction of sleep quality based on lifestyle and health data.

---

## Project Overview

This project combines **statistical analysis** and **Machine Learning** to study and predict sleep quality from a dataset of 374 individuals.

It follows a structured methodology inspired by **CRISP-DM** and covers the full data science pipeline — from descriptive statistics to predictive modeling.

---

## Objectives

- Explore and understand sleep health data
- Perform descriptive statistical analysis (mean, variance, confidence intervals)
- Apply hypothesis testing
- Build and evaluate ML classification models to predict sleep quality
- Interpret results and extract meaningful insights

---

## 📂 Project Structure

```
sleep-health-statistics/
│
├── data/                   # Raw dataset + extracted columns
├── notebooks/              # Jupyter notebooks (stats + ML)
├── machine_learning/       # ML models and results
├── requirements.txt        # Dependencies
└── README.md
```
---

##  Part 1 — Statistical Analysis

**Variable studied:** `Sleep Duration` (hours/day)

| Statistic | Value |
|-----------|-------|
| Min | 5.8h |
| Max | 8.5h |
| Mean | 7.13h |
| Variance | 0.63 |
| Std Dev | 0.80h |
| CI 95% | [7.05 , 7.21] |
| CI 98% | [7.03 , 7.23] |

**Hypothesis Test (t-test):**
- H0: mean = 7h → **Rejected** (p = 0.0014 < 0.05)
- Conclusion: individuals sleep significantly more than 7h on average

---

##  Part 2 — Machine Learning

### Problem
> Can we predict sleep quality from lifestyle and physiological features?

**Type:** Multi-class classification (Poor / Average / Good)

### Pipeline

1. **Data Cleaning** — handling missing values in `Sleep Disorder`
2. **Feature Engineering** — creating `Sleep_Quality_Category` from score
3. **Outlier Detection** — IQR method (15 outliers in Heart Rate, kept)
4. **Encoding** — One-Hot Encoding for categorical variables
5. **Normalization** — StandardScaler on numerical features
6. **Train/Test Split** — 80% train / 20% test (stratified)

### Model — Logistic Regression

| Metric | Score |
|--------|-------|
| Accuracy | **98.67%** |
| Precision (avg) | 0.99 |
| Recall (avg) | 0.99 |
| F1-score (avg) | 0.99 |

**Key findings:**
- `Average` and `Good` classes predicted with near-perfect accuracy
- `Poor` class correctly identified despite being underrepresented
- Very few misclassifications confirmed by the confusion matrix

---

##  Technologies

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

##  Author

**BENZHIR Wafa** — Bachelor's student in Data Science & Intelligent Systems

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/wafae-benzhir)
[![GitHub](https://img.shields.io/badge/GitHub-BenWafae-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/BenWafae)

---

##  Academic Context

Project completed as part of the **Statistiques Avancées** module
🎓 Academic year: 2025–2026
