# Neural_Network_Charity_Analysis
## Overview
The objective of this project is to use neural networks to be able to create a binary classifier where we will be helping a company "Alphabet Soup" to know if the applicants for its financing will be successful or not in their business.

## Results

Data Preprocessing


The objective variable with which the entire model will be developed is 'IS_SUCCESSFUL', all the other variables will be used to feed the model with the exception of two, the two variables that will be eliminated  are "EIN" and "NAME" since they are really insignificant and they do not add any value to the model.

For the first neural network, 2 hidden layers were used, where the first was formed with 86 neurons and the second with 43, both with the 'relu' activation function, and finally the output layer as we wanted a binary result only according to a neuron and the 'sigmoid' activation function.

![image](https://user-images.githubusercontent.com/66183125/153739455-9eef7557-7b40-4ab1-b2d0-131bd4cb55fa.png)

El resultado de la primer red neuronal nos dio un accuracy de .7252 , aunque es un buen resultado este no llega a la meta de .75
![image](https://user-images.githubusercontent.com/66183125/153739472-7a855273-a1e6-48aa-9eed-0f49613b21a0.png)



Attempt 1 

The following were several attempts to improve a little the result of our neural network.

The first thing that was done was to evaluate the variables of the model again to find out if there was any other variable that did not serve us much within the model and more than anything was affecting the result. When evaluating this, it was seen that the 'SPECIAL_CONSIDERATIONS' column had very different values ​​that almost 100% leaned towards one value, so we decided to eliminate that column in addition to those already eliminated previously, in addition to this in the neural network it was decided By expanding the number of neurons in the first hidden layer to 120 and the second to 80, this resulted in a small increase in accuracy of .7254

![image](https://user-images.githubusercontent.com/66183125/153739487-6667119c-197c-45d3-841e-87020f4db5a8.png)
![image](https://user-images.githubusercontent.com/66183125/153739498-61afb055-3e86-4d12-9d71-7c82285f2aac.png)


Attempt 2

In our second attempt to improve the accuracy of the neural network, it was decided to leave everything the same but with the difference that now a third hidden layer would be added with a total number of neurons of 40, which resulted in another small increase in the precision of .7265

![image](https://user-images.githubusercontent.com/66183125/153739523-68479042-8867-47a8-9fc8-8aac515ff097.png)
![image](https://user-images.githubusercontent.com/66183125/153739535-4bf40b0f-5721-4e96-bc5b-e27753ee62a7.png)


Attempt 3

And finally in our third attempt the third hidden layer was left but with the difference that different activation functions were used in the second and third hidden layers, instead of using 'relu', now 'tanh' was used, which gave us returned to give a new increase in the accuracy of the model with a result of .7269

![image](https://user-images.githubusercontent.com/66183125/153739543-59b4f91a-8e0d-4532-9a15-e4ffacf0d7ac.png)
![image](https://user-images.githubusercontent.com/66183125/153739555-28ca8d90-c02d-445d-bd8e-35c4bd24e3a1.png)

## Summary
The final precision that we can obtain from our neural network was .7269, which is why it failed to achieve the .75 target. although I think it is not so bad to get a precision of that degree, the main problem I see is the loss since in my opinion it is high with a total value of .5549, which could make me think that the model would be overfitted, which What could be done to improve these results would be to evaluate the variables again to know if all of them are really necessary and, in addition to this, to check if the values ​​in each column are well classified. Something that would be quite good to do is compare these results with other models, either with a random forest or with a logistic regression, because although it may seem simple, sometimes more basic models give better results than a complex one.
