# deep-learning-challenge

## Data Preprocessing

### What variable(s) are the target(s) for your model?
* The target variable is the IS_SUCCESSFUL feature.

### What variable(s) are the features for your model?
* The features of the model are NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, ASK_AMT

### What variable(s) should be removed from the input data because they are neither targets nor features?
* Removed variables are EIN, STATUS, and SPECIAL_CONSIDERATIONS

## Compiling, Training, and Evaluating the Model

### How many neurons, layers, and activation functions did you select for your neural network model, and why?

I selected 80 input dimensions starting with 64 units and leaky_relu activation followed by 5 hidden layers diminishing the units by half each layer and activation transitioning from leaky_relu to relu to tanh and a final sigmoid output. I chose this through trail and error and advice suggesting a larger to smaller pyramid shape for units per layer and advice suggesting starting with more complex activations transitioning to less complex activations.

### Were you able to achieve the target model performance? What steps did you take in your attempts to increase model performance?

Summary: The model acheived 75.96% performance on test data of 20% of total. I made several attempts to adjust and bin the input dimensions with a standard NN model. I discovered that more dimensions improved the validation accuracy and loss. I also noticed that having too many inputs on the standard model improved training performance but not validation performance. I tried a range of inputs from 23 to 106. It appeared that 50 to 80 inputs had the best results. I chose to stay with 80 inputs and then began to adjust the model with more and less layers and more and less units per layer as well as different activation functions.

### Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Since this is a binary classification and the organization may have to explain reasoning for denied applications, I would suggest trying a decision tree model which can show importance of features and decision process.