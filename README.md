# Bankruptcy Prediction Using Financial Ratios

## Overview

This project builds and interprets machine learning models to predict corporate bankruptcy using financial ratios. The workflow includes data preparation, model training, performance evaluation, and global interpretation using both model-specific and model-agnostic SHAP explainers. All analysis and code follow best practices for transparency and actionable insights.

---

## Dataset

- **Source:** `bankruptcy.csv`  
- **Samples:** 132 firms (manufacturing and retail sectors)
- **Target:**  
  - `D = 0`: Bankrupt firm  
  - `D = 1`: Healthy firm
- **Features:** 24 financial ratios (e.g., CASH/CURDEBT, ASSETS/DEBTS, WCFO/DEBTS, INC/ASSETS, etc.)

---

## Project Workflow

1. **Data Preparation:**  
   - Load data, split into training and test sets.

2. **Model Building:**  
   - Train Decision Tree and Random Forest classifiers.
   - Use cross-validation and grid search for hyperparameter tuning.

3. **Performance Evaluation:**  
   - Evaluate using accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrix.

4. **Global Interpretation:**  
   - Feature importances using built-in model attributes.
   - SHAP analysis using TreeExplainer (for tree models) and KernelExplainer (model-agnostic).
   - Compare consistency across interpretation methods.

5. **Business Interpretation and Recommendations:**  
   - Translate model findings into clear business insights.
   - Provide actionable recommendations based on top predictive financial ratios.

---

## Key Findings

- The models consistently identify leverage, cash flow, and profitability ratios as the most critical predictors of bankruptcy.
- Top features include:
    - **R21 (Assets/Debts)**
    - **R18 (Income + Depreciation/Debts)**
    - **R24 (Working Capital from Ops/Debts)**
    - **R15 (Income/Debts)**
    - **R14 (Income/Assets)**

- Results are robust across both TreeExplainer and KernelExplainer SHAP methods.

---

## Business Interpretation

- The model’s predictions are grounded in familiar financial signals, primarily leverage, operational cash flow, and profitability.
- This consistency and transparency enable stakeholders to trust and act on the model’s outputs.

---

## Recommendations

1. **Monitor and manage leverage ratios.**
2. **Enhance operational cash flow through improved working capital management.**
3. **Boost profitability and asset utilization.**
4. **Continuously track key financial ratios using real-time dashboards.**
5. **Integrate model insights into financial strategy and risk management.**
6. **Consult financial experts for persistent weaknesses in critical ratios.**

---

## Getting Started

### Requirements

- Python 3.x
- pandas
- scikit-learn
- matplotlib
- shap

### How to Run

1. Place `bankruptcy.csv` in the working directory.
2. Open the main notebook or script.
3. Follow the workflow cells, modifying parameters if desired.
4. Visualizations and interpretation results will appear inline.

---

## Credits

- Project based on accounting ratios case study and data provided in course materials.
- Analysis and code by Aurosikha Mohanty.
