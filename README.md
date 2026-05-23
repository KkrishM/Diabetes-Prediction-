#  Diabetes Prediction using Machine Learning

> *Predicting diabetes risk from diagnostic health data using supervised ML techniques.*

---

##  Project Overview

This project builds and evaluates multiple machine learning models to predict whether a patient has diabetes based on diagnostic health measurements. It uses the well-known **Pima Indians Diabetes Dataset** and covers the complete ML pipeline — from data cleaning and EDA to model training, evaluation, and comparison.

---

##  Problem Statement

Diabetes is a chronic disease affecting millions worldwide. Early detection is critical for effective treatment. Traditional diagnosis requires lab tests and expert interpretation — this project aims to automate risk prediction using patient health data.

---

##  Folder Structure

```
FDAProject/
│
├── data/
│   └── diabetes.csv          # Dataset (Pima Indians Diabetes)
├── project.ipynb             # Main Jupyter Notebook (EDA + ML pipeline)
├── eda_plots.png             # Exploratory Data Analysis visualizations
├── feature_importance.png    # Feature importance chart
├── model_results.png         # Model comparison results
└── README.md                 # This file
```

---

##  Dataset

- **Source:** Pima Indians Diabetes Dataset
- **Features:** 8 diagnostic measurements
- **Target:** Binary — `1` (Diabetic) / `0` (Non-Diabetic)

| Feature | Description |
|---|---|
| `Pregnancies` | Number of pregnancies |
| `Glucose` | Plasma glucose concentration |
| `BloodPressure` | Diastolic blood pressure (mm Hg) |
| `SkinThickness` | Triceps skin fold thickness (mm) |
| `Insulin` | 2-Hour serum insulin (mu U/ml) |
| `BMI` | Body mass index |
| `DiabetesPedigreeFunction` | Diabetes likelihood based on family history |
| `Age` | Age in years |

---

##  ML Pipeline

```
Raw Data → Data Cleaning → EDA → Feature Engineering → Model Training → Evaluation
```

### Data Preprocessing
- Replaced biologically invalid `0` values with `NaN` in columns: Glucose, BloodPressure, SkinThickness, Insulin, BMI
- Filled missing values with **column medians**
- Removed duplicate rows

### Models Used
| Model | Description |
|---|---|
| Logistic Regression | Baseline linear classifier |
| Decision Tree | Interpretable tree-based model |
| Random Forest | Ensemble of decision trees |

### Evaluation Metrics
- Accuracy Score
- Classification Report (Precision, Recall, F1)
- Confusion Matrix
- ROC-AUC Score

---

##  How to Run

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/FDAProject.git
cd FDAProject
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn jupyter
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook project.ipynb
```

### 4. Run all cells
`Kernel` → `Restart & Run All`

---

##  Results

The models were evaluated using 5-fold cross-validation and test set metrics. Random Forest achieved the best overall performance with the highest AUC score.

> See `model_results.png` and `feature_importance.png` for visual summaries.

---

##  Future Improvements

- Hyperparameter tuning with GridSearchCV
- Try XGBoost / LightGBM for better accuracy
- Deploy as a web app using Streamlit
- Add SHAP values for better explainability
- Handle class imbalance with SMOTE

---

##  Author

**Krish Malik**  
[GitHub](https://github.com/KkrishM)
