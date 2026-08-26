# Exploratory Data Analysis

## Overview

Exploratory Data Analysis (EDA) was performed to understand the structure, distribution, relationships, and characteristics of the House Prices dataset before applying machine learning models.

The analysis focused on:

- Understanding the target variable.
- Identifying missing values.
- Examining numerical feature distributions.
- Studying relationships between features and `SalePrice`.
- Identifying highly correlated variables.
- Comparing property characteristics across categories.

## SalePrice Distribution

A histogram was used to examine the distribution of `SalePrice`.

The original target distribution is right-skewed, with a relatively large number of properties concentrated toward lower price ranges and fewer properties with very high sale prices.

This observation motivated the use of a logarithmic transformation during preprocessing.

## Missing Values

Missing values were examined across the dataset to identify features requiring preprocessing.

A bar plot was used to visualize the number of missing values across features.

Understanding missing data before model training is important because machine learning algorithms generally require complete numerical inputs.

## Correlation Analysis

A correlation matrix was calculated for numerical features.

A heatmap was used to visualize the correlations between variables.

Correlation analysis helps identify:

- Features strongly associated with `SalePrice`.
- Relationships between independent variables.
- Potential multicollinearity.
- Features that may be useful during model development.

## GrLivArea vs SalePrice

A scatter plot was used to examine the relationship between `GrLivArea` and `SalePrice`.

`GrLivArea` represents above-ground living area.

The visualization demonstrates a generally positive relationship between living area and house price: larger living areas tend to be associated with higher sale prices.

## Overall Quality and SalePrice

A box plot was used to compare `SalePrice` across different `OverallQual` categories.

This visualization demonstrates how construction and material quality are associated with differences in house prices.

## Neighborhood and SalePrice

A box plot was used to compare sale prices across neighborhoods.

This helps demonstrate the importance of location in residential property pricing and reveals differences in price distributions across neighborhoods.

## Garage Capacity and SalePrice

A box plot was used to examine differences in sale prices across garage capacity categories.

This provides insight into how garage availability and capacity relate to property value.

## Year Built

A histogram was used to examine the distribution of `YearBuilt`.

The visualization helps understand the age distribution of the properties represented in the dataset.

## House Style

A box plot was used to compare `SalePrice` across different house styles.

This allows differences in price distributions between property styles to be examined.

## Key EDA Findings

The exploratory analysis highlighted several important characteristics of the dataset:

1. `SalePrice` is strongly right-skewed.
2. House size is an important factor associated with sale price.
3. Overall quality has a strong relationship with property value.
4. Neighborhood contributes substantially to price variation.
5. Several numerical features exhibit substantial skewness.
6. The dataset contains missing values requiring appropriate treatment.
7. Multiple property characteristics are correlated with one another.

These findings informed the preprocessing and feature engineering stages of the project.