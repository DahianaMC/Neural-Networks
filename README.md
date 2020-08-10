# Neural-Networks
## Summary Challenge 19 
- We have a dataset for Alphabet Soup that is a organization that over the years has funded more than 34000 organizations.  The client would like to know what projects are likely to be successful to receive future funding.
- We build a machine learning model, in this case we used Deep Learning Neural Network model to train the data.
- We preprocess all numerical and categorical variables, then appy the StandarScaler class.
- Finally we train and fit the model, and evaluate the model using the test data.
- We print the loss and accurary of the test data evaluation.

## Preprocessing
- We reviewed the variables and separate the categorical and numerical values.  We need bucketing the CLASSIFICATION and APPLICATION_TYPE.  We applied different tresholds for the bucketing to see if the accuracy of the model improves, but the changes in accuracy and loss were very little, the accuracy stays around 0.71 and loss 0.56.
- We removed the ID and name columns, since this information is not relevant for the model.
- We applied OneHotEncoder to the categorical variables.
- We merged the numerical variables with the categorical variables after applying the OneHotEncoder.
- We split the train and test data and defined the output variable, in this case IS_SUCCESFUL will determine if the funding for that project was successful.
- We have 58 features for the model.
- Finally, we standarized the data and scale to start working on the Deep Learning Model.

## Deep Learning Neural Network Model
