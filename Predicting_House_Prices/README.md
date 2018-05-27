# Challenge: What is the future selling price of a home?

This challenge (adapted from [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)) aims at predicting selling prices of a number of houses. To predict these prices, we are given a training set (with known selling prices). 

For each house, we are given around 80 characteristics (total area, building materials, number of floors, ...). 

### Our approach

We decided to really study in depth the training dataset before thinking about predicting anything. This analysis aimed at understanding what we were dealing with but also try to predict what we would need to change in our dataset to have it ready to be processed in the modeling part. We therefore spent quite a lot of time pre-processing our data (transforming strings into numerical values, applying *Box-Cox transformations*, ...). 

We then decided to use the *cross-validation* method to train and test our prediction models on one known datasets. We chose to test several models (*random forest decision trees*, *Lasso*, *multi-layer perceptron*, ...) to see which one would be the most accurate and most reliable. After many computations, we decided to mix models for our final prediction model. We train it on the whole training set (not using cross-validation anymore) and predicted the prices for the test dataset houses. The predictions are stored in the `csv` file. 
