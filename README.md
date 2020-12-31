# Azure-ML-Capstone

# Heart Diesease Prediction Using Azure

This project is part of the Udacity Azure ML Nanodegree. In this project we use Microsoft Azure to configure a cloud based machine learning production model, deploy it, consume it.

## Summary
The dataset used is Heart Diesease prediction dataset from <a href='https://www.kaggle.com/ronitf/heart-disease-uci'>kaggle</a>. <br>
We have to predict whether a patient has a heart diesease or not.<br>
The model used is a custom coded model-a sci-kit learn Logistic Regression model.
At first, the hyperparameters are tuned using the tool Hyperdrive.<br>
We save the best model obtained through this.<br>
Next, using Automated Machine Learning(AutoML) an optimal model is determined.<br>
We then compare both the results and find out which method gives better results.
The best model was AutoML which gave an accuracy of 93%.<br>
The best model is then deployed as a web service on Azure Container Instances.
The model endpoints are then consumed by using the custom <i>score.py</i> script.

<br><br>
<br><br>
## Dataset

### Overview
*TODO*: Explain about the data you are using and where you got it from.

### Task
*TODO*: Explain the task you are going to be solving with this dataset and the features you will be using for it.

### Access
*TODO*: Explain how you are accessing the data in your workspace.

## Automated ML
*TODO*: Give an overview of the `automl` settings and configuration you used for this experiment

### Results
*TODO*: What are the results you got with your automated ML model? What were the parameters of the model? How could you have improved it?

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

## Hyperparameter Tuning
*TODO*: What kind of model did you choose for this experiment and why? Give an overview of the types of parameters and their ranges used for the hyperparameter search


### Results
*TODO*: What are the results you got with your model? What were the parameters of the model? How could you have improved it?

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

## Model Deployment
*TODO*: Give an overview of the deployed model and instructions on how to query the endpoint with a sample input.

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:
- A working model
- Demo of the deployed  model
- Demo of a sample request sent to the endpoint and its response

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
