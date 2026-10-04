# Author: Sonia Mannepuli
## Data Analyst & Graduate Student
## GitHub: github.com/sonia-analytics
## LinkedIn: [Your LinkedIn Profile URL Here]
## Project Role: Lead Data Analyst — Responsible for data cleaning, exploratory

# Marketing Analytics & Customer Intelligence Platform

## Executive Summary
This project analyzes marketing performance, customer behavior, and sales revenue trends to evaluate channel effectiveness, segment customer groups, and build predictive machine learning models for customer retention and sales forecasting.

## Key Focus Areas
- **Marketing Campaign Analytics:** CAC, ROI, and channel conversion performance.
- **Customer Analytics:** RFM segmentation, Customer Lifetime Value (CLV), and churn patterns.
- **Sales & Revenue Analytics:** Revenue growth drivers, product performance, and seasonality.
- **Predictive Analytics:** Machine learning models for churn prediction and sales forecasting.

## Data Sources

| # | Dataset Name | Author / Source | Publication Date | Key Use Cases |
|---|--------------|-----------------|------------------|---------------|
| 1 | [Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis) | Akash Patel (Kaggle) | 2021 | Demographic segmentation, RFM analysis, campaign response rates, Customer Lifetime Value (CLV). |
| 2 | [Marketing Campaign Performance Dataset](https://www.kaggle.com/datasets/manishabhatt22/marketing-campaign-performance-dataset) | Manisha Bhatt (Kaggle) | 2024 | Channel evaluation (Google Ads, Social, Email), Acquisition Cost (CAC), Return on Investment (ROI). |
| 3 | [E-commerce Sales Transactions Dataset](https://www.kaggle.com/datasets/miadul/e-commerce-sales-transactions-dataset) | Miadul Islam (Kaggle) | 2024 | Revenue trends, regional performance, product profit margins, customer churn modeling. |

## Repository Workflow & Notebooks

* **`01_Data_Cleaning_and_EDA.ipynb`**: Data preprocessing, handling missing values, type conversions, and exploratory data analysis of customer demographics and campaign metrics.
* **`02_eda_segmentation.ipynb`**: Calculation of Recency, Frequency, and Monetary (RFM) scores, customer segment mapping, summary statistics, and strategic marketing insights.
* **`03_churn_prediction.ipynb`**: Target label engineering (`Is_Churn`), feature scaling, and machine learning models (Logistic Regression and Random Forest) to predict churn and extract feature importances.

## Tech Stack
- **Languages:** Python (Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib), SQL, R
- **Analytics & ML:** RFM Segmentation, Logistic Regression, Random Forest, Feature Importance
- **BI & Dashboards:** Streamlit Cloud / Power BI
- **Environment & Tools:** Jupyter Notebooks, Git, GitHub

---

## Key Visualizations

### Customer Demographics EDA
![Customer Demographics](01_customer_demographics_eda.png)

### RFM Segment Distribution
![RFM Segment Distribution](02_rfm_segment_distribution.png)

### Churn Feature Importance
![Feature Importance](03_feature_importance.png)

---

## How to Export Visualizations

To export high-resolution visualization charts (`.png`) directly from your Jupyter Notebooks into your root directory or an `images/` folder, use `plt.savefig()` before calling `plt.show()`.

### Chart Export Snippets

```python
# 01_Data_Cleaning_and_EDA.ipynb
plt.figure(figsize=(10, 6))
# [Your plot code here]
plt.title("Customer Demographics Distribution")
plt.tight_layout()
plt.savefig("01_customer_demographics_eda.png", dpi=300, bbox_inches="tight")
plt.show()

# 02_eda_segmentation.ipynb
plt.figure(figsize=(10, 6))
# [Your plot code here]
plt.title("RFM Customer Segment Distribution")
plt.xlabel("Customer Segment")
plt.ylabel("Customer Count")
plt.xticks(rotation=45)
plt.tight_layout()
plt.savefig(
    "02_rfm_segment_distribution.png", dpi=300, bbox_inches="tight"
)
plt.show()

# 03_churn_prediction.ipynb
plt.figure(figsize=(10, 6))
sns.barplot(
    x="Importance",
    y="Feature",
    data=feature_importance_df,
    hue="Feature",
    palette="viridis",
    legend=False,
)
plt.title("Random Forest - Feature Importance for Churn Prediction")
plt.xlabel("Importance Score")
plt.ylabel("Feature")
plt.tight_layout()
plt.savefig("03_feature_importance.png", dpi=300, bbox_inches="tight")
plt.show()
