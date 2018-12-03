# Coursera Activity Predictions
## Predict activities based on accelerometers

### Objective: 
The objective of this exercise is to predict which workouts are being performed given a set of information collected by accelerometers from participants. This process will include; loading the training and testing sets, exploring the data set, tidying data, training, and eventually testing the model on our hold out set. 

### Pre-Processing 
After reviewing the data set we can notice the number of values input as "NA" character values. These values can causes issues as the model will interpret these as factors, and not missing values. To remedy this proble we will convert all blank, and "NA" values to NA values. Once we have made this conversion I ntoiced there 34 attributes that had mostly NA values, which were removed from our training set. 

The response variable was also found to be balanced, with each of the 5 possible outcomes having approximately about the same probability of occurring. 

### Building the model
The Gradient Boosting Model was choosen for this test. Cross validation with only three folds were chosen due to the small training sample size (for GBMs). With such as large number of independent variables and small number of observations, a wide range of hyperparameters were chosen as to test both simple and complex models. 

After reviewing the performance of the out of sample observations I decided to use the following hyper-parameters; n.trees=200, interactio.depth=5, n.minobsinnode=10, and shrinkage=0.1.

