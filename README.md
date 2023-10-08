# Airbnb Booking Price Prediction Model
## Question 2:
 Let’s say we want to build a model to predict booking prices on Airbnb. Between linear regression and random forest regression, which model would perform better and why?

-This repository contains a machine learning model to predict booking prices on Airbnb.
Before we quickly answer “Random Forest”, let’s take a step back and put on our structured thinking cap to ask ourselves why and perhaps in real life, companies might take the other choice.

Questions to consider:
1) What are the features available for us to model?
If the features are mostly categorical, especially with large number of distinct values, then linear regression might not be a good choice because it can’t handle cardinality as well as random forest.

2) What are the underlying statistics of the features?
If extreme outliers are present and retained for valid reasons, then linear regression can be affected.

There are assumptions of linear regression that needs to be satisifed:
1) Linear relationship between indepedent and dependent variables
2) Residuals exhibits normality(mean of 0, unit variance)
3) Homoscedasticity: Variance of residuals is constant for all observations.
4) No multi-colinearity between indepedent variables.

## What is the definition of “better”?

We assume the definition refers to accuracy in prediction. Other definition could be processing speed, etc.



Solutions:
1) Extension of random forests: trees are grown where the terminal leaves contain linear regression models (eg.Cubist)
2) Neural networks
2) Use linear methods like linear regression

Business interpretability

Either models provide means for feature importance, which is helpful for business to understand the behavoir of the models or identify drivers behind the booking price.

## Model Selection

We explored two models for prediction:
- Linear Regression
- Random Forest Regression

Here's a brief comparison of the two models and their suitability for the task.

### Linear Regression

- Simple and interpretable.
- Assumes a linear relationship between predictors and booking prices.


### Random Forest Regression

- Can capture complex, nonlinear relationships.
- Robust to outliers.





## Conclusion

Based on your evaluation, you select the Random Forest Regression model for predicting Airbnb booking prices.Generally, random forest yields higher accuracy than linear regression but it cannot extrapolate values: unable to predict values beyond the range that it has observed during training time. In our context, this means that it cannot predict a sudden, extremely high increase in booking price that it hasn’t seen before.


