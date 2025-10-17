# DA5401 — Assignment 6: Imputation via Regression for Missing Data  

**Student Name:** Praveen  
**Roll Number:** MM22B014  
**Course Code:** DA5401  
**Assignment:** A6 — Handling Missing Values Using Regression-Based Imputation  

---

## ▶️ How to Run

1. Open the notebook **`DA5401_Assignment6_MM22B014.ipynb`** in **Google Colab** or Jupyter Notebook.  
2. Ensure that the dataset (`UCI_Credit_Card.csv` or similar) is placed in the working directory.  
3. Run all cells sequentially to reproduce the imputation, modeling, and evaluation results.  

---

## 📌 Summary of Work

- Explored **missing values in key numerical columns** of a financial dataset (e.g., `AGE`).  
- Implemented **multiple imputation strategies** to handle missing entries:  
  1. **Median Imputation** — robust baseline method resistant to outliers.  
  2. **Linear Regression Imputation** — predicts missing values based on relationships with other features.  
  3. **KNN Regression Imputation** — estimates missing values using nearest neighbors in feature space.  
  4. **Listwise Deletion** — removed all rows containing missing values for comparison.  
- Evaluated the impact of imputation on **predictive modeling** using:  
  - **Logistic Regression classifier** for default prediction.  
  - Metrics: Accuracy, Precision, Recall, F1-Score (especially for minority class).  
- Compared the **effectiveness of different imputation methods** in preserving data integrity and predictive performance.  
- Analyzed **trade-offs between dataset retention and model quality**, focusing on minority-class detection.  

---

## 🔎 Key Findings

- **Median Imputation:**  
  - Simple, robust to extreme values.  
  - Maintains dataset size, performs reasonably well as a baseline.  

- **Linear Regression Imputation:**  
  - Achieved the **highest F1-score**, indicating improved detection of defaulters.  
  - Effective when missing features have approximate linear relationships with other predictors.  

- **KNN Regression Imputation:**  
  - Slightly lower F1 than linear regression but preserves dataset structure.  
  - Sensitive to local noise and feature scaling, which may affect performance.  

- **Listwise Deletion:**  
  - Removes missing-value rows, resulting in a smaller dataset.  
  - Shows higher accuracy due to majority-class bias but suffers in recall and F1-score for the minority class.  

- **Overall Insight:**  
  - Regression-based imputation is recommended for features with missing values that correlate with other features.  
  - Balances **data retention** and **predictive accuracy**, improving model reliability for minority-class detection.  

---
