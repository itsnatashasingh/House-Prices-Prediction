# Results

## Model Performance

The six regression models were evaluated using five-fold cross-validation.

The final comparison was:

| Rank | Model | Average RMSE |
|---:|---|---:|
| 1 | **Lasso Regression** | **0.132640** |
| 2 | Ridge Regression | 0.132821 |
| 3 | Gradient Boosting Regressor | 0.133321 |
| 4 | Extra Trees Regressor | 0.141416 |
| 5 | Random Forest Regressor | 0.143468 |
| 6 | Linear Regression | 0.145000 |

Lower RMSE represents better performance.

## Best Model

The best-performing model according to five-fold cross-validation was:

**Lasso Regression**

with an average RMSE of:

```text
0.132640
```
- The model was subsequently retrained on the complete training dataset before generating predictions for the test dataset.

### Feature Analysis

- The final Lasso model's coefficients were analyzed to identify influential features.
- The top features included:
  1. `GrLivArea`
  2. `TotalHouseArea`
  3. `Condition2_PosN`
  4. `Neighborhood_StoneBr`
  5. `Neighborhood_Crawfor`
  6. `Neighborhood_NridgHt`
  7. `Neighborhood_NoRidge`
  8. `SaleType_New`
  9. `LotArea`
  10. `Exterior1st_BrkFace`

- `GrLivArea` and the engineered `TotalHouseArea` feature were among the strongest contributors to the model.
- This demonstrates the importance of property size in predicting residential sale prices.

### Kaggle Submission

- Predictions were generated for all observations in the test dataset and saved in the required Kaggle submission format:
  `Id,SalePrice`

- The generated file is:
  `submission.csv`

- The submission contains the original property IDs from the test dataset and the corresponding predicted sale prices.

### Conclusion

- The project demonstrates a complete supervised learning workflow for a real-world regression problem.

The workflow included:

- Dataset exploration.
- Exploratory Data Analysis.
- Missing value handling.
- One-Hot Encoding.
- Log transformation.
- Feature Engineering.
- Feature scaling.
- Multiple regression algorithms.
- Five-fold cross-validation.
- Model comparison.
- Final model selection.
- Feature coefficient analysis.
- Test-set prediction.
- Kaggle submission generation.

Lasso Regression produced the lowest cross-validation RMSE among the evaluated models and was selected as the final model.

The project demonstrates how appropriate preprocessing, feature engineering, model comparison, and systematic evaluation can be combined to build a machine learning solution for house price prediction.