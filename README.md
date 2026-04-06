# 🧠 Stroke Risk Prediction System  


---

## 📖 Project Overview  

This project focuses on developing a machine learning-based system for predicting stroke risk using both **clinical** and **behavioral** data.

Stroke is a critical health condition where early detection can significantly reduce mortality and complications. However, many prediction systems struggle due to **imbalanced datasets** and poor detection of actual stroke cases.

This project addresses these challenges by:
- Performing detailed data preprocessing and feature engineering  
- Handling class imbalance using **SMOTE**  
- Developing and comparing multiple machine learning models  
- Building both a **Main Model** and a **Hybrid Model**  
- Evaluating models based on **medical relevance (recall)** rather than just accuracy  

---

## 📊 Datasets Used  

The system was developed using multiple datasets:

- Cardiovascular Dataset (Cardio)  
- Stroke Dataset 1 (Healthcare Dataset)  
- Stroke Dataset 2 (Clinical Diagnosis Dataset)  
- Smoking & Lifestyle Dataset  

These datasets include:
- **Clinical features:** age, BMI, blood pressure, glucose levels  
- **Behavioral features:** smoking status, alcohol intake  

---

## 🧹 Data Preprocessing  

The following preprocessing steps were applied:

- Handling missing values (e.g., BMI imputation)  
- Removing duplicates and invalid records  
- Filtering unrealistic medical values (BP, height, weight)  
- Encoding categorical variables using Label Encoding  
- Feature engineering:
  - BMI calculation  
  - Pulse pressure  
- Feature scaling using StandardScaler  

---

## ⚖️ Handling Imbalanced Data  

The stroke dataset is highly imbalanced (very few stroke cases compared to non-stroke cases).

To address this:
- SMOTE (Synthetic Minority Oversampling Technique) was applied to training data  
- Models were evaluated **with and without SMOTE** for comparison  

---

## 🤖 Models Developed  

### 🔹 Main Model (Final Model)
- Logistic Regression  
- Class weighting applied  
- Threshold tuning (0.3 instead of 0.5)  
- Focus: **Maximize stroke detection (recall)**  

---

### 🔹 Hybrid Model (Stacking Approach)
- Base Models:
  - Logistic Regression  
  - Random Forest  
  - XGBoost  
- Meta Model:
  - Logistic Regression  

- Combined predictions using stacking  

---

## 📈 Results Summary  

### 🔸 Main Model (Logistic Regression + SMOTE)
- Accuracy: ~64%  
- Recall (Stroke): ~78%  
- Precision: ~10%  

Strong at detecting stroke cases.

---

### 🔸 Hybrid Model
- Accuracy: ~87%  
- Recall (Stroke): ~32%  
- Precision: ~14%  

Better accuracy but weaker stroke detection.

---

## 📌 Model Comparison  

| Model        | Accuracy | Recall (Stroke) | Precision |
|-------------|--------|----------------|----------|
| Main Model  | 0.64   | 0.78           | 0.10     |
| Hybrid Model| 0.87   | 0.32           | 0.14     |

---

## 🧪 Validation on Secondary Dataset  

Both models were tested on a separate dataset (Stroke2):

- Main Model maintained strong stroke detection  
- Hybrid Model showed balanced but weaker performance  

---

## ✅ Final Decision  

The **Main Model (Logistic Regression)** was selected because:

- It achieves high recall  
- It reduces missed stroke cases  
- It aligns with medical priorities  

---

## 🧠 Key Insight  

> In healthcare systems, recall is more important than accuracy.

Detecting stroke cases early is more valuable than avoiding false alarms.

---

## 📁 Project Structure  

stroke-risk-prediction/
│
├── notebook.ipynb
├── project_results/
│ ├── cleaned_data/
│ ├── outputs/
│ ├── metrics/
│ ├── models/
│
├── README.md

---

## 📦 Outputs  

The project includes:
- Cleaned datasets  
- Model predictions  
- Evaluation metrics  
- Feature importance  
- Trained models (.pkl files)  

---

## 🚀 Technologies Used  

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Imbalanced-learn (SMOTE)  
- Matplotlib  
- Seaborn  

---

## 🔍 Future Improvements  

- Improve precision while maintaining recall  
- Deploy as a web/mobile app  
- Use real-time health data  
- Explore deep learning models  

---

## 📎 Conclusion  

This project demonstrates how machine learning can be applied to healthcare problems, with a strong focus on real-world impact.

It emphasizes the importance of evaluating models beyond accuracy, especially in medical diagnosis.

---

## 👨‍💻 Author  

[Abidemi Aminat]  
Computer Science Student  
Backend Developer | AI Engineer  

---

## ⭐ Final Note  

This project focuses on building a system that aligns with real-world medical needs, where early detection can save lives.
