**Diabetes Progression Analysis & Dashboard**
---------------------------------------------

Overview
--------
This project performs Exploratory Data Analysis (EDA) on a diabetes progression dataset to uncover patterns, detect outliers, and understand feature importance. Using Python, Pandas, and Matplotlib, we explore dependencies between clinical features such as age, BMI, blood pressure, and serum measurements. The analysis is complemented by a Tableau dashboard that visualizes key insights into diabetes progression.

Dataset
-------
The dataset used in this project is from Stanford University’s Machine Learning Repository and contains 442 records of diabetes progression. The target variable "Y" represents the progression of diabetes. The dataset includes various clinical features like age, BMI, blood pressure, and serum measurements.

Dataset Link: [Stanford Diabetes Dataset](https://hastie.su.domains/Papers/LARS/diabetes.data)

Insights
--------
-> BMI is the most important feature influencing diabetes progression.
-> S5 and Blood Pressure (BP) also show a significant relationship with the target variable.
-> SEX has a minimal impact on diabetes progression, with a correlation of 0.04.
-> S3 has a negative correlation (-0.395), indicating that higher values of S3 are associated with lower diabetes risk.

Dashboard
The insights from the EDA are visualized through an interactive Tableau dashboard, providing an easy-to-understand view of the diabetes progression data.

View the Tableau Dashboard: https://public.tableau.com/views/DiabetesProgressionInsightsDashboard/DiabetesProgressionInsightsDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
