# 📊 Telco Customer Churn Analysis

## 📌 Project Overview
Customer churn (attrition) is a critical metric for subscription-based businesses like telecom companies. This project performs an **Exploratory Data Analysis (EDA)** on a Telco Customer Churn dataset to understand customer demographics, account information, and service usage patterns, ultimately identifying key factors contributing to customer churn.

---

## 📂 Dataset Information
* **File Name:** `Customer Churn.csv`
* **Total Records:** 7,043 rows
* **Total Features:** 21 columns
* **Target Variable:** `Churn` (Indicates whether the customer left within the last month: `Yes` or `No`)

### Key Features Included:
* **Demographics:** `customerID`, `gender`, `SeniorCitizen`, `Partner`, `Dependents`
* **Services Subscribed:** `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`
* **Account & Billing:** `tenure`, `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`

---

## 🛠️ Technologies & Libraries Used
* **Python 3.x**
* **Pandas:** Data manipulation, cleaning, and aggregation.
* **NumPy:** Numerical operations.
* **Matplotlib & Seaborn:** Data visualization and statistical plotting.
* **Jupyter Notebook:** Interactive development environment (`Telco_Churn_Analysis.ipynb`).

---

## 🧹 Data Cleaning & Preprocessing Steps
Before diving into visualizations, the dataset underwent thorough inspection and cleaning:
1. **Handling Missing/Blank Values:** Identified blank spaces (`" "`) in the `TotalCharges` column (which initially caused it to be read as an `object` data type). Replaced blanks with `0` and converted the column to `float64`.
2. **Null & Duplicate Checks:** 
   * Verified zero null values across all 21 columns (`df.isnull().sum()`).
   * Checked for duplicate rows and duplicate `customerID` entries—found `0` duplicates.
3. **Data Transformation:** Converted binary values (`1` and `0`) in the `SeniorCitizen` column into readable categorical labels (`"senior citizen"` and `"not senior citizen"`) for clearer visualization.

---

## 📈 Key Findings & Exploratory Data Analysis (EDA)

### 1. Statistical Summary (`df.describe()`)
* **Tenure:** Customers stay for an average of **32.37 months** (ranging from 0 to 72 months).
* **Monthly Charges:** Average monthly bill is **$64.76** (ranging from $18.25 to $118.75).
* **Total Charges:** Average total revenue per customer is **$2,279.73** (up to a maximum of $8,684.80).

### 2. Overall Churn Rate
* **Retained Customers (`No`):** 5,174 (**73.46%**)
* **Churned Customers (`Yes`):** 1,869 (**26.54%**)
* *Insight:* Roughly **1 in 4 customers** have churned, indicating a significant retention challenge that requires deeper segmentation.

### 3. Demographic Breakdown
* Initiated bivariate analysis starting with **Gender-wise Churn Count** (calculating exact counts and percentages per gender) to evaluate whether demographic attributes influence churn behavior. *(Additional feature breakdowns follow in the notebook).*

---

## 🚀 How to Run This Project
1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/Telco-Churn-Analysis.git
   ```
2. **Navigate to the project directory:**
   ```bash
   cd Telco-Churn-Analysis
   ```
3. **Install required dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook Telco_Churn_Analysis.ipynb
   ```

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to fork this repository and submit a pull request if you'd like to add predictive modeling (Machine Learning) or further visual insights.
