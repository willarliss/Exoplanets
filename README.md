# Exoplanets
This project builds a semi-supervised learning model for exoplanet detection. The data come from [kaggle](https://www.kaggle.com/keplersmachines/kepler-labelled-time-series-data).

Two rounds of the Local Outlier Factor (LOF) algorithm are used in the solution presented here. The first round performs LOF on its respective training set and determines outliers that are present within. These outliers are then removed in order to reduce noise in the training data. The second round performs LOF on the reduced training set then predicts novelties that may be present in the testing set. Testing observations predicted to be novelties are labeled as exoplanet observations and those not are labeled as non-exoplanet observations.

This yielded accuracy of 0.6889, specificity of 0.6875 and sensitivity 0.6905. Although the accuracy is not particularly high, the model correctly identified 69% of all the exoplanets and the non-exoplanets. This is significantly better than the supervised model, as it catches 2 of every 3 exoplanets instead of 0.
