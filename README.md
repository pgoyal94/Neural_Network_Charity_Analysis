# Neural Network Charity Analysis
Help Beks determine what charities to donate to.

## Overview of the analysis: 
Beks works for Alphabet Soup, a phylinthropic organization dedicated to helping organizations that protect the environment, improve people's wellbeing, and unify the world. Alphabet Soup has donated over $10 Billion over the last 20 years. Beks' job is to analyze the impact of each donation made by the organization and vet potential recipients to ensure donations are successful and make an impact. We are helping Beks determine figuring out which organizations are most likely to be successful.

## Results: 

### Data Preprocessing
What variable(s) are considered the target(s) for your model?
- The target variable is 'IS_SUCCESSFUL,' the variable that tells us if the money was used effectively.
What variable(s) are considered to be the features for your model?
- The features of our model are the remaining variables.
  - APPLICATION_TYPE—Alphabet Soup application type
  - AFFILIATION—Affiliated sector of industry
  - CLASSIFICATION—Government organization classification
  - USE_CASE—Use case for funding
  - ORGANIZATION—Organization type
  - STATUS—Active status
  - INCOME_AMT—Income classification
  - SPECIAL_CONSIDERATIONS—Special consideration for application
  - ASK_AMT—Funding amount requested
- For the optimized model, I removed the 'ASK_AMT' variable, as there was much noise.

![image](https://user-images.githubusercontent.com/92613639/160556126-7216baef-83eb-4db0-b5cc-b6d55805572c.png)

What variable(s) are neither targets nor features, and should be removed from the input data?
- EIN and NAME—Identification columns
- Identification columns would add no value in predicting if a donation would be successful or not, as it is an arbitary assignment simply meant to identify the donation.
### Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
- In the optimized model, I used the rule of thumb, which says we should use a neural network model with two to three times the neurons in the hidden layers to properly model the linear and nonlinear datasets.
Were you able to achieve the target model performance?
- Despite making numerous adjustments to the model, the accuracy remained largely unaltered. 
What steps did you take to try and increase model performance?
- Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
  - Dropping 'ASK_AMT' column (noisy variable)
  - Creating bins for rare occurrences in columns
- Adding more neurons to hidden layers
- Adding more hidden layers
- Using different activation functions for the hidden layers
- Increasing the number of epochs to the training regimen

## Summary: 
The deep learning model had a slightly higher accuracy prior to the optimization exercise (see below). This likely is a sign of overfitting - this is when the model is essentially remembering the values, so when it encounters a new set of data, is unable to make accurate predictions using the algorithms it has created. I would suggest looking at a supervised machine learning logistic regression model as we have a target variable defined. We may have better luck there. Additionally, the neural networks model was slow, and other machine learning models tend to provide quicker results.

Unoptimized:

![image](https://user-images.githubusercontent.com/92613639/160556605-f2856bff-0852-4da7-b55c-f2c96e2a97da.png)

Optimized:

![image](https://user-images.githubusercontent.com/92613639/160556479-8cdf5c25-e404-4539-af10-3a0434ce1aba.png)
