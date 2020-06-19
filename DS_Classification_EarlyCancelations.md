## Classification of Early policy Cancelation based on Adviser Features 

[Back to Project List](http://emilevdheyde.github.io/)

**Project Description:** 

This project objective is to build a classification model to identify policies that will default within six months of the acceptance date. 

The model scoring is done on an individual policy level at the point of acceptance.  This will allow management to reduce the commission debt that arrises when early defaulting occurs on a policy. This can be done by at finalisation of acceptance offering policies with a very high probability of early default to have a different payout structure for that policy the model confidently identifies as potentially going to be an early defaulting. 

Because this is an actual working problem, some details are not revealed for company privacy.

The objective of this page is to demonstrate the process of building the model as well as to provide the assessment metrics of the model.

### 1. Data Exploration and hypothesis testing 

Based on business information on what behaviours are risky or have caused adviser fraud before. I set about creating a base table of the data and the proposed variables in SQL.
Using Pandas, summary tables and graphs i assessed various variables with univariate analysis as well as bivariate analysis on the target variable.
Hypothesis testing was applied to see if relationships were statistically significant. 
A shortlist of variables were then moved to the next phase.

The input variables used are based on policy factors, particularly around the adviser selling the policy.

### 2. Data Preparation 

Preparing the data for modelling by creating dummies by hot codding, standardising data, balancing the data.
Data is split into Training, Test and validation for assessment. 
Data is converted to NPZ files for Tensor flow Neural networks. 


### 3. Classification Models

Models used were logistic regression, SVM , Decision Trees,  K-nearest neighbour using Sk learn kit 
A Neural network model was also used generated using TensorFlow. 

### 4. Assessment of the accuracy of the model 

The challenge of this model was to use techniques that could handle the imbalance in the data caused by rare events.
It was this reason and because the effect of calling a false positive was most costly.
That the Recall score was the most important measure to use. 


**Packages used :
Numpy | Pandas | Sklearn | Scipy | Tensorflow | StatsModels | Keras | MatplotLib** 

[Back to Project List](http://emilevdheyde.github.io/)
