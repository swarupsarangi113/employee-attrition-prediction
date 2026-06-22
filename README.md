# Employee Attrition Prediction

Predict employee attrition using the IBM HR Analytics dataset with five classification models.

## Project Overview

- Exploratory Data Analysis (EDA)
- Feature Encoding & Scaling
- Class Imbalance Handling (SMOTE)
- Classification Modelling (5 models)
- Model Evaluation (F1, ROC-AUC, Confusion Matrix)
- Feature Importance Analysis
- Business Recommendations

---

## Project Structure

```
employee-attrition-prediction/
├── data.csv                        # IBM HR Analytics dataset
├── employee_attrition.ipynb        # Main notebook
├── employee_attrition_executed.ipynb  # Notebook with saved outputs
├── model.pkl                       # Saved best model
├── preprocessor.pkl                # Saved ColumnTransformer
├── scaler.pkl                      # Saved StandardScaler
├── report.pdf                      # Project report with charts
├── requirements.txt                # Python dependencies
└── README.md
```

---

## Setup

### 1. Clone / navigate to the project directory

```bash
cd employee-attrition-prediction
```

### 2. Create a virtual environment

```bash
python3 -m venv venv
```

### 3. Activate the virtual environment

**macOS / Linux:**
```bash
source venv/bin/activate
```

**Windows:**
```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Run

### Open the notebook

```bash
jupyter notebook employee_attrition.ipynb
```

Then run all cells top to bottom (`Kernel → Restart & Run All`).

---

## Models Trained

| Model               | Notes                            |
|---------------------|----------------------------------|
| Logistic Regression | Linear baseline                  |
| Decision Tree       | Interpretable rules              |
| Random Forest       | Bagging ensemble                 |
| Gradient Boosting   | Sequential boosting              |
| K-Nearest Neighbors | Distance-based                   |

Best model is selected by **F1 Score** and saved to `model.pkl`.

---

## Key Findings

- **OverTime**, **MonthlyIncome**, **Age**, and **TotalWorkingYears** are the strongest attrition predictors
- Employees working overtime are significantly more likely to leave
- Lower income and fewer years at the company correlate with higher attrition
- Class imbalance (84% No / 16% Yes) was handled with SMOTE on training data only
