🏥 Hospital Readmission Prediction Using Machine Learning

**Author:** Anusha K    
**Dataset:** UCI Diabetes 130-US hospitals (1999–2008)

---

📌 Project Overview

Hospital readmissions, especially among diabetic patients, lead to increased healthcare costs and worse patient outcomes. In this project, we built a machine learning pipeline to predict whether a patient will be readmitted to the hospital. Our final model incorporates **Random Forest**, supported with **SHAP** and **LIME** for interpretability.

---

📊 Dataset Summary

- **Records:** 101,766 diabetic patient encounters  
- **Features:** 50 (demographics, diagnoses, labs, medications, hospital data)  
- **Target:** `readmitted` (1 = Yes, 0 = No)  
- **Source:** [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)

---

🧹 Preprocessing

- Dropped columns with >80% missing values
- Handled "?" and missing data via imputation or removal
- Label encoding for categorical features
- Standardization for numeric features
- Outlier detection using IQR
- Feature engineering: medication change, stay categories

---

🧠 Models Applied

| Model              | Purpose & Highlights                            |
|-------------------|--------------------------------------------------|
| Logistic Regression | Baseline & interpretable model                 |
| Decision Tree       | Rule-based interpretability                    |
| **Random Forest** ✅ | High precision & explainable with SHAP/LIME    |
| Gradient Boosting   | Strong ROC-AUC                                 |
| Neural Network      | Best recall, useful for thorough screening     |

---

🏆 Model Results

- **Best Balanced Model**: Logistic Regression  
  - F1-score: 0.2563 | Recall: 51.6% | AUC: 0.6453  
- **Best Precision**: Random Forest (~70.6%)  
- **Best AUC**: Gradient Boosting (0.6777)  
- **Best Recall**: Neural Network (53.2%)

---

🔍 Explainability with SHAP & LIME

- **SHAP**: Identified key features like number of inpatient visits, insulin usage, hospital time, discharge disposition, etc.
- **LIME**: Visualized individual predictions to support clinical interpretation.

These tools help clinicians understand why predictions are made and trust the model outputs.

---

📈 Evaluation Metrics

- Accuracy  
- Precision & Recall  
- F1-score  
- ROC-AUC  
- Confusion Matrix  
- McNemar’s test  
- Stratified 5-fold cross-validation  

---

💡 Key Insights

- Patients with multiple previous inpatient visits, longer stays, and complex medication regimes are at high risk.
- Model explainability is crucial for clinical decision-making.
- Combining machine learning with explainable AI improves trust and adoption in healthcare.

---

🛠️ Tools Used

- Python, Jupyter Notebook  
- Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- ML Models: Logistic Regression, Random Forest, Gradient Boosting, Neural Networks  
- XAI: SHAP, LIME  

---



