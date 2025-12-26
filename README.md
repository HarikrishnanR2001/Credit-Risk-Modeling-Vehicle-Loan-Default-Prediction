Loan Default Prediction Using Machine Learning

**Project Overview**
This repository contains an end-to-end machine learning project focused on predicting loan default risk. The objective is to identify high-risk borrowers using supervised learning techniques while addressing challenges associated with imbalanced classification. The project emphasizes appropriate evaluation metrics, particularly Precision–Recall AUC, rather than accuracy.

**Dataset**
The project uses a structured loan dataset consisting of borrower, loan, and branch-level attributes. A data dictionary is provided to describe feature definitions. The target variable is a binary indicator of loan default.

**Methodology**
The workflow begins with extensive data preprocessing and feature engineering. Irrelevant and high-cardinality identifier columns are removed. Missing values are handled systematically. Numeric features are extracted from tenure-based fields. Categorical variables are encoded using one-hot encoding. Branch-level historical default rates are computed in a leakage-safe manner and incorporated as risk indicators.

Class imbalance is addressed through stratified train-test splitting and model-specific weighting strategies. No resampling is performed on the test set to ensure unbiased evaluation.

**Models**
Multiple models are trained and evaluated, including Logistic Regression, Decision Tree, Random Forest, and XGBoost. Logistic Regression serves as a baseline model, while tree-based ensemble methods capture nonlinear relationships and feature interactions.

**Evaluation**
Models are evaluated using Precision–Recall AUC, F1-score, Recall, and Precision. Precision–Recall AUC is used as the primary model selection criterion due to its suitability for imbalanced classification. Decision thresholds are tuned separately to achieve business-appropriate trade-offs between false positives and false negatives.

**Results**
XGBoost achieves the highest Precision–Recall AUC, significantly outperforming the baseline and other models. This indicates superior ranking ability in identifying defaulters, even though overall accuracy remains moderate. The results demonstrate that accuracy alone is insufficient for evaluating credit risk models.

**Conclusion**
This project demonstrates a robust and industry-aligned approach to loan default prediction. By focusing on proper evaluation metrics, imbalance handling, and risk-based feature engineering, the final model provides meaningful insights for credit risk assessment and decision-makin
