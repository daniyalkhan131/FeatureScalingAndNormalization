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

in ML it is considered that if dealing with numerical quantities then eliminate units
of numerical value so bring them to common scale.

types-
min-max scaling
mean normalization
max absolute scaling
robust scaling
and many more....

90% time min max is used

min-max:
use formulae Xnew= (X-Xmin)/(Xmax-Xmin)
range we get 0 to 1
we are like squishing data into square from 0 to 1 for 2d and cube for 3d
mostly min max scaler retain the shape of distributin, try with different dist. you find
somewhere it changes a little

problem- outlier ka impact squish hojata h 0 to 1 k beechme


mean normalization:
Xnew= (X-Xmean)/(Xmax-Xmin)
doing mean centring here like in standardization
give range -1 to 1
no class in sklearn
used for ML algo where centered data required but generally people use standardization for that


max Absulute scaling:
Xnew= X/abs(Xmax)
sklearn class is MaxAbsScaler
useful in sparse data(if having 0's in data more)


robust scaling:
Xnew= (X-Xmedian)/IQR
skealr class in Robustscaler
it is robust to outliers, it generally performs well if data have lot of outliers
in ML we cannot say what thing work for what things, of something we know but in ML we have to expreiment all things to get to the best thing or find best thing.


normalization vs standardization
1- is feature scaling required? ( this can be understood byt learning internal working of model)
2- standard scaler class sabse zada use hota hai cuz achvhe results deta h hmesha
use min-max when you know about the range of your data like max and min value, like in
image processing using cnn where we know 0-255 so all use minmax scaler
if no idea use standardscling
if outliers use robust scaling
if sparse matrix use maxabsscaling
 
