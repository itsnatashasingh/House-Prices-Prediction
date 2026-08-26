# Feature Engineering

## Overview

Feature Engineering is the process of creating new variables from existing information in order to provide machine learning models with more meaningful representations of the data.

Several features were engineered in this project to capture broader characteristics of residential properties.

## TotalHouseArea

`TotalHouseArea` combines the major floor-area measurements of a property.

This feature provides the model with an overall representation of the property's size instead of requiring it to independently interpret several floor-area variables.

## TotalBathrooms

`TotalBathrooms` combines the property's bathroom information into a single feature.

This provides a more complete representation of the property's total bathroom capacity.

## TotalPorchSF

`TotalPorchSF` combines the available porch and outdoor-area measurements.

This captures the overall amount of porch space associated with a property.

## HouseAge

`HouseAge` represents the age of the property at the time of sale.

It is derived using the year the property was sold and the year it was originally built.

A property that was built more recently generally has a smaller `HouseAge` value.

## RemodelAge

`RemodelAge` represents the age of the most recent remodeling work.

This provides the model with information about how recently a property was updated.

## TotalRooms

`TotalRooms` combines relevant room-count information to provide a broader representation of the property's size and layout.

## HasGarage

`HasGarage` is a binary feature indicating whether the property has a garage.

This simplifies multiple garage-related variables into an indicator of garage availability.

## HasBasement

`HasBasement` indicates whether a property has a basement.

The feature allows the model to distinguish between properties with and without basement space.

## HasFireplace

`HasFireplace` indicates whether a property contains a fireplace.

This captures the presence of an additional property characteristic that may contribute to house value.

## HasPool

`HasPool` indicates whether a property has a swimming pool.

Although pools are relatively uncommon in the dataset, their presence may provide useful information for price prediction.

## Importance of Feature Engineering

Feature engineering is important because raw variables do not always provide the most useful representation of a problem.

The engineered features in this project:

- Combine related measurements.
- Reduce the need for the model to infer certain relationships independently.
- Provide broader representations of property characteristics.
- Capture information about property age and amenities.
- Potentially improve predictive performance.

The feature importance/coefficients analysis also showed that `TotalHouseArea` became one of the most influential features in the final model.