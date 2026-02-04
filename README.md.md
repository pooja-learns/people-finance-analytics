# People \& Finance Analytics Platform –

Employee Attrition



Predicting which employees are at risk of leaving using machine learning and HR analytics.



Project Overview



This project analyzes the IBM HR Analytics Employee Attrition dataset to understand key drivers of attrition and build models that predict which employees are likely to leave. It is part of a broader People \& Finance Analytics Platform aimed at supporting data‑driven HR decisions.



Objectives



Explore HR data to identify patterns associated with employee attrition.

​



Build baseline and advanced classification models to predict attrition risk.



Provide interpretable insights that HR teams can use for retention strategies.



Data

Source: IBM HR Analytics Employee Attrition \& Performance dataset (publicly available).



Target variable: Attrition (Yes/No), converted to binary 1/0.



Key features (examples): Age, JobRole, MonthlyIncome, DistanceFromHome, JobSatisfaction, WorkLifeBalance, OverTime.



Basic preprocessing steps include handling data types, encoding categorical variables, and splitting into train/test sets.



Modeling Approach

Train/test split: Supervised classification with a held‑out test set.



Preprocessing:



One‑hot encoding for categorical features.



Class balancing to address the minority attrition class.



Models

Logistic Regression (baseline)



Simple, interpretable linear model.



Combined with one‑hot encoding and class balancing.



Random Forest (advanced)



Ensemble of decision trees to capture non‑linear relationships.



Configured with multiple trees and class weights for imbalance.



Model Performance (Test Set)

Metric	Logistic Regression	Random Forest

ROC‑AUC	0.74	0.80

Accuracy	0.69	0.85

Recall (1)	0.66	0.09

Precision (1)	0.29	0.67

These numbers show that Random Forest improves ranking ability and overall accuracy, but still struggles to recall enough leavers because attrition is a minority class.



You can describe this in one line:



Built and compared Logistic Regression and Random Forest models for employee attrition prediction, achieving up to 0.80 ROC‑AUC on the test set while highlighting challenges with minority class recall in imbalanced HR data.



Repository Structure

Example structure (adapt to your repo):



text

.

├── data/

│   └── raw/                # Original IBM HR dataset

├── notebooks/

│   └── 01\_employee\_retention\_eda.ipynb

├── models/

│   ├── employee\_attrition\_log\_reg.joblib

│   └── employee\_attrition\_random\_forest.joblib

├── src/

│   └── (optional) model and utils scripts

└── README.md



How to Run

Clone the repository.



Create and activate a virtual environment.



Install dependencies from requirements.txt.



Open 01\_employee\_retention\_eda.ipynb and run all cells to reproduce EDA and models





\# HR Employee Attrition Dashboard (Power BI)



This project is an HR \*\*Employee Attrition Dashboard\*\* built in Power BI as one module of my broader \*\*People \& Finance Analytics Platform\*\*. It helps HR quickly understand how many employees are leaving, which departments and job roles are most affected, and how attrition differs by gender.



\## Dataset



\- Source: Public HR Employee Attrition dataset (tabular CSV format).

\- Key columns used: EmployeeNumber, Attrition, Department, JobRole, Gender, Age, MaritalStatus, MonthlyIncome, etc.

\- Row level: One row per employee.



\## Business Problem



HR wants to answer:

\- What is our overall attrition rate?

\- Which departments and job roles have the highest attrition?

\- How does attrition differ by gender?

\- Can managers filter the view to focus on specific groups of employees?



\## Dashboard Features



\- \*\*Key KPIs\*\*

&nbsp; - Total Employees.

&nbsp; - Overall Attrition Rate (%) as a card (e.g., ~14.8% in my dataset).

&nbsp; - Total number of employees who left.



\- \*\*Breakdown Visuals\*\*

&nbsp; - Column chart: \*\*Attrition by Department (Yes only)\*\*.

&nbsp; - Column chart: \*\*Attrition by Job Role (Yes only)\*\*.

&nbsp; - Basic comparisons using counts of EmployeeNumber.



\- \*\*Interactive Filters\*\*

&nbsp; - \*\*Gender slicer\*\* to filter all visuals (e.g., see attrition for Female only or Male only).



\- \*\*Design\*\*

&nbsp; - Single‑page, beginner‑friendly layout.

&nbsp; - Clean color theme and simple background to keep charts readable.



\## Key Insights (Example from my dataset)



\- Overall attrition rate is around \*\*14.8%\*\*.

\- Certain departments and job roles show noticeably higher attrition than others.

\- Gender-based filtering helps HR see if attrition is skewed towards a particular gender.



> Note: These insights are illustrative and depend on the underlying dataset.



\## Tools Used



\- \*\*Power BI Desktop\*\* for data modeling and visualization.

\- Basic \*\*DAX measures\*\* for:

&nbsp; - Counting employees who left.

&nbsp; - Counting total employees.

&nbsp; - Calculating Attrition Rate % using `DIVIDE()`.



\## How to Open the Dashboard



1\. Download the `.pbix` file from this repository.

2\. Open it in \*\*Power BI Desktop\*\*.

3\. Use the Gender slicer and other visuals to explore attrition patterns.



\## Part of a Larger Project



This HR Attrition Dashboard is one module of my end‑to‑end \*\*People \& Finance Analytics Platform\*\*, which will also include:

\- Additional HR analytics (e.g., tenure, age, or performance).

\- Finance/expense analytics dashboards.



\## Screenshots



\*\*Overall view filtered by Female\*\*



!\[HR Attrition Dashboard – Female](desktop/hr\_attrition\_dashboard/\_female.png)



\*\*Overall view filtered by Male\*\*



!\[HR Attrition Dashboard – Male](desktop/hr\_attrition\_dashboard/male.png)





