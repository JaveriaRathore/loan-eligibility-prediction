# Loan Eligibility Prediction Project

This project focuses on predicting whether a loan applicant is eligible for loan approval using Machine Learning in Python and Jupyter Notebook.

The project uses applicant details such as income, education, employment status, loan amount, credit history, and other financial information to build a prediction model.

The complete workflow includes data preprocessing, missing value handling, feature engineering, visualization, model training, model evaluation, and final loan prediction on test data.

---

## Tools & Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

## Project Workflow

### 1. Data Loading

Imported training and testing datasets using Pandas:

- `train_dataset.csv`
- `test_dataset.csv`

Performed initial analysis using:

- `head()`
- `shape`
- `info()`
- `describe()`

---

## 2. Exploratory Data Analysis (EDA)

Performed data visualization and analysis using:

- Credit History vs Loan Status using Crosstab
- Applicant Income Histogram
- Coapplicant Income Histogram
- Loan Amount Histogram
- Boxplots for:
  - Applicant Income
  - Loan Amount
  - Applicant Income by Education

This helped in understanding data distribution and identifying outliers.

---

## 3. Data Preprocessing

Handled missing values using:

- Mode for categorical columns
- Mean for numerical columns

Missing values were treated for:

- Gender
- Dependents
- Self Employed
- Loan Amount
- Loan Amount Term
- Credit History

---

## 4. Feature Engineering

Created new useful columns for better prediction:

### LoanAmount_log

Applied Log Transformation on Loan Amount to reduce skewness.

### TotalIncome

Calculated by:

ApplicantIncome + CoapplicantIncome

### TotalIncome_log

Applied Log Transformation on Total Income for normalization.

---

## 5. Feature Selection

Selected important input features for model training:

- Gender
- Married
- Dependents
- Education
- Self Employed
- Loan Amount
- Loan Amount Term
- Credit History
- Property Area
- Total Income Log

Target Variable:

- Loan Status

---

## 6. Data Encoding

Used `LabelEncoder()` to convert categorical values into numerical format for machine learning models.

Encoded:

- Input features (X)
- Target variable (Y)

---

## 7. Train-Test Split

Split the dataset into:

- Training Data → 80%
- Testing Data → 20%

Using:

```python
train_test_split()
