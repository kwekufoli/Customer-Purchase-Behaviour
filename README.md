# Customer Purchase Behaviour
 Analyzing data from Customer purchasing behaviour dataset on Kaggle
Data was obtained from Kaggle. The dataset contained information on 238 customers in a year with the following variables:
Age
Annual Income
Purchase Amount
Loyalty score
Region
Purchase frequency

After data cleaning and exploratory data analysis was performed. The following were observed:
1. The age variable had a range of 22 to 55 with a mean of 38.68 and a standard deviation of 9.35.
2. The annual income variable had a range of 30000 to 75000 with a mean of 57407.56 and a standard deviation of 11403.87.
3. The purchase amount variable had a range of 150 to 640 with a mean of 425.63 and a standard deviation of 140.05.
4. The loyalty score variable had a range of 3 to 9.5 with a mean of 6.79 and a standard deviation of 1.89.
5, The purchase frequency variable had a range of 10 to 28 with a mean of 19.79 and a standard deviation of 4.56.
6. The age variable did not follow a normal distribution.
7. The annual income, purchase amount, loyalty score and purchase frequency variables followed an approximately normal distribution. However, loyalty score was left skewed and there were a few outliers in the purchase amount variable.
8. The distribution of the region variable was as follows:
    North - 78
    South - 77
    West - 77
    East - 6
9. All the numeric variables (age, annual income, purchase amount, loyalty score and purchase frequency) were very highly positively correlated with each other with all correlations above 0.95.
10. The region variable was significantly related with all the numeric variables. The West appeared to have higher values for all the numeric variables, followed by North, then South and then East had the lowest values. However there were very few customers from the east as compared to the other regions.
11. The data appeared to occur in clusters likely due to the variance within the region variable and its significant relationship with the other variables.

After the exploratory data analysis, models were built to predict purchase amount using region, age, annual income and purchase frequency as the independent predictor variables.
However, before this regression model was built and fit on the data, dimension reduction was performed on the numeric variables to reduce the impact of the high correlations on the model.
Another model was built to predict the purchase frequency using the age, annual income, purchase amount and region as the independent predictor variables. Like before dimension reduction was performed on the numeric variables(PCA).
A final model was built to predict loyalty score using all the other variables as predictors. Principal Component Analysis was once again used to reduce the dimensions of the numeric variables.
In all 3 cases, at least 97 percent of variance was explained by the first principal component and so only that component was used to train the model.

After building and fitting these models, K means clustering was used to group the data into 3 clusters.