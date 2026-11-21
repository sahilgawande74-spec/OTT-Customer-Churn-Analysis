📺 OTT Customer Churn Analysis & Customer Retention Insights

End-to-End Data Analytics Project | SQL • Python • SQLite • Data Visualization

Who is leaving, why are they leaving, and how much revenue is at risk?

An end-to-end data analytics project focused on understanding customer churn behaviour in the OTT (Over-The-Top) streaming industry. This project uses SQL and Python to analyze customer demographics, subscription patterns, support interactions, churn drivers, and revenue impact to generate actionable customer retention strategies.

⸻

📌 1. Project Overview

In the highly competitive OTT streaming industry, retaining existing subscribers is essential for sustainable business growth.

This project analyzes customer, subscription, and customer support data to identify churn patterns, understand why subscribers leave, and highlight opportunities to improve customer retention.

The analysis focuses on three key business questions:

* WHO: Which customers are leaving?
* WHY: What factors influence customer churn?
* WHEN: When are customers most likely to leave?

The objective is to transform raw customer data into meaningful business insights and actionable retention recommendations.

🎯 2. Project Objectives

* Extract relational data from a SQLite database using Python.
* Perform data cleaning and preprocessing.
* Handle missing values, duplicates, and inconsistent data.
* Perform feature engineering to calculate customer tenure, age, churn flags, and risk categories.
* Calculate important business KPIs such as churn rate, retention rate, ARPU, and revenue at risk.
* Identify churn patterns across subscription plans, contract types, and acquisition channels.
* Analyze the relationship between customer support interactions and churn.
* Generate business insights and customer retention strategies.

🛠️ 3. Tools & Technologies

Technology	Purpose
Python	Data analysis and preprocessing
SQLite	Relational database management
SQL	Data extraction and querying
Pandas	Data manipulation and analysis
NumPy	Data transformation and feature engineering
Matplotlib	Data visualization
Seaborn	Statistical visualization
Jupyter Notebook	Interactive analysis and documentation

📂 4. Dataset & Database Structure

The project uses a SQLite database named customer_churn.db, containing three relational tables connected through customerid.

Table Name	Description	Records
db_customer	Customer demographic information	21
db_subscription	Subscription and churn details	21
db_support	Customer complaints and support interactions	9

Key Dataset Attributes

Customer Table

* Customer ID
* Customer Name
* Country
* State
* Gender
* Date of Birth

Subscription Table

* Subscription Start Date
* Subscription Type
* Plan Type
* Contract Type
* Renewal Date
* Cancellation Date
* Cancellation Reason
* Monthly Charges
* Customer Lifetime Value (CLTV)
* Churn Score

Support Table

* Complaint Date
* Escalations
* CSAT Score
* Customer Comments

🔄 5. Project Workflow

Step 1: Database Connection & Data Extraction

* Connected Python to SQLite using sqlite3.
* Retrieved database tables using SQL queries.
* Imported relational tables into Pandas DataFrames.
* Inspected table structures, column names, and data types.

Step 2: Data Cleaning & Preprocessing

Performed the following data cleaning activities:

* Renamed the name column to customer_name.
* Removed irrelevant columns such as interests and pincode due to missing values.
* Standardized gender values (Men/Women to Male/Female).
* Handled missing country values using state-to-country mapping.
* Converted date columns into appropriate datetime formats.
* Identified duplicate customer support records.
* Created complaint counts before handling duplicate support records.
* Merged customer, subscription, and support tables using LEFT JOIN logic.
* Exported the final cleaned dataset into CSV format.

Step 3: Feature Engineering

Created additional analytical features:

* churn_flag: Identifies whether a customer has cancelled their subscription.
* tenure_days: Calculates the number of days a customer has been subscribed.
* customer_age: Calculates customer age from date of birth.
* churn_risk: Categorizes customers into Low, Medium, and High risk.

Churn Risk Classification

Risk Category	Churn Score
Low	Below 50
Medium	50–69
High	70 and above

Step 4: Exploratory Data Analysis (EDA)

Analyzed customer behaviour and churn patterns across multiple dimensions:

* Churn rate by subscription plan.
* Churn rate by contract type.
* Churn rate by acquisition channel.
* State-wise customer churn.
* Monthly cancellation trends.
* Customer tenure analysis.
* Cancellation reasons.
* Customer support escalations and CSAT scores.
* Relationship between churn risk and customer retention.

Step 5: KPI & Business Metrics Calculation

Calculated important business performance indicators:

KPI	Description
Churn Rate	Percentage of customers who cancelled
Retention Rate	Percentage of customers retained
ARPU	Average Revenue Per User
Monthly Recurring Revenue	Total monthly subscription charges
Revenue at Risk	Revenue lost from churned customers
Customer Tenure	Average subscription duration
CLTV	Customer Lifetime Value
Escalation Rate	Customer support escalation percentage
Average Complaints	Average complaints per customer

📊 6. Key Business Insights & Findings

1. Overall Customer Churn

* Total customers analyzed: 21
* Churned customers: 6
* Overall churn rate: 28.6%
* Customer retention rate: 71.4%

2. Contract Type Analysis

Monthly subscription customers show significantly higher churn than annual subscribers.

