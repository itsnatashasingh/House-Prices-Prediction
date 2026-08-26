# Dataset

## Overview

This project uses the **House Prices: Advanced Regression Techniques** dataset from Kaggle.

The objective of the competition is to predict the final sale price of residential properties in Ames, Iowa, based on a wide range of characteristics describing each property.

The target variable for this project is:

```text
SalePrice
```

- Since `SalePrice` is a continuous numerical variable, this is a supervised learning regression problem.

### Dataset Files

The `data/` directory contains the following competition files:

- `train.csv` — Training dataset containing property features and the target `SalePrice`.
- `test.csv` — Test dataset containing property features without `SalePrice`.
- `sample_submission.csv` — Example submission file showing the required Kaggle submission format.

- The original competition also provides `data_description.txt`, which contains descriptions of the individual features.

### Training Dataset

The training dataset contains:

- Property identification information.
- Numerical property characteristics.
- Categorical property characteristics.
- Information about quality and condition.
- Garage and basement information.
- Exterior and interior characteristics.
- Sale information.
- The target variable, `SalePrice`.

### Test Dataset

- The test dataset contains the same general property characteristics as the training data but does not contain the target variable.
- After the model has been trained, it is used to generate `SalePrice` predictions for these properties.

### Target Variable

#### `SalePrice`

- `SalePrice` represents the final sale price of each residential property.
- Because the target is continuous, the project uses regression algorithms rather than classification algorithms.
- The target is log-transformed during model preparation to reduce skewness and improve regression performance.

### Dataset Preparation

- Before model training, the training and testing datasets are combined temporarily so that common preprocessing operations can be applied consistently.
- After preprocessing, the datasets are separated again for model training and prediction.

### Source

- The dataset is provided through the Kaggle **House Prices: Advanced Regression Techniques** competition.

- Kaggle Competition:
  https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques