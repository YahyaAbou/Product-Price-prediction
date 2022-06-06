# Product-Price-prediction

## Project Description

The objective is to predict the price for each drug in the test data set (`drugs_test.csv`). Please refer to the `sample_submission.csv` file for the correct format for submissions.


### Explanation :
The taken approach is a simple one using as a model a random forest regressor. 
It is a basic approach and while it gives okayish result, it is evident that there're ways to improve it.
While it is a generic model that often gives acceptable result, it has some problems like the fact that it can't extrapolate and so won't be able to predict possible outliers prices that are out of the scope of the training prices.

Since our data contains numeric + categorical features, it'd be possibly better to treat the two separately by using two models then combining the result.

With more time, I'd prefer to use a neural network with different layers that can treat either the numeric or categorical features.

I didn't find my work very satisfactory, and I'd say what I was most proud of is my preprocessing of the data and the encoding of the description.

### Performances :

For the performances, I used 3 metrics : the R2_score, the mean absolute error and the mean squared error :
    MAE 0.46485876761942135
    RMSE 0.6623003207983935
    R2 0.6639208548049347
But the current values were calculated on the normalized data (by using log(1+X) for the price to manage the outliers).    

### Improvements :

With more time and focus, I'd try to start with implementing the following improvements :
1.  Using a neural network with different layers to manage both numeric+categorical data and hypertuning the parameters.
2.  Deeper encoding of the description data (instead of just taking into account the labels, it may be more useful to get all the words then remove all stopwords and low frequency words then one hot encode the rest).
3.  Use of One Hot Encoding instead of Label Encoding for the other categorical data.
