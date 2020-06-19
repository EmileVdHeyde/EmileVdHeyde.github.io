## Good-Bad Classification EDA tool

[Back to Project List](http://emilevdheyde.github.io/)

**Project Description:** 

When starting classification models, we often want to investigate the relationship between our target variable and a host of exploratory variables that may become features in our model. 

This application provides a simple mechanism to select an exploratory variable and illustrate through graphing if there is a difference in the bad rate between the categories within a specific variable. 

It is available to demo at the following link.
[Demo model](https://goodbadclassification-eda.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/GoodBadEDA)

### 1. Product Vision Statement

The objective of this exploratory data analysis tool is to quickly investigate a data set and use the application to transform it in a way that we can produce the bad percentage graph per category and allow the users to toggle between different variables and variable ranges. 

The simplicity of the tool to handle different variables and variable types is the main objective of this application so that the user can quickly identify what variable is the big differentiator for your model. 

### 2. List of Features

For input, the application has an easy drag and drop tool to upload a CSV file of the users' data. 

The application will allow the user to choose a target variable.
When the target is continuous, the user will be able to toggle a specific value for the good/bad cut off. When the target is categorical, the user will be able to select the categories that fall within the bad grouping. 

Next, the application will allow the user to choose an exploratory variable which they would like to see in the output graphs. 

The chosen exploratory variable may need some preprocessing depending on its type and number of categories within the exploratory variable. The application provides a customisable and straightforward way to do this. This includes allowing to bin the continuous variables into groupings. In the case when there are too many categories within a given categorical variable, the application allows grouping of categories into a smaller number of groups. 

The additional feature to look at time range is provided with a time filter. This particularly useful when we want to see if the relationship we are trying to confirm is still consistent with the most recent time

The  application output will be ; 
The count of good and bad occurrences of each item within the exploratory variable. 
The percentage bad per category/group within each exploratory variable. 

### 3. Platform

The application is Python driven using pandas as the main data manipulation tool. Seaborn is used as the graphing tool. 
Streamlit is used to create the application and interactive widgets. 
Heroku used as a production server. 

### 4. Dependencies, Assumptions, Constraints

This application is aimed at someone who has some background in data analysis or data science sufficient to interpret the output.
The application does not aim to be a complete EDA solution, but another tool in the process to assist with model building.
The user should upload a CSV file with headers. 

[Demo model](https://goodbadclassification-eda.herokuapp.com/)

**Packages used :
Streamlit | Seaborn | WordCloud| Regex | Pandas |**

[Back to Project List](http://emilevdheyde.github.io/)
