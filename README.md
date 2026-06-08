# Chronic Disease Prediction

ML project for **U.S. Chronic Disease Indicators** - predicting disease rates, unit types, and value types using demographic and geographic features.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/OrkhanIsmayilov992/Chronic-Disease-Prediction/blob/main/U_S_A_Chronic_Disease_Indicators.ipynb)

---

## 📊 Dataset

- **Source:** CDC (Centers for Disease Control and Prevention)
- **Size:** 309,215 rows, 34 columns
- **Years:** 2015-2022
- **Coverage:** All 50 US states + territories

---

## 🎯 Three Prediction Targets

| Target | Type | Best Model | Score |
|--------|------|------------|-------|
| **DataValue** (Disease Rate) | Regression | XGBoost | R² = 0.86 |
| **DataValueUnit** (Unit Type) | Classification | Random Forest | 98.2% Accuracy |
| **DataValueTypeID** (Value Type) | Classification | XGBoost | 81.8% Accuracy |

---

## 📈 Project Workflow

### 1. Data Loading & Initial Exploration
- Dataset: 309,215 rows, 34 columns
- Source: CDC U.S. Chronic Disease Indicators

### 2. Data Cleaning
- Removed 100% empty columns (10 columns)
- Handled missing values in Footnote columns
- Removed duplicate/redundant columns

### 3. Feature Engineering
- Created Latitude/Longitude from Geolocation
- Created Year_Span, Decade from years
- Created Risk_Category, High_Risk from DataValue
- Created Confidence_Width from confidence limits

### 4. Encoding & Preprocessing
- One-Hot Encoding for low cardinality columns
- Label Encoding for high cardinality columns
- Target encoding for classification tasks

### 5. Model Training
- 3 Targets: DataValue, DataValueUnit, DataValueTypeID
- 4 Models per target: Linear/Logistic Regression, Decision Tree, Random Forest, XGBoost

### 6. Hyperparameter Tuning
- Used GridSearchCV for XGBoost and Random Forest
- Optimized parameters: n_estimators, max_depth, learning_rate

### 7. Model Evaluation
- Regression metrics: R², RMSE
- Classification metrics: Accuracy, F1-Score, Confusion Matrix

### 8. Model Interpretation
- SHAP values for feature importance
- Feature importance plots

### 9. Model Saving & Deployment
- Saved models to Google Drive
- Created GitHub repository
- Added Open in Colab badge

---

## 🛠 Technologies Used

ML project for U.S. Chronic Disease Indicators
