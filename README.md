
# MSCS-634 Assignment 2: Exploratory Data Analysis on Heart Disease Dataset

This project is part of the Advanced Big Data and Data Mining (MSCS-634) course. It focuses on performing data preprocessing and exploratory data analysis (EDA) on a heart disease dataset.

---

## 📁 Project Structure

```
.
├── heart_disease_data.csv       # Input dataset
├── MSCS-634-Assignment2.ipynb   # Main Jupyter Notebook with all code and analysis
├── screenshots/                 # Folder containing visual outputs
│   ├── missing-value-handling.png
│   ├── final-target-distribution.png
│   ├── age-group-distribution.png
│   ├── categorical-countplots.png
│   └── final-correlation-heatmap.png
└── README.md                    # This file
```

---

## 📦 Requirements

You can install all required libraries via pip:

```bash
pip install pandas numpy matplotlib seaborn
```

Or using a requirements.txt:

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run the Project

1. Clone this repository or download the ZIP file.
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

