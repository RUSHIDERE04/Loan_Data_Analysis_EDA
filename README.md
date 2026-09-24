# Loan Approval Data — Exploratory Data Analysis
Exploratory data analysis on a bank loan approval dataset containing 614 applicants and 13 features. The project covers data cleaning, exploratory analysis, visualization, outlier treatment, correlation analysis, and feature preprocessing.

## Objective
Understand how applicant characteristics such as income, credit history, education, dependents, and property area vary across loan approval outcomes, and prepare the dataset for further analysis or modeling.

## Dataset
* **Rows:** 614
* **Columns:** 13
* **Target variable:** `Loan_Status` (`Y` / `N`)
* **Features:** `Gender`, `Married`, `Dependents`, `Education`, `Self_Employed`, `ApplicantIncome`, `CoapplicantIncome`, `LoanAmount`, `Loan_Amount_Term`, `Credit_History`, `Property_Area`

## Tools & Libraries
`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn`

## Workflow

1. **Data Cleaning**
   * Removed the non-informative `Loan_ID` column
   * Handled missing categorical values using mode imputation
   * Handled missing numerical values using median imputation
   * Converted `Dependents` values such as `3+` into a numeric format

2. **Univariate Analysis**
   * Analyzed frequency distributions of categorical features
   * Visualized distributions of numerical features using histograms

3. **Bivariate Analysis**
   * Compared categorical features with `Loan_Status`
   * Analyzed numerical features across loan approval outcomes using KDE plots

4. **Outlier Detection & Treatment**
   * Identified potential outliers using the IQR method
   * Applied winsorization to cap extreme values
   * Compared distributions using box plots before and after treatment

5. **Correlation Analysis**
   * Calculated correlations among numerical features
   * Visualized relationships using a correlation heatmap

6. **Feature Preprocessing**
   * Applied one-hot encoding to categorical variables
   * Standardized numerical features using `StandardScaler`

## Key Observations
* The dataset contains **422 approved and 192 rejected loan applications**.
* The applicant dataset contains more male applicants than female applicants.
* Most applicants in the dataset are married and graduates.
* Most applicants are not self-employed.
* Applicants are distributed across Rural, Semiurban, and Urban property areas.
* Potential outliers were identified in several numerical/categorical-coded features and treated during the preprocessing stage.

## Skills Demonstrated
**Data Cleaning & Imputation · Exploratory Data Analysis · Data Visualization · Outlier Detection & Treatment · Correlation Analysis · Feature Preprocessing · Encoding · Feature Scaling**

*This project is part of my Data Analytics portfolio.*

