# Data_Preprocessing
A complete tool kit for data pre-processing in machine learning

## Steps Involved
1. Importing the Library
3. Importing dataset
4. Taking care of missing data
5. Encoding Cateogarical data
6. Splitting the dataset in training and test sets
7. Feature scalling (optional)

## Dataset
![](https://raw.githubusercontent.com/SahilHemnani777/Data_Preprocessing/main/2021-02-21.png)

## FAQ

1. Order of `Feature Scalling` and `Spliting in training and testing set`- Which should be done first ?

Normalization across instances should be done after splitting the data between training and test set, using only the data from the training set. This is because the test set plays the role of fresh unseen data, so it's not supposed to be accessible at the training stage.
Don't forget that testing data points represent real-world data. Feature normalization (or data standardization) of the explanatory (or predictor) variables is a technique used to center and normalise the data by subtracting the mean and dividing by the variance. If you take the mean and variance of the whole dataset you'll be introducing future information into the training explanatory variables (i.e. the mean and variance).
Therefore, you should perform feature normalisation over the training data. Then perform normalisation on testing instances as well, but this time using the mean and variance of training explanatory variables. In this way, we can test and evaluate whether our model can generalize well to new, unseen data points.
