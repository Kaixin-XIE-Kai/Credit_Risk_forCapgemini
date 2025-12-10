# Credit_Risk_forCapgemini# Credit Risk Scoring Engine: Ethical & Compliant Approach

## 📌 Project Overview
End-to-end development of a credit default prediction model for a retail bank. 
Focuses not just on accuracy, but on **profitability**, **explainability**, and **regulatory compliance (ECOA)**.

## 🚀 Key Features
* **Champion-Challenger Modeling**: Benchmarked XGBoost vs. CatBoost. Selected CatBoost for higher Recall (identifying 2% more defaulters).
* **Strategic Feature Engineering**: 
    * **Leakage Prevention**: Excluded `grade` and `int_rate` to simulate real-world origination.
    * **Compliance**: Removed `zip_code` and `ethnicity` features to prevent Redlining.
* **Business-Centric Evaluation**: Optimized decision thresholds based on **Expected Profit** rather than F1-score.
* **Fairness Audit**: Conducted disparate impact analysis across demographic groups.

## 📂 Repository Structure
* `notebooks/`: Step-by-step analysis consistent with the CRISP-DM methodology.
* `src/`: Production-ready python modules.
* `config.yaml`: Centralized configuration for feature governance.

## 📊 Results Summary
* **AUC**: 0.72 (Stable across 2018-2020)
* **Fairness**: Model demonstrates compliance with ECOA standards after removing proxy variables.