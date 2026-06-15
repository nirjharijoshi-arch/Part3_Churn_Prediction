# Model Card

## Model Name

Customer Churn Prediction Model

## Intended Use

Identify customers likely to churn within the next 60 days so that retention teams can proactively intervene.

## Data Used

The model uses customer behavioral, transactional, support, and engagement data available at the snapshot date.

## Model Type

Logistic Regression

## Target Variable

churn_next_60d

## Performance

| Metric    | Value  |
| --------- | ------ |
| Accuracy  | 82.14% |
| Precision | 83.33% |
| Recall    | 80.36% |
| F1 Score  | 81.82% |
| ROC-AUC   | 0.885  |

## Key Features

The strongest drivers of churn were:

1. return_rate_180d
2. negative_ticket_rate_90d
3. avg_discount_pct_180d
4. ticket_count_90d
5. marketing_consent

## Business Benefits

* Early identification of churn risk
* More effective retention spending
* Improved customer lifetime value

## Limitations

* Model performance may degrade as customer behavior changes.
* Historical patterns may not generalize to future market conditions.
* Predictions should support decision-making rather than replace human judgment.

## Ethical Considerations

The model should not be used to deny service or unfairly discriminate against customers.

## Monitoring Requirements

Monitor:

* Recall
* Precision
* Churn rate
* Data drift
* Feature distribution changes

## When Not To Use

The model should not be used when major business, pricing, product, or customer-service changes have occurred without retraining.
