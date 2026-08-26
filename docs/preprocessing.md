# Data Preprocessing

## Overview

Data preprocessing was performed to transform the raw House Prices dataset into a form suitable for machine learning.

The major preprocessing techniques used in the project are:

1. Handling Missing Values
2. Data Integration
3. One-Hot Encoding
4. Log Transformation
5. Feature Scaling
6. Train-Test Split
7. Cross Validation

## Handling Missing Values

Missing values were identified and handled according to the meaning and type of each feature.

For categorical features where the absence of a value indicates that a property does not contain that particular feature, missing values were represented using `"None"`.

Numerical features were handled using appropriate statistical replacement methods such as the median where required.

This prevents incomplete observations from causing errors during model training.

## Data Integration

The training and testing datasets were temporarily combined before common preprocessing operations were applied.

This ensures that categorical encoding and feature transformations are performed consistently across both datasets.

After preprocessing, the combined dataset was separated back into training and testing portions.

## One-Hot Encoding

Categorical variables were converted into numerical form using One-Hot Encoding.

Each category is represented by a separate binary feature.

For example, a categorical feature such as `Neighborhood` is converted into multiple columns representing individual neighborhoods.

This allows regression algorithms to process categorical information without assigning an artificial numerical order to categories.

## Log Transformation

Numerical features with substantial skewness were identified using their skewness values.

Features with an absolute skewness greater than `0.75` were log-transformed using:

```python
np.log1p()
```

### Feature Scaling

- The target variable `SalePrice` was also log-transformed to reduce its strong right skew.
- The logarithmic transformation helps make the distributions more suitable for regression modeling and reduces the influence of extremely large values.

- Robust Scaling was used for numerical data where appropriate.
- Robust Scaling uses the median and interquartile range instead of the mean and standard deviation.
- This makes it less sensitive to extreme values and outliers.

### Train-Test Split

- The available training data was divided into separate training and validation portions during model evaluation.
- The training portion was used to fit the models, while the validation portion was used to assess their performance on unseen observations.

### Cross Validation

- Five-Fold Cross Validation was used to compare the regression models.
- The training data was divided into five folds.

For each iteration:

- Four folds were used for training.
- One fold was used for validation.
- The process was repeated until every fold had been used as the validation set.

- The resulting RMSE values were averaged to obtain a more reliable estimate of model performance.

### Preprocessing Goals

The preprocessing stage was designed to:

- Remove or appropriately replace missing values.
- Convert categorical variables into numerical form.
- Reduce skewness.
- Improve model compatibility.
- Maintain consistent transformations between training and test data.
- Prepare the dataset for regression modeling.