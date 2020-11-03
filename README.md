# Credit-Card-Fraud-Detection

In this module, we will learn how to implement machine learning based Credit Card Fraud Detection. So far, we have learned many supervised and unsupervised machine learning algorithm and now this is the time to see their practical implementation.

## 1. Project Goal
Credit card companies shall be able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase.

## 2. Data set Description 

The datasets contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,315 transactions. It has 30 input features and 1 target variable. The dataset is highly unbalanced, the positive class (frauds) account for 0.173% of all transactions.

The data set is publicly available at https://www.kaggle.com/mlg-ulb/creditcardfraud/home

Due to confidentiality issues, Kaggle doesn’t provide the background information about the 28 features out of 30. The only Features defined are ‘Time’ and ‘Amount’. ‘Time’ contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature ‘Amount’ is the Transaction Amount. ‘Class’ is the target variable and it is 1 in case of fraud and 0 otherwise

## Data Cleansing

We have identified the input features and the target variable so we will separate them into two objects "X" and "y" and draw the histogram of all the input features to see the data at a glance.

NOTE :- We have a limitation to display histogram plot, so I will display only 9 subplots instead of 29 plots.

After doing all these do StandardScaler so that all the values will be in a particular range.

### StandardScaler : It transforms the data in such a manner that it has mean as 0 and standard deviation as 1.

It is clearly seen in the above that all the features are now normally distributed around zero. I hope your concept is also cleared for data standardization. 

## Supervised Machine Learning Model

First, we will split our dataset into train and test set using ‘train_test_split’ function. After that we will train our model and then we will predict using our trained model. In this example, we will use Logistic Regression model.

## Using Logistic Regression


### Logistic regression is the appropriate regression analysis to conduct when the dependent variable is dichotomous (binary). Logistic regression is used to describe data and to explain the relationship between one dependent binary variable and one or more nominal, ordinal, interval or ratio-level independent variables.

# Making Classification report and Confusion Matrix.

## Using Naive Bayes.

# Making Classification report and Confusion Matrix.

## 3. Unsupervised Outlier Detection

Now that we have processed our data, we can begin deploying our machine learning algorithms.  We will use the following techniques: 

**Local Outlier Factor (LOF)**

The anomaly score of each sample is called Local Outlier Factor. It measures the local deviation of density of a 
given sample with respect to its neighbors. It is local in that the anomaly score depends on how isolated the 
object is with respect to the surrounding neighborhood.


**Isolation Forest Algorithm**

The IsolationForest ‘isolates’ observations by randomly selecting a feature and then randomly selecting 
a split value between the maximum and minimum values of the selected feature.

Since recursive partitioning can be represented by a tree structure, the number of splittings required to 
isolate a sample is equivalent to the path length from the root node to the terminating node.

This path length, averaged over a forest of such random trees, is a measure of normality and our decision function.

Random partitioning produces noticeably shorter paths for anomalies. Hence, when a forest of random trees 
collectively produce shorter path lengths for particular samples, they are highly likely to be anomalies.

## Conclusion
We get to know that we are getting accuracy = 99.90% which is approximately equal to 100% means very accurate in using Logistic Regression, after that I have used Naive Bayes classifier and got the accuracy around = 99.26% which is also not too bad, after that I have used SVM and got the accuracy around = 99.88%. So, I can conclude that I have used 3 different classifier for the same model and got the accuracy between the range 99 - 100, so I can proudly say that my model is good in predicting and is accurate.
