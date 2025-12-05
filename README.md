<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/97ddaa59-cfb2-4fe0-b44c-9c679d756372" />

# Symptom-Based Disease Classification Using Machine Learning

This repository contains code, data preprocessing, model training, and evaluation for a **multi-class disease prediction system** based on patient symptom data.  
The project applies supervised machine learning to predict 42 possible diseases using 132 symptom features, supporting early clinical triage and computational diagnostics.

---

## Project Overview

- **Goal:** Predict disease outcomes from symptom patterns and identify key features contributing to model decisions.  
- **Dataset:** Public Kaggle dataset — [Disease Prediction Using Machine Learning](https://www.kaggle.com/datasets/itachi9604/disease-prediction-using-machine-learning).  
- **Records:** 4,900 patients × 132 binary symptom features + 1 target (disease label).  
- **Target:** 42 possible diseases (multi-class classification).
<img width="790" height="490" alt="download" src="https://github.com/user-attachments/assets/a33e91d7-cb44-4b4e-b300-3f676514b4e3" />
<img width="1295" height="989" alt="download" src="https://github.com/user-attachments/assets/50d4f42f-d3be-46fa-b141-e6e8a26dd44a" />
<img width="989" height="590" alt="download" src="https://github.com/user-attachments/assets/7aab2062-372a-4acf-8854-cb7f95c30b31" />


---

## Research Question

> Can machine learning accurately classify diseases using only symptom-based features, and which symptoms most strongly influence those predictions?

---

## Methods & Workflow

### **1. Data Preprocessing**
- Loaded dataset (`Training 2.csv`)  
- Dropped empty columns (e.g., `Unnamed: 133`)  
- Handled missing values using `SimpleImputer(strategy="most_frequent")`  
- Encoded target labels using `LabelEncoder`  
- Standardized features using `StandardScaler`  
- Split data using **Stratified 80/20 Train–Test** split

### **2. Models Implemented**
| Model | Description | Accuracy | Macro F1 |
|--------|--------------|-----------|-----------|
| Logistic Regression | Multinomial baseline classifier | 0.98 | 0.97 |
| Random Forest | Ensemble model for non-linear patterns | 1.00 | 1.00 |
| K-Nearest Neighbors (KNN) | Distance-based pattern learner | 0.94 | 0.92 |

### **3. Evaluation Metrics**
- Accuracy  
- Macro F1 Score  
- Confusion Matrices  
- Feature Importance (Random Forest)  

---

## Visualizations
<img width="783" height="705" alt="download" src="https://github.com/user-attachments/assets/f1c8c4df-ed71-4a44-9ba9-e2c46dccc2c0" />
<img width="783" height="705" alt="download" src="https://github.com/user-attachments/assets/bfcc719d-2835-4982-a570-c8eb6b97d5ed" />
<img width="911" height="790" alt="download" src="https://github.com/user-attachments/assets/24d0930c-c834-4469-a95f-07a5d141e32f" />
<img width="690" height="490" alt="download" src="https://github.com/user-attachments/assets/7fb2de03-ec2a-4739-9961-a20365d96dc2" />
<img width="790" height="989" alt="download" src="https://github.com/user-attachments/assets/11f22c7a-3dd6-48b2-8cd8-043ca880796a" />





| Figure | Description |
|--------|--------------|
| **Figure** | Logistic Regression – Confusion Matrix |
| **Figure** | Model Accuracy Comparison |
| **Figure** | KNN – Confusion Matrix |
| **Figure** | Top 20 Features by Random Forest Importance |

All figures are generated directly from the Notebook in the `/notebooks/` directory.

---

## Key Findings

- **Random Forest** achieved perfect accuracy, indicating strong relationships among symptom features.  
- **Top predictive symptoms** include: *muscle pain, itching, yellowing of eyes, family history,* and *fatigue*.  
- Linear and non-linear models both perform well, confirming dataset quality and informative features.  
- The project demonstrates the potential of machine learning for interpretable, symptom-based disease triage.

---

## Next Steps
- Hyperparameter tuning for Random Forest and KNN  
- Integrate **XGBoost** for boosted-tree comparison  
- Add **SHAP** or permutation-based interpretability methods  
- Validate results on larger or external medical datasets  

---

## Tools & Environment

| Library | Version |
|----------|----------|
| Python | 3.10 |
| pandas | 2.2+ |
| scikit-learn | 1.4+ |
| matplotlib | 3.8+ |
| seaborn | 0.13+ |
| numpy | 1.26+ |

---

##Reproducibility

To reproduce results:

```bash
# 1. Clone this repository
git clone https://github.com/isihack/DiseasePredictionML.git
cd DiseasePredictionML

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the notebook

