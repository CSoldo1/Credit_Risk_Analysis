# Credit Risk Analysis

## Overview
Using supervised machine learning and logistic regression to decide credit risk based on a variety of features

## Resources
* Python 3.7
* Jupyter Notebook
* Data: Loan Information

## Analysis
Python libraries Scikit-learn package
The performance of each model was assessed with accuracy_score(), a method that compares the actual outcome (y) values from the test set against the model's predicted values. The accuracy score, therefore, is simply the percentage of predictions that are correct. 

## Results

#### Naive Random Oversampling

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





