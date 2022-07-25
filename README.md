# Data-Information-Analysis-Course-Project

## Varibales meaning:
**1. datetime** - hourly date + timestamp

**2. season** - 1 = spring, 2 = summer, 3 = fall, 4 = winter 

**3. holiday** - whether the day is considered a holiday 

**4. workingday** - whether the day is neither a weekend nor holiday 

**5. weather** - 1: Clear, Few clouds, Partly cloudy, Partly cloudy 

2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist 

3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds 

4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog 

**6. temp** - temperature in Celsius 

**7. atemp** - "feels like" temperature in Celsius 

**8. humidity** - relative humidity 

**9. windspeed** - wind speed 

**10. casual** - number of non-registered user rentals initiated

**11. registered** - number of registered user rentals initiated 

**12. count** - number of total rental


## Different sections:
This project includes 5 main parts (as it was stated in the project description): 
1. importing libraries
2. reading data and EDA
3. identifying missing values
4. covariance analysis, plotting some feagures for correlation, and finally, Feature Selection
5. implementation of regression models and model's evaluation

# Different models:
For final part (implemetation of models and picking the best one), I tried the following models (note that the first 2 models' evaluation was based on train test split):
1. OLS:                                        train error: 0.6927   test error: 0.6941
2. Polynomial degree 2 with OLS:               train error: 0.9442   test error: 0.9030
3. Ridge (alpha=30) and Polynomial degree=2:   best score (using grid search): 0.7722
4. Lasso (alpha=0.1) and Polynomial degree=2:  best score (using grid search): 0.7507

**5. GradientBoostingRegressor(learning_rate=0.2 , n_estimators=1700) = best score (using grid search for both parameters): 0.7829**

The last model was tested on train and test split, the result is: 

train error: 0.9717 , test error: 0.9291

As you can see there is a significant improvement in model prediction.

## Some other evaluation on our Final Model (Gradient Boosting Regressor):

### 10 Fold Cross Validation:
each of 10 folds cross val score is [0.32675005, 0.77683452, 0.89014942, 0.89915596, 0.88259923, 0.78774746, 0.89772115, 0.90159288, 0.92306765, 0.93011269]

the average total score is 0.821573100848334

 **I think one of the main problems was the first fold (for poor prediction) and I didn't know how to improve the model for that fold, if you have any idea, I would be really glad to discuss it with you :))**
 
### Other metrics:
MAE for our model (based on the splited dataset) is: 31.653471054038057

R2 for our model (based on the splited dataset) is: 0.9291877151233694

Median Absolute Error for our model (based on the splited dataset) is: 20.3309283779628

MSE for our model (based on the splited dataset) is: 2282.1789896620635

RMSE for our model (based on the splited dataset) is: 47.77215705473287

