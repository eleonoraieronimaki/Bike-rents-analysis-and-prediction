# Bike rentals analysis and prediction with Machine Learning methods


## Description 
This repository contains the work done for the practical assignment for the course Introduction to Machine Learning. Specifically, the aim of this work is to analyze the provided data set using some of the algorithms discussed during the lectures of the course. 



## Dataset 
The data set contains data about bike rentals in a large European city and it is composed by the 15 following variables: instant, date, season, year, month, hour, weekday, weather, temperature, feeling temperature, humidity, windspeed, Subscribed, Non-subscribed, Total. 

## Contents: 
- ### Dataset analysis and visualisation
Check for missing values, statistics (mean, std, percentile) of the data, graphical representation of distribution patterns, correlations between features, and outliers check
- ### Pre-processing
Trying different approaches and transformations for the categorical values: Label encoding, One hot encoding, mixed one hot encoding and cycling labelling approach 
- ### Linear regression
Method used to predict the number of bikes rented by SUbscribers. Used to see which approach performs better based on the R2 score and MSE. It turns out the one hot encoded model yields better results. 
- ### Target transformations
Target values transformation: Logarithm, Square root and Power of Non-subscribe, Subscribe, Total features. The accuracy of the model drastically improves if the natural logarithm of the target value is considered whereas it degrades if we take the squared value of the target.
- ### Decision tree regressor
Method used to predict the number of bikes rented by Subscribers. GridSearch is used to find the best hyperparameters. The same method is followed to predict the number of rented bikes by Non-Subscribers. Comparison of the results obtained. The best hyperparameters used to predict Subscribed rents are different from the hyperparameters used to predict Non-Subscribed rents.
- ### Logistic regression (One-vs-One and One-vs-all)
Transformation of the problem of predicting the total number of bikes rented into a classification problem (around 5 classes) using 2 methods: One vs Rest and One vs One Classifiers.
- ### Perceptron
Perceptron model to predict the weather situation based on other some features in the data set selected using the SelectKBest. 20 to 30 features give the best F1 score on both train and test set. 
- ### SVM regressor
SVM regressor model to predict the number of bike rentals by subscribers and see how using different kernels (Linear, RBF, Polynomial) impacts the performance. RBF kernel performs better than the other two.
- ### PCA
PCA to reduce the dimensionality of the data set.
- ### Hierarchical clustering
Cluster the data using hierarchical clustering. 
- ### Random forest regressor
Random forest regressor model to predict the number of bike rentals. In order to tune the parameters the random search method is used.
- ### MLP regressor
MLP regressor to predict the total number of bikes rented. RandomizedSearchCV is used to with cv=5 to use a validation set to find the best parameters: hidden_layer_sizes (165,77). MLP is the best model for this problem as it yields the highest R2 score both on train and test sets.
