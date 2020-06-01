
## Text Analysis for Moderation of posted comments using Deep Learning

[Back to Project List](http://emilevdheyde.github.io/)

**Project description:** 

This project classification model , using a Neural Network algorithm to identify if a post should be accepted or rejected because it contains a high possiblity of abusive or discriminatory language. 

The model uses a rich sample of publicly avalible blog comments and classifies them using Tensor flow keras.
Training has been done to create accuracy and recall to x% and x% recpectively.

The model was then saved and deployed and is avalible to demo at the following link.

(https://commentmoderator.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/My-Python-Projects/tree/master/4.NLP%20Comments%20Moderator)

### 1. Data Exploration 

Using a large volume of public data , where comments have already been classified into Accept and reject.
The sample size was xxxx with % of the reviews being rejected. Average word count per comment was x with it being relatively balanced between accepted and rejected posts. 

The source data can be found from the package nlp, civil comments. 

### 2. Data Preparation 

Preparing the data for modeling by performing classic text preperation. This inluded Removing special characters and removing common stop words such as (     ,   ,    etc). The paragraphs was then tranformed into numerical tokens and then into tensors in order for the Tensor flow keras algorism to learn and classify. For traning we split the data set into a training an validation set. 


### 3. Classification Models

A Neaural network model was also used generated using TensorFlow. We attempted to use the following type of models using binary_crossentropy. 
1. Classic sequential 
2. BIDIRECTIONAL LSTM (Selected model)
3. Bi directional GRU 

We also wanted to use the very popular vaderSentiment  to compare our model to. 

### 4. Assesment of the accuracy of the model 

The model was enhanced awith 
Training ; accuracy of  x% and Recall of x% 
Validation ; x% of accuracy and Recall of x% 

In comparison with the vaderSentiment  the allignment was x% with recall x%

### 5. Model and App Deployment 

I then used Heroku to deploy a live model that does real time assesment of any input paragraph you may input. 


Packages used :
Numpy | Pandas | Sklearn | Tensorflow | Keras | MatplotLib |Pickle |Flask| Heroku

[Back to Project List](http://emilevdheyde.github.io/)
