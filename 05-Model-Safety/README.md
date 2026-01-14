# 05. Model Safety & Robustness 🛡️⚡

Model safety ensures that AI systems behave predictably and resist intended or unintended harms. This is critical for systems deployed in the physical world (self-driving cars) or social systems (financial credit).

## 1. Adversarial Attacks 🏹

An attacker tries to fool a model by providing carefully crafted inputs.
- **Evasion Attacks**: Adding imperceptible noise to an image to make a CNN misclassify a "Stop Sign" as a "Speed Limit" sign.
- **Poisoning Attacks**: Injecting malicious data into the training set to create a "backdoor" in the model.

---

## 2. Red Teaming 🕵️‍♂️🛡️

The process of "playing the attacker" to find vulnerabilities before the model is released.
- **Scenario Testing**: What happens if the input is completely out-of-distribution?
- **Stress Testing**: Pushing the model to its limits (e.g., massive request bursts, extreme edge cases).

---

## 3. Robustness Techniques 🏗️

| Technique | Description |
| :--- | :--- |
| **Adversarial Training** | Training the model on both clean data and adversarial examples to make it "tougher." |
| **Defensive Distillation** | Using a smaller model to learn from a larger one in a way that smooths out sensitivity to noise. |
| **Input Sanitization** | Filtering or transforming inputs to remove potential adversarial noise before inference. |

---

## 🛠️ Essential Snippet (FGSM - Fast Gradient Sign Method)

```python
# The simplest way to create an adversarial example:
# perturbed_image = image + epsilon * sign(gradient_of_loss_wrt_image)
```

---

## 🚨 Summary
Safety is not a one-time check; it's a continuous process. As models become more powerful, Red Teaming and Robustness audits are becoming mandatory steps in the MLOps lifecycle.
