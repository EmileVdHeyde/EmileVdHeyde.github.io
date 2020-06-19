## GoodBad Classification EDA tool

[Back to Project List](http://emilevdheyde.github.io/)

**Project Description:** 

When starting classification models we often want to investigate the relationship between our target variable and a host of exploratory variables that may become features in our model. 

This application provides a simple mechanism to select an exploratory variable and illustrate through graphing if there is a difference in the bad rate between the categories within a specific variable. 

It is available to demo at the following link.
[Demo model](https://goodbadclassification-eda.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/GoodBadEDA)

### 1. Product Vision Statement

The objective of this exploratory data analysis tool is to quickly investigate a data set and use the application to transform it in a way that we can produce the bad percentage graph per category and allow the users to toggle between different variables and variable ranges. 

The simplicity of the tool to handle different variables and variable types is the main objective of this application so that the user can quickly identify what variable is the big differentiator for your model. 

### 2. List of Features

An easy drag and drop tool to upload a .csv file of your data. 

Allow user to choose a target variable, and be able to toggle a value if the target in continuous, or choose a good bad range if the value is categorical.

Choose a feature variable as a selection to see in the graph against the target variable. 

The chosen feature variable may need some preprocessing and we want to provide a customisable and simple way to do this within this application This includes allowing to bin the continuous variables in groupings. We also want to allow groupings within categorical variables where there are two many categories. 

A basic time filter to see if relationships are consistent over time, or to view the latest range of months patterns. 

The basic output will be 
1. The count of good and bad occurrences of each item within the exploratory variable. 
2. The percentage bad per category/group within each Feature variable. 


### 3. Platform

The product is Python driven using pandas as the main data manipulation tool.
Seaborn is used as the main graphing tool. 
Streamlit is used to create the Application and the interactive widgets. 
Heroku used as a production server. 

### 4. Dependencies, Assumptions, Constraints

This is not aimed at someone who does not have some background in data analysis or data science.
This tool does not aim to be everything in EDA, but another tool in the process to assist. 
There is a variety of data types and possible, we attempt to address the most common ones. 
The user should upload a CSV file with headers. 

[Demo model](https://goodbadclassification-eda.herokuapp.com/)

**Packages used :
Streamlit | Seaborn | WordCloud| Regex | Pandas |**

[Back to Project List](http://emilevdheyde.github.io/)
