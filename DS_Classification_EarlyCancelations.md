## Classification Model to minimise commission debt of insurance policies

[Back to Project List](http://emilevdheyde.github.io/)

**Project Description:** 

This project objective is to build a classification model to identify policies that will likely default within six months of the policies acceptance date. 

The model scoring is done on an individual policy level at the point of acceptance, allowing this model to extended to real-time.  This will allow commission structure negotiation with the selling adviser that will minimise commission debt eg. an adviser wil be offered an 'as and when' contract instead of all commission upfront.

Because this is an actual working problem,  some model details are not revealed here for company privacy. Instead, the objective of this page is to demonstrate the process I had taken building the model. 

### 1. Data Exploration and hypothesis testing 

The starting point was a discussion with business on typical adviser behaviours that have caused a large amount of brokerage default in the past.  

I then went about identifying these behaviours and how to measure them. Using real business data in the database, I generated a data set on a policy level that contained various custom metrics as well as details about the adviser and policy holder using SQL. 

Summary tables, graphs and hypothesis testing were used to understand the relationship of the variables to early default.  

A shortlist of variables were then moved to the next phase of analysis. 

The target variable was set at , any policy that defaulted within six months of being accepted. 

The input variables used are based on policy factors, particularly around the adviser selling the policy.

### 2. Data Preparation 

A number of steps were followed to process the data to prepare them for modeling.  This included dummy creation or binary variable creation.  Data standarsation. Balancing the data using an undersampling method.  Lastly, randomly splitting the data into training, test and validation. 

### 3. Classification Models

A variety of classification models were attempted on the data. 
Namely, logistic regression, SVM, Decision Trees,  K-nearest neighbour using the SK-learn kit was used. A Neural network model was also used generated using TensorFlow. Ensemble models were also attempted. I also used CatBoost to train the model. 

Eventually, I used the logistic regression, which I then used a grid search to tune the hyperparameters. 

### 4. Assessment of the accuracy of the model 

The logistic model was chosen because it delivered the best recall score on the test data set. Additionally the logistic regression model was chosen because of being a relatively simple model to explain to business and to implement. 

Recall score for the chosen logistic model is 67% with an AUC of 0.76.

### 4. Model Implementation 

The model parameters were exported using pickle, and a production script prepared to do preprocessing of new data.

The application of the model was to score all policies and flag any policy that had the probability of early default >90% and then alerts the business on a PowerBi Alert Dashboard.

**Packages used :
Numpy | Pandas | Sklearn | Scipy | Tensorflow | StatsModels | Keras | MatplotLib** 

[Back to Project List](http://emilevdheyde.github.io/)
