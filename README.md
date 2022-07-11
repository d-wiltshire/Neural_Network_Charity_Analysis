# Neural_Network_Charity_Analysis

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


Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
Dropping more or fewer columns.
Creating more bins for rare occurrences in columns.
Increasing or decreasing the number of values for each bin.
Adding more neurons to a hidden layer.
Adding more hidden layers.
Using different activation functions for the hidden layers.
Adding or reducing the number of epochs to the training regimen.
