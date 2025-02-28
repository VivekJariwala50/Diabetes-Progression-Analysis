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
- **SEX**: The coefficient is **-22.8596** with a **p-value of 0.000**, indicating that sex is a significant predictor of diabetes progression. Being female (**SEX=2**) is associated with a **22.86-unit decrease** in diabetes progression compared to males (**SEX=1**).
- **BMI**: The coefficient is **5.6030** with a **p-value of 0.000**, indicating that BMI is a significant predictor. A **1-unit increase** in BMI is associated with a **5.60-unit increase** in diabetes progression.
- **BP**: The coefficient is **1.1168** with a **p-value of 0.000**, indicating that blood pressure is a significant predictor. A **1-unit increase** in BP is associated with a **1.12-unit increase** in diabetes progression.
- **S5**: The coefficient is **68.4831** with a **p-value of 0.000**, indicating that S5 (a blood serum measurement) is a significant predictor. A **1-unit increase** in S5 is associated with a **68.48-unit increase** in diabetes progression.
- **AGE**: The coefficient is **-0.0364** with a **p-value of 0.867**, indicating that age does not significantly affect diabetes progression in this model.
- **S1**: The coefficient is **-1.0900** with a **p-value of 0.058**, which is close to the significance threshold but not statistically significant at the 5% level.
- **S2**, **S3**, **S4**, **S6**: These predictors have **p-values greater than 0.05**, indicating they do not significantly contribute to the model.

Dashboard
The insights from the EDA are visualized through an interactive Tableau dashboard, providing an easy-to-understand view of the diabetes progression data.

View the Tableau Dashboard: https://public.tableau.com/views/DiabetesProgressionInsightsDashboard/DiabetesProgressionInsightsDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
