# 09. Ethics & Responsible AI Interview Prep 🧠🏛️

For modern AI roles, "Culture Fit" and "Technical Prowess" are joined by "Ethical Awareness." You status on these topics determines if you can be trusted with production systems.

## 1. Scenario Questions 🎭

*   **Q: Your high-accuracy model has a 10% lower accuracy for a minority group. What do you do?**
    - *A:* 1. Investigate the data (under-representation?). 2. Try re-weighing the loss function. 3. Adjust decision thresholds (Post-processing). 4. If nothing works, document the limitation and consider if the model is safe for deployment.
*   **Q: A stakeholder asks you to use 'Gender' to improve the model. Is this okay?**
    - *A:* It depends. In healthcare, gender might be a valid biological feature. In hiring or lending, it is often illegal/unethical. Even if permitted, it can lead to "Disparate Impact."

---

## 2. Technical Concepts 📖

*   **Q: Explain the difference between Demographic Parity and Equal Opportunity.**
    - *A:* Demographic Parity wants equal outcomes for everyone ($P(\hat{Y}=1)$). Equal Opportunity wants equal True Positive Rates (Recall) for everyone.
*   **Q: How does SHAP work conceptually?**
    - *A:* It uses Game Theory to see how the prediction changes when a feature is included vs. when it is not, averaging this over all possible orderings of features.
*   **Q: What is a "Privacy Budget" in Differential Privacy?**
    - *A:* Represented by Epsilon ($\epsilon$). It quantifies how much privacy is "spent" with each query. Lower $\epsilon$ = higher privacy but more noise.

---

## 3. The "Right" Mindset 🛡️

*   **Proactive over Reactive**: Don't wait for a lawsuit; audit before launch.
*   **Transparency**: Document your model's limitations clearly (Model Cards).
*   **Alignment**: The goal is to build AI that helps, not just AI that predicts.

---

## 🎯 Ethics Cheat Sheet
1. **Bias**: Detection via Slicing.
2. **Fairness**: Mitigation via In/Post-processing.
3. **XAI**: local (SHAP/LIME) vs Global.
4. **LLM**: RLHF for alignment + Moderation APIs.
