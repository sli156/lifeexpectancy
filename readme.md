# Machine Learning Project - USF MSDS 699
### This repo contains course work from MSDS 699
As a member of cohort MSDS 621, this is my final project to utilize the methodologies that we acquired in the class.
I select the [Life Expectancy Dataset](https://www.kaggle.com/kumarajarshi/life-expectancy-who) collected by the WHO to build the prediction model for future human beings life expectancy.

### Introduction of the dataset
This dataset includes 2938 observations and 21 raw features including income facors, immunization facors, mortality factors, economic factors, social factors and other health related factors. 

For this dataset including life expectancy values from 2000 - 2015, I split the data into year 2015 and year 2000-2014 for test and train dataset. I build the model based on data before 2015(not included) and validate it using data in 2015.

### EDA Notebooks
In this notebooks, I have showned the life expectancy trend in 2000-2015, developing and developed life expectancy for data exploration. And I add the features importance plot for my final model.

### Models 
I chose Linear Regression, Ridge, Lasso, Decision Tree Regressor and RandomForest Regressor. For evaluation metric, I chose the mean absolute error for following reasons. First, life expectancy varies in a small range so MAE is a good and interpretable measure. Unlike MSE, it is also robust to outliers.  Moreover, in the practice, the MSE or R2_score metrics would tend to build a less general model which will cause overfitting problem.

### Conclusion
After we fit all the models, we find out that `RandomForestRegressor` with parameters `n_estimators=600` works best among the search space. The root mean squared error is `1.82` and the R2 score is `0.949`. It means that `94.9%` of the life expectancy values in 2015  could be explained by the model. Then we analyse the feature importancy of each predictors and we surprisingly to see the `income, adult mortality and HIV/AIDS` are three top most influential factors to the life expectancy. Also, children healthcare plays an important role as influencing factors to global life expectancy.

### Next Step
For the next step, I will look more into how to polish the model so that there is less overfitting because for now the R2 scored is really high and it will perform a bad gernality to other dataset. Also, I will add some time series analysis since there is a time series in the dataset. It will also improve the performance of the final model.
