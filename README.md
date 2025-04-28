# 📈 Financial Indicator Classification

This project uses over 200 financial indicators to classify whether a stock’s price will increase during 2018. The goal is to develop predictive models to assist in buy/sell decisions at the beginning of the year, using only information available at that time.

---

## 🎯 Objective

Predict whether a stock should be bought at the start of 2018 based on financial fundamentals and ratios, without using any future price information.

---

## 📚 Study Summary

- **Data Source**: [Kaggle](https://www.kaggle.com/datasets/cnic92/200-financial-indicators-of-us-stocks-20142018/data)
- **Target Variable**: `Class` (1 = stock price increased, 0 = stock price did not increase)
- **Features**: Over 200 financial indicators including profitability ratios, liquidity ratios, and market valuation metrics
- **Languages Used**: R
- **Goal**: Build classification models to predict stock movement direction realistically without overfitting

---

## 🧠 Methods

- Removed future-looking variables (`X2019.PRICE.VAR...`) to simulate a real investment decision
- Performed variable selection using LASSO regression to reduce dimensionality
- Applied classification algorithms:
  - Logistic Regression
  - Linear Discriminant Analysis (LDA)
  - Quadratic Discriminant Analysis (QDA)
  - k-Nearest Neighbors (kNN)
- Evaluated model performance using:
  - Accuracy
  - Kappa statistic
  - ROC Curve and AUC
  - Scatter plots of predictions 

---

## ✅ Key Findings

- Logistic Regression and LDA performed similarly, but struggled to classify minority classes accurately.
- kNN achieved the highest Kappa, suggesting better relative performance in imbalanced settings.
- All models had difficulty predicting the minority class (`Class = 0`), reflecting the challenges of real-world imbalanced datasets.
- Variable selection with LASSO helped improve model generalizability by focusing on the most predictive financial indicators.

---

## 🛠 Tools Used

- **R**: `caret`, `glmnet`, `pROC`, `ggplot2`
- **Version Control**: Git and GitHub


