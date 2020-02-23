# Model Analysis

## Model description
The final model used for the analysis was a neural network with two hidden layers. There was a total of 2,017 parameters which was broken down into 45 input features, 32 neurons in the first hidden layer, 16 neurons in the second hidden layer, and 1 neuron as the output. These values and schema were chosen after multiple rounds of training different models to achieve the goal of 75% accuracy on the test data. This goal was never reached but the process of attempted optimization is documented below. The highest achieved accuracy was 72.6% with the parameters listed above.

## Improving performance
Attempts:
- Start with 2 hidden layers; hidden layer 1 = 24 neurons, hidden layer 2 = 12 neurons -> produced 70% accuracy 
- Increased number of hidden nodes to match the number of features; hidden layer 1 = 32 neurons, hidden layer 2 = 8 neurons -> slight increase, up to 72%
- Remove one of the hidden layers -> drop in accuracy, 71%
- Remove outliers from dataset (specicially capping ASK_AMT at 3 billion) & add second hidden layer back -> drop in accuracy, 68%
- Remove hidden layer again -> no change, 68%
- Increase nodes in second hidden layer; hidden layer 2 = 16 nodes -> no change, 69%
- Increase nodes to be multiples of # features; hidden layer 1 = 36 nodes, hidden layer 2 = 18 nodes -> no change, 68%
- Restored outliers -> increase in accuracy, 72.5%
- Increase number of epochs to 100 -> no change, 72.5%
- Removed SPECIAL_CONSIDERATIONS from features -> no change, 72%
- Changed second hidden layer to sigmoid activation function -> no change, 72.5%
- Increased epochs to 100 -> no change, 72.5%
- Changed second hidden layer to tanh activation function -> no change, 72.5%
- Added a third hidden layer -> no change, 72.5%
- Remove third hidden layer, set nodes to multiples of 8 ('groups' of features); hidden layer 1 = 32 nodes, hidden layer 2 = 16 nodes, set second hidden layer to sigmoid activation function -> slight improvement, 72.6%

## Alternate approaches
For further exploration I would attempt to employ a Random Forest Classifier algorithm to this dataset to see if it could perform better than the neural network. I would try the Random Forest because the data is nonlinear and contains a substantial amount of outliers. It is also easier to interpret/disect than a neural network which would make it easier to optimize. 