
## GoodBad Classification EDA tool

[Back to Project List](http://emilevdheyde.github.io/)

**Project description:** 

When starting classification models we often want to investigate the relationship between our target varible and a host of variables.
This model looks within the categories if each varaible and illistrates though graphing if there is a difference in the bad rate between cateorgoies within a specific varible. 

It is avalible to avalible to demo at the following link.
[Demo model](https://analysis-whatsapp.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/WhatsAppSL)

### 1. Product Vision Statement

The objective is to quickly investigate a data set and transform it in a awy that we can produce the graphs and toggele between different varibles. 

### 2. List of Features

Upload a csv of your data. 

Choose a target varible, and be able to toggle to chose a good bad range if the value is categorical.

Chose a feauture varible as a selection to see in the graph against the target varible. 

The feature variable will need some preprossing that we will make dynamic and aoumote in the application; 
This includes alowing to bin the continous varibles in groupings.
Some mechanism to group categorical varibles into groupings where there are two many categories within that variable. 

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

[Demo model](https://analysis-whatsapp.herokuapp.com/)

**Packages used :
Streamlit | Seaborn | WordCloud| Regex | Pandas |**

[Back to Project List](http://emilevdheyde.github.io/)
