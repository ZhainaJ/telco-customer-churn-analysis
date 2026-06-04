# Telco Customer Churn Analysis

## Project Overview

Customer retention is a critical challenge in the telecommunications industry. Acquiring new customers is often significantly more expensive than retaining existing ones, making customer churn a major business concern.

This project analyzes customer behavior data from a telecommunications company to identify factors associated with customer attrition and develop machine learning models capable of predicting churn. The analysis combines exploratory data analysis (EDA), statistical investigation, and predictive modeling to generate actionable business insights.

The project follows an end-to-end data science workflow, from data cleaning and visualization to model evaluation and business recommendations.

---

## Business Problem

Customer churn occurs when a customer stops using a company's services.

The objective of this project is to answer the following questions:

- Which customers are most likely to churn?
- What factors contribute most to customer attrition?
- Can churn be predicted using historical customer information?
- What actions can the business take to improve retention?

By identifying high-risk customers and understanding churn drivers, telecommunications companies can design targeted retention strategies and reduce revenue loss.

---

## Dataset

Dataset: IBM Telco Customer Churn Dataset

The dataset contains customer-level information including:

- Customer demographics
- Account information
- Contract details
- Internet service subscriptions
- Payment methods
- Monthly charges
- Total charges
- Customer tenure
- Churn status

### Target Variable

| Variable | Description |
|-----------|-------------|
| Churn | Indicates whether a customer left the company (Yes/No) |

---

## Project Structure

```text
telco-customer-churn-analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── Telco_Customer_Churn_Analysis.ipynb
│
├── images/
│   ├── churn_distribution.png
│   ├── contract_vs_churn.png
│   ├── tenure_vs_churn.png
│   ├── monthly_charges_vs_churn.png
│   ├── payment_method_vs_churn.png
│   ├── correlation_heatmap.png
│   └── feature_importance.png
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

### Development Environment

- Jupyter Notebook
- Git
- GitHub

---

## Data Cleaning and Preprocessing

Several preprocessing steps were performed before analysis:

### Data Type Corrections

- Converted `TotalCharges` from object to numeric format.
- Handled conversion errors using null value replacement.

### Missing Value Treatment

- Identified missing values in numerical features.
- Replaced missing values using median imputation.

### Duplicate Detection

- Checked for duplicate records.
- Removed duplicates when necessary.

### Feature Encoding

- Converted categorical variables into numerical representations suitable for machine learning models.

### Feature Scaling

- Standardized numerical variables for model training.

---

## Exploratory Data Analysis (EDA)

The exploratory analysis focused on understanding patterns associated with customer churn.

### Customer Churn Distribution

![Customer Churn Distribution](images/churn_distribution.png)

**Objective**

Understand the overall churn rate within the customer base.

**Insight**

A significant proportion of customers leave the service, indicating that churn prediction represents a meaningful business problem.

---

### Contract Type vs Churn

![Contract Type vs Churn](images/contract_vs_churn.png)

**Hypothesis**

Customers with short-term contracts are more likely to churn.

**Finding**

Month-to-month customers exhibit substantially higher churn rates compared to customers with one-year or two-year contracts.

**Business Interpretation**

Long-term contracts appear to strengthen customer retention and reduce attrition risk.

---

### Monthly Charges vs Churn

![Monthly Charges vs Churn](images/monthly_charges_vs_churn.png)

**Hypothesis**

Higher service costs increase churn probability.

**Finding**

Customers with higher monthly charges demonstrate increased churn behavior.

**Business Interpretation**

Pricing sensitivity may contribute to customer attrition and should be investigated further.

---

### Customer Tenure vs Churn

![Customer Tenure vs Churn](images/tenure_vs_churn.png)

**Hypothesis**

New customers are more likely to leave than long-term customers.

**Finding**

Customers with shorter tenure exhibit significantly higher churn rates.

**Business Interpretation**

Customer retention efforts should be concentrated during the early stages of the customer lifecycle.

---

### Payment Method vs Churn

![Payment Method vs Churn](images/payment_method_vs_churn.png)

**Hypothesis**

Certain payment methods may correlate with customer retention.

**Finding**

Electronic check users demonstrate higher churn rates compared to customers using automated payment methods.

**Business Interpretation**

Promoting automatic payment methods may improve customer retention.

---

### Correlation Analysis

![Correlation Heatmap](images/correlation_heatmap.png)

The correlation analysis highlights relationships among customer characteristics and identifies variables with stronger associations to churn.

---

## Machine Learning Models

Several classification algorithms were trained and evaluated.

### Models Used

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier

---

## Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Performance Comparison

| Model | Accuracy |
|---------|---------|
| Logistic Regression | XX% |
| Decision Tree | XX% |
| Random Forest | XX% |

*(Replace with actual results from your analysis.)*

---

## Feature Importance Analysis

![Feature Importance](images/feature_importance.png)

The Random Forest model was used to identify the most influential predictors of customer churn.

Key drivers typically include:

- Contract Type
- Tenure
- Monthly Charges
- Total Charges
- Internet Service Type

Understanding these factors helps the business focus retention efforts where they are most impactful.

---

## Key Findings

The analysis revealed several important patterns:

### High-Risk Customers

Customers are more likely to churn when they:

- Have month-to-month contracts
- Have short customer tenure
- Pay higher monthly charges
- Use electronic checks
- Recently joined the service

### Retention Factors

Customers are less likely to churn when they:

- Maintain long-term contracts
- Remain with the company for extended periods
- Use automatic payment methods

---

## Business Recommendations

Based on the analysis, the following recommendations are proposed:

### 1. Encourage Long-Term Contracts

Offer incentives that encourage customers to move from month-to-month contracts to annual agreements.

### 2. Improve Early Customer Experience

Develop onboarding and engagement programs targeting new customers during their first year.

### 3. Monitor High-Risk Segments

Identify customers with high monthly charges and implement targeted retention campaigns.

### 4. Promote Automatic Payments

Encourage customers to adopt automated billing options to increase convenience and retention.

### 5. Deploy Predictive Monitoring

Integrate churn prediction models into operational workflows to identify at-risk customers before they leave.

---

## Future Improvements

Potential extensions of this project include:

- Hyperparameter optimization
- XGBoost implementation
- Customer segmentation analysis
- Interactive dashboard development
- Real-time churn monitoring pipeline
- Deployment using Streamlit

---

## How to Run the Project

### Clone the Repository

```bash
git clone https://github.com/your-username/telco-customer-churn-analysis.git
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/Telco_Customer_Churn_Analysis.ipynb
```

---

## Author

Zhaina Abdulla

Aspiring Data Analyst / Data Scientist with interests in analytics, machine learning, business intelligence, and data-driven decision making.

---

## License

This project is licensed under the MIT License.
