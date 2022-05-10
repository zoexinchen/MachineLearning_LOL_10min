# MachineLearning_LOL_10min
### Intro

In this project we acquired ranking data of leagur of legends from kaggle ([link](https://www.kaggle.com/datasets/bobbyscience/league-of-legends-diamond-ranked-games-10-min)). The original data set contains up to 40 sections of data from almost 10,000 ranking games for the first 10 minutes, including how many kills red side or blue side got, the gold differences etc.. It also records the winning side of the game. 

For the full explanation of the varibles included in this data set, please consult the [webpage](https://www.kaggle.com/datasets/bobbyscience/league-of-legends-diamond-ranked-games-10-min) for detailed information.

Our work is to use machine learning methods to predict the winner of the game based on the data of the first 10 minutes.

### Methods

Before model building, we inspected the raw data set to check for any missing data, strong collinearity variables, and cahnged some categorical varaibles into factors. We've also split the data set into training and test set by the ratio of 80:20. The cross-validation sets are created by spliting the training set into 5 parts, but in our cross-validation process we mainly used the `caret::train()` function.

As this is a classification problem, we applied various supervised machine learning skills such as **Logsitic Regression**, **LDQA**, **QDA**, **KNN**, **Dicision Tree** and **Random Forest**. We trained the model and tuned the parameters using the cross-validation sets, and computed the goodness of prediction by recording and comparing the test errors, AUC scores on the test set.

In the final part we compared the performances of each model, and discussed which one is the best and why.
