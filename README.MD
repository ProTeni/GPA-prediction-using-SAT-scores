![Alt Text](./Images/istockphoto-1146185198-612x612.jpg)


# Predicting University GPA from SAT Scores — Simple Linear Regression

**A foundational regression project: estimating graduating GPA from SAT score, built three
different ways to compare modelling approaches.**

> A clean simple-linear-regression study using statsmodels, NumPy polyfit, and scikit-learn to
> predict university GPA from a single predictor. A demonstration of regression fundamentals and
> fluency across the standard Python modelling tools.

---

## Business problem
A university wants 70% of its graduates to achieve high GPAs and is exploring whether SAT score
at admission can help identify prospective students likely to perform well academically. The
task: quantify the SAT–GPA relationship and build a model to predict GPA from SAT.

## Dataset
100 student records with two fields — SAT score and final university GPA. Source: course dataset.

## What I did
- **EDA:** summary statistics, distribution checks, and a correlation check (SAT–GPA ≈ 0.62,
  a moderate positive relationship)
- **Visualisation:** scatter and regression plots to show the trend and slope
- **Modelled three ways** to compare tooling:
  - **statsmodels OLS** — full statistical summary (coefficients, p-values, R²)
  - **NumPy polyfit** — quick coefficient/intercept extraction
  - **scikit-learn LinearRegression** — train/test split, prediction, evaluation
- **Evaluation:** residual analysis, MAE, RMSE
- **Tested non-linearity:** added polynomial terms (SAT², SAT³) to check for improvement

## Results — and an honest read
SAT score alone is a **moderate** predictor of GPA (correlation ≈ 0.62). The model captures a
real trend but leaves a lot of variance unexplained — unsurprising, since GPA depends on far
more than a single admissions test. The polynomial terms didn't meaningfully improve the fit,
confirming the relationship is essentially linear and the limiting factor is the single feature,
not the model.

## Key takeaway
SAT is a useful but partial signal for academic success — valuable as one input, not a sole basis
for prediction. A stronger model would add features such as prior academic record, attendance,
and engagement.

## Tools
Python (pandas, NumPy, seaborn, matplotlib) · statsmodels · scikit-learn

---

*Foundational regression exercise (Feb 2024). Planned upgrade: add multiple predictors beyond
SAT score to raise explanatory power.*

