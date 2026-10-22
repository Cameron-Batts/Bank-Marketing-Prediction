# Bank Marketing Model Selection with a Custom Payoff

**Author:** Cameron Batts

## Business Problem
Compare classifiers using explicit marketing payoff assumptions rather than accuracy alone.

## Approach
Use 45,211 bank marketing records and a 75/25 split with random_state=42. Drop day, month, duration, pdays and poutcome; one-hot encode categorical fields. Compare AdaBoost, a decision tree and a balanced random forest tuned across 12 parameter combinations using five-fold cross-validation.

## Results
The workflow was rerun on October 22, 2026 with the included data. These are retrospective simulations under assumed payoffs, not realized business profit.

| Model | Historical campaign payoff | Rerun campaign payoff |
| --- | ---: | ---: |
| AdaBoost | €13,700 | €13,700 |
| Decision tree | €23,510 | €24,000 |
| Tuned random forest | €57,190 | €57,190 |

Rerun best forest parameters: `max_depth=5`, `n_estimators=200`. Historical results are preserved separately in [the validation record](Reports/rerun_metrics.json); library-version differences were not isolated experimentally.

## Validation and Limitations
The CV tuning objective values TN=+€10, FP=−€10, FN=−€100 and TP=+€100 per observation, while the final contacted-customer payoff uses only TP=+€100 and FP=−€10. These are different objectives. One-hot vocabulary was formed before splitting; fit encoders on training folds for stricter evaluation. A single random split and fixed payoffs do not establish deployment performance.

All notebook code cells executed sequentially on October 22, 2026 in a fresh Python 3.12.14 namespace using scikit-learn 1.8.0, pandas 2.2.3 and NumPy 2.3.5. The included dataset produced 33,908 training rows and 11,303 test rows. Confusion-matrix totals and both payoff formulas were independently checked. Jupyter rendering and a separate clean-environment reinstall were not tested. Core numerical dependencies are pinned in `requirements-validation.txt`; the notebook editor remains unpinned.

## Data
The repository includes Data/bank_data.csv, a semicolon-delimited file with 45,211 rows and 17 columns (16 predictors and the target). Preserve existing data attribution; verify redistribution terms before reuse.

## Run
```bash
python -m pip install -r requirements-validation.txt
python -m pip install jupyterlab
jupyter lab
```
Open the notebook linked below and run cells in order.

## Files
- [Analysis notebook](Notebooks/bank_marketing_prediction.ipynb): code and rerun outputs.
- [Readable analysis](Reports/bank_marketing_prediction.html): narrative report.
- [Existing PDF](Reports/bank_marketing_prediction.pdf): original exported report; it may predate these interpretation corrections.
- [Dependencies](requirements.txt).
- [Validated numerical environment](requirements-validation.txt).
- [Rerun metrics and checks](Reports/rerun_metrics.json).

[Live portfolio report](https://cameron-batts.github.io/bank_marketing_prediction.html) · [Portfolio](https://cameron-batts.github.io)
