# predicting-superconducting-tc
Machine learning project for predicting superconducting critical temperature from engineered material descriptors
# Predicting Superconducting Critical Temperature with Machine Learning

This project explores machine learning approaches for predicting the critical temperature (`critical_temp`) of superconducting materials using engineered material descriptors.

## Project Goal
The goal of this project is to compare several regression models and evaluate how well they predict superconducting critical temperature from material-related numerical descriptors.

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
The project also includes:
- feature importance analysis
- correlation analysis
- target distribution visualization
- PCA-based visualization of feature-space structure

## Conclusion
The results suggest that the relationship between engineered descriptors and critical temperature is strongly nonlinear, and that tree-based ensemble methods are especially suitable for this task.

## Files
- `predicting_critical_temperature_ml.ipynb` — main project notebook
