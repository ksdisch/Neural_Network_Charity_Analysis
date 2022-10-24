# Neural Network Charity Analysis

## Analysis Overview
The purpose of this analysis was to develop a neural network model from a charity organization dataset. The goal of the model was to predict whether applicants will be successful in terms of utilizing the money effectively or not.

## Results

### Data Preprocessing
- Target variable(s): 'IS_SUCCESSFUL' is the only target variable. This model is conducting binary classification to predict whether an applicant will be successful if granted the charity. Success in this scenario is based on whether the money was used effectively or not.
- Feature variable(s): 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT'
- Removed variable(s): 'EIN' and 'NAME' columns were removed as they were identification columns that would not benefit the model. 

### Compiling, Training, and Evaluating the Model
- Neurons: 
    - First hidden layer: 80 nodes because there are 38 inputs and a good rule of thumb for number of nodes is 2-3 times the number of inputs.
    - Second hidden layer: Used 30 inputs so as not to use an excessive amount of resources.
- Layers: I used two hidden layers to provide the benefits of multiple layers without using excessive resources by adding more layers.
- Activation functions: 
    - Hidden layers: I used the ReLu act because there are no negative values in the inputs and ReLu is effective for binary classification
    - Output layer: I used the sigmoid activation function because it is ideal for binary classification, which is what I wanted for my output.

I was not able to achieve the target model performance of 75% accuracy.

Optimization Steps:
- Added more neurons to hidden layer 2.
- Added a third hidden layer.
- Changed activation functions of hidden layers from ReLu to sigmoid.

#### Performance
- Peak Performance: 72.50% accuracy. This model used sigmoid as the activation function for both hidden layers versus ReLu in the other models.
- Steps Taken to Optimize Model
    - Increased neurons in first hidden layer from 30 to 50.
    - Added a third hidden layer.
    - Changed the activation function of both the first and second hidden layers from ReLu to sigmoid.


## Summary
The best accuracy achieved with this model was 72.50% accuracy, with 56.08% loss. 

### Model Recommendation
I think a supervised machine learning model would be good for this classification problem. I think this because we know what our desired outputs are and have labels for our input features. It would be comparable in terms of performance while demanding fewer resources than a neural network.
