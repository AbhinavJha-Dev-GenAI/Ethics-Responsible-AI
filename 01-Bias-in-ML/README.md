# 01. Bias in Machine Learning 🔍📉

Understanding bias is the first step toward building responsible AI. Bias isn't just a "bug"; it often reflects systemic inequalities in the real world.

## 1. Types of Bias 🎭

*   **Historical Bias**: Occurs when the data reflects historical prejudices (e.g., hiring data from 1950 mirroring gender bias).
*   **Representation Bias**: Occurs when certain groups are under-represented or over-represented in the training set (e.g., facial recognition trained mostly on light-skinned faces).
*   **Measurement Bias**: Occurs when the proxies used for a target variable are flawed (e.g., using "healthcare costs" as a proxy for "healthcare need").
*   **Aggregation Bias**: Occurs when a single model is used for a diverse population where different subgroups have different underlying relationships.

---

## 2. The Bias Lifecycle 🌀

Bias can enter at any stage:
1.  **Data Collection**: Sampling bias, label bias.
2.  **Preprocessing**: Handling missing values in ways that disadvantage groups.
3.  **Model Choice**: Some models are more prone to overfitting on noise/bias.
4.  **Deployment**: Feedback loops where the model's predictions affect future data.

---

## 3. Detection Techniques 🔬

| Method | Description |
| :--- | :--- |
| **Slicing Analysis** | Evaluating model performance (Accuracy, recall) across different demographic slices (age, gender, region). |
| **Statistical Tests** | Using tests like Chi-Square to see if model errors are significantly correlated with sensitive attributes. |
| **Data Auditing** | Visualizing feature distributions across subgroups *before* training. |

---

## 🛠️ Essential Snippet (Slicing with Pandas)

```python
import pandas as pd

# Assume 'preds' is our model predictions and 'gender' is a sensitive attribute
results = pd.DataFrame({'actual': y_true, 'pred': y_pred, 'gender': df_test['gender']})

for group, data in results.groupby('gender'):
    accuracy = (data['actual'] == data['pred']).mean()
    print(f"Accuracy for group {group}: {accuracy:.4f}")
```

---

## 🚨 Summary
Bias is a multifaceted problem. As an ML Engineer, your job is to **proactively** search for these biases using slicing and auditing, rather than waiting for a failure in production.
