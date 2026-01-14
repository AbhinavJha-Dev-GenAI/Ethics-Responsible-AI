# 08. Ethics Case Studies: Learning from Failure 📉🚩

Examining real-world AI failures helps us understand how subtle biases and technical shortcuts can have massive social consequences.

## Case 1: Amazon's Biased Hiring Tool (2018) 💼
*   **The Issue**: AI screened resumes based on 10 years of historical data. Since tech was male-dominated, the model penalized resumes with the word "women's" (e.g., "Women's Chess Club").
*   **Lesson**: Historical bias in data will lead to discriminatory models. Representation matters in training sets.

---

## Case 2: COMPAS Recidivism Prediction (2016) ⚖️
*   **The Issue**: A tool used by US judges to predict future crime. Investigation found it had a much higher False Positive rate for Black defendants than White defendants.
*   **Lesson**: Fairness definitions matter. Even if you don't use "race" as a feature, other variables (zip code, income) can act as **proxies** for race.

---

## Case 3: Google Photos Tagging (2015) 🖼️
*   **The Issue**: Image recognition model mislabeled Black people as gorillas.
*   **Lesson**: Extreme representation bias can lead to dehumanizing and harmful errors. Continuous monitoring and diverse auditing teams are essential.

---

## Case 4: Microsoft Tay (2016) 🐦
*   **The Issue**: A Twitter chatbot that became highly toxic and racist within 24 hours due to users "feeding" it coordinated hateful prompts.
*   **Lesson**: Models in the wild face **adversarial feedback loops**. Security and moderation filters must be live and robust.

---

## 💡 How to avoid these?
1.  **Diverse Teams**: Diverse people spot diverse biases.
2.  **External Audits**: Hire 3rd parties to red-team your models.
3.  **Human-in-the-Loop**: High-stakes decisions should never be 100% automated.
