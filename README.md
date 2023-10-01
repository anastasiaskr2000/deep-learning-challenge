# deep-learning-challenge
## Neural Network Model Report 
## Overview: 

The purpose of this analysis is to build a neural network that can best evaluate and select applicants for funding with the best chance of success in their ventures by creating a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. 

##Results: 

Data Preprocessing: 
- Targt Variable for the Model: <img width="1171" alt="Screenshot 2023-10-01 at 6 45 26 PM" src="https://github.com/anastasiaskr2000/deep-learning-challenge/assets/131491720/bd256acc-a887-4fd0-94d3-143d858daf5a">
- Features for the model: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, ASK_AMT
- Variables removed because they are neither targets nor features: <img width="1169" alt="Screenshot 2023-10-01 at 6 47 49 PM" src="https://github.com/anastasiaskr2000/deep-learning-challenge/assets/131491720/2614fc3b-06a3-49ee-acdb-4063df96fbe2">

Compiling, Training, and Evaluating the Model:
- For my neural network model I initially initially selected 2 layers with 80, 30 neurons respectively with a "relu" activation function at 200 epochs
- Using the keras_tuner library I was able to search for the best hyperparameters as I was unable to train my model to hit above 73% accuracy during the first 2 optimization attempts
- The best hyperparameters produced by the kerastuner are: <img width="1177" alt="Screenshot 2023-10-01 at 6 57 03 PM" src="https://github.com/anastasiaskr2000/deep-learning-challenge/assets/131491720/bb9de6ad-9a1e-4a07-80ed-3f39ee3811f2">
- The highest I was able to train my model to was 74%
- In order to increase model performance I removed an additonal column from the dataframe (as it contained one unvarying value), narrowed down the cutoff_value, and used a kerastuner search function to perform a number of trials to determine the highest-performing hyperparameters (trial results can be found in the "trials" folder)

##Summary: 

The best resulting neural network model achieved 74% acccuracy at 50 epochs, comprising 1 layer at 46 neurons corresponding to tuner/trial_id': '0047' which can be found in the "trails" folder with additional hyperparameters. Experimenting with the parameters and initial layout of the dataframe could produce a high-performing model, as well as adding more data to train the model, however, for the purpose of this initial model only the Alphabet Soup data was provided for analysis.

Module 21 Challenge 
