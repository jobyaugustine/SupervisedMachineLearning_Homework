# SupervisedMLHomework
## Predicting Credit Risk

The assignment is to build a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not. 

The data for this assignment is from a peer-to-peer lending services company called LendingClub
that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

The data is used to create machine learning models to classify the risk level of given loans.  The Logistic Regression model and Random Forest Classifier are used to compare the risks.

## Development Process
### Retrieval of the data

The data is downloaded from LendingClub and output is written to two CSVs:
* `2019loans.csv`
* `2020Q1loans.csv` using 
[GenerateData.ipynb](GenerateData.ipynb) notebook.

* `2019loans.csv` has an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020). * `2020Q1loans.csv` has the first quarter of the data of 2020.

## Preprocessing of the Data

## Convert categorical data to numeric
 All the categorical columns of the training data set of the 2019 loans and testing data set of the 2020 are changed to numeric columns.
 
 'hardship_flag','debt_settlement_flag','home_ownership','verification_status','loan_status','initial_list_status','application_type' are converted to numeric columns.
 
 `pd.get_dummies()` is used for the training data set and the testing data set to convert the categorical columns to numeric columns.

## Creating the models

Two models are used for the comparison - logistic regression and random forests classifier. 


## Fit a LogisticRegression model and RandomForestClassifier model

LogisticRegression model is created, fit it with the data, and the model's score is printed. 
Same process is done for RandomForestClassifier. 

Testing and Training score with the Random Forest model are higher than with the Logistic regression model.

## Scale the data

The data to both the models are scaled using the  `StandardScaler` . The training and testing sets are scaled. 

LogisticRegression and RandomForestClassifier models are fit and scored on the scaled data. 

LogisticRegression model showed an increase in both the training and testing score. 

Random Forest scores did not change.
