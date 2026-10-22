# Bank Marketing Model Selection with a Custom Payoff

**Author:** Cameron Batts

## Business Problem
Compare classifiers using explicit marketing payoff assumptions rather than accuracy alone.

## Approach
Use 45,211 bank marketing records and a 75/25 split with random_state=42. Drop day, month, duration, pdays and poutcome; one-hot encode categorical fields. Compare AdaBoost, a decision tree and a balanced random forest tuned across 12 parameter combinations using five-fold cross-validation.

## Results
The saved test-set campaign payoff was €13,700 for AdaBoost, €23,510 for the decision tree and €57,190 for the tuned random forest. The forest used max_depth=5 and n_estimators=200. This is a retrospective simulation under assumed payoffs, not realized business profit.

## Validation and Limitations
The CV tuning objective values TN=+€10, FP=−€10, FN=−€100 and TP=+€100 per observation, while the final contacted-customer payoff uses only TP=+€100 and FP=−€10. These are different objectives. One-hot vocabulary was formed before splitting; fit encoders on training folds for stricter evaluation. A single random split and fixed payoffs do not establish deployment performance.

Original numerical outputs are retained. The revised workflow was syntax-checked but not fully rerun. Dependencies are unpinned.

## Data
The repository includes Data/bank_data.csv, a semicolon-delimited file with 45,211 rows and 17 input columns. Preserve existing data attribution; verify redistribution terms before reuse.

## Run
```bash
python -m pip install -r requirements.txt
jupyter lab
```
Open the notebook linked below and run cells in order.

## Files
- [Analysis notebook](Notebooks/bank_marketing_prediction.ipynb): code and original outputs.
- [Readable analysis](Reports/bank_marketing_prediction.html): narrative report.
- [Existing PDF](Reports/bank_marketing_prediction.pdf): original exported report; it may predate these interpretation corrections.
- [Dependencies](requirements.txt).

[Live portfolio report](https://cameron-batts.github.io/bank_marketing_prediction.html) · [Portfolio](https://cameron-batts.github.io)
