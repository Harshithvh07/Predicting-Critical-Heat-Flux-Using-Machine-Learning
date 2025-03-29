# Predicting Critical Heat Flux Using Machine Learning

## Overview
This project focuses on predicting **Critical Heat Flux (CHF)** using machine learning techniques. The dataset originates from the paper *"On the prediction of critical heat flux using a physics-informed machine learning-aided framework."* The goal is to build predictive models and analyze feature importance to understand which factors influence CHF the most.

---

## Dataset Description
The dataset contains experimental **CHF measurements** along with boundary conditions like:
- **Pressure (MPa)**
- **Mass Flux (kg/m²s)**
- **Outlet Quality (x_e_out)**
- **Diameter (mm)**
- **Hydraulic Diameter (mm)**
- **Length (mm)**

The target variable is **CHF (MW/m²)**, which we aim to predict using machine learning models.

---

## Exploratory Data Analysis (EDA)
### Correlation Heatmap:
- A heatmap was generated to visualize relationships between features.
- Some features showed strong correlation, which can affect model performance.

### Feature Importance Analysis:
- Random Forest and Gradient Boosting were used to determine which parameters most affect CHF.
- Pressure, mass flux, and outlet quality had the highest importance scores.

---

## Machine Learning Models & Performance

| Model                | RMSE  | MAE   | R² Score |
|----------------------|--------|--------|----------|
| **Linear Regression**  | 1.338 | 0.778 | 0.642 |
| **Random Forest**      | 0.484 | 0.314 | 0.871 |
| **Gradient Boosting**  | 0.461 | 0.409 | 0.877 |
| **K-Nearest Neighbors** | 0.684 | 0.436 | 0.817 |

✅ **Best Model:** **Gradient Boosting (R² = 0.877, RMSE = 0.461)**  
✅ **Random Forest performed similarly with slightly lower RMSE.**  
✅ **Linear Regression struggled due to non-linearity in data.**  

---

## Project Workflow
1. **Data Preprocessing:** Converted non-numeric values, handled missing data, and encoded categorical features.
2. **EDA:** Correlation analysis, feature distributions, and insights.
3. **Model Training:** Built and tested multiple regression models.
4. **Feature Importance Analysis:** Identified key factors affecting CHF.
5. **Performance Evaluation:** Compared RMSE, MAE, and R² scores across models.

---

## Key Takeaways
✔ **Gradient Boosting performed the best, capturing complex relationships in CHF prediction.**  
✔ **Random Forest also showed strong performance, validating the model's reliability.**  
✔ **Linear Regression struggled due to the non-linear nature of the data.**  
✔ **Feature importance analysis highlighted pressure, mass flux, and outlet quality as key predictors.**  

---

## How to Use This Project
### Setup & Installation
```bash
pip install pandas seaborn matplotlib scikit-learn
```

### Running the Project
1. Place the dataset in the same directory as the script.
2. Run `python heat_flux.ipynb` to execute the analysis.
3. Review the correlation heatmap, feature importance plots, and model results.

---

## References
- **Dataset Source:** Zhao, Xingang (2020), Mendeley Data.
- **Research Paper:** DOI: [10.1016/j.applthermaleng.2019.114540](https://doi.org/10.1016/j.applthermaleng.2019.114540)

