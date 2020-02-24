# Predicting Venture Success

## Overview
A nonprofit, philanthropic foundation that funds organizations that protect the environment, improve people's well-being, and unify the world has raised over $10 billion in the past 20 years. The organization needs to know the impact of each donation they receive and vet potential recipients to ensure their money is being used effectively. The foundation needs a way to predict which organizations are safe and worth donating to and which are too high risk.  

## Resources
Software:
- Tensorflow 2.0.0
- Pandas 1.0.0
- Matplotlib 3.1.3
- Python 3.7.4

Data Sources:
- https://www.theramenrater.com/resources-2/the-list/
- https://www.kaggle.com/inugami/dataset-on-company-clients-satisfaction
- https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset
- https://www.kaggle.com/raosuny/success-of-bank-telemarketing-data
- https://www.kaggle.com/zaurbegiev/my-dataset#credit_train.csv

## Summary
The analysis required for the venture predictions is too complex for standard statistical analysis. In order to create a mathematical solution to this problem, a neural network will be used. This is a mathematical algorithm meant modeled after the human brain that recognizes patters and features in the input data and provides quantative output. It's basic structure is composed of neurons which function individually and are interconnected and weighed with other neurons. Information flows through the network and produces result at the final layer of the network. These types of models can produce high degrees of accuracy on complex data; however there is a cost of interpretability as well as computational power. 

## Challenge
With the newly aquired knowledge of neural networks, the real analysis can be begin by analyzing the organizations that have received money from the foundation over the years. Based upon this past data, a neural network can be trained and used to predict the success of future organizations down the road. The mission is to create a binary classifier that can predict the success of an applicant if funded by the foundation. 

## Challenge Summary
The target accuracy of the model was 75% which unfortunately was not attained with the highest accuracy score after optimization being 72.6%. This was achieved using a deep neural network with two hidden layers and a total of 2,017 parameters. Further exploration into alternate machine learning algorithms may prove to be more successful, such as a random forest classifier. Refer to the `Challenge` folder for more details. 