# Deliverable 3 – Advanced Data Mining Project

This project focuses on applying advanced data mining techniques to a cleaned heart disease dataset. The major objectives include classification, clustering, and association rule mining, followed by interpretation and discussion of practical relevance.

---

## 🔍 Classification Insights

We developed and evaluated four classification models:
- **Decision Tree**
- **k-Nearest Neighbors (k-NN)**
- **Naïve Bayes**
- **Support Vector Machine (SVM)**

Each model was assessed using accuracy, F1-score, confusion matrix, and ROC curve. After evaluating base models, we performed **hyperparameter tuning** using `GridSearchCV` for Decision Tree, k-NN, and SVM to improve performance.

**Key Results:**
- k-NN with tuned parameters yielded the best accuracy (~85%) and balanced performance.
- SVM showed strong boundary formation even before tuning.
- Hyperparameter tuning noticeably improved F1-scores for all selected models.

---

## 🔗 Clustering Insights

We applied **two clustering techniques**:
- **K-Means Clustering** (with Elbow Method to determine optimal clusters)
- **Hierarchical Clustering** (using dendrogram to visualize linkage and cluster structure)

**Key Observations:**
- K-Means identified 2–3 meaningful clusters indicating different patient risk profiles.
- Hierarchical clustering gave deeper insights into subgroup relationships among patients.

Both clustering results were visualized using 2D PCA-reduced feature plots.

---

## 🧠 Pattern Mining Insights

We implemented **association rule mining** using the Apriori algorithm:
- Frequent itemsets were generated based on conditions like `chest pain type`, `exercise induced angina`, and `fasting blood sugar`.
- Rules such as `chest pain type 4 → heart disease presence` with high confidence provided meaningful interpretations.

These insights help uncover **non-obvious patterns** and potential red flags in patient symptoms.

---

## 🌍 Practical Relevance

- The classification models can assist healthcare professionals in predicting heart disease risk more accurately.
- Clustering helps stratify patients into groups based on symptom severity, enabling tailored treatment plans.
- Association rules reveal symptom combinations that frequently occur together, potentially aiding early diagnosis and intervention strategies.

---

## ⚠️ Challenges & Resolutions

1. **Categorical Variables Handling:**
   - Several models required numerical input, so we applied one-hot encoding to categorical features.

2. **Warnings in Naïve Bayes:**
   - Encountered `RuntimeWarning: divide by zero` during GaussianNB training, which was acknowledged and handled by ignoring constant features.

3. **Clustering Interpretation:**
   - High-dimensionality posed challenges for visualization; we used PCA for dimensionality reduction.

4. **Apriori Algorithm Performance:**
   - Running Apriori on the full dataset was slow. We reduced the feature set and focused on high-impact variables to improve performance.

---

