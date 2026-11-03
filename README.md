Project Overview
This practical work evaluates various regression algorithms and model evaluation techniques on a dataset mapping study hours to exam scores. The project focuses on demonstrating underfitting, overfitting, regularized regression techniques (Ridge, Lasso), and cross-validation performance evaluation.

Objectives
Build and evaluate standard Linear Regression and Polynomial Regression models.
Analyze the impact of polynomial degrees on model bias vs. variance.
Validate models using Leave-One-Out Cross-Validation (LOOCV).
Apply regularization techniques (Ridge and Lasso) to mitigate overfitting.
Compare classical linear models against non-linear estimators (Decision Trees, Random Forests, SVR, KNN).
Installation
Ensure you have the required dependencies installed:

pip install numpy pandas matplotlib scikit-learn
Methodology & Execution Flow
1. Data Exploration & Initial Modeling
Initial scatter plot visualization of raw data.
Baseline fitting using Simple Linear Regression (
d
=
1
), Polynomial Regression (
d
=
2
), and Polynomial Regression (
d
=
3
).
2. Model Evaluation Metrics
Models are evaluated on:

RMSE (Root Mean Squared Error): 
RMSE
=
1
n
∑
i
=
1
n
(
y
i
−
y
^
i
)
2
R
2
 Score (Coefficient of Determination)
3. Overfitting Analysis & LOOCV
Evaluation of polynomial degrees 
d
∈
1
,
2
,
3
,
5
,
9
.
Implementation of Leave-One-Out Cross-Validation (LOOCV) combined with StandardScaler inside a Pipeline to measure true generalization error and identify overfitting at higher degrees (e.g., 
d
=
5
,
9
).
4. Regularized Models
Applied regularization to high-degree (
d
=
5
) polynomial pipelines across hyperparameter choices 
α
∈
0.01
,
0.1
,
1
,
10
:

Ridge Regression (
L
2
 Regularization)
Lasso Regression (
L
1
 Regularization)
5. Benchmark with Alternative Regressors
Compared polynomial linear pipelines against standard machine learning regressors via LOOCV:

Decision Tree Regressor
Random Forest Regressor
Support Vector Regressor (SVR)
K-Nearest Neighbors Regressor (KNN)
Results Summary
Linear Models (
d
=
1
,
d
=
3
): Provide strong linear trends with low cross-validation error due to the highly linear nature of the data.
High-Degree Polynomials (
d
≥
5
): Show low training error but increased LOOCV RMSE without regularization (overfitting).
Ridge & Lasso: Successfully constrain coefficients of higher-degree polynomials to control model complexity.
