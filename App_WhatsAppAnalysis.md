
## WhatsApp Chat Analysis Application 

[Back to Project List](http://emilevdheyde.github.io/)

**Project Description:** 

This application is just for fun. Every day we chat on WhatsApp with friends and family, but do we have a good idea of how often we message,  if there are any common words we use and if there are certain behaviours you or friends exhibit in the chatters-sphere. 

It is available to demo at the following link.
[Demo model](https://analysis-whatsapp.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/WhatsAppSL)

### 1. Product Vision Statement

The objective of this application is to provide a simple method to upload WhatsApp text files and instantly allow the user to discover insights, via interactive visualisations that allow the user to understand you and your friends chat language and habits on WhatsApp. 

The focus is providing an application that is focused around on being fun, informative and usable to someone with basic data literacy. 

### 2. List of Features

For input, the application has an easy drag and drop tool to upload a TXT file of the users’ data.

The application allows for both one-on-one person chat to be analysed, as well as analysis of multiperson group chat.  

The application allows users to export graphs to share with friends.

Specific views: 
A timeline view of the frequency of messaging and the average number of words per message.
Word cloud and bar chart of Top 50 words
Selection of a word and compare the usage of that word in comparison to a friend(s).
Persona Classifications such as ( Night owl, short text chatter, Initiator)

### 3. Platform

The application is Python driven using pandas as the main data manipulation tool. Altair is used as the graphing tool. Streamlit is used to create the application. Heroku used as a production server.

### 4. Dependencies, Assumptions, Constraints

Users should know how to download the TXT chat file from their WhatsApp. It is a relatively simple process, and the application provides a link on how to do this.  

It is expected that some users may be apprehensive with uploading personal conversations online. An added message is posted that the application creators and the server partner do not store the data or chat messages as it is only temporarily available and is removed once the web page containing the application is closed. 

Whatsapp provides a zip file that requires an additional unzipping tool, while most users would have it on their laptops, it is not as common to unzip on mobile without adding a separate application to unzip the file.  

Whatsapp could change the format of the TXT file in the future, meaning special data-wrangling programming that was done may cause a bug that will need to be corrected. 

[Demo model](https://analysis-whatsapp.herokuapp.com/)

**Packages used :
Streamlit | Heroku| Altair | WordCloud| Regex | Pandas |**

[Back to Project List](http://emilevdheyde.github.io/)
