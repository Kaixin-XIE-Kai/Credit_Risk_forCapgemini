# Credit Default Risk Prediction  
### End-to-End Credit Risk Modeling with Business-Driven Metrics & Fairness Considerations

## 📌 Project Overview

This project aims to build an **end-to-end credit default risk prediction system** for lending decision support, with a strong focus on:

- **Business-driven decision metrics** (Expected Profit)  
- **Risk-sensitive modeling** with emphasis on **Recall**  
- **Regulatory and fairness considerations** in credit scoring  
- **Model interpretability** for real-world deployment  
- **Robust and reproducible data science pipeline**

The project is designed to reflect a **real consulting use case** in the financial services industry, where predictive performance alone is not sufficient: **explainability, compliance, and business impact** are equally critical.

---

## 🎯 Business Problem

Financial institutions need to decide **whether to grant or reject a loan** based on the probability of default.  
A poor decision can lead to:

- **Financial losses** due to defaulted loans  
- **Opportunity costs** from rejecting good customers  
- **Regulatory and reputational risks** due to biased or non-compliant models  

**Objective:**  
Build a credit risk model that **maximizes expected profit** while maintaining **high recall** to minimize missed defaults and ensuring **fairness and regulatory compliance**.

---

## 📊 Dataset Description

- Historical loan application data  
- Target variable: **Default (1) / No Default (0)**  
- Mix of numerical and categorical features  
- Imbalanced classes (typical in credit risk datasets)

### Data Challenges Addressed
- Class imbalance  
- Potential proxy variables for sensitive attributes  
- Risk of data leakage  
- Need for explainability  

---

## 🧠 Methodology

### 1. Exploratory Data Analysis (EDA)

- Analysis of default rate and class imbalance  
- Distribution and correlation analysis of key features  
- Identification of potential proxy variables (e.g. ZIP code–related information)  
- Detection of missing values and data quality issues  

---

### 2. Feature Engineering & Compliance

To align with **credit scoring regulations and fairness principles**:

- Removed or carefully evaluated features that could act as **proxies for sensitive attributes** (e.g. geographical indicators)  
- Applied appropriate encoding strategies for categorical variables  
- Ensured no target leakage during preprocessing  

This step reflects **real-world regulatory constraints** faced by financial institutions.

---

### 3. Modeling Strategy

A **Champion–Challenger framework** was adopted:

| Model | Purpose |
|------|--------|
| Logistic Regression | Baseline & interpretability reference |
| XGBoost | High-performance benchmark and final selected model |

Key considerations:  
- Performance vs interpretability trade-off  
- Stability on imbalanced data  
- Suitability for production environments  

---

### 🧠 Evaluation Metrics

This project evaluates models using both **business-oriented metrics** and **standard ML metrics**, reflecting real-world credit risk decision priorities.

#### Standard ML Metrics
- **ROC-AUC**: Measures overall model discrimination  
- **Precision / Recall**: Especially **Recall** is emphasized to minimize the risk of missing defaults  
- **F1-Score**  
- **Confusion Matrix**

#### Business-Oriented Metric
- **Expected Profit Optimization**  
  - Different decision thresholds evaluated  
  - Trade-off between false positives and false negatives analyzed  
  - Optimal threshold selected based on **maximizing expected profit**, while also ensuring **high recall** for default detection  

This approach ensures the model is **both financially beneficial and risk-sensitive**, aligning with practical lending decision-making.

---

### 4. Model Interpretability

To ensure transparency and trust:

- Feature importance analysis  
- Model behavior interpretation using surrogate models  
- Analysis of key drivers behind default predictions  

This step is critical for:  
- Regulatory compliance  
- Stakeholder communication  
- Model governance  

---

### 5. Fairness & Bias Analysis

A fairness audit was conducted to assess whether model predictions disproportionately impact specific groups:

- Comparison of default prediction rates across sub-populations  
- Evaluation of potential indirect discrimination  
- Discussion of mitigation strategies  

This aligns with **ethical AI and financial regulation requirements**.

---

## 📈 Key Results

- Final XGBoost model achieves strong discriminative power (ROC-AUC ≈ 0.71)  
- Business-optimized decision threshold improves expected profit compared to naïve cutoff  
- High recall ensures most defaults are detected  
- Model decisions remain interpretable and aligned with compliance constraints  

---

## 🏗️ Project Structure

