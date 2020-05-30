
## Classification of Early policy Cancelation based on Adviser Features 

[Back to Project List](http://emilevdheyde.github.io/)

**Project description:** 

This project classification model , identifies policies that will default within 6 months of acceptence. 
The scoring is done at policy stage so that management can act on a different commission sctructure for tht policy.
The variables used are based on policy factor particularly around the adviser selling the policy.

Because this is an actual working problem , some details are not revealed for company privacy.
The object of the below is to demonstrate the process and sucsess of the model.

[Click here to View .py or .ipynb files relating to this project](http://github.com/EmileVdHeyde/My-Python-Projects/tree/master/1.Covid%20Data%20Web%20Scraping)

### 1. Data Exploration and hypothesis testing 

Based on business information on what behaviors are risky or have caused adviser fraud before. I set about creating a base table of the data and the preposed varibles in SQL.
Using Pandas, summary tables and graphs i asessed various variables with univerite anysis as well as bivariate analysis on the target varible.
Hypothesis testing was applied to see if relationships were statsically signicant. 
A short list of varibles were then moved to the next phase.

### 2. Data Preparation 

Preparing the data for modeling by creating dummys by hot codding , standardising data , balancing the data.
Data is split into Training , Test and validation for assesment. 
Data is converted to NPZ files for Tensor flow Neaural networks. 


### 3. Classification Models

Models used were logistic regression , SVM , Decision Trees ,  K-neirest neighbour using Sk learn kit 
A Neaural network model was also used generated using TensorFlow. 

### 4. Assesment of the accuracy of the model 

The challeng of this model was to use techniquues that could handle the imbalnce in the data caused by rare events.
it was this reason and because the effect of calling a false positive was most costly.
That the Recall score was the most important measure to use. 


Packages used :
Numpy | Pandas | Sklearn | Scipy | Tensorflow | StatsModels | Keras | MatplotLib

[Back to Project List](http://emilevdheyde.github.io/)
