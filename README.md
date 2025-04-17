# 🌱 Stunting Prediction using Machine Learning

This project aims to classify whether a child is stunted or not based on various health and demographic indicators using supervised machine learning models.

---

## 📦 Dataset Overview

The dataset consists of multiple features related to health, nutrition, and socio-demographic information. The target variable is binary:
- **YES** → Stunted
- **NO** → Not stunted

---

## 🧼 Data Preprocessing

### 1. **Handling Outliers**
- Outliers were identified and removed using statistical methods such as IQR (Interquartile Range) to reduce noise and improve model generalization.

### 2. **Handling Categorical Variables**
- All categorical columns were encoded using **LabelEncoder** to transform non-numeric features into numeric form.

### 3. **Feature Scaling**
- Features were standardized using **StandardScaler** to ensure all features have a mean of 0 and a standard deviation of 1, improving the performance of distance-based algorithms.

---

## 🧠 Machine Learning Models

Five different classification models were trained and evaluated:

| Model                        | Accuracy | Precision | Recall   | F1-Score |
|-----------------------------|----------|-----------|----------|----------|
| K-Nearest Neighbors (KNN)   | 0.869    | 0.829     | 0.738    | 0.770    |
| Decision Tree (DT)          | 0.941    | 0.900     | 0.927    | 0.912    |
| Random Forest (RF)          | 0.941    | 0.925     | 0.889    | 0.906    |
| Support Vector Machine (SVM)| 0.832    | 0.806     | 0.618    | 0.644    |
| Naive Bayes (NB)            | 0.828    | 0.745     | 0.666    | 0.690    |

---

## 📊 Evaluation Summary

### ✅ Random Forest & Decision Tree
- Achieved the highest performance across all evaluation metrics.
- Both models are capable of handling complex, non-linear relationships and show strong predictive power.

### ✅ K-Nearest Neighbors (KNN)
- Performs well with decent precision and F1-score.
- Sensitive to feature scaling and the value of k.

### ⚠️ Support Vector Machine (SVM)
- Lower recall and F1-score, indicating underperformance in identifying positive (stunted) cases.

### ⚠️ Naive Bayes (NB)
- The simplest model, performs the worst among the five, especially in recall.

---

## 🔚 Conclusion

Based on the performance metrics, **Decision Tree** and **Random Forest** are the best choices for stunting classification, offering high accuracy and excellent recall. These models can be further deployed for real-time decision support in public health interventions.

