# Predicting Student Performance in Nepal: Analysis & Modeling

**Author:** Manish Kumar Tiwari  
**Date:** 26 December 2025

---

## Title
Predicting Student Performance in Nepalese Schools Using Machine Learning and Exploratory Data Analysis

## Abstract 
This study investigates factors influencing student academic performance and develops predictive models for both pass/fail classification and continuous score regression. Using a publicly available student performance dataset as a proxy for Nepalese student data, we perform comprehensive data cleaning, exploratory data analysis, and feature engineering to extract meaningful patterns. We apply logistic regression and XGBoost Classifier to predict pass/fail outcomes and linear regression alongside XGBoost Regressor to predict average exam scores. Model performance is evaluated using confusion matrices, precision, recall, F1-score for classification, and mean squared error (MSE) and R² for regression. Statistical summaries (mean, median, mode, variance, standard deviation, skewness) and visualizations (histograms, boxplots, scatter plots, correlation heatmap) are provided to support interpretations. The results identify key predictors such as study time proxies, parental education, and test preparation, offering actionable recommendations for educators and policymakers in Nepal. Limitations and suggestions for future work — including collecting localized Nepalese datasets, incorporating geospatial and socioeconomic variables, and deploying a user-friendly dashboard — are discussed.

## Keywords
Nepal, Education, Machine Learning, Student Performance, XGBoost

## Introduction, Aims, and Objectives
### Introduction
Improving student outcomes is a priority for Nepal's education system. Predictive models can help identify at-risk students and guide interventions. This project leverages machine learning and EDA to analyze determinants of student success and build models that can assist teachers and administrators.

### Aim
To develop robust classification and regression models to predict student pass/fail status and final exam scores, while demonstrating data science workflow and visualization techniques.

### Objectives
1. Collect and preprocess student performance data relevant to Nepalese context.
2. Perform exploratory data analysis to uncover relationships and distributional properties.
3. Build and compare logistic regression and XGBoost classifier for pass/fail prediction.
4. Build and compare linear regression and XGBoost regressor for score prediction.
5. Evaluate model performance and discuss implications for educational policy.

## Methodology and Data Preprocessing
### Data Source
Primary dataset used: "StudentsPerformance.csv" (Kaggle: Students Performance in Exams) — used as a proxy dataset; for final submission, replace with any local Nepalese dataset if available and state the source.

### Tools and Libraries
Python 3.x, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, Jupyter Notebook.

### Data Cleaning Steps
- Inspect for missing values and duplicates; report counts.
- Encode categorical variables (Label Encoding / One-Hot where appropriate).
- Create derived features: `average_score`, `pass_fail` (threshold = 40).
- Scale numeric features when required for linear models.
- Handle outliers using IQR method and report removed/adjusted rows.

### Feature Engineering
- Aggregate subject scores into an average score.
- Convert parental education and test preparation into ordinal encodings where justified.
- Create interaction features (e.g., parental_education * test_prep) and rationalize their inclusion.

## Analysis, Results, and Discussion
### Descriptive Statistics
Provide table of mean, median, mode, variance, std dev, skewness for `math score`, `reading score`, `writing score`, and `average_score`.

### Visualizations
- Correlation heatmap (Pearson) showing relationships among features.
- Boxplots for subject scores (IQR) indicating outliers.
- Histograms + KDE for score distributions.
- Scatter plot: actual vs predicted for regression models.
- Confusion matrix heatmaps for classification results.

### Modeling Results
- **Classification (Pass/Fail):** Logistic Regression and XGBoost Classifier
  - Present confusion matrices, precision, recall, F1-score, and accuracy.
  - Discuss class balance and implications for threshold selection.

- **Regression (Average Score):** Linear Regression and XGBoost Regressor
  - Present MSE and R² for both models.
  - Show residual analysis and discuss model fit.



### Discussion
Interpret what features were most predictive (feature importance from XGBoost), how model errors manifest (e.g., systematic underprediction for low-scoring students), and real-world implications for interventions (e.g., support for students with low parental education level).

## Conclusion and Future Work
Summarize the main results; recommend targeted tutoring, improved test preparation programs, and collection of localized Nepalese educational data. Suggest future directions: longitudinal studies, integration of attendance and socioeconomic data, and deployment as an educational dashboard.

## References
- Students Performance in Exams dataset — Kaggle.
- Scikit-learn documentation: https://scikit-learn.org
- XGBoost documentation: https://xgboost.readthedocs.io


*Notes for Academic Integrity*
- This report and accompanying notebook are original and provided to help you learn. Do not submit text verbatim without running the analysis yourself and adding personal interpretation. Replace placeholders (author name, institution) and include proper local data sources when available.
