
## GoodBad Classification EDA tool

[Back to Project List](http://emilevdheyde.github.io/)

**Project description:** 

When starting classification models we often want to investigate the relationship between our target variable and a host of exploratory variables that may become features in our model building. 

This application looks within the categories inside each candidate varaible and illistrates though graphing if there is a difference in the bad rate between cateorgoies within a specific varible. 

It is avalible to demo at the following link.
[Demo model](https://goodbadclassification-eda.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/GoodBadEDA)

### 1. Product Vision Statement

The objective is to quickly investigate a data set and transform it in a awy that we can produce the bad percentage graph per category and toggele between different varibles and ranges. 

Simplicity of a tool , and demonstating quickly the varible that may be a big differentiator for your model. 

### 2. List of Features

Easy drag and drop tool to upload a csv of your data. 

Alow user to choose a target varible, and be able to toggle a value if the target in contiuous or choose a good bad range if the value is categorical.

Choose a feauture varible as a selection to see in the graph against the target varible. 

The feature variable will need some preprossing that we will make dynamic and automate in the application; 
This includes alowing to bin the continuous varibles in groupings.
Also a feature to group categorical varibles into groupings where there are two many categories within that variable. 

A basic time filter to see if relationships are consistant over time , or to view the latest x months patterns. 

The basic output will be 
1. The Count of occurances , raw counts. 
2. % Bad per category/ group within each Feature varible. 


### 3. Platform

The Product is Phython driven using pandas as the main data minipulation tool.
Seaborn is used as the main Graphing tool. 
Streamlit is used to create the Application and the interactive widgets. 
No deployment server. 

### 4. Dependencies, Assumptions , Constraints

This is not aimed at someone who does not have some background in data analysis or data science.
This tool does not aim to be everything in EDA, but another tool in the process to asist. 
There is a variety of data types and possible , we attempt to adress the most common ones. 

[Demo model](https://goodbadclassification-eda.herokuapp.com/)

**Packages used :
Streamlit | Seaborn | WordCloud| Regex | Pandas |**

[Back to Project List](http://emilevdheyde.github.io/)