Contract Type	Churn Rate
Monthly	55.6%
Annual	8.3%

Insight: Monthly subscribers are approximately 6.7 times more likely to churn than annual subscribers.

3. Subscription Plan Analysis

Plan Type	Churn Rate
Basic	60.0%
Standard	22.2%
Premium	14.3%

Insight: Basic subscribers have the highest churn rate, making the Basic plan an important area for retention improvement.

4. Acquisition Channel Analysis

Acquisition Channel	Churn Rate
Referral	83.3%
Paid	16.7%
Organic	0%

Key Finding: All five customers with both referral acquisition and monthly contracts churned (5 out of 5).

5. Customer Support Analysis

* 6 out of 7 customers who contacted support eventually churned.
* All 4 customers with escalated support cases churned.
* No customers without complaints churned in this dataset.
* Churned customers who rated support had an average CSAT score of 34/100.

Insight: Customer support interactions and unresolved escalations can be important early-warning indicators for customer churn.

6. Churn Reasons & Customer Behaviour

The major cancellation reasons identified were:

* Switching to competitors.
* Pricing concerns.
* Content-related dissatisfaction.
* Streaming quality issues.
* Forgetting to cancel a trial.

Switching to a competitor was the most common individual reason, accounting for 2 of the 6 cancellations.

7. Revenue Impact Analysis

Metric	Value
Total Monthly Revenue	395.79
Monthly Revenue Lost	73.94
MRR Lost Percentage	18.7%
Total CLTV	17,294
CLTV Lost	2,047
CLTV Lost Percentage	11.8%

Insight: Customer churn resulted in an estimated 18.7% loss of monthly recurring revenue.

8. Churn Risk Analysis

* All 6 churned customers had churn scores of 76 or higher.
* All retained customers had scores of 62 or lower.
* A churn score threshold of 70+ identified all six churned customers without false alarms in this dataset.

This indicates that churn scores can help prioritize customers for retention follow-up, although the result requires validation on larger independent data.

💡 7. Business Recommendations

Based on the analysis, the following strategies are recommended:

1. Promote Annual Subscriptions: Encourage monthly subscribers to switch to annual plans through discounts and exclusive content.
2. Improve Referral Programmes: Review referral incentives, onboarding, and the trial-to-paid conversion journey.
3. Strengthen Customer Support: Introduce early-warning alerts for support complaints and escalations, followed by faster resolution and customer follow-up.
4. Monitor High-Risk Customers: Prioritize customers with churn scores of 50 and above for proactive retention campaigns.
5. Improve Basic Plan Retention: Review pricing, content availability, and customer experience for Basic subscribers.
6. Improve Streaming Experience: Address streaming quality issues and monitor competitor offerings.
7. Improve Trial Communication: Make trial expiry dates and cancellation policies clearer to customers.

📁 8. Project Repository Structure

OTT-Customer-Churn-Analysis/
│
├── customer_churn.db
│
├── exported_churn_data.csv
│
├── Churn_analysis.ipynb
│
├── Churn_analysis.html
│
├── Churn_Analysis.pdf
│
├── Churn_Analysis Report.pdf
│
├── README.md
│
└── .gitignore

🚀 9. How to Run the Project

Prerequisites

* Python 3.x
* Jupyter Notebook
* SQLite
* Required Python libraries

Install Dependencies

pip install pandas numpy matplotlib seaborn

Steps to Execute

1. Clone or download this repository.
2. Keep customer_churn.db in the same directory as the notebook.
3. Open Churn_analysis.ipynb using Jupyter Notebook.
4. Execute the notebook cells sequentially.
5. Review the data cleaning, feature engineering, EDA, and business insights.
6. Explore exported_churn_data.csv for the cleaned and merged dataset.
7. Refer to the PDF reports for detailed business findings and recommendations.

⚠️ 10. Project Limitations

* The analysis is based on a small sample of 21 customers and 6 churn cases.
* State-wise and cancellation-reason groups have limited observations.
* Churn percentages are directional and should not be generalized to a larger customer population.
* The churn score may be derived from information related to the churn outcome, potentially overstating its predictive performance.
* Tenure and age calculations change when the notebook is re-executed on a different date.

The findings should be validated using a larger dataset before making production business decisions.

🔮 11. Future Scope

* Expand the analysis using a larger customer dataset.
* Build a machine learning-based churn prediction model.
* Experiment with Logistic Regression and Random Forest.
* Evaluate model performance using Precision, Recall, F1-score, and ROC-AUC.
* Incorporate customer viewing activity, watch time, and login frequency.
* Develop an interactive Power BI dashboard using the cleaned dataset.
* Build a proactive customer retention monitoring system.

👨‍💻 12. Author

Sahil Gawande

Aspiring Data Analyst | Data Analytics Enthusiast

Technical Skills: Python | SQL | SQLite | Pandas | NumPy | Matplotlib | Seaborn | Data Cleaning | EDA | Business Analysis

⸻

⭐ If you find this project useful, feel free to explore the repository and share your feedback!

Project Context: This project was developed using a guided dataset .The analysis, calculations, findings, and business recommendations presented here were developed as part of my project work.
