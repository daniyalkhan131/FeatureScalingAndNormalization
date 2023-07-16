# FeatureScalingAndNormalization

before just giving our input to do model we do feature scaling
it is a tech to standardize the independent features present in data in a fized range

why do-
so that one feature dont dominate the other like in knn salary will dominate the age, and
-ML model wont work well

types-
1. standardization
2. normalization

Standardization- 
also called z-score normalization
use this formulae for every column (X-mean)/std
and the new dataset we got wil always have mean=0 and std=1

mean centering is done, our data comes around point 0 at x axis, implies mean=0
and our data points come closer or apart to where it make std=1

Remember distribution of data remain same.

on logistic reg. scaling has a strong impact while on decision tree no impact at all

Standardization dont reduce the impact of outliers, outlier remian as it was,
so we need to handle outlier explicitly

when to use-
when using these algos-
	K-means
	KNN
	PCA
	ANN
	gradient descent
and in these algos scaling not required- Decisiontree randomforest gradientboos Xgboost



Normalization-

Normalization is a technique often applied as part of data preparation for machine learning. The goal of normalization is to change the values of numeric columns in the dataset to use a common scale, without distorting differences in the ranges of values or losing information

