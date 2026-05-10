# Bank Marketing Campaign Prediction & Profit Optimization

**Tools:** Python · scikit-learn · AdaBoost · Random Forest · Decision Tree · GridSearchCV · Pandas · Matplotlib

---

## Business Problem

A financial institution needed to identify which customers were most likely to subscribe to a term deposit campaign while maximizing overall marketing profitability rather than focusing solely on prediction accuracy.

---

## Project Approach

- Cleaned and prepared customer marketing campaign data
- Applied one-hot encoding to categorical variables
- Performed train/test splitting for model evaluation
- Built and compared:
  - AdaBoost
  - Decision Tree
  - Random Forest
- Tuned the Random Forest model using 5-fold GridSearchCV
- Evaluated model performance using a custom marketing profit value function

---

## Results & Business Impact

The tuned Random Forest model generated:

# $57,190 Predicted Marketing Profit

### Performance Improvements
- 317% improvement over AdaBoost
- 143% improvement over Decision Tree

This project demonstrates how machine learning model selection and hyperparameter tuning can directly improve business decision-making and campaign profitability.

---

## Project Visuals

### Marketing Profit Performance

Comparison of machine learning model profitability across campaign prediction scenarios.

![Marketing Profit Comparison](images/model-profit-comparison.png)

### Key Predictive Features

Visualization of the most influential variables impacting customer subscription predictions.

![Feature Importance Analysis](images/feature-importance.png)

---

## Repository Structure

```text
data/        -> datasets used for analysis
images/      -> charts and project visuals
notebooks/   -> Jupyter notebooks and modeling workflows
reports/     -> exported reports and final outputs
```

---

## Files

| File | Description |
|------|-------------|
| `notebooks/bank_marketing_prediction.ipynb` | Full machine learning workflow and analysis |
| `reports/bank_marketing_prediction.pdf` | Exported project report |
| `images/` | Model visuals and performance charts |

---

## Portfolio

Portfolio Website: https://cameronbatts.github.io/

GitHub Profile: https://github.com/cameronbatts
