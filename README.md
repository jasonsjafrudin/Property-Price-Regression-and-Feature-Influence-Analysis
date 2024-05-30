# Property-Price-Regression-and-Feature-Influence-Analysis

This repo contains complete pipeline for conducting EDA, building machine learning model for predicting property prices, and identifying how different features influence the model. I have utilized mean absolute percent error as the basis for model evaluation. 

My Regresstion Model Summary:
For null values, numerical variables are imputed with their median, while categorical are imputed with their mode, with the exception of "leasures_available", in which null values are replaced with 'none'. Categorical variables undergo ordinal encoding as part of the X_train dataset. The optimized model utilizes XGBoost algorithm with decision trees as the base trees and with best parameters obtained from grid search; learning rate of 0.1, max_depth of 7, n_estimators/number of ensembles of 200, and default max_nodes of 6. The MAPE of the model is 0.18. The feature importance are ranked as follows:
1. parking_spots
2. type
3. area
4. attached_rooms
5. lon
6. bathrooms
7. lat
8. bedrooms
9. condo_fee
10. leasures_available
11. year_built
12. has_elevator
13. overall_condition


