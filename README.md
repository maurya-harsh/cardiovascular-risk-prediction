# Predictive Cardiovascular Analytics & Risk Classification

## Project Overview
This repository contains a comprehensive statistical analysis and predictive modeling framework designed to assess cardiovascular disease risk. Using a clinical dataset of 918 patient records, the project isolates key demographic, symptomatic, and physiological risk factors, culminating in a binary logistic regression classification model that achieved 86.04% diagnostic accuracy.

## Dataset Features
The analysis is based on the `heart_disease_data.csv` dataset, which includes:
* **Demographics:** Age, Sex
* **Symptomatic Indicators:** ChestPainType (ASY, ATA, NAP, TA), ExerciseAngina
* **Clinical Measurements:** RestingBP (mm Hg), Cholesterol (mg/dl), FastingBS, RestingECG, MaxHR (bpm), Oldpeak (ST depression), ST_Slope

## Methodology
1. **Data Engineering & Cleaning:** Addressed implicit missing values (e.g., zero-value cholesterol readings) using targeted median imputation. Preserved genuine physiological outliers (e.g., extreme blood pressure/cholesterol) to maintain critical clinical signals.
2. **Exploratory Data Analysis (EDA):** Engineered programmatic visualizations using Matplotlib to map feature distributions and cross-tabulate demographic vulnerabilities.
3. **Statistical Hypothesis Testing:** 
   * Chi-square tests of independence (e.g., identifying significant associations between Sex and Heart Disease).
   * Welch's independent samples t-tests to evaluate mean differences in Age and Cholesterol across patient subgroups.
4. **Predictive Modeling:** 
   * Evaluated feature relationships using Pearson correlation matrices and Multiple Linear Regression.
   * Built and evaluated a Binary Logistic Regression model to classify patient risk, calculating feature significance and Odds Ratios (OR).

## Key Discoveries
* **Demographic Risk:** Male patients exhibited a drastically higher susceptibility to heart disease, with model odds 5.58 times higher than female patients. 
* **Symptomatic Paradox:** Asymptomatic (ASY) chest pain presentation was the strongest clinical indicator of a positive diagnosis (79% incidence rate), whereas Typical/Atypical Angina correlated with lower risk.
* **Stress-Response Superiority:** Cardiac stress-induced metrics (ST-segment depression, exercise-induced angina, ST_Slope) proved to be significantly stronger predictors of heart disease than baseline physiological measurements like resting blood pressure or total cholesterol.

## Technologies Used
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Statistical Analysis:** SciPy, Statsmodels
* **Machine Learning:** Scikit-Learn
* **Data Visualization:** Matplotlib

## Author
**Harsh Suresh Maurya**  
*BSc in Statistics and Mathematics | Oracle Certified Data Science Professional*
