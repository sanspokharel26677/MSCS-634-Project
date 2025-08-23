
# Heart Disease Risk Analysis Project (MSCS-634)

## 📊 Dataset Summary

We used the **Heart Disease UCI dataset**, which contains patient-level health information to predict the presence of heart disease. This dataset includes attributes like age, gender, cholesterol levels, chest pain type, fasting blood sugar, resting ECG results, exercise-induced angina, and more. It is widely used in clinical prediction and medical research due to its completeness and relevance.

Dataset Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+Disease)

---

## 🔍 Project Objectives

This project aims to:
- Perform exploratory data analysis (EDA) to uncover trends and anomalies.
- Build predictive models using regression and classification algorithms.
- Apply clustering to group similar patient profiles.
- Use association rule mining to identify frequent patterns among risk factors.
- Provide practical recommendations and address ethical considerations like fairness and data bias.

---

## 🔧 Project Steps

1. **Data Preprocessing:**
   - Handled missing/null values.
   - Renamed and standardized column names.
   - Converted categorical variables and cleaned inconsistencies.

2. **Exploratory Data Analysis (EDA):**
   - Visualized feature distributions and correlations.
   - Identified trends such as higher heart disease risk with increasing age and cholesterol.

3. **Feature Engineering:**
   - Encoded categorical variables.
   - Created new features like “RiskGroup” based on age and cholesterol thresholds.

4. **Regression Analysis:**
   - Built a linear regression model to estimate heart disease risk scores.

5. **Classification Models:**
   - Applied Logistic Regression, Decision Trees, and Random Forest.
   - Evaluated using accuracy, precision, recall, and confusion matrices.

6. **Clustering (K-Means):**
   - Grouped patients based on health metrics.
   - Visualized clusters to identify high-risk groups.

7. **Association Rule Mining:**
   - Discovered frequent itemsets and rule-based patterns like “High Cholesterol + Chest Pain ➝ Heart Disease”.

8. **Ethical Considerations:**
   - Addressed dataset biases, ensured no personally identifiable information was used, and acknowledged fairness limitations.

---

## 🧠 Major Findings

- **Age**, **cholesterol**, and **chest pain type** are strong indicators of heart disease.
- Random Forest outperformed other models in terms of prediction accuracy.
- Clustering revealed that high-risk patients form distinct, identifiable groups.
- Association rules suggest actionable insights for early screening based on co-occurring conditions.
- Ethical concerns such as demographic imbalance must be considered when generalizing these models.

---


