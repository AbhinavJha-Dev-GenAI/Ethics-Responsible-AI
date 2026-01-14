# 02. AI Fairness ⚖️🤖

Fairness is the mathematical attempt to define what "unbiased" looks like. Since there are multiple definitions of fairness that often conflict, choosing the right one is a design decision.

## 1. Group Fairness Metrics 📊

*   **Demographic Parity**: The probability of receiving a positive outcome should be the same for all groups. ($P(\hat{Y}=1 | G=a) = P(\hat{Y}=1 | G=b)$).
*   **Equal Opportunity**: The True Positive Rate (Recall) should be the same for all groups.
*   **Equalized Odds**: Both True Positive Rate and False Positive Rate should be the same for all groups.

---

## 2. Individual Fairness 👤

*   **The Principle**: "Similar individuals should be treated similarly."
*   This is often harder to calculate as it requires a distance metric to define "similarity" between individuals.

---

## 3. Mitigation Strategies 🛡️

1.  **Pre-processing**: Transforming the data before training (e.g., re-weighing instances or removing biased correlations).
2.  **In-processing**: Adding a fairness constraint directly into the model's loss function (e.g., Penalizing the model if it can predict 'gender' from its internal embeddings).
3.  **Post-processing**: Adjusting the decision thresholds for different groups *after* the model is trained to meet fairness targets.

---

## 🛠️ Essential Snippet (Post-processing Logic)

```python
# To achieve Equal Opportunity, we might lower the threshold for Group A 
# if the model is naturally more conservative with them.

def fair_predict(probs, group, threshold_a=0.4, threshold_b=0.6):
    if group == 'A':
        return 1 if probs >= threshold_a else 0
    else:
        return 1 if probs >= threshold_b else 0
```

---

## 🧩 The Fairness-Accuracy Tradeoff
Strictly enforcing fairness constraints often leads to a slight decrease in overall model accuracy. The goal is to find the **Pareto Optimal** point where you minimize bias while maintaining utility.
