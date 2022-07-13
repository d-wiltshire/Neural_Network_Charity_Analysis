# Neural_Network_Charity_Analysis

## Overview

This challenge involved using a deep learning model to predict a binary target outcome. The data come from a fictitious philanthropy organization, Alphabet Soup, which is aiming to improve the utility of its donated funds by predicting which applicants will be successful, if funded.

The dataset is a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup. The columns include: EIN and NAME (Identification columns), Application Type, Affiliation (Industry sector), Government organization classification, Use case for funding, Organization type, Status (Active or Inactive), Income classification, Special Considerations, Funding amount requested, and Success (whether the money previously funded had been used effectively). 


## Data Preprocessing
* What variable(s) are considered the target(s) for your model? 
  * The target is the IS_SUCCESSFUL column, which indicates whether the money previously funded had been used effectively.

* What variable(s) are considered to be the features for your model?
  * The features included:  Application Type, Affiliation (Industry sector), Government organization classification, Use case for funding, Organization type, Status (Active or Inactive), Income classification, Special Considerations, and Funding amount requested.

* What variable(s) are neither targets nor features, and should be removed from the input data?
  * The EIN and NAME columns were removed from the input data, as these contained unique organization identifiers.


## Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * The initial model included two hidden layers (the first with 86 neurons, and the second with 43). Both used the ReLu activation function. Two hidden layers were used initially to take advantage of the benefit of an additional hidden layer. The first layer included 86 neurons as a doubling of the number of features post-encoding (43). The second layer included 43 as a step down between the initial layer and the output layer.

* Were you able to achieve the target model performance?
  * The optimization steps taken did not achieve target model performance (75%). 

* What steps did you take to try and increase model performance? 
  * Please see "Optimization" below.



## Optimization

Before optimizing, the loss after 50 epochs was .558, and the accuracy was 72.9% as depicted below:

![image](https://user-images.githubusercontent.com/100863488/178786394-1dfcb34f-8b12-44db-95b7-427d0e919d7b.png)



The goal of optimizing was to achieve a target predictive accuracy higher than 75%. 

The steps taken to optimize the model included:

* Adding a third hidden layer, with 22 neurons. This resulted in a slightly higher loss and lower accuracy, as depicted below: 

![image](https://user-images.githubusercontent.com/100863488/178787400-350a9063-1e27-46a9-b6af-7074ed29b863.png)

![image](https://user-images.githubusercontent.com/100863488/178787461-cfc621c5-33e6-45af-a404-83cd98135d46.png)




* Changing the activation function from ReLu to Tanh in both the first and second hidden layers. Again, the loss and accuracy were very similar, as depicted below:

![image](https://user-images.githubusercontent.com/100863488/178788000-c23a5d5c-2ac9-4740-b3b5-e4078ea0185d.png)

![image](https://user-images.githubusercontent.com/100863488/178788114-d44ef55f-5f69-4581-8c29-9576857c5ee7.png)




* Increasing the number of epochs to 100. Again, the loss and accuracy were very similar, as depicted below:

![image](https://user-images.githubusercontent.com/100863488/178788970-45488904-8376-426b-bccd-df328c3d7526.png)

![image](https://user-images.githubusercontent.com/100863488/178789026-ce9ede28-ffd5-40d6-9c00-5ee7849a7e9f.png)




## Summary

None of these three attempts at optimization achieved a target predictive accuracy as high as the original model, but all were very close to one another. The accuracy of this model achieved was around 73% in all attempts.

If the needed accuracy score is 75%, I would encourage the use of other machine learning models on this dataset, to see whether any could help provide greater accuracy. For example, using Random Forest would allow for a better understanding of feature importances, so that we could reduce the number of features in this dataset in an effective way for further trials (whether using neural networks or other machine learning options).


