# Heart Disease Prediction Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange)
![AUC](https://img.shields.io/badge/AUC-0.953-brightgreen)
![Status](https://img.shields.io/badge/Status-Complete-success)

## Overview

A machine learning project to predict the presence of heart disease 
using the **Cleveland Heart Disease Dataset** (UCI Repository).

Cardiovascular disease is the leading cause of death worldwide. Early 
and accurate prediction can significantly improve patient outcomes. 
This project builds and compares multiple ML models to support 
clinical screening decisions.

---

## Results

| Model | Accuracy | AUC | Recall (Disease) | False Negatives |
|---|---|---|---|---|
| **Logistic Regression** | **91.7%** | **0.953** | **82.1%** | **5** |
| Random Forest | 83.3% | 0.930 | 71.4% | 8 |

**Selected Model: Logistic Regression**
Reason: Higher AUC and better recall — in medical screening, missing 
a sick patient is far more dangerous than a false alarm.

---

## Dataset

- **Source:** [Cleveland Heart Disease Dataset — Kaggle](https://www.kaggle.com/datasets/cherngs/heart-disease-cleveland-uci)
- **Size:** 297 patients, 13 clinical features
- **Target:** Binary — Heart Disease (1) or No Disease (0)
- **Balance:** 53.9% No Disease / 46.1% Heart Disease

### Key Features

| Feature | Description | Importance |
|---|---|---|
| thalach | Maximum heart rate achieved | 0.159 |
| cp | Chest pain type | 0.142 |
| ca | Major vessels colored by fluoroscopy | 0.141 |
| oldpeak | ST depression induced by exercise | 0.127 |
| thal | Thalassemia type | 0.112 |

---

## Project Structure

heart-disease-prediction/

│

├── Heart_Disease_Prediction.ipynb   # Main notebook

├── heart_cleveland_upload.csv       # Dataset

└── README.md                        # Project documentation

## Pipeline

Data Loading → EDA → Preprocessing → Model Training → Evaluation → Comparison

---

## Key Findings

- **thalach** (max heart rate) is the strongest predictor — diseased 
  hearts cannot achieve high heart rates under stress
- **Cholesterol** showed surprisingly weak predictive power (correlation: 0.08)
- **Logistic Regression outperformed Random Forest** on this dataset — 
  likely due to the small sample size and relatively linear feature relationships
- Model achieves **AUC of 0.953** — correctly ranks a sick patient above 
  a healthy one 95.3% of the time

---

## How to Run

```bash
# Clone the repository
git clone https://github.com/amin-chokzadegan/heart-disease-prediction.git

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch notebook
jupyter notebook Heart_Disease_Prediction.ipynb
```

---

## Technologies

- **Python 3.8+**
- **pandas** — Data manipulation
- **numpy** — Numerical operations
- **matplotlib / seaborn** — Visualization
- **scikit-learn** — Machine learning models

---

## Author

**Amin Chokzadegan**
- LinkedIn: [linkedin.com/in/amin-chokzadegan](https://www.linkedin.com/in/amin-chokzadegan/)
- Kaggle: [kaggle.com/aminchokzadegan](https://www.kaggle.com/aminchokzadegan)

---

## Future Work

- Threshold tuning to improve recall further
- Feature engineering (interaction terms)
- XGBoost and Neural Network comparison
- Cross-validation for more robust evaluation
- SHAP values for deeper model explainability
