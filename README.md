
# MSCS-634 Assignment 2: Exploratory Data Analysis on Heart Disease Dataset

This project is part of the Advanced Big Data and Data Mining (MSCS-634) course. It focuses on performing data preprocessing and exploratory data analysis (EDA) on a heart disease dataset.

---


## Dataset Summary

We used the **UCI Heart Disease dataset**, which contains **920 patient records**. Each record includes medical attributes such as age, sex, chest pain type (`cp`), fasting blood sugar (`fbs`), cholesterol (`chol`), maximum heart rate (`thalach`), and more. The goal is to predict whether a patient is likely to have heart disease (`num`: 0 = No, 1 = Yes).

### Key Attributes
- `age`, `sex`, `cp`, `fbs`, `restecg`, `thalach`, `chol`, `slope`, `thal`, `exang`, `ca`, `oldpeak`
- `num`: Target variable, indicating heart disease presence.

---


## Key Insights from EDA

- **Middle-aged and senior groups** show higher prevalence of heart disease.
- **Cholesterol** and **resting blood pressure** distributions contain noticeable outliers.
- Positive correlation seen between `cp`, `thal`, and heart disease.
- **Males** were more frequently diagnosed with heart disease in this dataset.
- `thalach` and `oldpeak` showed correlation with heart disease presence.

---

## Steps Taken in Data Cleaning

1. **Initial inspection**: Checked data types, missing values, and statistical summaries.
2. **Missing value handling**:
   - Categorical columns: imputed using **mode**.
   - Numerical columns: imputed using **median**.
   - Dropped `ca` column due to **excessive missing values**.
3. **Binary encoding**:
   - Converted `sex`, `fbs`, `exang` to 1s and 0s.
4. **Simplified target**: Mapped all heart disease types (num > 0) to `1` for binary classification.

---

## Steps in Exploration (EDA)

- **Distribution plots**: Histograms and boxplots for outlier detection.
- **Target variable**: Countplots to show balance of heart disease cases.
- **Violin plots**: Showed feature distributions across `num` classes.
- **Correlation heatmap**: Highlighted feature relationships.
- **Grouped analysis**: Age-grouped analysis, categorical split by disease presence.

---

## Challenges Encountered & Solutions

| Challenge | Solution |
|----------|----------|
| Many features had missing values | Used safe imputation (mode/median), dropped only high-missing columns |
| Some features were binary strings ('True', 'False') | Converted to numeric binary manually |
| Target variable had multiple heart disease types (1-4) | Simplified to binary classification problem |
| Imbalanced class distributions | Used visualizations (countplots) to validate model readiness |

## Project Structure

```
.
├── heart_disease_data.csv       # Input dataset
├── MSCS-634-Assignment2.ipynb   # Main Jupyter Notebook with all code and analysis
├── screenshots/                 # Folder containing visual outputs
│   ├── somefile.png
│   ├── somefile.png
└── README.md                    # This file
```

---

## Requirements

You can install all required libraries via pip:

```bash
pip install pandas numpy matplotlib seaborn
```

Or using a requirements.txt:

```bash
pip install -r requirements.txt
```

---

## How to Run the Project

1. Clone this repository.
2. Ensure you have Python 3.8+ and Jupyter Notebook installed. If not:

```bash
pip install notebook
```

3. Launch Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `MSCS-634-Assignment2.ipynb` and run each cell step-by-step.

---

## 📊 Key Tasks Performed

- Missing value handling (safe mode)
- Categorical encoding
- Numeric imputation (mean/mode)
- Data visualization:
  - Histogram of numerical features
  - Boxplots for outlier detection
  - Correlation heatmaps (before and after cleaning)
  - Target class distribution
  - Age group vs. Heart Disease analysis
  - Categorical feature analysis vs. Heart Disease

---

## 📸 Additional EDA Screenshots

All visualizations are saved under the `screenshots/` folder for reference and submission.

---

## 🧠 Author

Sandesh Pokharel  
MSCS Student, University of the Cumberlands  
Course: Advanced Big Data and Data Mining (MSCS-634)

---

## ✅ Final Note

This project demonstrates a structured and clean approach to real-world medical dataset analysis and will serve as a foundation for further modeling and predictions.

