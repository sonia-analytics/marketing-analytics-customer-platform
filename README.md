# Author: Sonia Mannepuli
Data Analyst & Graduate Student
GitHub: github.com/sonia-analytics
Project Role: Lead Data Analyst — Responsible for data cleaning, exploratory

# Marketing Analytics & Customer Segmentation Project

An end-to-end data analytics and machine learning project focused on customer segmentation via **RFM Analysis (Recency, Frequency, Monetary)** and predictive **Churn Modeling** to optimize marketing spend, target high-value customers, and mitigate churn risk.

---

## Project Overview
Understanding customer behavior is vital for modern data-driven marketing. This project leverages a comprehensive customer dataset to:
1. **Clean and Transform Raw Data:** Handle missing values, engineer behavioral metrics, and format features for analysis.
2. **Perform Exploratory Data Analysis (EDA):** Uncover spending patterns, purchasing channels, and demographic trends.
3. **Execute RFM Segmentation:** Segment customers into actionable groups (e.g., *Champions*, *Loyal Customers*, *At Risk*) using quartile-based scoring.
4. **Build Predictive Models:** Implement **Logistic Regression** and **Random Forest** classifiers to predict customer churn risk based on purchasing behavior.

---

## Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (Logistic Regression, Random Forest, Metrics)
* **Data Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebooks

---

## 📁 Repository Structure
```text
marketing-analytics-customer-segmentation/
│
├── data/
│   ├── marketing_campaign.csv          # Cleaned dataset
│   └── rfm_customer_data.csv           # Segmented customer output
│
├── notebooks/
│   ├── 01_Data_Cleaning_and_EDA.ipynb  # Data preparation & exploratory analysis
│   ├── 02_eda_segmentation.ipynb       # RFM modeling & behavioral segmentation
│   └── 03_churn_prediction.ipynb       # Predictive classification models
│
├── outputs/
│   └── figures/                        # Saved charts and distribution plots
│
└── README.md                           # Project documentation
```

---

## Key Methodology & Workflow

### 1. Data Cleaning & Feature Engineering (`01_Data_Cleaning_and_EDA.ipynb`)
* Handled missing values (such as income imputations) and cleaned structural inconsistencies.
* Engineered core analytical features including **Total Spend** (across product categories like wines, fruits, and gold) and customer **Age / Tenure**.

### 2. RFM Customer Segmentation (`02_eda_segmentation.ipynb`)
* Assigned numerical scores from 1 to 5 for **Recency**, **Frequency**, and **Monetary** value.
* Mapped composite scores into business segments:
  * **Champions:** High spenders who buy frequently and recently.
  * **Loyal Customers:** Consistent buyers with steady engagement.
  * **At Risk / Inactive:** Customers showing high recency gaps and declining purchases.

### 3. Predictive Churn Modeling (`03_churn_prediction.ipynb`)
* Defined a target churn label based on customer segment status (*At Risk* / *Lost*).
* Trained and evaluated baseline **Logistic Regression** and robust **Random Forest** classifiers.
* Analyzed **Feature Importance** (identifying Recency and Total Purchases as top predictors of churn risk) and generated ROC-AUC curves.

---

## Strategic Business Recommendations
* **Retention Campaigns:** Deploy automated, personalized re-engagement discounts for the *At Risk* segment before they transition to *Lost*.
* **VIP Reward Programs:** Implement tiered loyalty perks for *Champions* to maximize lifetime value (LTV).
* **Targeted Channel Spend:** Shift marketing budget toward digital web and catalog channels that drive higher conversion rates based on EDA insights.

---

## How to Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/marketing-analytics-customer-segmentation.git
   ```
2. Install required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Run the Jupyter notebooks sequentially from `01` to `03`.
