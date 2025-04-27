# 🛡️ Microsoft: Classifying Cybersecurity Incidents with Machine Learning

A machine learning project focused on classifying cybersecurity incidents (True Positive, Benign Positive, False Positive) to support and automate triage workflows in Security Operations Centers (SOCs).

---

## 📊 Project Overview

This project simulates the role of a **data scientist at Microsoft** tasked with improving SOC efficiency. Using the GUIDE dataset, the objective is to develop a classification model that predicts the triage grade of cybersecurity alerts based on historical evidence and contextual signals.

---

## 🧠 Key Skills

- Data Preprocessing & Feature Engineering  
- Model Selection: Logistic Regression, Random Forest, XGBoost  
- Hyperparameter Tuning (Grid Search with Cross-Validation)  
- Evaluation Metrics: Macro-F1, Precision, Recall  
- SHAP for Feature Importance  
- Error Analysis & Model Interpretation  
- Handling Imbalanced Datasets  

---

## 🧾 Problem Statement

Build a robust classification model to categorize security incidents into:
- **True Positive (TP)**
- **Benign Positive (BP)**
- **False Positive (FP)**

The model must generalize well to unseen data and support real-world SOC decisions.

---

## 📌 Project Steps

### 1. Data Preparation
- Handled missing values
- Encoded categorical features with `LabelEncoder`
- Normalized features for Logistic Regression
- Split into **train/validation sets (stratified)**

### 2. Baseline Model
- Trained a **Logistic Regression** classifier
- Baseline Macro-F1 Score: **~0.55**

### 3. Model Building & Tuning
- Trained **XGBoost** classifier with initial configuration
- Tuned using **GridSearchCV** with `f1_macro` scoring
- Best Parameters:  
  `{'colsample_bytree': 0.8, 'learning_rate': 0.1, 'max_depth': 10, 'n_estimators': 100, 'subsample': 0.8}`

### 4. Model Evaluation (Validation Set)
- **Accuracy:** 0.91  
- **Macro F1 Score:** 0.90  
- **Precision:** 0.91  
- **Recall:** 0.89

### 5. Final Evaluation (Test Set)
```text
              precision    recall  f1-score   support

           0       0.88      0.95      0.92    822164  
           1       0.91      0.83      0.87    406393  
           2       0.94      0.89      0.92    664543  

    Accuracy                           0.91   1893100  
    Macro Avg       0.91      0.89      0.90
``` 
### 6. Model Interpretation
- Used SHAP values for feature importance

- Identified top contributing features

- Visualized via SHAP summary plot

### 7. Error Analysis
- Analyzed misclassified records for pattern identification

- Sampled from incorrect predictions to refine interpretation

---

### 📈 Final Results

- Model	Macro F1	Precision	Recall
- Logistic Regression (Baseline)	0.55	0.63	0.56
- XGBoost (Tuned)	0.90	0.91	0.89

---

### 🚀 Recommendations for SOC Integration
- Integrate the model into a real-time alert triage pipeline

- Automate suggested responses using classification outcomes

- Use SHAP insights for SOC dashboards to enhance interpretability

- Continuously retrain model with newly labeled incidents

---

## 🛠️ Tech Stack & Tools

- **Languages:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Shap  

---

## Contact
For any questions or suggestions, feel free to reach out:
* Name: Prakash B
* **LinkedIn**: [Prakash B](https://www.linkedin.com/in/prakash-b-4b509a321)
* **GitHub**: [21-Prakash](https://github.com/21-Prakash)
* **Email**: pprakash7285@gmail.com

Thank you for exploring this project!
