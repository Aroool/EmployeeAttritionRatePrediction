# 🔍 Employee Attrition Analysis Project

## 🔹 Project Overview
This project analyzes employee attrition using advanced machine learning models to predict which employees are at risk of voluntarily resigning.  
Leveraging the IBM HR Analytics dataset, we performed data cleaning, exploratory data analysis (EDA), model building, and feature interpretation using SHAP analysis.  
The goal is to enable organizations to proactively design retention strategies based on data-driven insights.

## 👨‍💼 Tools and Libraries Used
- Python 3
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- SHAP (SHapley Additive exPlanations)

## 📊 Dataset Description
The dataset contains detailed HR data about employees, including:
- **Demographics**: Age, Gender, Marital Status, Education, Education Field
- **Job Information**: Department, Job Role, Business Travel, Job Level, Years at Company, Years in Current Role
- **Compensation**: Monthly Income, Hourly Rate, Daily Rate, Stock Option Level, Percent Salary Hike
- **Work Conditions**: Distance From Home, OverTime, Work-Life Balance, Environment Satisfaction, Job Satisfaction
- **Performance Metrics**: Performance Rating, Training Times Last Year, Job Involvement

The target variable is **Attrition**:
- `1` = Voluntarily Resigned
- `0` = Current Employee

## 📊 Key Steps

### 🔢 1. Data Cleaning
- Imputed missing numerical values using the median.
- Imputed missing categorical values with 'Missing'.
- Dropped irrelevant columns such as `EmployeeNumber`, `Over18`, `StandardHours`.
- Removed duplicate records.

### 🔄 2. Exploratory Data Analysis (EDA)
- Identified that **OverTime**, **JobRole**, **MonthlyIncome**, and **DistanceFromHome** strongly impact attrition.
- Observed approximately **16% attrition rate**, highlighting a **class imbalance**.

### 📊 3. Model Building
- **Logistic Regression**: Baseline model for binary classification.
- **Naive Bayes**: Fast probabilistic model.
- **Random Forest**: Main model with high interpretability and performance.
- **XGBoost**: Gradient boosting model known for superior predictive power.

### 📊 4. Model Evaluation
- **Confusion Matrix**: Evaluates true/false positives and negatives.
- **ROC-AUC Curve**: Measures model’s ability to distinguish between the two classes.

### 📈 5. Feature Interpretation
- Used **SHAP analysis** to explain model predictions.
- Found that **OverTime**, **JobRole**, **Age**, and **MonthlyIncome** were key contributors to attrition.

## 📊 Results
- **Random Forest** and **XGBoost** models achieved high precision and recall.
- SHAP interpretation revealed actionable factors influencing employee resignations.

## ⚠️ Limitations
- Lack of external factors such as economic conditions and personal events.
- Risk of overfitting if the model is not periodically updated.

## 📊 Future Work
- Integrate external labor market and economic data.
- Implement time-based validations and retraining cycles.
- Explore survival analysis for predicting "when" an employee may leave.
- Deploy a real-time attrition prediction dashboard.

## 🔹 How to Run
1. Clone this repository.
2. Install required dependencies: 
   ```bash
   pip install -r requirements.txt
   ```
3. Open the `EmployeeAttrition.ipynb` notebook.
4. Run the cells to reproduce the analysis.

---

_If you found this project helpful, feel free to star or fork this repository!_

---

