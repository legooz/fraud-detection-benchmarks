# Fraud Detection Benchmarks

Compare supervised and anomaly-detection approaches to transaction fraud, then explore evaluation when transactions arrive over time.

**Stack:** pandas, scikit-learn, XGBoost, LightGBM, TensorFlow/Keras.  
**Status:** research experiments, including a synthetic-data option in the streaming notebook.

## Start here

Open [`Fraud_Detection_LightGBM_Online_Simulation.ipynb`](notebooks/Fraud_Detection_LightGBM_Online_Simulation.ipynb). It trains on an initial block, predicts incoming chunks before revealing labels, and periodically retrains. If expected files are absent, it creates synthetic data.

```bash
python -m venv .venv
# Activate .venv, then:
python -m pip install -r requirements.txt
python -m jupyter lab
```

Python 3.11 or 3.12 is a starting point. Run cells in order. Install `requirements-neural.txt` for the TensorFlow comparison.

## Experiments

- Random Forest, XGBoost, and SVM classification.
- LightGBM and dense neural-network comparisons.
- Isolation Forest, neighborhood-based, and one-class anomaly detection.
- IEEE-CIS transaction/identity data preparation.
- Streaming simulation with ROC-AUC, average precision, precision, recall, and F1 tracking.

## Data and interpretation

See [DATA.md](DATA.md). Raw financial records, competition archives, and trained models are not distributed. Set `PROJECT_DATA_DIR` to use permitted local data.

The notebooks use different datasets and protocols; their scores are not a controlled benchmark without matched data, splits, and preprocessing. Synthetic scores demonstrate the pipeline, not real fraud-detection performance. The online experiment simulates periodic batch retraining, not a deployed transaction-scoring service.

Saved outputs are cleared. CI checks format and syntax, not training quality. Exact historical dependency versions have not been recovered. See [NOTICE.md](NOTICE.md).
