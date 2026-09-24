# Loan Approval Data — Exploratory Data Analysis
Exploratory data analysis on a bank loan-approval dataset (614 applicants, 13 features), covering data cleaning, univariate & bivariate analysis, outlier treatment, correlation analysis, and feature preprocessing for modeling.

## Objective
Understand which applicant characteristics (income, credit history, property area, dependents, etc.) are associated with loan approval, and prepare a clean, model-ready dataset through a full EDA pipeline.

## Dataset
- **Rows:** 614 | **Columns:** 13
- **Target variable:** `Loan_Status` (Y/N)
- **Features:** Gender, Married, Dependents, Education, Self_Employed, ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, Property_Area

## Tools & Libraries
`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn`

## Workflow
1. **Data Cleaning**
   - Dropped the non-informative `Loan_ID` column
   - Imputed missing categorical values with mode (e.g. Gender: 13 missing, Self_Employed: 32 missing, Credit_History: 50 missing)
   - Imputed missing numerical values with median
   - Standardized `Dependents` (converted `'3+'` to `3`, cast to integer)

2. **Univariate Analysis**
   - Frequency distributions and bar charts for all categorical features
   - Histograms for all numerical features

3. **Bivariate Analysis**
   - Categorical features vs. `Loan_Status` (count plots)
   - Numerical features vs. `Loan_Status` (KDE plots)

4. **Outlier Detection & Treatment**
   - Identified outliers using the IQR method across all numeric columns
   - Applied winsorization (clipping) to cap extreme values
   - Re-validated with box plots before/after treatment

5. **Correlation Analysis**
   - Computed and visualized a correlation heatmap across numerical features
   - Checked for low-variance / near-constant columns

6. **Feature Engineering**
   - One-hot encoded categorical variables
   - Standardized numerical features using `StandardScaler`

## Key Observations
- The dataset is imbalanced toward approvals: **422 "Y" vs. 192 "N"** loan outcomes.
- Applicant pool skews **male (502 vs. 112 female)**, **married (401 vs. 213 unmarried)**, and **graduate (480 vs. 134 non-graduate)**.
- Most applicants are **not self-employed (532 vs. 82)**.
- Property area is fairly balanced across Semiurban (233), Urban (202), and Rural (179).
- Notable outliers were found in `Credit_History` (89), `Loan_Amount_Term` (88), and `Dependents` (51), which were treated via winsorization before correlation/scaling steps.

## Skills Demonstrated
Data cleaning & imputation · Exploratory data analysis · Data visualization · Outlier detection & treatment · Correlation analysis · Feature engineering (encoding & scaling)
---
*This project is part of my Data Analytics portfolio.*
