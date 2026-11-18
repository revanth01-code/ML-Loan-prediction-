# Smart Loan Prediction System

A machine learning pipeline designed to automate and predict loan approval status based on applicant financial profiles, credit history, and personal details.

---

## 📋 Project Overview
The goal of this project is to build a robust predictive model that determines whether an applicant is eligible for a loan. By automating the preliminary review process, financial institutions can reduce manual overhead, speed up decision-making, and mitigate risk.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3.x
* **Core Libraries:**
  * `pandas` & `numpy` for data manipulation and preprocessing
  * `scikit-learn` for machine learning algorithms and evaluation metrics
  * `matplotlib` & `seaborn` for exploratory data analysis (EDA) and visualization

---

## 📂 Dataset Description
The project utilizes two primary datasets:
* **`loan_sanction_train.csv`:** Contains historical applicant data alongside the target variable (`Loan_Status`).
* **`loan_sanction_test.csv`:** Contains applicant data without the target variable, used for final model evaluation and predictions.

### Key Features:
* **Loan_ID:** Unique Loan Identifier
* **Gender, Married, Dependents, Education, Self_Employed:** Demographic and background details
* **ApplicantIncome, CoapplicantIncome:** Individual and co-applicant earnings
* **LoanAmount, Loan_Amount_Term:** Financial request parameters
* **Credit_History:** Credit history meets guidelines (1.0 = Yes, 0.0 = No)
* **Property_Area:** Urban, Semi-Urban, or Rural location
* **Loan_Status:** Target variable (Y/N)

---

## ⚙️ Data Preprocessing & Pipeline
1. **Missing Value Imputation:** Automated handling where categorical columns are filled with the mode and numerical columns are filled with the median.
2. **Feature Engineering:** Dropping unique identifiers (`Loan_ID`) that hold no predictive power.
3. **Categorical Encoding:** One-hot encoding via pandas `get_dummies` with automatic column alignment between training and test sets.

---

## 🚀 Getting Started & Usage

1. **Clone or download the project repository.**
2. **Ensure your dataset paths are correctly specified:**
   ```python
   train = pd.read_csv("path/to/loan_sanction_train.csv")
   test = pd.read_csv("path/to/loan_sanction_test.csv")
   ```
3. **Run the preprocessing and training scripts** to clean data, train models, and generate your submission file.

---

## 🔮 Future Improvements
* Incorporate advanced hyperparameter tuning using Grid Search or Random Search.
* Experiment with ensemble models (Random Forest, Gradient Boosting, XGBoost).
* Build an interactive web application (e.g., using Streamlit or Flask) for real-time loan prediction inference.