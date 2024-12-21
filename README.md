# Predictive-Modeling-for-Obesity-Analysis.

**Project Overview**
The Obesity Forecast project explores predictive modeling techniques to analyze Body Mass Index (BMI) trends. The primary goal is to identify individuals at risk of obesity by analyzing various lifestyle and hereditary factors. This project leverages multiple machine learning models to predict obesity likelihood and proposes targeted interventions based on data-driven insights.

**Introduction**
Obesity is a significant public health challenge worldwide, linked to numerous chronic diseases. This project aims to develop a robust predictive framework using machine learning to assess obesity risk factors. Our approach includes:

- Cleaning and preprocessing a comprehensive dataset.
- Engineering features for improved predictive accuracy.
- Training and evaluating various machine learning models.
- Identifying the best model based on performance metrics such as AUC and RMSE.

**Dataset**
The dataset consists of various demographic, lifestyle, and hereditary factors, including:

**Demographics:** 
- Age, Gender.
**Lifestyle Habits**
  Dietary patterns: Frequency of high-calorie foods (FAVC), vegetable consumption (FCVC), main meals (NCP), consumption of food between meals (CAEC).

**Physical activity:**
- Frequency of physical activity (FAF), transportation modes (MTRANS).
- Technology usage: Time using technological devices (TUE).
- Alcohol consumption (CALC) and daily water intake (CH20).

**Hereditary Factors:**
- Family history of overweight/obesity.
- Smoking habits.

​![image](https://github.com/user-attachments/assets/e93e2502-2cc9-4bae-88e0-90d02a21b501)

**Data Preprocessing** 
Data preprocessing involved several steps to ensure quality and relevance:

**Data Cleaning:**
Handled missing or inconsistent values.
Validated data types for all columns.

**Feature Engineering:**
Recoded categorical variables (e.g., grouped transportation modes and obesity levels).
Removed target leakage variables (e.g., Weight and Height for models predicting BMI).

**Normalization:**
Applied normalization to numeric variables for consistent scaling.

**Splitting:**
Split the dataset into training and validation subsets (random seed = 888).

**Models Developed**

A variety of predictive models were trained and evaluated:

**Linear Regression**

Target variable: BMI.
Key drops: Weight, Height (to avoid target leakage); Gender; and SCC (calorie monitoring bias).

**Performance:** 

RMSE (Training): 5.7
RMSE (Validation): 5.8

**Logistic Regression** 

Target variable: Obesity categories.
Dropped variables based on feature significance, including Age, FAF, and FCVC.

**Decision Tree**

Splits: 14
AUC: 0.8770

**Bootstrap Forest**
AUC: 0.9300 (Best performing model).

**Boosted Tree**
AUC: 0.9132

**Neural Network**
AUC: 0.9007
Alternative configurations tested activation functions: TANH, NLINEAR, NGAUSSIAN.

**Conclusion**
Through rigorous model development and evaluation:
- The Bootstrap Forest model outperformed others with an AUC of 0.9300.
- Key predictors, such as family history and lifestyle variables, are critical in assessing obesity risk.
- This analysis underscores the importance of integrating familial predisposition and personal habits in predictive modeling for healthcare.
