# 📉 Customer Churn Prediction using Machine Learning

This project focuses on predicting customer churn in a telecom company using various machine learning algorithms, including **XGBoost**, which provides competitive performance. Accurately predicting churn helps businesses proactively retain customers and reduce revenue loss.

---

## 🎯 Objectives

* Analyze customer data to identify churn patterns.
* Build predictive models using tree-based algorithms.
* Compare model performances and interpret results.
* Support business decisions with insights and visualizations.

---

## 📁 Project Structure

```
Customer_Churn_Prediction/
│
├── Customer_Churn_Prediction_using_ML.ipynb  # Main Jupyter Notebook
├── Customer_Churn_Prediction_using_ML.html   # HTML version of the notebook
└── README.md                                 # Project overview and instructions
```

---

## 🧰 Technologies Used

| Category       | Libraries / Tools                     |
| -------------- | ------------------------------------- |
| Programming    | Python                                |
| Data Wrangling | Pandas, NumPy                         |
| Visualization  | Seaborn, Matplotlib                   |
| ML Algorithms  | XGBoost, Random Forest, Decision Tree |
| Evaluation     | Accuracy, F1-Score, Confusion Matrix  |
| Environment    | Jupyter Notebook                      |

---

## 📊 Dataset Summary

The dataset includes features such as:

* **Demographics**: `gender`, `SeniorCitizen`, `Partner`, `Dependents`
* **Service Info**: `PhoneService`, `InternetService`, `StreamingTV`, etc.
* **Account Info**: `tenure`, `Contract`, `PaymentMethod`, `PaperlessBilling`
* **Charges**: `MonthlyCharges`, `TotalCharges`
* **Target**: `Churn` (Yes/No)

> Dataset source: `WA_Fn-UseC_-Telco-Customer-Churn.csv` (commonly available on Kaggle)

---

## 🔄 Workflow

### 1. Data Preprocessing

* Converted data types
* Handled missing values
* Applied encoding (label, one-hot)
* Used **SMOTE** to balance the dataset

### 2. Exploratory Data Analysis (EDA)

* Visualized churn distribution
* Identified churn correlations with `tenure`, `contract`, and `charges`

### 3. Model Training

* Models used:

  * Decision Tree
  * Random Forest
  * **XGBoost**
* All models trained using 5-fold cross-validation

### 4. Model Performance (Cross-Validation Accuracy)

| Model         | Accuracy (mean of CV) |
| ------------- | --------------------- |
| Decision Tree | 78%                   |
| Random Forest | **84%**               |
| XGBoost       | **83%**               |

---

## 📈 Final Evaluation

* **Random Forest** slightly outperformed others in cross-validation.
* **XGBoost** showed very close and reliable results.
* Accuracy on test data: \~77.8%
* Churn class metrics (Precision/Recall): \~58–59%
* Insights derived from classification report and confusion matrix.

---

## 🚀 How to Run

1. Install required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
   ```

2. Launch Jupyter Notebook and open the project:

   ```bash
   jupyter notebook Customer_Churn_Prediction_using_ML.ipynb
   ```

---

## 🔍 Key Business Insights

* Customers with **short tenure** and **month-to-month contracts** are most likely to churn.
* Those using **fiber optic internet** and paying **higher monthly charges** also show higher churn tendencies.
* Longer-tenured customers show stronger loyalty.

---

## 🔮 Future Enhancements

* Hyperparameter tuning (GridSearchCV or Optuna)
* Model ensembling for better generalization
* Feature importance visualization (SHAP/Permutation Importance)
* Deploy the best model using Flask or Streamlit
* Build interactive dashboards using Power BI or Tableau

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

