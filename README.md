# Churn Prediction Model

## Objective

Build a machine learning model that predicts whether a customer will churn within the next 60 days.

## Dataset

The project uses the provided RFM modeling snapshot containing customer demographics, purchasing behavior, support interactions, and marketing engagement metrics.

## Leakage Prevention

Only information available on or before the customer snapshot date was used.

Excluded fields:

* customer_id
* snapshot_date
* split
* churn_next_60d (target)

No future information was used as model input.

## Models Evaluated

### Baseline Model

Logistic Regression

### Stronger Model

Random Forest Classifier

## Final Model Selected

Logistic Regression

The baseline model outperformed Random Forest across Accuracy, Precision, Recall, F1 Score, and ROC-AUC while remaining highly interpretable.

## Test Performance

| Metric    | Value  |
| --------- | ------ |
| Accuracy  | 82.14% |
| Precision | 83.33% |
| Recall    | 80.36% |
| F1 Score  | 81.82% |
| ROC-AUC   | 0.885  |

## Top Drivers of Churn

1. return_rate_180d
2. negative_ticket_rate_90d
3. avg_discount_pct_180d
4. ticket_count_90d
5. marketing_consent

## Repository Contents

* churn_model.ipynb
* model.pkl
* metrics.json
* error_analysis.md
* model_card.md
* requirements.txt

## Model Loading

```python
import joblib

model = joblib.load("model.pkl")
```
