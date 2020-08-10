# Neural-Networks
## Summary Challenge 19 
- We have a dataset for Alphabet Soup that is a organization that over the years has funded more than 34000 organizations.  The client would like to know what projects are likely to be successful to receive future funding.
- We build a machine learning model, in this case we used Deep Learning Neural Network model to train the data.
- We preprocess all numerical and categorical variables, then appy the StandarScaler class.
- Finally we train and fit the model, and evaluate the model using the test data.
- We print the loss and accurary of the test data evaluation.

## Preprocessing
- We reviewed the variables and separate the categorical and numerical values.  We needed bucketing the CLASSIFICATION and APPLICATION_TYPE.  We applied different tresholds for the bucketing to see if the accuracy of the model improved, but the changes in accuracy and loss were very little, the accuracy stayed around 0.74 and loss 0.53.
- We removed the ID and name columns, since this information was not relevant for the model.
- We applied OneHotEncoder to the categorical variables.
- We merged the numerical variables with the categorical variables after applying the OneHotEncoder.
- We split the train and test data and defined the output variable, in this case IS_SUCCESFUL will determine if the funding for that project was successful.
- We have 58 features for the model.
- Finally, we standarized and scaled the data to start working on the Deep Learning Model.

## Deep Learning Neural Network Model
- We started defining the model, the deep neural net, for number_input_features we had the number of features, and we started our first hidden_nodes_layer1 with 69 neurons (maximum number of variables), for the second hidden layer we had 35 neurons.
- The tensorflow Keras model Sequential was used for the model.
- We used for the activation for the hidden layer "relu function".
- We used for the activation of the output layer "sigmoid function".
- We compiled using loss="binary_crossentropy", optimizer="adam", metrics="accuracy".
- We used 50 epochs to train the model.
- Finally we evaluate the model using the test data and compute the loss and accuracy of the test.

## Results
- When we run the parameters described in the model, we had a loss around 0.5318 and accuracy of 0.7409.  
-  We decided to try more neurons for the first hidden layer, but the accuracy and loss stayed almost the same, also we run 3 hidden layers to see if any improvement, but we kept getting almost same results.
- We changed the activation function for the hidden layers, tried Tanh, Selu, Elu, Softsign, softplus, but Relu gave me the best results.  I also changed the activation function for the output layer but only I got worst results.
- I tried to bucket the variables with different tresholds to see if might get a better results, but I could not get anything better than 0.7409 for accuracy and loss 0.5318.
- I ran the model for 50 epochs, I changed to 100, got a little bit better, accuracy of 0.7424 but I could not get any better than 0.7424.  I noticed after 50 epochs the accurary and loss did not really improve.
- I ran 2 more models to see if I can get a better accuracy, I ran Random Forest Classifier and Logistic Regression.  For the Ramdom Forest the accuracy was 0.69 and for the Logistic Regression was 0.47.  I got better results with the neural network model.
- I expected to get a similar result with the Ramdom Forest since these 2 models have similar accuracy.
- I expected for the Logistic Regression to give me worst results, since the accuracy is much lower than the Neural Network.
- I increased the number of neurons for the hidden layers (up to 2 times the features), changed activation functions for hidden layers and output layer, I added a third layer, I used 100 epochs, I bucket the variables different and any of these changes make the accuracy goes higher than 0.7424.
