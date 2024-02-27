# Report on the Neural Network Model


## Overview of the analysis

The general purpose of this analysis is to determine whether or not a applicant for funding will be successful in thier goals and to help Alphabet Soup determine who to fund based on the results. The model uses the data from previous applicants who were successful and not successful. Ir takes the provided data to learn what it takes for an applicant to be succesful.

## Results

### Data Preprocessing

### What variable(s) are the target(s) for your model?
"IS_SUCCESSFUL", to see if the resources were used effectively

### What variable(s) are the features for your model? 

APPLICATION_TYPE — Alphabet Soup application type
AFFILIATION — Affiliated sector of industry
CLASSIFICATION — Government organization classification
USE_CASE — Use case for funding
ORGANIZATION — Organization type
STATUS — Active status
INCOME_AMT — Income classification
SPECIAL_CONSIDERATIONS — Special considerations for application
ASK_AMT — Funding amount requested

### What variable(s) should be removed from the input data because they are neither targets nor features?

Initially 'EIN' AND 'NAME' were removed, for the optimization only 'EIN'

## Compiling, Training, and Evaluating the Model

### How many neurons, layers, and activation functions did you select for your neural network model, and why?

#### First Model
removed variables : EIN - NAME (ID columns)
Neurons: 3 layers, 80 neurons in the first layer, 40 neurons in the second layer, and 1 neuron in the final layer.
Activation Functions:  For first and second hidden layer ReLu was selected cause its effectiveness on achieving a good performance. 
For the output layer it was sigmoid
loss="binary_crossentropy"
optimizer="adam"
Training: 100 epochs
Accuracy: 72.64%

#### Second Model

removed variables : EIN 
Neurons: 4 layers, 97 neurons in the first layer, 11 neurons in the second layer, 25 neurons in the third layer, and 11 neuron in the final layer.
Activation Functions:  For first  hidden layer ReLu was selected cause its effectiveness on achieving a good performance. 
For the second, third, fourth and output layers sigmoid was selected
loss="mse"
optimizer="rmsprop"
Training: 100 epochs
Accuracy: 79.34%


### Were you able to achieve the target model performance?

Not at the first attempt, but with the second shown model i was able to achieve the target model performance.

### What steps did you take in your attempts to increase model performance?
In order to improve the performance it was necesary to try other activation functions and evaluate the performance with different layers and nerons on each layer


## Summary

I was quite confident with the performance but it is necesaarry to explore more options trying with different configuraations and especifications in order to improve the performance of the model and be able to have a better accuracy.
As a recommendation, improvement of the accuracy is key to good results and in order to achieve that it is important to continue  the assesmet of the model and the refinement of it.

