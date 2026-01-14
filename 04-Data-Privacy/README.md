# 04. Data Privacy 🔐🛡️

Data is the lifeblood of AI, but protecting the privacy of the individuals who provided that data is a legal and ethical requirement.

## 1. Core Concepts 🏗️

*   **Anonymization vs. Pseudonymization**: Removing direct identifiers (names) vs. replacing them with IDs. Note: Anonymization is often reversible with enough aggregate data!
*   **PII (Personally Identifiable Information)**: Any data that can be used to distinguish or trace an individual's identity.

---

## 2. Privacy-Preserving ML Techniques 🏗️

| Technique | How it Works |
| :--- | :--- |
| **Differential Privacy (DP)** | Adding "mathematical noise" to the data or gradients so that a single individual's info cannot be extracted. |
| **Federated Learning (FL)** | Training a model on edge devices (phones) without ever sending the raw data to a central server. |
| **Homomorphic Encryption** | Performing math/inference on encrypted data without ever decrypting it. |

---

## 3. Attacks on Privacy 🏹

*   **Membership Inference**: An attacker tries to determine if a specific record was part of the model's training set.
*   **Model Inversion**: Reconstructing an image or text from the model's weights or API outputs.

---

## 🛠️ Essential Snippet (DP Slogan)

> "The output of an algorithm should be roughly the same whether or not a specific individual's data is included in the input."

---

## 🛡️ Summary
Privacy isn't just about "encryption." It's about ensuring that the **patterns** learned by your model don't leak the **secrets** of your training data. For high-stakes fields like Finance or Healthcare, `DP-SGD` is becoming the production standard.
