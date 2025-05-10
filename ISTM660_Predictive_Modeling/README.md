# ISTM 660 – Predictive Modeling & Data Translation

**Course:** ISTM 660 – Business Analytics and Intelligence  
**Project:** Predicting Self-Employment from Household Characteristics  
**Tools Used:** Google BigQuery, Python, Tableau  
**Dataset:** CPS Labor Force Survey (10-year span, ~3.4 million rows)

---

## 📊 Project Overview

This project focused on using predictive modeling to understand how household structure and personal circumstances (such as marriage and children) influence an individual's likelihood of being self-employed. The team worked with the Current Population Survey (CPS) data, leveraging Google BigQuery for extraction and Python for modeling and dashboard development. A logistic regression model was built to predict self-employment, and dashboard visualizations were created to assist the Small Business Administration (SBA) in policy-making and resource allocation.

---

## 📏 Report Breakdown

### 1. 📅 Business Problem & Objectives
- **Question:** How do household factors such as marriage, childcare responsibility, and household structure affect self-employment status?
- **Goal:** Help the SBA target potential entrepreneurs for support and policy development.

### 2. 📚 Data Source & Preparation
- Data pulled from CPS over 10 years via BigQuery
- Combined 3.4M+ records with selected fields: `age`, `married`, `children (various age brackets)`, `ownchild`, `hhnum`, `hoh79`, and self-employment indicators
- Cleaned and filtered down to 2.2M records
- Created a `self_employment` target variable by merging `selfemp` and `selfinc`
- Assumptions made:
  - Adults only (age ≥ 18)
  - Child age variables grouped for simplicity

### 3. 📊 Modeling & Evaluation
- **Model Used:** Logistic Regression
- **Performance Metrics:**
  - AUC Score: **0.67** (moderate prediction power)
  - Accuracy: **89.39%** (but heavily class imbalanced)
  - Precision/Recall for self-employed (class 1): poor (Recall = 0.00)
  - Pseudo R-squared: **0.05** (low explanatory power)
- **Insights from Model Coefficients:**
  - **Positive Predictors:** Age, Married, Ownchild
  - **Negative Predictors:** Young children (ch05, ch613, ch1417), Household Head, Household Size
- **SHAP Analysis:** Age had the strongest predictive impact, followed by married and ownchild

### 4. 🎭 Dashboard & Visual Insights
- Built using **Plotly**
- Variable-level analysis (age, marriage, children, household head) with logistic regression overlays and interpretability notes
- Dashboard allows interaction by selecting different predictors
- Self-employment percentages, logistic coefficients, and model accuracy shown live

---

## 🌐 Business Recommendations

For targeting potential entrepreneurs, the SBA should focus on:
- Older individuals (strongest positive correlation with self-employment)
- Married individuals without school-aged children
- Individuals who **own children** (likely over 18 years)
- Avoid over-relying on household head status, which was negatively associated with self-employment

---

### ⚠️ Deficiencies & Next Steps
- **Imbalanced model**: Only 6 true positives out of ~234k possible
- **Data limitations**: CPS variables may not reflect entrepreneurial mindset or intent
- **Suggested fixes:**
  - Try resampling (e.g., SMOTE)
  - Test tree-based models (e.g., Random Forests)
  - Add more behavioral and income-based variables
  - Create interaction terms (e.g., married + children)

---

## 📂 Project Files

| File Name                                  | Description                                |
|--------------------------------------------|--------------------------------------------|
| `Final Data Analysis Report.pdf`           | Detailed write-up and model interpretation |
| `Final Data Analysis Presentation.pdf`     | Slide deck for 20-minute oral presentation |
| `hhdSit_dataCleaning.txt`                  | Python code for data import and cleaning   |
| `hhdSit_logReg.txt`                        | Logistic regression and ROC analysis       |
| `hhdSit_dashboard(runInPrompt).txt`        | Streamlit dashboard implementation         |
| `README.md`                                | This file – documentation overview         |

---

## 📌 Key Takeaways

- Logistic regression revealed clear trends: older, married individuals without school-aged children are more likely to be self-employed
- However, the model lacks precision in predicting self-employed individuals and should be improved for deployment
- Dashboards effectively communicate trends and predictions for policy audiences
- Strong demonstration of end-to-end data science workflow: BigQuery → Python modeling → SHAP interpretability → dashboard
