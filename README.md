#  Pima Diabetes - Predicting Diabetes from Imperfect Medical Data

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)


---

##  Description

This project aims to **predict diabetes** in Pima women using a real medical dataset containing biologically impossible zero values (missing data). The project covers the full data science pipeline: cleaning, visualization, feature engineering, and machine learning modeling.

> (2025)

---

##  Dataset

- **Source :** Pima Indians Diabetes Dataset
- **768 patients**, 9 variables
- **Target variable :** `Outcome` (0 = Not Diabetic, 1 = Diabetic)
- **Challenge :** Some columns contain impossible zero values (missing data)

---

##  Project Steps

###  Data Cleaning & Preparation
- Detected biologically impossible zeros in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`
- Replaced zeros with `NA` then imputed with median values
- Result: clean dataset ready for modeling

###  Feature Engineering
- Created `BMICategory` variable (Underweight, Normal, Overweight, Obese)
- Created `BPCategory` variable (Low, Normal, High)
- Standardized numeric features for better model performance

###  Visualization (ggplot2)
- Correlation heatmap before and after cleaning
- Diabetes Pedigree vs Age scatter plot
- Glucose distribution histograms
- BMI vs Outcome boxplot

###  Modeling & Prediction
| Model | Accuracy | Precision | Recall |
|-------|----------|-----------|--------|
| Logistic Regression | **78%** | 78% | 78% |
| K-Nearest Neighbors (KNN) | **80%** | 74% | 85% |
| Cross-Validation (avg) | **77%** | — | — |

###  Impact of Data Cleaning
- Cleaned data accuracy: **76.47%**
- Dirty data accuracy: **77.12%**
-  Cleaning significantly improves model reliability and interpretability

---
##  Technologies Used

- **Language :** R
- **Libraries :** ggplot2, dplyr, caret, corrplot, ggcorrplot, janitor, gmodels, gridExtra

---

##  Project Structure

```
PROJECT_R-Pima_Diabetes/
│
├── data/
│   └── diabetes.csv          # Raw dataset
├── scripts/
│   └── analysis.R            # Main R script
├── output/
│   └── plots/                # Generated visualizations
└── README.md
```

---

##  Key Findings

- **Glucose**, **BMI** and **DiabetesPedigreeFunction** are the strongest predictors of diabetes
- Data cleaning is **crucial** for model reliability
- Logistic Regression is preferred for **interpretability**
- KNN performs slightly better on **recall** (detecting diabetic patients)


