# Neural Network Charity Analysis

# Overview of the Analysis

The objective of this analysis is to train a neural network that is able tp predict whether a funding applicant will be successsful or not.  Alphabet Soup our sponsor will use this prediction to select the best candidate for investment in their the Charitable Funding Program.
Neural Network Exploration

The dataset consistes of 34,000 organization that have previously received funding in the past.  This will be the base used to train our model.




# Results: Using bulleted lists and images to support your answers, address the following questions.
There is a bulleted list that answers all six questions (15 pt)

##Data Preprocessing
    * <b>Target Variable:</b>  The target variable is the final result "IS_SUCCESSFUL"  Using historical data classifying those who received funding and where or will be successful.
    * <b>Features include:</b> APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS and ASK_AMT.
    * <b>Removed:</b>  
        * In the initial model the columns EIN and NAME were removed.
        * For optimization only the columns EIN were removed.  

##Compiling, Training, and Evaluating the Model
    * Neurons, Layers, and Activation functions
        * ?? Neurons in Layer 1, ?? Neurons in Layer 2
        * Relu activation function was used in each layer
        * This combination was drawn from the results of running an optimizer.
    * With optimization model improvements were seen.  
        The original model returned a Loss of ??  and Accuracy score of ??  With optimization the results improved to a Loss of ?? and 0panAccuracy of ??
    * The name column was returned to the dataset.  This increased substantilly the number of inputs (input breadth).  Therefore the number of neurons were increased accordingly. 


# Summary
The overall results despite optimization are still not ideal.  Accuracy is still below 90% and loss numbers remain high.

As an improvement option running Random Forest on the initial dataset first would help to detect features bagging them for later use in deep learning. Providing a early siffoning prior to training the deep learning model


