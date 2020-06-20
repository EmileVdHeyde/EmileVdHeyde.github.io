## Web Scraping Data from an HTML page to database 

[Back to Project List](http://emilevdheyde.github.io/)

**Project Description:** 

This project uses very inconsistent HTML data that is stored on multiple web pages that were archived to retrieve COVID 19 data across various measures on a country level.

[Click here to View .py or .ipynb files relating to this project](http://github.com/EmileVdHeyde/My-Python-Projects/tree/master/1.Covid%20Data%20Web%20Scraping)

### 1. Extract the web page links to do data extraction from 

This Script looks at the Links archived for this website which has a CSV of all the links to the snapshot.
We extract from the web, filter out some records and the make a Dataframe

### 2. Build up a Metadata file and store in DataBase

Run through the HTML to get the column names and column count to allow us to this in the next step.
This is done to assist in the changing number of variables over time.

### 3. Extract the actual data 

Run through the HTML per day, to extract the values and store in database 

### 4. Visualise the data 

Use Seaborn to display the data. 


**Packages used :
Beautiful Soup | Pandas | Requests | SQL Lite | Seaborn | MatplotLib **

[Back to Project List](http://emilevdheyde.github.io/)
