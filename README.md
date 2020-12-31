# Azure-ML-Capstone

# Heart Diesease Prediction Using Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree. In this project we use Microsoft Azure to configure a cloud based machine learning production model, deploy it, consume it.<br>
The data used in this project is taken from kaggle open datasets.
<br><br>
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
## Dataset

### Overview
The dataset is Heart Diesease prediction and is taken from kaggle open datasets.<br>
The dataset has 13 different attributes about the patients's heart condition.<br>
<a href='https://www.kaggle.com/ronitf/heart-disease-uci'>Link to dataset</a><br>
### Task
The task we are going to solve with this dataset is to determine whether the given patient has a heart diesease( Binary - Classification).<br>
For the task we are going to use all the given features in the dataset.
### Access
The data is accessed in ML Studio workspace by using its url.<br>
<br><br>
## Automated ML
Automated Machine Learning(AutoML) is the process of automating the entire Machine Learning pipeline.
The AutoMLConfig class is used specify paramters such as experiment_timeout_minutes, task,primary_metric, training_data, label_column_name, n_cross_validations.
Automated machine learning supports ensemble models, which are enabled by default. Ensemble learning improves machine learning results and predictive performance by combining multiple models as opposed to using single models.<br>
The best model obtained through AutoML is VotingEnsemble. Voting Ensemble predicts based on the weighted average of predicted class probabilities (for classification tasks).<br>
### Results
The automl model has an acuuracy of 84%. The accuarcy could have been improve by increasing the<i>experiment_timeout_minutes</i> parameter as will run the automl for longer which may increase its accuracy.
<img src='screenshots/aml runcomp.png">
<img src='screenshots/aml model.png">
<img src='screenshots/aml modelparam.png">

## Hyperparameter Tuning
*TODO*: What kind of model did you choose for this experiment and why? Give an overview of the types of parameters and their ranges used for the hyperparameter search
As this task is a classification task I have chosen a logistic-regression model from scikit-learn.
The hyperparameters such as 'Inverse of Regularization Strength' and 'Maximum number of iterations to converge' are used for parameter sampling.<br>
The sampling method used is RandomSampling. It supports both discrete and continuous values. It supports early termination of low-performance runs. In Random Sampling, the values are selected randomly from a defined search space.<br>
The early stopping policy used is Bandit Policy.
Bandit Policy is based on slack factor/slack amount and evaluation interval.
This policy will terminate runs whose primary metric is not within the specified slac factor/slack amount.<br>
By using this policy we could improve the computational efficiency.<br>
The best model obtained is saved.

The acccuracy obtained in hyperdrive model is 


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
