# Telco Client Churn Analysis & Machine Learning

## 1. Business Problem
Telecommunication companies face significant revenue impacts when customers leave. This project identifies behavioral patterns tied to client attrition and builds predictive models.

## 2. Tech Stack
* Python (Pandas, NumPy)
* Visualization: Matplotlib, Seaborn
* Modeling: Scikit-Learn (Logistic Regression, Random Forest)

## 3. Key Data Insights & Visualizations
### Insight A: Class Imbalance
The client base contains an unequal distribution of non-churners and churners, requiring stratified modeling adjustments.
![Churn Distribution](notebooks/churn_distribution.png)

### Insight B: Price Sensitivity Thresholds
Customers with mid-to-high monthly charges (specifically between $70–$110) demonstrate non-linear, heightened churn behavior compared to low-tier clients.
![Price Sensitivity](notebooks/price_sensitivity.png)

## 4. Model Performance
We evaluated multiple architectures including Random Forest to capture non-linear relationships. 
* **Confusion Matrix Diagnosed Metrics:** Tracked True Negatives and mitigated Type II Errors (False Negatives) to capture high-risk clients before they exit.
