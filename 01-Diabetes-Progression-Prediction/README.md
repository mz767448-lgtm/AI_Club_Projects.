# Diabetes Progression Prediction Using Regression

## 1. Project Overview

This project focuses on predicting diabetes disease progression using Machine Learning Regression algorithms.

The main objective is to explore the relationship between different medical features and diabetes progression by implementing and comparing multiple regression models.

## 2. Dataset Description

The dataset was obtained from the Scikit-learn library using `load_diabetes()`.

- Number of Samples: 442
- Number of Input Features: 10
- Target Variable: Diabetes Progression
- Total Columns: 11
- Missing Values: 0
- Duplicate Rows: 0

### Features
- age
- sex
- bmi
- bp
- s1, s2, s3, s4, s5, s6

The target represents a quantitative measure of diabetes disease progression, not a binary diagnosis.

## 3. Data Analysis & Preprocessing

The following steps were performed:

- Data loading and exploration.
- Dataset inspection using Pandas.
- Checking missing values and duplicates.
- Statistical analysis using `describe()`.
- Correlation analysis.
- Data visualization using Matplotlib and Seaborn.
- Outlier detection using the IQR method.
- Feature and target separation.
- Train-test splitting (80% training, 20% testing).

Note: Outliers were identified and analyzed but were not removed from the dataset.

## 4. Models Implemented

Three main regression approaches were explored:

### Simple Linear Regression
- Used BMI as the single input feature.
- Analyzed the relationship between BMI and diabetes progression.

### Multiple Linear Regression
- Used all 10 input features.
- Evaluated the contribution of multiple features to prediction performance.

### Polynomial Regression
- Used Polynomial Features with degree 2.
- Tested both BMI-based and all-feature polynomial models.

## 5. Model Evaluation

Models were evaluated using:

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- RMSE (Root Mean Squared Error)
- R² Score (Coefficient of Determination)

### Results Comparison

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Simple Linear Regression | 52.26 | 63.73 | 0.233 |
| Multiple Linear Regression | 42.79 | 53.85 | 0.453 |
| Polynomial Regression (BMI) | 52.38 | 63.91 | 0.229 |
| Polynomial Regression (All Features) | 43.58 | 55.64 | 0.416 |

## 6. Feature Selection & Model Optimization

Additional experiments were performed to improve model evaluation:

- Feature Selection using SelectKBest.
- Feature scoring using f_regression.
- Comparing different numbers of selected features (k = 3, 5, 7, 10).
- 5-Fold Cross Validation using KFold.
- Hyperparameter Tuning using GridSearchCV.
- Pipeline implementation.

The GridSearchCV process selected 10 features as the best configuration based on cross-validation R².

Best Cross-Validation R²: 0.4804

## 7. Visualization & Residual Analysis

The project includes visualizations such as:

- BMI vs Diabetes Progression.
- Correlation Heatmap.
- Outlier Detection using Boxplots.
- Actual vs Predicted Values.
- Residual Analysis.

## 8. Final Conclusion

Multiple Linear Regression achieved the best overall performance among the main regression models evaluated on the test set.

It achieved:

- MAE: 42.79
- RMSE: 53.85
- R² Score: 0.453

The experiments showed that using multiple features improved prediction performance compared with using BMI alone.

This project provided practical experience in data analysis, regression modeling, feature selection, model evaluation, and cross-validation.

## 9. Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 10. Project Files

- `Diabetes_Regression_Project.ipynb`: Complete project implementation.
- `diabetes.csv`: Dataset used in the project.
- `requirements.txt`: Required Python libraries.

## 11. How to Run

1. Clone or download this repository.
2. Install the required libraries:

```bash
pip install -r requirements.txt
```

3. Open the Jupyter Notebook or upload it to Google Colab.
4. Run the notebook cells sequentially.
