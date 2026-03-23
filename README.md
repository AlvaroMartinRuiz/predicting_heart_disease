# Predicting Heart Disease

![R](https://img.shields.io/badge/Language-R-276DC3?style=for-the-badge&logo=r)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange?style=for-the-badge)

This repository contains a comprehensive data science and machine learning project aimed at predicting cardiovascular disease (Heart Failure) in patients using 11 distinct medical features.

## 📖 Overview

Heart failure is one of the leading causes of mortality globally. By leveraging historical medical data (such as resting blood pressure, cholesterol, maximum heart rate, and chest pain type), this project develops several predictive models to ascertain the likelihood of a patient having a heart disease.

### Key Features Used
* Age, Sex, ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope.

## ⚙️ Methodology

Detailed exploratory data analysis (EDA), preprocessing, and modeling are available inside `HWK2_AlvaroMartin.Rmd`. Key steps included:

1. **Exploratory Data Analysis & Cleaning**: 
   * Handled extensive missing values via `knnImpute` and Random Forest (`mice`).
   * Visualized distributions and correlations (e.g., using `GGally`, Boxplots, and Density plots).
2. **Modeling Approaches**:
   * **Binary Logistic Regression**: Established base probabilities with threshold adjustments tailored towards optimizing **Sensitivity** (prioritizing the reduction of false negatives in medical diagnostics).
   * **Penalized Logistic Regression**: Used `glmnet` with cross-validation to find the optimal $\lambda$ and $\alpha$ hyperparameters.
   * **Decision Trees (`rpart`)**: Built intuitive logical trees to visualize feature splits (e.g., the high impact of the `ST_Slope` variable).
   * **Random Forest**: Implemented ensemble learning to greatly stabilize the predictive performance and achieve high accuracy alongside >95% Sensitivity.

## 🚀 How to View
To view the analysis without running the code:
1. Open the pre-compiled `HWK2_AlvaroMartin.html` file in any modern web browser.

To run the R Markdown notebook directly:
```bash
git clone https://github.com/AlvaroMartinRuiz/predicting_heart_disease.git
```
Open `HWK2_AlvaroMartin.Rmd` in RStudio, install the required packages (such as `caret`, `mice`, `randomForest`, `glmnet`, and `pROC`), and click **Knit**.
