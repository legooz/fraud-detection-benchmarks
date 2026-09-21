# Datasets

The IEEE-CIS notebooks use the [IEEE-CIS Fraud Detection competition](https://www.kaggle.com/competitions/ieee-fraud-detection/data). Obtain `train_transaction.csv`, `train_identity.csv`, `test_transaction.csv`, and `test_identity.csv` through Kaggle under its terms.

`Full_Kaggle_Fraud_Detection.ipynb` contains merge/preparation work. Later experiments expect `train_merged_submission.csv` or `train_merged.csv`. Review feature selections before reproducing a comparison.

The Random Forest/XGBoost/SVM notebooks instead expect `Fraud Detection Transactions Dataset.csv`. Its original download reference has not been recovered. Do not substitute an unrelated dataset and present it as the original experiment.

Place permitted inputs in `data/` or set `PROJECT_DATA_DIR`. The streaming notebook falls back to synthetic data when prepared transaction files are absent.
