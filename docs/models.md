# Machine Learning Models

## Overview

The project uses supervised machine learning regression algorithms to predict the continuous `SalePrice` target.

Six different regression models were trained and evaluated.

The models were:

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Random Forest Regressor
5. Extra Trees Regressor
6. Gradient Boosting Regressor

## Linear Regression

Linear Regression models the relationship between independent variables and a continuous target by fitting a linear equation.

It was included as a baseline regression model against which the other algorithms could be compared.

### Advantages

- Simple to understand.
- Fast to train.
- Easy to interpret.
- Useful as a baseline model.

## Ridge Regression

Ridge Regression is a regularized version of Linear Regression that applies an L2 penalty to the model coefficients.

Regularization helps reduce model complexity and can improve generalization when features are correlated.

### Advantages

- Reduces overfitting.
- Handles multicollinearity.
- Produces more stable coefficients.

## Lasso Regression

Lasso Regression applies an L1 regularization penalty.

The L1 penalty can shrink some coefficients toward zero, making Lasso useful for feature selection as well as regression.

Lasso achieved the lowest average cross-validation RMSE among the models evaluated in this project.

### Advantages

- Reduces overfitting.
- Performs implicit feature selection.
- Produces a simpler model.
- Handles high-dimensional feature sets effectively.

## Random Forest Regressor

Random Forest is an ensemble learning algorithm that combines predictions from multiple decision trees.

Each tree is trained using randomized subsets of the data and features, and their predictions are aggregated.

### Advantages

- Captures nonlinear relationships.
- Reduces overfitting compared with a single decision tree.
- Handles complex feature interactions.
- Provides feature importance.

## Extra Trees Regressor

Extra Trees, or Extremely Randomized Trees, is an ensemble tree-based algorithm that introduces additional randomness when constructing decision trees.

The predictions from multiple randomized trees are averaged.

### Advantages

- Captures nonlinear relationships.
- Handles high-dimensional datasets.
- Can model complex interactions.
- Provides feature importance.

## Gradient Boosting Regressor

Gradient Boosting builds an ensemble of decision trees sequentially.

Each new tree attempts to improve upon the errors made by the previous trees.

### Advantages

- Captures nonlinear relationships.
- Can achieve strong predictive performance.
- Learns from previous model errors.
- Works effectively with structured tabular data.

## Model Selection

The models were compared using five-fold cross-validation.

The model with the lowest average RMSE was selected as the best-performing model.

In the final evaluation, **Lasso Regression** achieved the lowest average RMSE and was therefore selected as the final model.