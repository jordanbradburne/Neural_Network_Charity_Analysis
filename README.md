# Neural_Network_Charity_Analysis

## Overview of the analysis: 
Use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

## Deliverables:
Deliverable 1: Preprocessing Data for a Neural Network Model
Deliverable 2: Compile, Train, and Evaluate the Model
Deliverable 3: Optimize the Model

## Results: 

### Compiling, Training and Evaluating the Model

* For my neural network model I had 2 hidden layers. My first layer had 80 neurons, the second has 30 there is also an output layer. 
* The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid."

<img width="818" alt="Screen Shot 2021-10-31 at 7 00 43 PM" src="https://user-images.githubusercontent.com/85847344/139611354-5d45f31b-62f4-4b3c-80a6-dc59228bf078.png">

## Data Preprocessing

### What variable(s) are considered the target(s) for your model?
* The model was not able to reach the target 75%. 
* The accuracy for my model was about 69%.

<img width="551" alt="Screen Shot 2021-10-31 at 7 16 09 PM" src="https://user-images.githubusercontent.com/85847344/139612403-49b37611-0faf-44df-a997-a8def82c57d7.png">


### What steps did you take to try and increase model performance?

## Attempt 1: Removed additional feature. 
* Removed the 'USE_CASE' column, rest of the model components stayed the same, however model accuracy was only around 66%.

<img width="502" alt="Screen Shot 2021-10-31 at 7 13 54 PM" src="https://user-images.githubusercontent.com/85847344/139612235-1e03108a-1788-4bf4-976f-378e4ec0a9c8.png">
<img width="496" alt="Screen Shot 2021-10-31 at 7 14 09 PM" src="https://user-images.githubusercontent.com/85847344/139612255-6a13c8eb-0790-4bb5-95fc-9ff24c20a66d.png">

## Attempt 2: Adding Additional neurons to hidden layers and additional layers are added
* The accuracy went down again, this time it was 53%.

<img width="737" alt="Screen Shot 2021-10-31 at 7 14 41 PM" src="https://user-images.githubusercontent.com/85847344/139612291-63ce1404-9f57-47b0-a264-9f920a043fa2.png">
<img width="500" alt="Screen Shot 2021-10-31 at 7 14 55 PM" src="https://user-images.githubusercontent.com/85847344/139612309-a5c05413-99f2-4c0b-a7d8-cda648cf0403.png">

## Attempt 3: Changing activation function of output layer from "sigmoid" to "tanh." 
* The accuracy of the model went down to 47%.

<img width="742" alt="Screen Shot 2021-10-31 at 7 15 13 PM" src="https://user-images.githubusercontent.com/85847344/139612329-6ee6dcb9-71ba-4876-85f7-53b26d42cd62.png">
<img width="514" alt="Screen Shot 2021-10-31 at 7 15 31 PM" src="https://user-images.githubusercontent.com/85847344/139612353-b6ae0f8f-3d5d-4272-8f6f-f215c5ac2426.png">

## Summary: 
The model ended with an accuracy of below %50% after optimization. The initial network had the highest accuracy of about 70%. The loss in accuracy is due to overfitting of data. So we could also optimize the neural network by removing more features or adding more data to increase the accuracy. Random Forest, since it is robust and accuracte due to due to tree depth and such, that may have been a better calssifier for the data given.  In addition to that, Random Forest midels also have a very fast performance than neural networks.
