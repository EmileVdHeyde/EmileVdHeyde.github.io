## Web Scraping Data from a HTML page to Database 

[Back to Project List](http://emilevdheyde.github.io/)

**Project description:** 

This project uses very inconsistant HTML data that is stored on multiple web pages that were archived to retrive Covid 19 data across various measures on a country level.

[Click here to View .py or .ipynb files relating to this project](http://github.com/EmileVdHeyde/My-Python-Projects/tree/master/1.Covid%20Data%20Web%20Scraping)

### 1. Extract the web page links to do data exraction from 

This Script looks at the Links archived for this website which has a csv of all the links to the snap shot.
We extract from web , filter out some records and the make a Dataframe

### 2. Build up a Meta data file and store in DataBase

Run through the HTML to get the column names and column count to alow us to this in the next step.
This is done to assist in the changing number of varaibles over time.

### 3. Exctact the actual data 

Run through the HTML per day, to extract the values and store in database 

### 4. Visualise the data 

Use Seaborn to display the data 


**Packages used :
Beautiful Soup | Pandas | Requests | SQL Lite | Seaborn | MatplotLib **

[Back to Project List](http://emilevdheyde.github.io/)
