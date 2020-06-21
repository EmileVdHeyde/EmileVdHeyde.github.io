
## Text Analysis for Moderation of posted comments using Deep Learning

[Back to Project List](http://emilevdheyde.github.io/)

**Project Description:** 

This project is a classification model, using a Neural Network algorithm to identify if a post should be accepted or rejected because it contains a high possibility of abusive, discriminatory language or it being potential spam.  

The model uses a rich sample of publicly available blog comments and classifies them using Tensor flow and Keras.
A bi-directional convoluted Neural net algorism was used to model the accept and reject classification.

The model was then saved and a package was created for with flask and deployed on heroku.  

It is available to demo at the following link.

Flask Built : 
[Demo model](https://commentmoderator.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/My-Python-Projects/tree/master/4.NLP%20Comments%20Moderator)

Streamlit Built: 
[Demo model](https://commentsmoderator-2.herokuapp.com/)

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/NLP_Comments_SL-)

### 1. Data Exploration 

Using a large volume of public data , where comments have already been classified into Accept and reject.
The random sample size was 50 000 data points was used which we balanced the data to 50% accepted and 50% reject.
The data had an average number of 51 words per data point(comment). This was approximately equal between approved and rejected cases. 

The source data can be found from the package NLP, civil comments. 

### 2. Data Preparation 

Preparing the data for modelling by performing classic text preparation. This included Removing special characters and removing common stop words such as ( the, his, and ..). 

The paragraphs were then transformed into numerical tokens and then into tensors in order for the Tensor flow keras algorism to learn and classify. A limit of the top 5000 words were used with a maximum of 120 words allowed, post truncation and post padding meaning that the beginning of the text in the rare cases when the text limit was exceeded. 

For traning, we split the data set into a training an validation set in a ratio of 60:20:20. 


### 3. Classification Models

A Neural network model was also used generated using TensorFlow. We attempted to use the following type of models using binary_crossentropy. 
1. Classic sequential 
2. BiDirectional LSTM (Selected model)
3. Bi-directional GRU 

### 4. Assessment of the accuracy of the model 

The model was the accuracy of training was 90% , and validation accuracy was 62%
Using the independent test sample accuracy of  63% was obtained.

Due to this overfitting, it was decided to band the responses where <30% would be accepted, >70% would be rejected and between would be a neutral category. The recall improved slightly to 66% for rejects. 

### 5. Model and App Deployment 

A function was used to summarise the model , along with the save model weights and the tokenisers. Flask was used to prepare the model for deployment. 

A very basic HTML and CSS template was used to allow user interface. 

I also did a version of the same model in Stremlit instead of Flask

I then used Heroku to deploy a live model that does a real-time assessment of any input paragraph you may input. 


**Packages used :
Numpy | Pandas | Sklearn | Tensorflow | Keras | MatplotLib |Pickle |Flask| Heroku **

[Back to Project List](http://emilevdheyde.github.io/)
