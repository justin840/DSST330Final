# DSST330Final

---
title: Understanding and Implementing Poisson Regression

author: Your Name

date: March 31, 2024

output: pdf_document
---

# Understanding and Implementing Poisson Regression

## 1. General Motivation

- Poisson Regression is a statistical method used for analyzing count data.
- It models the relationship between predictors and the expected count of occurrences.
- Useful for data with a Poisson distribution, like customer arrivals or accident counts.

## 2. Mathematical Description

- Response variable \( Y \) follows a Poisson distribution with mean \( \lambda \).
- Model: \( \log(\lambda) = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \ldots + \beta_p x_p \).
- Link function: natural logarithm.

## 3. Authoritative References

- Agresti, A. (2002). Categorical data analysis.
- Cameron, A. C., & Trivedi, P. K. (2013). Regression analysis of count data.
- Hilbe, J. M. (2011). Negative binomial regression.

## 4. R Package: glm()

- Use the `glm()` function in R to fit Poisson Regression models.
- Example:
  ```r
  # Fit Poisson Regression model
  model <- glm(counts ~ predictor1 + predictor2, data = data, family = "poisson")
