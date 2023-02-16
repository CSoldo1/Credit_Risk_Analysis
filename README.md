# Credit Risk Analysis

## Overview
In this challenge, I used supervised machine learning to solve a real-world challenge: credit card risk. I employed various techniques to train and evaluate models with unbalanced classes. 

## Resources
* Python 3.7
* Packages: imbalanced-learn and scikit-learn
* Jupyter Notebook
* Data: Credit Card Dataset from LendingClub

## Analysis
Credit card risk data is an inherently imbalanced dataset. There is a severe skew in class distribution: there are for fewer risky borrowers. ed he credit card dataset using RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. 
The performance of each model was assessed with accuracy_score(), a method that compares the actual outcome (y) values from the test set against the model's predicted values. The accuracy score, therefore, is simply the percentage of predictions that are correct. Along with quantifying the accuracy score, a confusion matrix was collated to evaluate the precision of the test. In machine learning, precision i s a measure of how reliable a positive classification is. The sensitivity of the model was also assessed. 

## Results
#### RandomOverSampler

balanced accuracy score = 0.657

![Naive Random Oversampling](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/Naive_Random_Oversample.PNG)

#### SMOTE Oversampling

balanced accuracy score = 0.66

![SMOTE](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/SMOTE_Oversampling.PNG)


#### Cluster Centroids Undersampling

balanced accuracy score = 0.54

![Cluster Centroids](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/Cluster_Centroids.PNG)

#### Over and Under Sampling

balanced accuracy score = 0.644
![SMOTEEN](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/SMOTEEN.PNG)

### Ensemble Learners
#### Balanced Random Forest Classifier

balanced accuracy score = 0.788
![Balanced Random Forest Classifier](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/balanced_random_forest_classifier.PNG)

![Feature Performance](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/feature_importance.PNG)

#### Easy Ensemble AdaBoost Classifier

balanced accuracy score = 0.93

![Easy Ensemble Classifier](https://github.com/CSoldo1/Credit_Risk_Analysis/blob/main/Images/Easy_Ensemble_Classifier.PNG)





