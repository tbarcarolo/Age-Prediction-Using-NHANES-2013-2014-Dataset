# Age-Prediction-Using-NHANES-2013-2014-Dataset

## Project Overview
This project aims to develop machine learning models for predicting age categories ("Senior" or "Adult") using health and nutrition data from the National Health and Nutrition Examination Survey (NHANES) 2013-2014. The goal is to create accurate models to assist healthcare professionals in understanding age-related health trends and identifying potential health issues early.

## Dataset
The dataset used for this project is the NHANES 2013-2014 Age Prediction Subset.

## Features
- **SEQN:** A unique identifier for each participant.
- **age_group:** Categorical age descriptor ("Senior" or "Adult").
- **RIDAGEYR:** Respondent's age in years.
- **RIAGENDR:** Respondent's gender (1 for male, 2 for female).
- **PAQ605:** Physical activity level (1 for active, 2 for inactive).
- **BMXBMI:** Body Mass Index (BMI).
- **LBXGLU:** Plasma glucose level.
- **DIQ010:** Diabetes indicator (1 for Yes, 2 for No, 3 for Borderline).
- **LBXGLT:** Glucose tolerance test result.
- **LBXIN:** Insulin level.

## Project Objective
The primary objective is to create machine learning models that can accurately predict whether an individual is classified as a "Senior" (age 60 or older) or "Adult" (younger than 60) based on health and nutrition data.

## Methodology

### Data Engineering
- **Data Cleaning:** Handled missing values through imputation or removal and managed outliers using winsorization.
- **Data Transformation:** Encoded categorical variables using `LabelEncoder` and created polynomial features with `PolynomialFeatures`.
- **Normalization:** Standardized features using `StandardScaler` to ensure equal weight across variables.

### Model Selection
- **Models Used:** K-Nearest Neighbors (KNN) and Support Vector Machine (SVM).
- **Baseline Model:** Mean Age Predictor (predicts the mean age from training data).

### Feature Selection
Utilized Exploratory Data Analysis (EDA) and domain knowledge to identify relevant features for age prediction.

### Cross-Validation and Hyperparameter Tuning
- Employed k-fold cross-validation to evaluate model performance.
- Conducted hyperparameter tuning using grid search to optimize model settings.

## Results
- **KNN Model:** Achieved an accuracy of 94.73%.
- **SVM Model:** Achieved an accuracy of 99.34%.

## Conclusion
The SVM model outperformed the KNN model in all performance metrics, demonstrating superior efficacy in accurately classifying both younger and older demographics. This project highlights the importance of model selection and tuning in achieving optimal results for age prediction using health data.
