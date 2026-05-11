# Bank Marketing Campaign Prediction & Profit Optimization

**Tools:** Python · scikit-learn · AdaBoost · Random Forest · Decision Tree · GridSearchCV

---

## Problem

A bank needed to identify which customers were likely to subscribe to a term deposit following a marketing campaign while maximizing campaign profitability rather than focusing solely on prediction accuracy.

---

## Approach

- Prepared and cleaned marketing campaign data
- Applied one-hot encoding to categorical variables
- Performed train/test splitting for model evaluation
- Built and compared:
  - AdaBoost
  - Decision Tree
  - Random Forest
- Tuned the Random Forest model using 5-fold GridSearchCV
- Evaluated models using a custom marketing profit value function

---

## Results

The tuned Random Forest generated:

# $57,190 Predicted Marketing Profit

### Performance Improvements
- 317% improvement over AdaBoost
- 143% improvement over Decision Tree

This project demonstrates how machine learning model selection and hyperparameter tuning can directly improve campaign profitability and business decision-making.

---

## Repository Structure

```text
bank_data.csv                         -> marketing campaign dataset
notebooks/                            -> Jupyter notebook workflows
reports/                              -> exported HTML/PDF outputs
```

---

## Files

| File | Description |
|------|-------------|
| `notebooks/bank_marketing_prediction.ipynb` | Full machine learning workflow and analysis |
| `reports/bank_marketing_prediction.html` | Rendered HTML version of the project |

---

# Author

Cameron Batts

GitHub: https://github.com/Cameron-Batts

Portfolio: https://cameron-batts.github.io

