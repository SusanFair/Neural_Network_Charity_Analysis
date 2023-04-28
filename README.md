# Neural Network Charity Analysis

## Overview of the Analysis

The objective of this analysis is to train a neural network that is able tp predict whether a funding applicant will be successsful or not.  Alphabet Soup our sponsor will use this prediction to select the best candidate for investment in their the Charitable Funding Program.
Neural Network Exploration

The dataset consistes of 34,000 organization that have previously received funding in the past.  This will be the base used to train our model.




## Results: <br>
Two models were created.  The first can be found in the notebook [AlphabetSoupCharity](https://github.com/SusanFair/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb)

A second model was created to optimize the model deriving better results.  This optimized model can be ound in the notebook [AlphabetSoupCharite_OPtimized](https://github.com/SusanFair/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimized.ipynb)
<br>

#### Data Preprocessing<br>
* <b>Target Variable:</b>  The target variable is the column "IS_SUCCESSFUL"  This classifies, using historical data, those who received funding and where successful.

* <b>Features include:</b> APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS and ASK_AMT.

* <b>Removed:</b>  
        * In the initial model the columns EIN and NAME were removed.<br>
        * For optimization only the columns EIN were removed.  

#### Compiling, Training, and Evaluating the Model<br>
* <b>Initial Model</b> The initial model returned a Loss of .5362 and an Accuracy score of .7412.  Lower than desired result
    * Total input were 43
    * First Hidden Layer - 80 Neurons
    * Second Hidden Layer - 30 Neurons
    * Relu activation function was used in both layers
    * The model was saved in the [AlphabetSoupCharity.h5](https://github.com/SusanFair/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.h5)
    

*<b> Optimized Model</b>  With optimization the results improved to a Loss of ?? and 0panAccuracy of ??
    * The NAME column was returned to the dataset.  This increased substantilly the number of inputs (input breadth).  Therefore the number of neurons were increased accordingly. 
    * Total input were 835
    * First Hidden Layer - 1800 Neurons.  This number was based on the rule of thumb that the total number of neurons should be 2 times the number of inputs
    * Second Hidden Layer - 1200 Neurons.  This number was based on the concept on concentration of results.  The initial layer handling all of the inputs and the second layer only working with the output of the first layer
    * Relu activation function was used in both layers
This overall combination was drawn from the results of running an optimizer.

## Summary<br>
The overall results despite optimization are still not ideal.  Accuracy is still below 90% and loss numbers remain high.

As an improvement option running Random Forest on the initial dataset first would help to detect features bagging them for later use in deep learning. Providing a early siffoning prior to training the deep learning model


