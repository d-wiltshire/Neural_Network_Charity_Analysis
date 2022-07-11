# Neural_Network_Charity_Analysis

## Overview

This challenge involved using a deep learning model to predict a binary target outcome. The data come from a fictitious philanthropy organization, Alphabet Soup, which is aiming to improve the utility of its donated funds by predicting which applicants will be successful, if funded.

The dataset is a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup. The columns include: EIN and NAME (Identification columns), Application Type, Affiliation (Industry sector), Government organization classification, Use case for funding, Organization type, Status (Active or Inactive), Income classification, Special Considerations, Funding amount requested, and Success (whether the money previously funded had been used effectively). 


## Data Preprocessing
* What variable(s) are considered the target(s) for your model? 
*   The target is the IS_SUCCESSFUL column, which indicates whether the money previously funded had been used effectively.

* What variable(s) are considered to be the features for your model?
*   The features included:  Application Type, Affiliation (Industry sector), Government organization classification, Use case for funding, Organization type, Status (Active or Inactive), Income classification, Special Considerations, Funding amount requested

* What variable(s) are neither targets nor features, and should be removed from the input data?
*   The EIN and NAME columns were removed from the input data, as these contained unique organization identifiers.


## Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * The initial model included two hidden layers (the first with 16 neurons, and the second with 5). Both used the ReLu activation function. Two hidden layers were used initially to take advantage of the benefit of an additional hidden layer

* Were you able to achieve the target model performance?
  * The optimization steps taken did not achieve target model performance (75%). 

* What steps did you take to try and increase model performance? 
  * Please see "Optimization" below.



## Optimization

Before optimizing, the loss after 50 epochs was .55, and the accuracy was .73, as depicted below:

![19originallosserror](https://user-images.githubusercontent.com/100863488/178315798-90d600af-894e-437b-b54f-ae2dcd71f1cf.png)


The goal of optimizing was to achieve a target predictive accuracy higher than 75%. 

The steps taken to optimize the model included:

* Increasing the number of units in the second hidden layer from 5 to 10. This resulted in a loss and accuracy very similar to the original, as depicted below:

![191sttry1](https://user-images.githubusercontent.com/100863488/178316451-cc0c5a97-dcd1-40ce-99e3-f0e0bbcf0f85.png)

![191sttry](https://user-images.githubusercontent.com/100863488/178316190-513dddc1-df32-4bb9-8c39-3e6908790cb6.png)


* Changing the activation function from ReLu to Tanh in both the first and second hidden layers. Again, the loss and accuracy were very similar, as depicted below:

![192ndtry1](https://user-images.githubusercontent.com/100863488/178317219-baf6373f-1839-4b45-af89-02020672bed3.png)

![192ndtry2](https://user-images.githubusercontent.com/100863488/178317230-63a81d07-1a84-4edd-837f-1e6442d009c8.png)


* Dropping the "ASK_AMT" column from the original dataframe (which required also changing the input dimensions of our model). The accuracy went up slightly with this adjustment.

![193rdtry1](https://user-images.githubusercontent.com/100863488/178319335-a8c76ac5-94cb-400f-bc01-fe7dab22e21c.png)

![193rdtry2](https://user-images.githubusercontent.com/100863488/178319353-1fa72f40-8d34-46cc-aedc-9ef6680b708e.png)


## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
### Optimization Summary

None of these three attempts at optimization achieved a target predictive accuracy as high as the original model, but all were close to one another. 

Please note that the three attempts were performed independently of one another, resetting the code to the original model before making the next optimization attempt. The Jupyter Notebook optimization file included in this repository combines the code of all three attempts. 


