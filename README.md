# NHANES Fasting Glucose Prediction

Author: Robert Giurcanu  
Date: November 2025  

## About this Project
This project predicts fasting glucose levels using NHANES 2021–2023 data. Two models were implemented:

- Linear Regression
- Random Forest Regression  

This projects goal is to compare model performance and understand which features (age, BMI, diabetes status, and dietary intake) most influence glucose levels.

## Data

- Demographics: Age, Sex (DEMO_L.XPT)  
- Glucose & Biomarkers: Fasting glucose (GLU_L.XPT), HbA1c (GHB_L.XPT)  
- Dietary Intake: Calories, Protein, Carbs, Sugar, Fiber, Fats, Cholesterol, Sodium, Potassium (DR1TOT_L.XPT)  
- Body Measures: BMI, Waist circumference (BMX_L.XPT)  
- Diabetes Status: Diabetes diagnosis (DIQ_L.XPT)  

## Results

**Linear Regression**  
R²: 0.33    
MSE: 773  
Clinical Accuracy (within 10%): 68%  
Clinical Accuracy (within 15%): 81%  

**Random Forest**  
R²: 0.36  
MSE: 731  
Clinical Accuracy (within 10%): 66%  
Clinical Accuracy (within 15%): 79%  

Features:  
Diabetes status, waist circumference, and age were the strongest predictors in both models. Other variables, like calories, sex, and prediabetes status, were of less influence.

Residual analysis shows Random Forest predictions are generally centered around zero, while linear regression shows larger deviations for higher glucose values (~140–170 mg/dL).
