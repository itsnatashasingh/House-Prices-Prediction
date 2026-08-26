# Model Evaluation

## Evaluation Metric

The primary evaluation metric used in this project is **Root Mean Squared Error (RMSE)**.

RMSE measures the average magnitude of prediction errors while giving greater weight to larger errors.

It is calculated as:

```text
RMSE = √(mean((Actual - Predicted)²))
```

A lower RMSE indicates better model performance.

## Log-Transformed Target

Because SalePrice is strongly right-skewed, the target was log-transformed during model development.

Therefore, the RMSE values reported during cross-validation represent error on the transformed target scale.

This is appropriate for comparing the regression models within the same modeling pipeline.

## Five-Fold Cross-Validation

Five-Fold Cross Validation was used to obtain a more reliable estimate of model performance.

Each model was evaluated across five different validation folds, and the resulting RMSE values were averaged.

This reduces dependence on a single train-validation split.

### Model Comparison

The resulting average cross-validation RMSE values were:

- Lasso Regression: `0.132640`
- Ridge Regression: `0.132821`
- Gradient Boosting Regressor: `0.133321`
- Extra Trees Regressor: `0.141416`
- Random Forest Regressor: `0.143468`
- Linear Regression: `0.145000`

### Model Selection

- Lasso Regression achieved the lowest average RMSE: `0.132640`.
- Therefore, Lasso Regression was selected as the final model.
- The difference between Lasso and Ridge was very small, while Gradient Boosting also produced a competitive result.

### Final Model Training

After model comparison, the selected Lasso Regression model was retrained using the complete available training dataset.

The final model was then used to generate predictions for the unseen test dataset.

### Feature Analysis

For the final Lasso model, feature coefficients were analyzed to identify influential features.

Since Lasso is a linear model, it does not provide the tree-based feature_importances_ attribute.

Instead, the absolute values of its coefficients were used to determine the relative importance of features.