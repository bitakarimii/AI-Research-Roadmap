# ISLP - Chapter 2: Statistical Learning

**Date:** 2026-11-23

---

# Summary

Chapter 2 introduces the foundations of statistical learning. It explains the difference between prediction and inference, supervised and unsupervised learning, regression and classification, model flexibility, bias-variance trade-off, and model evaluation using training and test error.

---

# Important Definitions

### Statistical Learning

\[
Y = f(X) + \epsilon
\]

- **X:** Predictors / Features / Independent Variables
- **Y:** Response / Dependent Variable
- **f:** Unknown relationship between X and Y
- **ε:** Random error (mean = 0)

---

# Prediction vs Inference

## Prediction

Goal:
Predict future values accurately.

Prediction error consists of:

- Reducible Error
- Irreducible Error

### Reducible Error

Can be reduced by choosing a better learning algorithm.

### Irreducible Error

Cannot be reduced because it comes from random noise (ε).

---

## Inference

Goal:
Understand how predictors affect the response.

Main questions:

- Which predictors are important?
- How does each predictor affect Y?
- Is the relationship linear or nonlinear?

---

# Linear vs Nonlinear Models

### Linear Models

Advantages

- Simple
- Easy to interpret
- Good for inference

Disadvantages

- May underfit complex data

---

### Nonlinear Models

Advantages

- More flexible
- Better prediction

Disadvantages

- Harder to interpret
- Higher risk of overfitting

---

# Parametric vs Non-parametric Methods

## Parametric

- Assume a specific form of f
- Estimate model parameters

Advantages

- Simple
- Interpretable
- Requires less data

Disadvantages

- Poor performance if assumptions are wrong

---

## Non-parametric

- No assumption about f
- Learn directly from data

Advantages

- Flexible
- Can model complex relationships

Disadvantages

- Requires more data
- May overfit

---

# Model Flexibility

As flexibility increases:

- Training Error ↓
- Interpretability ↓
- Variance ↑
- Risk of Overfitting ↑

---

# Supervised vs Unsupervised Learning

## Supervised Learning

Available:

- X
- Y

Goals

- Prediction
- Inference

Examples

- Linear Regression
- Logistic Regression
- SVM
- Boosting

---

## Unsupervised Learning

Available:

- X only

Goal

- Discover hidden patterns

Example

- Clustering

---

## Semi-supervised Learning

- Some samples have labels.
- Some samples do not.

---

# Regression vs Classification

## Regression

Response variable:

- Quantitative

Examples

- House Price
- Income

Method

- Linear Regression

---

## Classification

Response variable:

- Qualitative

Examples

- Spam Detection
- Cancer Diagnosis

Method

- Logistic Regression

---

# Model Evaluation

Mean Squared Error (MSE)

Two important metrics:

- Training MSE
- Test MSE

Goal:

Minimize Test MSE.

Increasing flexibility:

- Training MSE always decreases.
- Test MSE follows a U-shaped curve.

Too simple → Underfitting

Too flexible → Overfitting

When a test set is unavailable:

- Cross Validation can estimate Test Error.

---

# Bias-Variance Trade-off

Expected Test Error consists of:

- Bias²
- Variance
- Irreducible Error

Increasing flexibility:

- Bias ↓
- Variance ↑

Goal:

Find the best balance between Bias and Variance.

---

# K-Nearest Neighbors (KNN)

- Uses the K nearest observations.
- Predicts using the majority class.

Small K

- High flexibility
- Low Bias
- High Variance
- May overfit

Large K

- Low flexibility
- High Bias
- Low Variance
- May underfit

Best K:

The one with the lowest Test Error.

---

# My Understanding

- Training Error is not the real objective.
- The goal is to build models that generalize well to unseen data.
- Model selection always depends on the problem, not on a single "best" algorithm.
- Increasing flexibility improves prediction only up to a certain point; beyond that, overfitting becomes a problem.

---

# Questions

- Why does variance increase as model flexibility increases?
- When should I prefer a parametric model over a non-parametric one?
- How can I choose the optimal value of K in KNN?

---

# Key Takeaways

- Statistical learning has two main goals: prediction and inference.
- Every prediction contains reducible and irreducible error.
- Flexible models usually improve prediction but reduce interpretability.
- Test MSE is more important than Training MSE.
- The Bias-Variance Trade-off is one of the most important concepts in machine learning.
- There is no universally best learning algorithm (No Free Lunch).

---

# References

- ISLP (Introduction to Statistical Learning with Python), Chapter 2
