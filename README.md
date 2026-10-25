# Customer Churn Prediction using Machine Learning

## Project Overview

Customer churn is a major challenge for businesses, as losing existing customers can directly impact revenue and growth.

The goal of this project is to build a Machine Learning model that can identify customers who are likely to churn, allowing the business to take proactive retention actions.

In this project:

- **Class 0** → Customer will not churn
- **Class 1** → Customer will churn

Since identifying potential churners is the primary objective, I focused particularly on improving the model's **Recall for Class 1 (Churn)**.

---

## Why Recall Matters in This Project

For a churn prediction problem, a **False Negative** occurs when:

> A customer is actually going to churn, but the model predicts that the customer will not churn.

This can be costly for a business because the company may lose the opportunity to retain that customer.

Therefore, instead of focusing only on overall accuracy, I prioritized **Recall for the churn class (Class 1)**.

**Recall tells us:**

> Out of all customers who actually churned, how many were correctly identified by the model?

---

## Initial Problem: Low Recall

After training the initial model, the Recall for **Class 1 (Churn)** was approximately:

**Recall = 0.41**

This means the model was identifying only about **41% of the customers who actually churned**, while missing a large proportion of potential churners.

After investigating the dataset, I found an important issue:

### Class Imbalance

The dataset contained significantly more non-churn customers than churn customers.

Because of this imbalance, the model was biased toward predicting the majority class (**Class 0 — Non-Churn**), resulting in poor recall for the minority class (**Class 1 — Churn**).

---

## 🛠️ Handling Class Imbalance

To improve the model's ability to detect churners, I addressed the class imbalance in the training data.

After handling the imbalance, I retrained and evaluated the model.

This resulted in better detection of customers belonging to the churn class and improved **Recall for Class 1**.

---

## Model Improvement

### Before Handling Class Imbalance

- Model performed relatively well on the majority class.
- Recall for churn customers was only **0.41**.
- A large number of actual churners were being missed.

### After Handling Class Imbalance

- The model became more sensitive to the churn class.
- Recall for **Class 1** improved.
- The model was able to identify a larger proportion of customers who were actually going to churn.

This improvement is especially important from a business perspective because identifying more potential churners gives the company an opportunity to take retention actions such as:

- Personalized offers
- Discounts
- Customer support interventions
- Loyalty programs
- Targeted retention campaigns

---

## Key Learning

This project demonstrates why **accuracy alone is not always the best metric for evaluating a classification model**.

The appropriate evaluation metric depends on the business problem.

For customer churn prediction, missing an actual churner can be more costly than incorrectly flagging a non-churn customer as a potential churner.

Therefore, **Recall for the churn class** was treated as one of the most important evaluation metrics in this project.
