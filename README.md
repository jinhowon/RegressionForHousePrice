# RegressionForHousePrice

Hello, this is a project that uses different models to predict and test housing prices in Ames, Iowa. We used two datasets to help with this prediction: 'train.csv' and 'test.csv'. I also cleaned the data to help with better prediction such as I removed houses with a above ground living area that is greater than 4500 sqft. I also filled in missing data, scaled number

# For the actual prediction itself
I used a ridge regression model on the log of the housing price and trained it.  Trained on log(SalePrice) instead of raw price, because house prices are right-skewed. Predictions are converted back to dollars with `np.exp`. Ridge regression with alpha = 10.  Evaluated with a train/test split (`random_state = 42`), using RMSE in dollars

# Result

 Ridge on log prices cut the error by about 75% compared with the baseline and about 30% compared with plain linear regression. It also overfit less: train RMSE was $16,843 vs. test RMSE of $19,978

Refer to the last Small Reggresion Group File for the codes.
