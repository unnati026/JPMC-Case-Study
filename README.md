# CCB Risk Modelling: A Data-Driven Approach to Fair Lending Practices

This repository contains the implementation, analysis, and outcomes of a risk modelling project conducted as part of the **JP Morgan Chase & Co. CCB Risk Modelling Mentorship Programme**. The objective was to develop an unbiased, data-driven decision-making model to evaluate loan applications while ensuring compliance with the **Fair Housing Act (FHA)** and **Equal Credit Opportunity Act (ECOA)**.

---

## Project Overview

The project aims to establish effective screening criteria for loan approvals, ensuring fair and non-discriminatory lending practices. This includes:
- Analysing a dataset of 42,534 loan accounts (2007–2011).
- Identifying factors affecting customer risk profiles.
- Developing machine learning models to classify applicants as `Good` or `Bad` based on pre-loan data.
- Ensuring the model is free of unintended bias using SHAP (SHapley Additive Explanations).

---

## Key Features

- **Data Pre-Processing**:
  - Addressed missing values, scaled continuous variables, and one-hot encoded categorical variables.
  - Removed sensitive attributes such as `race`, `gender`, and `address_state` to ensure compliance with anti-discrimination laws.

- **Exploratory Data Analysis (EDA)**:
  - Studied the impact of demographic, financial, and historical attributes on loan status.
  - Created visualisations to understand correlations and distributions.

- **Model Development**:
  - Implemented Logistic Regression, Decision Tree, Random Forest, XGBoost, and Ensemble models.
  - Handled class imbalance using SMOTE (Synthetic Minority Oversampling Technique).
  - Ensured model generalisability by avoiding data leakage from post-loan approval features.

- **Bias Detection and Mitigation**:
  - Conducted statistical tests to detect unintentional bias.
  - Used SHAP to ensure model transparency and compliance with regulatory guidelines.

---

## Results

- **Model Accuracy**:
  - Best performance achieved with the XGBoost model after mitigating data leakage.
  - Validation metrics demonstrate high precision and recall for `Bad` customers, aligning with the goal of minimising risky loans.

- **Insights from SHAP**:
  - Key predictors include `fico_score`, `loan-to-income ratio`, and `number of recent inquiries`.
  - SHAP plots provided interpretable insights into individual loan application decisions.

---

## Files in Repository

- **`Case_study_problem_statement.pdf`**: PDF containing the problem statement for this project.
- **`loan_dataset_final.csv`**: The given dataset consisting of around 42,000 accounts, with several features.
- **`data_dictionary.xlsx`**: Excel sheet giving the description of each column in the dataset.
- **`final (2).ipynb`**: Jupyter notebook with code for data preprocessing, EDA, and modelling.
- **`Output.xlsx`**: Output excel sheet with the loans marked as approved or rejected.
- **`Report2.pdf`**: The report for explaining the methodolgy for arriving at the presented conclusions.
- **`JPMC CCB Risk Modelling Case Study.pptx`**: The Powerpoint Presentation, explaining the process.
- **`README.md`**: This README file.

---

## Acknowledgements

This project was developed as part of the **JP Morgan Chase & Co. CCB Risk Modelling Mentorship Programme**. Special thanks to the mentors and team for their guidance.
