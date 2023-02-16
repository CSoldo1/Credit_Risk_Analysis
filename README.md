# Credit Risk Analysis

## Overview
In this challenge, I used supervised machine learning to solve a real-world challenge: credit card risk. I employed various techniques to train and evaluate models with unbalanced classes. 

## Resources
* Python 3.7
* Packages: imbalanced-learn and scikit-learn
* Jupyter Notebook
* Data: Credit Card Dataset from LendingClub

## Analysis
Credit card risk data is an inherently imbalanced dataset. In other words, there is a severe skew in class distribution (i.e. there are for fewer risky borrowers). This bias in a data set can lead to the minority class being ignored entirely. Randomly resampling the training dataset is one way to account for this bias. The two main approaches to resampling datasets are to delete samples from the majority class (undersampling) or to duplicate samples from the minority class (oversampling). I over sampled the credit card dataset using RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. 
The performance of each model was assessed with accuracy_score(), a method that compares the actual outcome (y) values from the test set against the model's predicted values. The accuracy score, therefore, is simply the percentage of predictions that are correct. Along with quantifying the accuracy score, a confusion matrix was collated to evaluate the precision and sensitivity of each test. 

## Results
#### RandomOverSampler
Random oversampling involves randomly selecting points from the minority data set and adding them to the training data set. 
The balanced accuracy score from the model was 0.657 and the results of the confusion matrix can be seen below:

![Naive Random Oversampling](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/Naive_Random_Oversample.PNG)

#### SMOTE Oversampling
SMOTE oversampling involves synthesizing new data points from exisiting examples. The balanced accuracy score from the SMOTE model was 0.66 and the results of the confusion matrix can be seen below:

![SMOTE](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/SMOTE_Oversampling.PNG)


#### Cluster Centroids Undersampling
The cluster centroids method undersamples the majority calss by replacing a cluster of majority samples by the cluster centroid of a KMeans algorithm. The balanced accuracy score for the Cluster Centroids model was 0.54 and the results of the confusion matrix can be seen below:

![Cluster Centroids](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/Cluster_Centroids.PNG)

#### Over and Under Sampling
Both undersampling and oversampling can be used in isolation. However, both types of resampling can be more effective when used together. In this instance, I relies on the SMOTEEN algorithm. The balanced accuracy score for this combinatorial approach was 0.644. The results from the confusion matrix can be seen below. 

![SMOTEEN](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/SMOTEEN.PNG)

#### Balanced Random Forest Classifier
Ensemble algorithms fit multiple models on different subsets of the training dataset, and then they combine the predictions from all the models. Random Forest is a type of ensemble learner that randomly selects subsets of features used in each data sample. Using the balanced random forest classifier, the balanced accuracy score was 0.788. The results of the confusion matrix can be seen below:

![Balanced Random Forest Classifier](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/balanced_random_forest_classifier.PNG)

Furthermore, using the random forest classifier, we can rank feature performance, as shown below:

![Feature Performance](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/feature_importance.PNG)

#### Easy Ensemble AdaBoost Classifier
Boosting algorithms combine multiple low-accuracy models to create a high accuracy model. AdaBoost is an iterative ensemble method that combines multiple classifiers to increase the accuracy of the model. In this instance, the balanced accuracy score of the model was 0.93. The results of the confusion matrix can be seen below. 

![Easy Ensemble Classifier](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/Easy_Ensemble_Classifier.PNG)

### Summary
Precision was high for each model while the balanced accuracy score varied. The majority of the one-method models (either oversampling or undersampling) had balanced accuracy scores within the 60% range. The cluster centroids model was the least accurate model with a score of 0.54. The ensemble learners, on average, performed better. The AdaBoost Classifier method performed the best with an balanced accuracy score of 0.93. Therefore, the ensemble AdaBoost Classifier is the best model to use because it has the highest recall score and the highest balanced accuracy score. 


