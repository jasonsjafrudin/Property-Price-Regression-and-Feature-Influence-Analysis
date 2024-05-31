# Property-Price-Regression-and-Feature-Influence-Analysis

This repo contains complete pipeline for conducting EDA, building machine learning model for predicting property prices, and identifying how different features influence the model. I have utilized mean absolute percent error as the basis for model evaluation. 

## EDA Insights:
- nearly half of year_built and leasures_available values are NULL
- 5 Cateogrical Variable, 3 Integer Variable, 7 Float Variable
- Correlation Analysis
<img width="307" alt="image" src="https://github.com/jasonsjafrudin/Property-Price-Regression-and-Feature-Influence-Analysis/assets/61297201/192f4440-fdda-44f0-95d1-93266ec2f6a1">

loan and year_built has lowest correlations with out target variable (price), while, area and bathrooms has strongest correlation with price.

- unique values of Categorical Features:
  <img width="258" alt="image" src="https://github.com/jasonsjafrudin/Property-Price-Regression-and-Feature-Influence-Analysis/assets/61297201/f4857683-5c82-415a-abb8-5050b7e910aa">
based on results, I aim to reduce leasures_available unique values; I had achieved this through lowering all case letters, succesfully reducing from 258 to 13 unique values.



## My Regresstion Model (XGBoost):
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


