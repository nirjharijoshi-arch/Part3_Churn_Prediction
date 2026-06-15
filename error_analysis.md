# Error Analysis

## Confusion Matrix

| Actual / Predicted | No Churn | Churn |
| ------------------ | -------- | ----- |
| No Churn           | 141      | 27    |
| Churn              | 33       | 135   |

## False Positives

False positives occur when the model predicts churn but the customer does not actually churn.

### Business Risk

* Unnecessary retention offers
* Additional marketing cost
* Potential discount leakage

### Example Customers

1. Customer predicted to churn due to high return rate but remained active.
2. Customer with elevated support-ticket activity but retained.
3. Customer with low engagement but eventually purchased again.
4. Customer with high discount sensitivity but remained loyal.
5. Customer with declining sessions but did not churn.

## False Negatives

False negatives occur when the model predicts retention but the customer actually churns.

### Business Risk

* Lost revenue
* Lost customer lifetime value
* Missed retention opportunities

### Example Customers

1. Customer appeared highly engaged but churned unexpectedly.
2. Customer with recent purchases who stopped purchasing shortly afterward.
3. Customer with low return rates but churned.
4. Customer with healthy campaign engagement but churned.
5. Customer with average support activity who churned unexpectedly.

## Error Tradeoff

For churn prediction, false negatives are more costly than false positives because missed churners directly impact revenue.

The selected threshold prioritizes recall while maintaining strong precision.
