# 🫀 Heart Disease Prediction – Deliverable 2: Regression Modeling & Evaluation

This README documents the work done in **Deliverable 2** for **MSCS-634: Advanced Big Data and Data Mining**.  
We built and evaluated multiple regression models to predict heart disease using the cleaned dataset from Deliverable 1.

---

## 📦 Dataset Summary

We reused the **cleaned Heart Disease dataset** prepared in Deliverable 1.  
- **Records:** 920  
- **Features:** 17 after one-hot encoding categorical variables  
- **Target:** `num` (binary – presence or absence of heart disease)

Key features include: `age`, `sex`, `cp` (chest pain type), `chol`, `thalach`, `thal`, and others.

---

## 🛠️ Steps Taken in Deliverable 2

### 1. Data Preparation
- Loaded the cleaned dataset from Deliverable 1.
- Applied **StandardScaler** to normalize the features (mean=0, std=1) for better convergence of models.

### 2. Model Building
- Implemented **three regression models**:
  1. Logistic Regression (baseline)
  2. Ridge Regression (L2 regularization)
  3. Lasso Regression (L1 regularization)

### 3. Hyperparameter Tuning
- Used **GridSearchCV** to optimize the regularization parameter `alpha` for Ridge and Lasso models:
  - Ridge: best alpha = **50**
  - Lasso: best alpha = **0.001**

### 4. Model Evaluation
- Evaluated each model using metrics:
  - **R²** (coefficient of determination)
  - **MSE** (Mean Squared Error)
  - **RMSE** (Root Mean Squared Error)
- Performed **5-fold cross-validation** to assess generalization performance.

### 5. Feature Importance
- Visualized coefficients for Ridge and Lasso models to identify the most influential features.

---

## 🔍 Key Insights

1. **Model Performance**
   - Logistic Regression had the lowest predictive power (Test R² = 0.34).
   - Tuned Ridge and Lasso significantly outperformed Logistic Regression:
     - Ridge: Test R² = **0.50**, CV Mean R² = **0.42**
     - Lasso: Test R² = **0.49**, CV Mean R² = **0.42**

2. **Feature Insights**
   - Features like **chest pain type (cp_atypical angina)**, **age**, and **sex** were the strongest predictors.
   - Lasso shrunk some coefficients to zero, helping with feature selection and model simplification.

3. **Best Model**
   - **Ridge Regression** is the best-performing model based on error metrics and stability.
   - **Lasso Regression** is a strong alternative when simpler models with fewer features are desired.

---

## 🧗 Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Selecting the best regularization strength (`alpha`) | Used GridSearchCV for hyperparameter tuning |
| Ensuring model convergence for Logistic Regression | Applied StandardScaler to normalize feature scales |
| Interpretability of features in high-dimensional space | Visualized coefficients for Ridge and Lasso models |

---

## ⚙️ Setup Instructions

### Clone the Repository
```bash
git clone <repository_url>
cd MSCS-634-Project
git checkout feature/deliverable2
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Run the Notebook
Launch Jupyter Notebook and open `MSCS-634-Project-Deliverable2.ipynb`.

---

## 📂 Files Included

- `MSCS-634-Project-Deliverable2.ipynb`: Jupyter Notebook with all analysis and models.
- `README_deliverable2.md`: This file (summary of Deliverable 2).
- `requirements.txt`: Dependencies used for the project.
- `MSCS-634-Project-Deliverable2-report.pdf`: Final report with screenshots and detailed explanations.

---

## Author
**Sandesh Pokharel**  
University of the Cumberlands | MSCS-634
