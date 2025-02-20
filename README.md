**Diabetes Progression Analysis & Dashboard**
---------------------------------------------

Overview
--------
This project performs Exploratory Data Analysis (EDA) on a diabetes progression dataset to uncover patterns, detect outliers, and understand feature importance. Using Python, Pandas, and Matplotlib, we explore dependencies between clinical features such as age, BMI, blood pressure, and serum measurements. The analysis is complemented by a Tableau dashboard that visualizes key insights into diabetes progression.

Dataset
-------
The dataset used in this project is from Stanford University’s Machine Learning Repository and contains 442 records of diabetes progression. The target variable "Y" represents the progression of diabetes. The dataset includes various clinical features like age, BMI, blood pressure, and serum measurements.

Dataset Link: [Stanford Diabetes Dataset](https://hastie.su.domains/Papers/LARS/diabetes.data)

Data Preparation
----------------
The data is loaded using Pandas, and basic checks are performed for missing values. Here's a snippet of how the dataset is loaded and prepared for analysis:

-------------------------------------------------
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

file_path = "diabetes.data.txt"
df = pd.read_csv(file_path, sep=r'\s+', header=0)

# Checking for missing values and data types
print(df.shape)
print(df.isnull().sum())
print(df.dtypes)
-------------------------------------------------

EDA Process
-----------
The Exploratory Data Analysis involves several steps:

Handling Outliers
-----------------
Outliers are detected using boxplots and the Interquartile Range (IQR) method:

-------------------------------------------------------------
plt.figure(figsize=(12, 6))
df.boxplot()
plt.xticks(rotation=45)
plt.title("Boxplot to detect outliers")
plt.show()

# Identifying outliers using IQR
Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3 - Q1
outliers = ((df < (Q1 - 1.5 * IQR)) | (df > (Q3 + 1.5 * IQR)))
-------------------------------------------------------------

Feature Correlation
-------------------
The correlation matrix is calculated and visualized using a heatmap:

----------------------------------------------------------------------------
correlation_with_target = df.corr()["Y"].abs().sort_values(ascending=False)
print(correlation_with_target)
----------------------------------------------------------------------------

Insights
--------
-> BMI is the most important feature influencing diabetes progression.
-> S5 and Blood Pressure (BP) also show a significant relationship with the target variable.
-> SEX has a minimal impact on diabetes progression, with a correlation of 0.04.
-> S3 has a negative correlation (-0.395), indicating that higher values of S3 are associated with lower diabetes risk.

Dashboard
The insights from the EDA are visualized through an interactive Tableau dashboard, providing an easy-to-understand view of the diabetes progression data.

View the Tableau Dashboard: https://public.tableau.com/views/DiabetesProgressionInsightsDashboard/DiabetesProgressionInsightsDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
