# Predicting Superconducting Critical Temperature with Machine Learning

This project explores machine learning methods for predicting the critical temperature (`critical_temp`) of superconducting materials from engineered material descriptors.

## Motivation
Superconducting materials are important in modern physics and materials science because they exhibit unusual electronic behavior and may support future technologies. Predicting critical temperature from material descriptors can help build an early screening pipeline for identifying promising superconducting candidates.

## Dataset
The project uses a real superconductivity dataset containing engineered numerical descriptors and the target variable `critical_temp`.

## Models Tested
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- Ridge Regression
- XGBoost Regressor

## Main Result
Among the tested models, **Random Forest** achieved the best performance on the current dataset.

## Additional Analysis
The notebook also includes:
- feature importance analysis
- correlation analysis
- target distribution visualization
- PCA-based feature-space visualization

## Key Takeaway
The results suggest that the relationship between engineered descriptors and critical temperature is strongly nonlinear, and that tree-based ensemble methods are especially suitable for this task.

## File
- `predicting_critical_temperature_ml.ipynb` — main project notebook
