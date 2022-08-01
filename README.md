# Neural_Network_Charity_Analysis

## Environment
Tensorflow v. 2.4.1

## Overview 
1. Compare the differences between the traditional machine learning classification and regression models and the neural network models.
2. Describe the perceptron model and its components.
3. Implement neural network models using TensorFlow.
4. Explain how different neural network structures change algorithm performance.
5. Preprocess and construct datasets for neural network models.
6. Compare the differences between neural network models and deep neural networks.
7. Implement deep neural network models using TensorFlow.
8. Save trained TensorFlow models for later use.

## Purpose
A foundation, Alphabet Soup, wants to predict where to make investments.  The goal is to use machine learning and neural networks to apply features on a provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.  The initial file has 34,000 organizations and a number of columns that capture metadata about each organization from past successful fundings.

## Results
### Data Preprocessing

1. What variable(s) are considered the target for your model?

The target for the model is the "Is-Successful" column. It signifies if the money was use effectively.

2. What variable(s) are considered to be the features for your model?

The features of this model are the APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT

3. What variable(s) are neither and should be removed from the input data? 

* EIN (Employer identificaiton) was dropped because the numbers could confuse the system into thinking its significant.
* A student could drop SPECIAL_CONSIDERATIONS because there is only a small percentage of cases that had any special consideration, and special considerations cannot be quantified.
* A student could drop STATUS because  all rows were the same value, 1.

### Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and and activation functions did you select for your neural network model, and why?

I tried 3 optimizations:

Optimization 1:
* Dropped STATUS and SPECIAL_CONSIDERATION
* increased epochs 

Optimization 2:
In addition to optimization 1..
* added a 3rd layer. I chose 5 units and a "tanh" activation
* changed output layer to "sigmoid" activation

Optimization 3:
In addition to optimization 2..
* added a 4th layer. I chose 5 units and a "tanh" activation
* changed units in layer 1-3 to 135, 45, and 15 respectivly 
* changed the first layer to "relu" activation to speed up the model

2. Were you able to achieve the target model performance?
ANSWER: Yes 

3. What steps did you take to try and increase model performance?
ANSWER: It required converting the NAME column into data points, which has the biggest impact on improving efficiency. And, it also required adding a third layer and using the "sigmoid" activation function for the 2nd and 3rd layer.

## Summary

Overall, by increasing the accuracy above 75% we are able to correctly classify each of the points in the test data 75% of the time. And, an applicant has a 80% chance of being successful if they have the following:
* The NAME of the applicant appears more than 5 times (they have applied more than 5 times)
* The type of APPLICATION is one of the following; T3, T4, T5, T6, T7, T8, T10, and T19
* The application has the following CLASSIFICATION; C1000, C2000, C3000, C1200, and C2100.

A good model to recommend is the Random Forest model because Random Forest is good for classification problems. Using this model produces a 78% accuracy.


Deliverable 3:

Optimization 1:
*Dropped STATUS and SPECIAL_CONSIDERATION
*&increased epochs 

Optimization 2:
In addition to optimization 1..
* added a 3rd layer. I chose 5 units and a "tanh" activation
* changed output layer to "sigmoid" activation

Optimization 3:
In addition to optimization 2..
* added a 4th layer. I chose 5 units and a "tanh" activation
* changed units in layer 1-3 to 135, 45, and 15 respectivly 
* changed the first layer to "relu" activation to speed up the model
