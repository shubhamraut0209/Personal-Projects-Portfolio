# 🎓 Education Analytics – Factors Affecting 10th & 12th Grade Marks

This project investigates the key factors influencing students' academic performance in 10th and 12th grade using multivariate regression analysis in R. The goal is to provide data-driven insights into how various time-based habits correlate with students' marks.

## 📌 Objective

- Analyze the impact of study-related activities on 10th and 12th grade marks.
- Use multivariate regression and correlation analysis to identify significant predictors.
- Visualize the data to aid interpretation and conclusions.

## 🧰 Technologies Used

- **Language:** R
- **IDE/Platform:** RStudio
- **Libraries:** `ggplot2`, `psych`, `ppcor`, `car`, `lmtest`, `olsrr`, `tseries`
- **Data Collection:** Google Forms (Primary data)

## 📊 Dataset Overview

**Sample Size:** 79 students  
**Target Variables:**
- `Y1`: Marks in 10th grade (in %)
- `Y2`: Marks in 12th grade (in %)

**Predictor Variables (All in hours):**
- `X1`: Time spent in school/college per day
- `X2`: Time spent in coaching/tuition per day
- `X3`: Time allocated to self-study per day
- `X4`: Time for relaxation per day
- `X5`: Time for physical exercise per day
- `X6`: Time for extra events per week

## 🔍 Methodology

1. **Data Collection** – Collected via Google Forms.
2. **Data Cleaning** – Ensured all responses were quantitative; no missing values.
3. **Exploratory Data Analysis** – Bar plots and pie charts to understand distribution.
4. **Modeling** – 
   - Multiple Linear Regression (MLR)
   - Forward Selection
   - Multivariate Regression
5. **Assumption Testing** – Normality, autocorrelation, heteroscedasticity, and multicollinearity checks.

## 📈 Key Results

### Model 1: Predicting 10th Grade Marks
`Y1 = 79.763 – 2.979X5 + 1.193X1`

- X5 (physical activity) was **significant**, X1 (school time) was **not**.
- R² ≈ 16.4%

### Model 2: Predicting 12th Grade Marks
`Y2 = 72.538 – 3.366X5 + 1.344X3`

- X5 was **significant**, X3 (self-study) was **not**.
- R² ≈ 11.94%

### Model 3: Full Multivariate Regression
- Both Y1 and Y2 predicted simultaneously using all six variables.
- Showed acceptable statistical assumptions except heteroscedasticity in model 3.

## 📌 Assumption Check Summary

| Assumption        | Model 1 | Model 2 | Model 3 |
|-------------------|---------|---------|---------|
| Normality         | ❌      | ✅      | ✅      |
| Autocorrelation   | ✅      | ✅      | ✅      |
| Heteroscedasticity| ✅      | ✅      | ❌      |
| Multicollinearity | ❌      | ❌      | ❌      |

✅ = No issue found, ❌ = Assumption violated

## 👤 Author

**Shubham Umesh Raut**  
M.Sc. Statistics Student  
Roll No: 11

## 📜 License

This project is open for academic and educational use. Please credit the author appropriately.
