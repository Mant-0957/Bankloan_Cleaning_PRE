#  Bank Loan Data Preprocessing & Feature Engineering Project

##  Project Overview

This project demonstrates a complete **end-to-end Data Preprocessing and Feature Engineering pipeline** for a Customer Credit Risk Dataset.
The objective is to transform raw banking customer data into a clean, structured, and machine-learning-ready dataset capable of supporting loan default prediction models.

This project covers the entire Data Science preprocessing workflow including:

* Data Acquisition
* Data Understanding
* Data Cleaning
* Missing Value Treatment
* Outlier Detection & Handling
* Feature Engineering
* Feature Scaling
* Feature Transformation
* Data Encoding
* Pipeline Construction

The final output is a fully processed dataset suitable for Machine Learning applications.

---

##  Problem Statement

A fintech company wants to predict whether a customer is likely to default on a loan.

The dataset contains:

### Customer Demographics

* Age
* Gender
* Region
* Education Level
* Employment Type

### Financial Information

* Annual Income
* Loan Amount
* Loan Purpose
* Credit Score

### Behavioral Information

* Transaction Count
* Spending Ratio
* Repayment History

### Target Variable

* Default Flag

  * 0 = No Default
  * 1 = Default

---

##  Dataset Features

| Feature           | Description                |
| ----------------- | -------------------------- |
| customer_id       | Unique Customer Identifier |
| age               | Customer Age               |
| gender            | Male/Female/Other          |
| region            | Customer Region            |
| education_level   | Education Category         |
| employment_type   | Employment Status          |
| annual_income     | Annual Income              |
| loan_amount       | Loan Requested             |
| loan_purpose      | Purpose of Loan            |
| credit_score      | Credit Score               |
| repayment_history | Missed Payments            |
| transaction_count | Number of Transactions     |
| spending_ratio    | Spending-to-Income Ratio   |
| join_date         | Date Joined Bank           |
| default_flag      | Target Variable            |

---

#  Technologies Used

## Programming Language

* Python

## Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Missingno
* SciPy
* YData Profiling
* SQLAlchemy
* Requests

---

#  Project Workflow

## Part A: Conceptual Foundation

Covered theoretical concepts including:

* Data Analysis
* Data Science Project Lifecycle
* Machine Learning Problem Framing
* Tensor Fundamentals using NumPy

---

## Part B: Data Acquisition

Data imported from multiple sources:

### CSV Files

Main customer credit risk dataset

### JSON Files

Customer metadata

### SQL Database

Loan repayment history

### REST API

External economic indicators

---

## Part C: Data Understanding & Cleaning

### Dataset Inspection

Performed:

```python
df.info()
df.describe()
df.shape
df.columns
```

### Data Quality Report

Generated using:

```python
from ydata_profiling import ProfileReport
```

### Missing Value Analysis

Visualized using:

```python
import missingno as msno
```

---

#  Missing Value Handling Techniques

The following methods were implemented:

### Simple Imputation

* Mean Imputation
* Median Imputation
* Most Frequent Imputation

### Advanced Imputation

* Missing Indicator Method
* Random Sample Imputation
* KNN Imputer
* MICE (Multiple Imputation by Chained Equations)

### Complete Case Analysis

* Row Removal Strategy

---

#  Outlier Detection & Treatment

Implemented multiple techniques:

### Z-Score Method

Used for:

* Annual Income

### IQR Method

Used for:

* Loan Amount

### Percentile Method

Used for:

* Credit Score

### Winsorization

Used for:

* Income Distribution Control

---

#  Feature Engineering

## Date-Time Feature Extraction

Extracted:

* Join Year
* Join Month
* Join Day
* Join Weekday

---

## Encoding Techniques

### Ordinal Encoding

Applied to:

* Education Level

### Label Encoding

Applied to:

* Gender

### One-Hot Encoding

Applied to:

* Region
* Loan Purpose

---

## Numerical Feature Engineering

### Binning

Applied to:

* Annual Income

### Binarization

Applied to:

* Credit Score

### Quantile Binning

Applied to:

* Transaction Count

### K-Means Binning

Applied to:

* Transaction Count

---

#  Feature Scaling

Implemented multiple scaling methods:

## StandardScaler

Z-score normalization

## MinMaxScaler

Range scaling between 0 and 1

## MaxAbsScaler

Scale by maximum absolute value

## RobustScaler

Robust against outliers

---

#  Feature Transformation

## Function Transformer

Applied:

* Log Transformation
* Reciprocal Transformation
* Square Root Transformation

---

## Power Transformer

### Box-Cox Transformation

Applied on:

* Annual Income

### Yeo-Johnson Transformation

Applied on:

* Loan Amount

---

#  Feature Construction

New features created:

## Debt-To-Income Ratio

```python
loan_amount / annual_income
```

---

## Average Monthly Transactions

```python
transaction_count / 6
```

---

## Spending-To-Income Ratio

```python
spending_ratio / annual_income
```

---

#  Pipeline Development

Implemented Scikit-Learn Pipelines using:

### Numerical Pipeline

* Median Imputation
* Standard Scaling

### Categorical Pipeline

* Most Frequent Imputation
* One-Hot Encoding

### Column Transformer

Used for handling mixed data types efficiently.

---

#  Final Deliverables

✔ Cleaned Dataset

✔ Transformed Dataset

✔ Feature Engineered Dataset

✔ Data Quality Report

✔ Jupyter Notebook

✔ Machine Learning Ready Dataset

---

#  Project Outcome

By completing this project, the following objectives were achieved:

* Complete data preprocessing workflow implementation
* Handling missing values using multiple techniques
* Outlier detection and treatment
* Advanced categorical encoding
* Numerical feature engineering
* Feature scaling and transformation
* Pipeline creation using Scikit-Learn
* Production-ready dataset preparation

---

#  Repository Structure

```text
Bankloan_Cleaning_PRE/
│
├── Project_FinaL_PRE.ipynb
├── bank_loan_dataset_1000_rows.csv
├── Data_Quality_Report.html
├── Final_Cleaned_CreditRisk_Dataset.csv
├── README.md
│
└── screenshots/
```

---

#  Future Improvements

* Hyperparameter Optimization
* Model Training & Evaluation
* Feature Selection
* Ensemble Learning Models
* Deployment using Flask/FastAPI
* MLflow Experiment Tracking

---

#  Author

**Mant Patel**

GitHub Repository:

[Bankloan_Cleaning_PRE Repository](https://github.com/Mant-0957/Bankloan_Cleaning_PRE?utm_source=chatgpt.com)

---

## ⭐ If you found this project useful, consider giving the repository a star.
